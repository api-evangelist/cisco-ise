# Harvested Cisco ISE API descriptions

Every file in this directory is a **verbatim, unmodified copy** of a document Cisco publishes itself.

- **Source host:** `pubhub.devnetcloud.com` — Cisco's own DevNet documentation CDN.
- **DevNet project:** `identity-services-engine-api-v1` — "Cisco Identity Services Engine API v1" (project_id 3039), the media backend that renders <https://developer.cisco.com/docs/identity-services-engine/>.
- **Enumerated from:** that project's own `docs/config.json` manifest, which lists each document with `type: swagger` (Swagger 2.0) or `type: swagger3` (OpenAPI 3.x).
- **Fetched:** 2026-08-19, anonymously, no credentials, HTTP 200 on all 101 documents.

**101 documents / 1,481 operations.** 32 are OpenAPI 3.0.x, 69 are Swagger 2.0.

Nothing here was authored, padded, or repaired by API Evangelist. Per-file provenance —
source URL, HTTP status, byte count, SHA-256, spec version, operation count and the
`servers[]` block as published — is recorded in [`../cisco-ise-openapi-index.yml`](../cisco-ise-openapi-index.yml).

## Known defects in the published documents (Cisco's, not ours)

These are recorded, not corrected. Repairing them here would destroy the provenance.

1. **30 of the 69 legacy ERS Swagger 2.0 files contain literal TAB characters** and therefore fail a
   strict YAML 1.1/1.2 parse. They are saved exactly as served.
2. **860 of 1,481 operations (58%) carry no `operationId`.** Codegen and agent tool-naming cannot
   bind to them.
3. **95 of 101 documents declare no `securitySchemes`/`securityDefinitions`,** although every ISE API
   requires HTTP Basic authentication.
4. **`servers[]` mostly names Cisco lab appliances** (`https://10.56.60.25:443`, `https://172.23.9.91:443`,
   `https://iseui-vm11.cisco.com:443`) rather than the templated on-premises form. Only
   `https://{server}:{port}/ers/config` and `https://{server}/v1/` are templated. This is expected for an
   on-premises product — the real base URL is each customer's own appliance — but the leaked lab
   addresses are not usable by a consumer.

## Why 30 of these are not split into `openapi/`

Thirty of the legacy ERS Swagger 2.0 documents contain literal TAB characters and therefore fail a
strict YAML parse. They cannot be split per-tag and cannot carry an `x-provenance` block without
rewriting bytes Cisco served — which would destroy the very provenance this directory exists to keep.

They stay here, verbatim. `build_provenance.py` excludes `_original/`, so they are neither credited
nor counted, which is the correct treatment for a document that no consumer can parse either.
The defect is Cisco's and is reported, not repaired.
