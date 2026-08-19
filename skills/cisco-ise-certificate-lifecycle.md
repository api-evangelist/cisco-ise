---
name: Manage Cisco ISE system certificates
description: Inventory system and trusted certificates, generate a CSR, bind the signed certificate back, and renew expiring certificates — the PKI flow that keeps 802.1X working.
api: openapi/_original/cisco-ise-open-api-certificates.yaml
operations: [getSystemCertificates, getSystemCertificateById, getTrustedCertificates, getTrustedCertificateById, generateCSR, getCSRs, getCSRById, exportCSR, bindCSR, renewCerts, importSystemCert, importTrustCert, generateSelfSignedCertificate, deleteSystemCertificateById]
---

# Manage Cisco ISE system certificates

An expired EAP or admin certificate on ISE takes 802.1X authentication down for the whole estate.
This flow is about seeing that coming and handling it deliberately.

## Before you start

- HTTP Basic, **ERS Admin**, against the customer's own PAN. Certificate operations are per-node:
  most paths take a `{hostName}`.
- Get the node list first from the Deployment API (`getDeploymentNodes`,
  `GET /deployment/node/`) so you know which hostnames to iterate.

## Steps

1. **Inventory.** For each node, `getSystemCertificates`
   (`GET /api/v1/certs/system-certificate/{hostName}`) and `getTrustedCertificates`
   (`GET /api/v1/certs/trusted-certificate`). Read expiry dates and the assigned usages
   (EAP, admin, portal, pxGrid). Fetch detail with `getSystemCertificateById` or
   `getTrustedCertificateById` where you need it.

2. **Decide the path.**
   - Renewing something already issued by the ISE internal CA → `renewCerts`
     (`POST /api/v1/certs/renew-certificate`).
   - Getting a certificate from an external CA → go to step 3.
   - A lab or stop-gap → `generateSelfSignedCertificate`
     (`POST /api/v1/certs/system-certificate/generate-selfsigned-certificate`). Never for production
     EAP.

3. **Generate a CSR.** `generateCSR` (`POST /api/v1/certs/certificate-signing-request`). List them
   back with `getCSRs`, read one with `getCSRById`, and pull the PEM with `exportCSR`
   (`GET /api/v1/certs/certificate-signing-request/export/{hostname}/{id}`). For a subordinate CA use
   `generateIntermediateCACsr`.

4. **Get it signed out of band**, then **bind it**: `bindCSR`
   (`POST /api/v1/certs/signed-certificate/bind`). Binding is what actually activates the
   certificate for its usages.

5. **Or import directly** where you already hold the key material: `importSystemCert`
   (`POST /api/v1/certs/system-certificate/import`) for a node certificate,
   `importTrustCert` (`POST /api/v1/certs/trusted-certificate/import`) for a CA into the trust store.

## Rules

- **Changing the EAP or admin certificate restarts services on that node.** Never do it unattended.
  Confirm the maintenance window with a human before step 4 or 5.
- **Never send certificate private keys or the export password into logs or a model context.** The
  export operations take a password; treat it as a secret and keep it out of transcripts.
- **`deleteSystemCertificateById` and `regenerateISERootCA` are destructive.** Regenerating the ISE
  root CA invalidates every certificate the internal CA issued — including every BYOD endpoint
  certificate. Do not automate it.
- No idempotency key exists. If `bindCSR` times out, read back with `getSystemCertificates` before
  retrying — a second bind of the same CSR will not be silently absorbed.
