# Cisco Identity Services Engine

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Cisco Identity Services Engine (ISE) is Cisco's network access control and zero-trust policy platform: 802.1X and RADIUS authentication, TACACS+ device administration, guest and BYOD onboarding, endpoint profiling, posture assessment, and TrustSec security-group segmentation.

## Ownership

Part of the Cisco family.

## Contract status

**Published — corrected 2026-08-19.**

An earlier pass on this profile recorded *"the contract is served by each customer's own on-premises
controller, so there is no central anonymously fetchable specification."* That was wrong. It was
reached by checking only the JavaScript-rendered docs shell at `developer.cisco.com`.

Cisco publishes **103 machine-readable API descriptions covering 1,490 operations** for Cisco ISE,
anonymously and without credentials, on its own DevNet documentation CDN at
`pubhub.devnetcloud.com`, under the DevNet project `identity-services-engine-api-v1` (project_id
3039). They are enumerable from that project's own `config.json` manifest. All 103 were fetched at
HTTP 200 and are saved verbatim in [`openapi/_original/`](openapi/_original/) with per-file source
URL, SHA-256, byte count and operation count recorded in
[`openapi/cisco-ise-openapi-index.yml`](openapi/cisco-ise-openapi-index.yml).

What is customer-specific is the **runtime**, not the **contract**. The API is served by each
customer's own appliance behind the Cisco ISE API Gateway, so base URLs in this profile are
templated (`https://{server}:{port}/ers/config`, `https://{ise-node}`) — which is correct and
expected for an on-premises product.

| | |
|---|---|
| Documents | 103 (32 OpenAPI 3.0.x, 71 Swagger 2.0) |
| Operations | 1,490 |
| Largest | ERS Open API — 395 operations, OpenAPI 3.0.1 |
| Authentication | HTTP Basic; ERS Admin (read/write) or ERS Operator (read-only) |
| Published rate limit | 100 TPS concurrent ERS connections, no response headers |
| Event surface | Webhooks OpenAPI (ISE 3.6 Beta), Prometheus AlertManager, pxGrid |

### Defects found in Cisco's published documents

Recorded, not repaired — repairing them here would destroy provenance.

- **860 of 1,490 operations (58%) carry no `operationId`**, including all 395 in the ERS Open API.
- **30 of the 69 legacy ERS Swagger 2.0 documents contain literal tab characters** and fail a strict
  YAML parse.
- **95 of 103 documents declare no `securitySchemes`**, although every ISE API requires HTTP Basic.
- **`servers[]` mostly names Cisco lab appliances** (`10.x`, `172.x`, `iseui-vm11.cisco.com`) rather
  than the templated on-premises form.
- **Zero operations are marked `deprecated: true`**, although Cisco's published policy says
  deprecated operations are marked in the OpenAPI description and the changelog records real
  deprecations (Transport Gateway, ISE 3.3 Patch 2 and 3.4 GA).
- **No idempotency key of any kind**, on either surface — writes are not safely retryable.

## Agent surface

- **No first-party MCP server.** Cisco publishes none for ISE. `mcp/cisco-ise-mcp.yml` holds a
  *derived candidate* tool set and is deliberately **not** wired as an `MCPServer` pointer.
  Community servers exist (automateyournetwork/ISE_MCP, dlhace/cisco-ise-mcp) and are recorded as
  third-party, not credited to Cisco.
- **No A2A agent card.** `/.well-known/agent-card.json` and `/.well-known/agent.json` both return
  404 on `developer.cisco.com`. Nothing is written for it.
- **No `llms.txt` published** by Cisco; one is generated at `llms/cisco-ise-llms.txt`.
- Five Agent Skills in [`skills/`](skills/), every `operationId` verified against the harvested
  documents.

## Verified links

- [Developer portal](https://developer.cisco.com/identity-services-engine/)
- [API reference](https://developer.cisco.com/docs/identity-services-engine/latest/)
- [Getting started](https://developer.cisco.com/docs/identity-services-engine/latest/setting-up/)
- [Changelog](https://developer.cisco.com/docs/identity-services-engine/latest/changelog/)
- [Versioning and deprecation policy](https://developer.cisco.com/docs/identity-services-engine/latest/versioning/)
- [DevNet Sandbox](https://developer.cisco.com/site/sandbox/)
- [Licensing guide](https://www.cisco.com/c/en/us/products/collateral/security/identity-services-engine/guide-c07-656177.html)
- [GitHub (CiscoISE)](https://github.com/CiscoISE)
- [Blog](https://blogs.cisco.com/tag/cisco-ise)
- [Cisco PSIRT security.txt](https://www.cisco.com/.well-known/security.txt)
- [ParentCompany](https://apis.io/providers/cisco/)

All URLs above returned HTTP 200 when probed on 2026-08-19.
