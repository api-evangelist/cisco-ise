---
name: Review Cisco ISE TrustSec segmentation
description: Read the TrustSec posture of an ISE deployment — security groups, SGT reservations, classification and inbound rules, ACI integration and general settings — without changing enforcement.
api: openapi/_original/cisco-ise-open-api-trustsec.yaml
operations: [getSecurityGroups, getTrustsecGeneralSettings, getClassificationRuleList, getClassificationRuleById, getIngressFilterList, getIngressFilterById, getFiltersForSgt, getReservedSgtRanges, getACIConnections, getCTSHttpsServers, getSgtReservedRanges, getSgtReservedRange]
---

# Review Cisco ISE TrustSec segmentation

TrustSec is where ISE stops being an authentication server and starts being a segmentation control
plane. This skill reads that control plane. **It writes nothing.** A wrong SGT or SGACL change is a
production outage in the data path, not a config typo.

## Before you start

- HTTP Basic against the customer's PAN. **ERS Operator** is enough — everything here is a `GET`.
- Two documents cover this ground and they overlap:
  `openapi/_original/cisco-ise-open-api-trustsec.yaml` (139 operations, the modern surface) and the
  legacy per-resource ERS documents for `sgt`, `sgacl`, `egressmatrixcell`, `sgmapping`, `sgtvnvlan`,
  `sxpconnections`, `sxplocalbindings` and `sxpvpns`. The legacy documents carry **no
  `operationId`s** — bind those by method and path.
- TrustSec requires an **ISE Advantage** licence tier. On an Essentials deployment these resources
  will be empty or unavailable, and that is the answer, not an error to work around.

## Steps

1. **Read the ground rules.** `getTrustsecGeneralSettings`
   (`GET /api/v1/trustsec/general-settings`) — this tells you how the deployment treats TrustSec
   before you interpret anything else.

2. **List the tags.** `getSecurityGroups` (`GET /api/v1/trustsec/security-group`). Every policy
   decision below is expressed in terms of these.

3. **Check the reserved ranges.** `getSgtReservedRanges` (`GET /api/v1/sgt/reservation`, from the
   SGT Reservation API) and `getReservedSgtRanges`
   (`GET /api/v1/trustsec/integration/aci-connection/sgt-range`). Reserved ranges are where
   collisions with other controllers happen.

4. **Read classification.** `getClassificationRuleList`
   (`GET /api/v1/trustsec/classification-policy`), then `getClassificationRuleById` for the rules
   that matter. `getFiltersForSgt` (`GET /api/v1/trustsec/rule/sgt`) shows what maps to a given tag.

5. **Read inbound enforcement.** `getIngressFilterList` (`GET /api/v1/trustsec/inbound-rule`) and
   `getIngressFilterById`.

6. **Read the integrations.** `getACIConnections`
   (`GET /api/v1/trustsec/integration/aci-connection`) and `getCTSHttpsServers`
   (`GET /api/v1/trustsec/https-server`) — these are where TrustSec state leaves ISE.

7. **Read the matrix itself** from the legacy ERS documents: egress matrix cells, SGACLs and
   IP-to-SGT mappings. Bind by path (`/ers/config/egressmatrixcell`, `/ers/config/sgacl`,
   `/ers/config/sgmapping`) since those documents publish no operation ids.

## Rules

- **Do not call the preview or re-rank operations casually.** `getClassificationRuleFilterPreview`
  and `getInboundRuleFilterPreview` are `POST`s that evaluate rules; `reRankClassificationRules`
  (`POST /api/v1/trustsec/classification-policy/re-rank`) **changes rule order and therefore changes
  enforcement.** It is not a read.
- **Never call `pushCOA`** (`PUT /api/v1/trustsec/coa/push`) from an automated flow. A Change of
  Authorization re-authorises live sessions across the network.
- Report what you found and stop. Any SGT, SGACL or matrix change belongs in a change window with a
  named human owner.
