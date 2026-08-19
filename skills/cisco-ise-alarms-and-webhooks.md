---
name: Wire Cisco ISE alarms to a webhook
description: List alarm rules, create a webhook configuration, associate alarms with it, and verify delivery — the event-driven integration path introduced in ISE 3.6.
api: openapi/_original/cisco-ise-open-api-webhooks.yaml
operations: [getAllAlarmRules, getAlarmRuleById, getAllWebhooks, createWebhook, getWebhookById, updateWebhook, associateAlarmRules, getAlarmsByWebhookId, getRecentWebhookDeliveriesByConfigurationId, setWebhookConfigStatus, removeWebhook]
---

# Wire Cisco ISE alarms to a webhook

ISE 3.6 Beta added a first-party webhook surface. It is the only push integration Cisco describes
with a machine-readable contract — pxGrid is richer but has no published schema.

## Before you start

- HTTP Basic, **ERS Admin**, against the customer's PAN. Requires **ISE 3.6 Beta or later**; on
  earlier releases these paths do not exist and you will get
  `400 UNSUPPORTED_RESOURCE_EXCEPTION`.
- Cisco publishes **no schema for the body ISE POSTs to your endpoint.** The receiving side must be
  written defensively. Do not tell anyone you know the payload shape — you do not.

## Steps

1. **See what can fire.** `getAllAlarmRules` (`GET /api/v1/webhooks/alarms`), and
   `getAlarmRuleById` (`GET /api/v1/webhooks/alarms/{id}`) for detail. Alarm rules carry a category
   (for example `Posture`), a severity and a type id — use those to pick a meaningful subset rather
   than subscribing to everything.

2. **Check for an existing configuration.** `getAllWebhooks` (`GET /api/v1/webhooks`). Do not create
   a duplicate.

3. **Create the webhook.** `createWebhook` (`POST /api/v1/webhooks`) with the destination URL and
   its settings. **Send once** — there is no idempotency key, so on a timeout call `getAllWebhooks`
   and look for it before retrying.

4. **Bind the alarms.** `associateAlarmRules` (`PUT /api/v1/webhooks/{id}/alarms`) with the
   `alarmRuleIds` you chose in step 1. Confirm with `getAlarmsByWebhookId`
   (`GET /api/v1/webhooks/{id}/alarms`).

5. **Verify delivery.** `getRecentWebhookDeliveriesByConfigurationId`
   (`GET /api/v1/webhooks/{id}/deliveries`) returns the **most recent 10** deliveries. That is the
   entire delivery-observability surface Cisco publishes — there is no delivery log, no replay and no
   dead-letter queue. Build your own receipt tracking on the receiving side.

6. **Enable or disable without deleting.** `setWebhookConfigStatus` (`PUT /api/v1/webhooks`) toggles
   configuration status — prefer this to `removeWebhook` when pausing an integration.

## Rules

- **No delivery guarantee is published.** No retry policy, no signature/HMAC verification scheme, no
  ordering guarantee. Treat every delivery as at-most-once and unauthenticated unless the customer
  has put their own mutual TLS in front of the receiver.
- Alarms are an **operational** signal, not an audit trail. For posture, session and authentication
  history use the Monitoring (MnT) API instead.
- `bulkDeleteWebhooks` (`DELETE /api/v1/webhooks`) removes many configurations at once. Never call
  it from an automated flow.
