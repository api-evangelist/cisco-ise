---
name: Inventory and classify endpoints in Cisco ISE
description: Read the endpoint inventory an ISE deployment holds, summarise it by device type, and look up one endpoint by MAC — the read-only reconnaissance flow before any policy change.
api: openapi/_original/cisco-ise-open-api-endpoints.yaml
operations: [list_1, get_1, getDeviceTypeSummary, createEndPointTask]
---

# Inventory and classify endpoints in Cisco ISE

Cisco ISE is the record of what is on the network. This skill reads that record. It is
**read-only on purpose** — every write in ISE changes who can reach the network.

## Before you start

- ISE has **no shared API host.** The base URL is the customer's own appliance:
  `https://{ise-node}` with paths under `/api/v1`. Ask for it; never guess it, and never use the
  `10.x`/`172.x` addresses that appear in Cisco's published `servers[]` blocks — those are Cisco lab
  hosts.
- Authenticate with **HTTP Basic** over TLS. The account must be in **ERS Operator** (read-only) or
  **ERS Admin**. See `authentication/cisco-ise-authentication.yml`.
- **API services are disabled by default.** If calls time out or error immediately, the Open API
  service has not been enabled on that node — that is a configuration answer, not a retry.
- Send `Accept: application/json`. Omitting it returns `415 MEDIA_TYPE_EXCEPTION`.

## Steps

1. **Get the shape of the estate.** Call `getDeviceTypeSummary`
   (`GET /api/v1/endpoint/deviceType/summary`). This is the cheapest orientation call — it tells you
   what kinds of device ISE believes are present before you page through anything.

2. **Page the inventory.** Call `list_1` (`GET /api/v1/endpoint`). Pagination is `page` (1-based,
   default 1) and `size` (default 20, **max 100**). Ask for `size=100` and walk pages until a short
   page comes back. A `size` above 100 returns `400 QUERY_VALIDATION_EXCEPTION`.

3. **Filter rather than paging everything.** ISE filters take the form
   `filter=field.OPERATOR.value` and the parameter repeats:
   `?filter=name.STARTW.a&filter=identityGroup.EQ.Finance`. Operators seen in the published
   documents include `EQ`, `NOTEQ`, `STARTW` and `CONTAINS`.

4. **Resolve one endpoint.** Call `get_1` (`GET /api/v1/endpoint/{value}`), where `{value}` is the
   MAC address or the endpoint id. MAC is the natural key for endpoints.

5. **If you need a long-running endpoint job**, `createEndPointTask`
   (`POST /api/v1/endpointTask`) returns a task handle. Poll it with `getTaskStatus`
   (`GET /api/v1/task/{taskId}`) from the Task Service API — do not busy-loop the endpoint list
   waiting for a change to appear.

## Rules

- **Never retry a write.** ISE supports no idempotency key of any kind. A timed-out `POST` may have
  succeeded. Read back before resending. This is the single most important constraint on this API.
- **Respect 100 TPS.** That is the published ERS ceiling, and ISE returns **no** rate-limit headers
  and no documented 429 — you cannot detect the ceiling, only stay under it.
- **Sessions idle out at 60 seconds.** If CSRF checking is enabled and you pause longer than that,
  fetch a fresh CSRF token before the next request.
- On failure, read the ERS exception name in the body, not just the status. `400` covers query
  validation, schema validation and semantic validation, and they need different fixes. The registry
  is in `errors/cisco-ise-problem-types.yml`.
