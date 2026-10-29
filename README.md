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
> **Not from the company, and here with a question?** You are welcome here — we would rather be the
> front line and point you the right way than have a good report go nowhere. What this repository
> can answer is narrow, though, so it is worth knowing who you are actually looking for:
>
> - **A question about how the API works, an account, billing, or a bug in the service** — that is
>   the company's own support, not us. We profile this API; we do not operate it and cannot see
>   your account.
> - **A bug in an open-source project we only catalog** — file it on that project's own repository.
>   This has happened with a real and correct bug report that reached us instead of the people who
>   could fix it, which helped nobody.
> - **Anything about this listing itself** — the description, the tags, the rating, a missing or
>   wrong artifact — is ours. Open an issue here.
> - **Not sure, or something general about API Evangelist or APIs.io** — open an issue on the
>   [APIs.io Inbox](https://github.com/api-search/inbox) and we will route it.
>
> **This repository contains no software, and we will never ask you to download anything.** There is
> no build, release, installer, or binary here — only text and machine-readable API descriptions, so
> there is nothing here that can be "corrupt" or need "repairing". Any issue, comment, or email
> claiming otherwise and offering a download link is not from us and is hostile. Do not follow the
> link; it is a lure. Report it to GitHub and, if you like, tell us at
> [info@apievangelist.com](mailto:info@apievangelist.com) so we can take it down.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

Cisco Identity Services Engine (ISE) is Cisco's network access control and zero-trust policy platform: 802.1X and RADIUS authentication, TACACS+ device administration, guest and BYOD onboarding, endpoint profiling, posture assessment, and TrustSec security-group segmentation, all driven from a central policy service. It is deployed on-premises or in AWS, Azure and OCI, so its APIs are served by each customer's own appliance behind the Cisco ISE API Gateway rather than a shared public host. The contracts themselves are public: Cisco publishes 103 machine-readable API descriptions covering 1,490 operations on its DevNet documentation CDN — a consolidated 395-operation ERS Open API, 30 OpenAPI 3.0.x documents for the newer Open API surface (Policy, TrustSec, Certificates, Deployment, Webhooks, Licensing, pxGrid Direct and more), a Monitoring (MnT) OpenAPI, 69 legacy per-resource Swagger 2.0 references, and an outbound Mobile Device Management contract that ISE calls on third-party MDM vendors. Authentication is HTTP Basic with ERS Admin and ERS Operator roles; API services are disabled by default and enabled per node.

**Areas:** Identity · Network Access · Zero Trust · Security · Policy · Enterprise · 802.1X · RADIUS · TACACS+ · TrustSec · Guest Access · BYOD

## Cisco Identity Services Engine on APIs.io

Everything profiled for Cisco Identity Services Engine is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/cisco-ise/](https://apis.io/providers/cisco-ise/)** — or go straight to one of the APIs or properties below.

### APIs (198)

- [Cisco Identity Services Engine Acct Status API](https://apis.io/apis/cisco-ise/cisco-ise-acctstatus-api/) — The AcctStatus API from Cisco Identity Services Engine — 1 operation(s) for acctstatus.
- [Cisco Identity Services Engine Acct Status TT API](https://apis.io/apis/cisco-ise/cisco-ise-acctstatustt-api/) — The AcctStatusTT API from Cisco Identity Services Engine — 1 operation(s) for acctstatustt.
- [Cisco Identity Services Engine ACI Connection API](https://apis.io/apis/cisco-ise/cisco-ise-aci-connection-api/) — The ACI Connection API from Cisco Identity Services Engine — 13 operation(s) for aci connection.
- [Cisco Identity Services Engine ACI Data API](https://apis.io/apis/cisco-ise/cisco-ise-aci-data-api/) — The ACI Data API from Cisco Identity Services Engine — 10 operation(s) for aci data.
- [Cisco Identity Services Engine Acibindings API](https://apis.io/apis/cisco-ise/cisco-ise-acibindings-api/) — The acibindings API from Cisco Identity Services Engine — 3 operation(s) for acibindings.
- [Cisco Identity Services Engine Acisettings API](https://apis.io/apis/cisco-ise/cisco-ise-acisettings-api/) — The acisettings API from Cisco Identity Services Engine — 7 operation(s) for acisettings.
- [Cisco Identity Services Engine Active Directories API](https://apis.io/apis/cisco-ise/cisco-ise-activedirectories-api/) — The ActiveDirectories API from Cisco Identity Services Engine — 1 operation(s) for activedirectories.
- [Cisco Identity Services Engine Admin Groups API](https://apis.io/apis/cisco-ise/cisco-ise-admin-groups-api/) — The Admin Groups API from Cisco Identity Services Engine — 4 operation(s) for admin groups.
- [Cisco Identity Services Engine Admin Users API](https://apis.io/apis/cisco-ise/cisco-ise-admin-users-api/) — The Admin Users API from Cisco Identity Services Engine — 4 operation(s) for admin users.
- [Cisco Identity Services Engine Adresourcereservation API](https://apis.io/apis/cisco-ise/cisco-ise-adresourcereservation-api/) — The adresourcereservation API from Cisco Identity Services Engine — 8 operation(s) for adresourcereservation.
- [Cisco Identity Services Engine Alarm details API](https://apis.io/apis/cisco-ise/cisco-ise-alarm-details-api/) — The Alarm details API from Cisco Identity Services Engine — 2 operation(s) for alarm details.
- [Cisco Identity Services Engine Alarm Instances Services API](https://apis.io/apis/cisco-ise/cisco-ise-alarm-instances-services-api/) — The Alarm Instances Services API from Cisco Identity Services Engine — 6 operation(s) for alarm instances services.
- [Cisco Identity Services Engine AlarmConfigurations Services API](https://apis.io/apis/cisco-ise/cisco-ise-alarmconfigurations-services-api/) — The AlarmConfigurations Services API from Cisco Identity Services Engine — 3 operation(s) for alarmconfigurations services.
- [Cisco Identity Services Engine Allowedprotocols API](https://apis.io/apis/cisco-ise/cisco-ise-allowedprotocols-api/) — The allowedprotocols API from Cisco Identity Services Engine — 3 operation(s) for allowedprotocols.
- [Cisco Identity Services Engine Ancendpoint API](https://apis.io/apis/cisco-ise/cisco-ise-ancendpoint-api/) — The ancendpoint API from Cisco Identity Services Engine — 11 operation(s) for ancendpoint.
- [Cisco Identity Services Engine Ancpolicy API](https://apis.io/apis/cisco-ise/cisco-ise-ancpolicy-api/) — The ancpolicy API from Cisco Identity Services Engine — 9 operation(s) for ancpolicy.
- [Cisco Identity Services Engine Authorizationprofile API](https://apis.io/apis/cisco-ise/cisco-ise-authorizationprofile-api/) — The authorizationprofile API from Cisco Identity Services Engine — 3 operation(s) for authorizationprofile.
- [Cisco Identity Services Engine Auth Status API](https://apis.io/apis/cisco-ise/cisco-ise-authstatus-api/) — The AuthStatus API from Cisco Identity Services Engine — 1 operation(s) for authstatus.
- [Cisco Identity Services Engine Backup And Restore API](https://apis.io/apis/cisco-ise/cisco-ise-backup-and-restore-api/) — The Backup And Restore API from Cisco Identity Services Engine — 5 operation(s) for backup and restore.
- [Cisco Identity Services Engine Byodportal API](https://apis.io/apis/cisco-ise/cisco-ise-byodportal-api/) — The byodportal API from Cisco Identity Services Engine — 2 operation(s) for byodportal.
- [Cisco Identity Services Engine Certificateprofile API](https://apis.io/apis/cisco-ise/cisco-ise-certificateprofile-api/) — The certificateprofile API from Cisco Identity Services Engine — 7 operation(s) for certificateprofile.
- [Cisco Identity Services Engine Certificates API](https://apis.io/apis/cisco-ise/cisco-ise-certificates-api/) — The Certificates API from Cisco Identity Services Engine — 16 operation(s) for certificates.
- [Cisco Identity Services Engine Certificatetemplate API](https://apis.io/apis/cisco-ise/cisco-ise-certificatetemplate-api/) — The certificatetemplate API from Cisco Identity Services Engine — 7 operation(s) for certificatetemplate.
- [Cisco Identity Services Engine Classification rule API](https://apis.io/apis/cisco-ise/cisco-ise-classification-rule-api/) — The Classification rule API from Cisco Identity Services Engine — 4 operation(s) for classification rule.
- [Cisco Identity Services Engine Clearthreatsandvulneribilities API](https://apis.io/apis/cisco-ise/cisco-ise-clearthreatsandvulneribilities-api/) — The clearthreatsandvulneribilities API from Cisco Identity Services Engine — 2 operation(s) for clearthreatsandvulneribilities.
- [Cisco Identity Services Engine Co A API](https://apis.io/apis/cisco-ise/cisco-ise-coa-api/) — The CoA API from Cisco Identity Services Engine — 2 operation(s) for coa.
- [Cisco Identity Services Engine Configuration API](https://apis.io/apis/cisco-ise/cisco-ise-configuration-api/) — The Configuration API from Cisco Identity Services Engine — 1 operation(s) for configuration.
- [Cisco Identity Services Engine Ctsenvdata API](https://apis.io/apis/cisco-ise/cisco-ise-ctsenvdata-api/) — The ctsenvdata API from Cisco Identity Services Engine — 3 operation(s) for ctsenvdata.
- [Cisco Identity Services Engine Ctsmatrix API](https://apis.io/apis/cisco-ise/cisco-ise-ctsmatrix-api/) — The ctsmatrix API from Cisco Identity Services Engine — 3 operation(s) for ctsmatrix.
- [Cisco Identity Services Engine Data Access API](https://apis.io/apis/cisco-ise/cisco-ise-data-access-api/) — The Data Access API from Cisco Identity Services Engine — 2 operation(s) for data access.
- [Cisco Identity Services Engine Dataconnect Services API](https://apis.io/apis/cisco-ise/cisco-ise-dataconnect-services-api/) — The Dataconnect Services API from Cisco Identity Services Engine — 5 operation(s) for dataconnect services.
- [Cisco Identity Services Engine Device Admin - MFA Rules API](https://apis.io/apis/cisco-ise/cisco-ise-device-admin-mfa-rules-api/) — The Device Admin - MFA Rules API from Cisco Identity Services Engine — 3 operation(s) for device admin - mfa rules.
- [Cisco Identity Services Engine Device Administration - Authentication Rules API](https://apis.io/apis/cisco-ise/cisco-ise-device-administration-authentication-rules-api/) — The Device Administration - Authentication Rules API from Cisco Identity Services Engine — 3 operation(s) for device administration - authentication rules.
- [Cisco Identity Services Engine Device Administration - Authorization Exception Rules API](https://apis.io/apis/cisco-ise/cisco-ise-device-administration-authorization-exception-rules-api/) — The Device Administration - Authorization Exception Rules API from Cisco Identity Services Engine — 3 operation(s) for device administration - authorization…
- [Cisco Identity Services Engine Device Administration - Authorization Global Exception Rules API](https://apis.io/apis/cisco-ise/cisco-ise-device-administration-authorization-global-exception-rules-api/) — The Device Administration - Authorization Global Exception Rules API from Cisco Identity Services Engine — 3 operation(s) for device administration -…
- [Cisco Identity Services Engine Device Administration - Authorization Rules API](https://apis.io/apis/cisco-ise/cisco-ise-device-administration-authorization-rules-api/) — The Device Administration - Authorization Rules API from Cisco Identity Services Engine — 3 operation(s) for device administration - authorization rules.
- [Cisco Identity Services Engine Device Administration - Command Sets API](https://apis.io/apis/cisco-ise/cisco-ise-device-administration-command-sets-api/) — The Device Administration - Command Sets API from Cisco Identity Services Engine — 1 operation(s) for device administration - command sets.
- [Cisco Identity Services Engine Device Administration - Conditions API](https://apis.io/apis/cisco-ise/cisco-ise-device-administration-conditions-api/) — The Device Administration - Conditions API from Cisco Identity Services Engine — 6 operation(s) for device administration - conditions.
- [Cisco Identity Services Engine Device Administration - Dictionary Attributes List API](https://apis.io/apis/cisco-ise/cisco-ise-device-administration-dictionary-attributes-list-api/) — The Device Administration - Dictionary Attributes List API from Cisco Identity Services Engine — 3 operation(s) for device administration - dictionary…
- [Cisco Identity Services Engine Device Administration - Identity Stores API](https://apis.io/apis/cisco-ise/cisco-ise-device-administration-identity-stores-api/) — The Device Administration - Identity Stores API from Cisco Identity Services Engine — 1 operation(s) for device administration - identity stores.
- [Cisco Identity Services Engine Device Administration - Network Conditions API](https://apis.io/apis/cisco-ise/cisco-ise-device-administration-network-conditions-api/) — The Device Administration - Network Conditions API from Cisco Identity Services Engine — 2 operation(s) for device administration - network conditions.
- [Cisco Identity Services Engine Device Administration - Policy Sets API](https://apis.io/apis/cisco-ise/cisco-ise-device-administration-policy-sets-api/) — The Device Administration - Policy Sets API from Cisco Identity Services Engine — 3 operation(s) for device administration - policy sets.
- [Cisco Identity Services Engine Device Administration - Service Names API](https://apis.io/apis/cisco-ise/cisco-ise-device-administration-service-names-api/) — The Device Administration - Service Names API from Cisco Identity Services Engine — 1 operation(s) for device administration - service names.
- [Cisco Identity Services Engine Device Administration - Shell Profiles API](https://apis.io/apis/cisco-ise/cisco-ise-device-administration-shell-profiles-api/) — The Device Administration - Shell Profiles API from Cisco Identity Services Engine — 1 operation(s) for device administration - shell profiles.
- [Cisco Identity Services Engine Device Administration - Time/Date Conditions API](https://apis.io/apis/cisco-ise/cisco-ise-device-administration-time-date-conditions-api/) — The Device Administration - Time/Date Conditions API from Cisco Identity Services Engine — 2 operation(s) for device administration - time/date conditions.
- [Cisco Identity Services Engine Downloadableacl API](https://apis.io/apis/cisco-ise/cisco-ise-downloadableacl-api/) — The downloadableacl API from Cisco Identity Services Engine — 2 operation(s) for downloadableacl.
- [Cisco Identity Services Engine Duo Identity Sync API](https://apis.io/apis/cisco-ise/cisco-ise-duo-identitysync-api/) — The Duo-IdentitySync API from Cisco Identity Services Engine — 5 operation(s) for duo-identitysync.
- [Cisco Identity Services Engine Duo Mfa API](https://apis.io/apis/cisco-ise/cisco-ise-duo-mfa-api/) — The Duo-Mfa API from Cisco Identity Services Engine — 3 operation(s) for duo-mfa.
- [Cisco Identity Services Engine Egressmatrixcell API](https://apis.io/apis/cisco-ise/cisco-ise-egressmatrixcell-api/) — The egressmatrixcell API from Cisco Identity Services Engine — 13 operation(s) for egressmatrixcell.
- [Cisco Identity Services Engine Enable MFA API](https://apis.io/apis/cisco-ise/cisco-ise-enable-mfa-api/) — The enable-MFA API from Cisco Identity Services Engine — 1 operation(s) for enable-mfa.
- [Cisco Identity Services Engine Endpoint API](https://apis.io/apis/cisco-ise/cisco-ise-endpoint-api/) — The endpoint API from Cisco Identity Services Engine — 7 operation(s) for endpoint.
- [Cisco Identity Services Engine Endpoint Stop Replication Service API](https://apis.io/apis/cisco-ise/cisco-ise-endpoint-stop-replication-service-api/) — The Endpoint Stop Replication Service API from Cisco Identity Services Engine — 1 operation(s) for endpoint stop replication service.
- [Cisco Identity Services Engine Endpointcert API](https://apis.io/apis/cisco-ise/cisco-ise-endpointcert-api/) — The endpointcert API from Cisco Identity Services Engine — 1 operation(s) for endpointcert.
- [Cisco Identity Services Engine Endpointcertificate API](https://apis.io/apis/cisco-ise/cisco-ise-endpointcertificate-api/) — The endpointcertificate API from Cisco Identity Services Engine — 2 operation(s) for endpointcertificate.
- [Cisco Identity Services Engine Endpoints API](https://apis.io/apis/cisco-ise/cisco-ise-endpoints-api/) — The endpoints API from Cisco Identity Services Engine — 5 operation(s) for endpoints.
- [Cisco Identity Services Engine Export Posture API](https://apis.io/apis/cisco-ise/cisco-ise-export-posture-api/) — The Export-Posture API from Cisco Identity Services Engine — 6 operation(s) for export-posture.
- [Cisco Identity Services Engine External Connection API](https://apis.io/apis/cisco-ise/cisco-ise-external-connection-api/) — The External Connection API from Cisco Identity Services Engine — 1 operation(s) for external connection.
- [Cisco Identity Services Engine Externalradiusserver API](https://apis.io/apis/cisco-ise/cisco-ise-externalradiusserver-api/) — The externalradiusserver API from Cisco Identity Services Engine — 3 operation(s) for externalradiusserver.
- [Cisco Identity Services Engine Failure Reasons API](https://apis.io/apis/cisco-ise/cisco-ise-failurereasons-api/) — The FailureReasons API from Cisco Identity Services Engine — 1 operation(s) for failurereasons.
- [Cisco Identity Services Engine Filterpolicy API](https://apis.io/apis/cisco-ise/cisco-ise-filterpolicy-api/) — The filterpolicy API from Cisco Identity Services Engine — 2 operation(s) for filterpolicy.
- [Cisco Identity Services Engine Guestlocation API](https://apis.io/apis/cisco-ise/cisco-ise-guestlocation-api/) — The guestlocation API from Cisco Identity Services Engine — 5 operation(s) for guestlocation.
- [Cisco Identity Services Engine Guestsmtpnotificationsettings API](https://apis.io/apis/cisco-ise/cisco-ise-guestsmtpnotificationsettings-api/) — The guestsmtpnotificationsettings API from Cisco Identity Services Engine — 2 operation(s) for guestsmtpnotificationsettings.
- [Cisco Identity Services Engine Guestssid API](https://apis.io/apis/cisco-ise/cisco-ise-guestssid-api/) — The guestssid API from Cisco Identity Services Engine — 2 operation(s) for guestssid.
- [Cisco Identity Services Engine Guesttype API](https://apis.io/apis/cisco-ise/cisco-ise-guesttype-api/) — The guesttype API from Cisco Identity Services Engine — 4 operation(s) for guesttype.
- [Cisco Identity Services Engine Hotspotportal API](https://apis.io/apis/cisco-ise/cisco-ise-hotspotportal-api/) — The hotspotportal API from Cisco Identity Services Engine — 2 operation(s) for hotspotportal.
- [Cisco Identity Services Engine Identitygroup API](https://apis.io/apis/cisco-ise/cisco-ise-identitygroup-api/) — The identitygroup API from Cisco Identity Services Engine — 3 operation(s) for identitygroup.
- [Cisco Identity Services Engine Identitygroups API](https://apis.io/apis/cisco-ise/cisco-ise-identitygroups-api/) — The identitygroups API from Cisco Identity Services Engine — 4 operation(s) for identitygroups.
- [Cisco Identity Services Engine Idstoresequence API](https://apis.io/apis/cisco-ise/cisco-ise-idstoresequence-api/) — The idstoresequence API from Cisco Identity Services Engine — 3 operation(s) for idstoresequence.
- [Cisco Identity Services Engine Import Posture API](https://apis.io/apis/cisco-ise/cisco-ise-import-posture-api/) — The Import-Posture API from Cisco Identity Services Engine — 16 operation(s) for import-posture.
- [Cisco Identity Services Engine Inbound Rule API](https://apis.io/apis/cisco-ise/cisco-ise-inbound-rule-api/) — The Inbound Rule API from Cisco Identity Services Engine — 5 operation(s) for inbound rule.
- [Cisco Identity Services Engine Internaluser API](https://apis.io/apis/cisco-ise/cisco-ise-internaluser-api/) — The internaluser API from Cisco Identity Services Engine — 7 operation(s) for internaluser.
- [Cisco Identity Services Engine Is MFA Enabled API](https://apis.io/apis/cisco-ise/cisco-ise-is-mfa-enabled-api/) — The is-MFA-Enabled API from Cisco Identity Services Engine — 1 operation(s) for is-mfa-enabled.
- [Cisco Identity Services Engine Ldap API](https://apis.io/apis/cisco-ise/cisco-ise-ldap-api/) — The ldap API from Cisco Identity Services Engine — 8 operation(s) for ldap.
- [Cisco Identity Services Engine Licensing API](https://apis.io/apis/cisco-ise/cisco-ise-licensing-api/) — The Licensing API from Cisco Identity Services Engine — 7 operation(s) for licensing.
- [Cisco Identity Services Engine Mdm Action API](https://apis.io/apis/cisco-ise/cisco-ise-mdm-action-api/) — The mdm-action API from Cisco Identity Services Engine — 2 operation(s) for mdm-action.
- [Cisco Identity Services Engine Mdm Device Attributes API](https://apis.io/apis/cisco-ise/cisco-ise-mdm-device-attributes-api/) — The mdm-device-attributes API from Cisco Identity Services Engine — 3 operation(s) for mdm-device-attributes.
- [Cisco Identity Services Engine Mdm Messaging API](https://apis.io/apis/cisco-ise/cisco-ise-mdm-messaging-api/) — The mdm-messaging API from Cisco Identity Services Engine — 2 operation(s) for mdm-messaging.
- [Cisco Identity Services Engine Mdm Server Info API](https://apis.io/apis/cisco-ise/cisco-ise-mdm-server-info-api/) — The mdm-server-info API from Cisco Identity Services Engine — 2 operation(s) for mdm-server-info.
- [Cisco Identity Services Engine Menu Access API](https://apis.io/apis/cisco-ise/cisco-ise-menu-access-api/) — The Menu Access API from Cisco Identity Services Engine — 2 operation(s) for menu access.
- [Cisco Identity Services Engine Mydeviceportal API](https://apis.io/apis/cisco-ise/cisco-ise-mydeviceportal-api/) — The mydeviceportal API from Cisco Identity Services Engine — 2 operation(s) for mydeviceportal.
- [Cisco Identity Services Engine Native IPsec API](https://apis.io/apis/cisco-ise/cisco-ise-native-ipsec-api/) — The Native IPsec API from Cisco Identity Services Engine — 6 operation(s) for native ipsec.
- [Cisco Identity Services Engine NBAR Application Management API](https://apis.io/apis/cisco-ise/cisco-ise-nbar-application-management-api/) — The NBAR Application Management API from Cisco Identity Services Engine — 2 operation(s) for nbar application management.
- [Cisco Identity Services Engine Network Access - Authentication Rules API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-authentication-rules-api/) — The Network Access - Authentication Rules API from Cisco Identity Services Engine — 3 operation(s) for network access - authentication rules.
- [Cisco Identity Services Engine Network Access - Authorization Exception Rules API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-authorization-exception-rules-api/) — The Network Access - Authorization Exception Rules API from Cisco Identity Services Engine — 3 operation(s) for network access - authorization exception rules.
- [Cisco Identity Services Engine Network Access - Authorization Global Exception Rules API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-authorization-global-exception-rules-api/) — The Network Access - Authorization Global Exception Rules API from Cisco Identity Services Engine — 3 operation(s) for network access - authorization global…
- [Cisco Identity Services Engine Network Access - Authorization Profiles API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-authorization-profiles-api/) — The Network Access - Authorization Profiles API from Cisco Identity Services Engine — 1 operation(s) for network access - authorization profiles.
- [Cisco Identity Services Engine Network Access - Authorization Rules API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-authorization-rules-api/) — The Network Access - Authorization Rules API from Cisco Identity Services Engine — 3 operation(s) for network access - authorization rules.
- [Cisco Identity Services Engine Network Access - Conditions API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-conditions-api/) — The Network Access - Conditions API from Cisco Identity Services Engine — 6 operation(s) for network access - conditions.
- [Cisco Identity Services Engine Network Access - Dictionaries API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-dictionaries-api/) — The Network Access - Dictionaries API from Cisco Identity Services Engine — 2 operation(s) for network access - dictionaries.
- [Cisco Identity Services Engine Network Access - Dictionary Attributes API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-dictionary-attributes-api/) — The Network Access - Dictionary Attributes API from Cisco Identity Services Engine — 2 operation(s) for network access - dictionary attributes.
- [Cisco Identity Services Engine Network Access - Dictionary Attributes List API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-dictionary-attributes-list-api/) — The Network Access - Dictionary Attributes List API from Cisco Identity Services Engine — 3 operation(s) for network access - dictionary attributes list.
- [Cisco Identity Services Engine Network Access - Identity Stores API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-identity-stores-api/) — The Network Access - Identity Stores API from Cisco Identity Services Engine — 1 operation(s) for network access - identity stores.
- [Cisco Identity Services Engine Network Access - MFA Rules API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-mfa-rules-api/) — The Network Access - MFA Rules API from Cisco Identity Services Engine — 3 operation(s) for network access - mfa rules.
- [Cisco Identity Services Engine Network Access - Network Conditions API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-network-conditions-api/) — The Network Access - Network Conditions API from Cisco Identity Services Engine — 2 operation(s) for network access - network conditions.
- [Cisco Identity Services Engine Network Access - Policy Sets API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-policy-sets-api/) — The Network Access - Policy Sets API from Cisco Identity Services Engine — 3 operation(s) for network access - policy sets.
- [Cisco Identity Services Engine Network Access - Security Groups API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-security-groups-api/) — The Network Access - Security Groups API from Cisco Identity Services Engine — 1 operation(s) for network access - security groups.
- [Cisco Identity Services Engine Network Access - Service Names API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-service-names-api/) — The Network Access - Service Names API from Cisco Identity Services Engine — 1 operation(s) for network access - service names.
- [Cisco Identity Services Engine Network Access - Time/Date Conditions API](https://apis.io/apis/cisco-ise/cisco-ise-network-access-time-date-conditions-api/) — The Network Access - Time/Date Conditions API from Cisco Identity Services Engine — 2 operation(s) for network access - time/date conditions.
- [Cisco Identity Services Engine Networkdevice API](https://apis.io/apis/cisco-ise/cisco-ise-networkdevice-api/) — The networkdevice API from Cisco Identity Services Engine — 9 operation(s) for networkdevice.
- [Cisco Identity Services Engine Networkdevicegroup API](https://apis.io/apis/cisco-ise/cisco-ise-networkdevicegroup-api/) — The networkdevicegroup API from Cisco Identity Services Engine — 3 operation(s) for networkdevicegroup.
- [Cisco Identity Services Engine Node API](https://apis.io/apis/cisco-ise/cisco-ise-node-api/) — The node API from Cisco Identity Services Engine — 7 operation(s) for node.
- [Cisco Identity Services Engine Node Deployment API](https://apis.io/apis/cisco-ise/cisco-ise-node-deployment-api/) — The Node Deployment API from Cisco Identity Services Engine — 6 operation(s) for node deployment.
- [Cisco Identity Services Engine Node Group API](https://apis.io/apis/cisco-ise/cisco-ise-node-group-api/) — The Node Group API from Cisco Identity Services Engine — 5 operation(s) for node group.
- [Cisco Identity Services Engine Node Services API](https://apis.io/apis/cisco-ise/cisco-ise-node-services-api/) — The Node Services API from Cisco Identity Services Engine — 3 operation(s) for node services.
- [Cisco Identity Services Engine Nspprofile API](https://apis.io/apis/cisco-ise/cisco-ise-nspprofile-api/) — The nspprofile API from Cisco Identity Services Engine — 2 operation(s) for nspprofile.
- [Cisco Identity Services Engine OIDC API](https://apis.io/apis/cisco-ise/cisco-ise-oidc-api/) — The OIDC API from Cisco Identity Services Engine — 6 operation(s) for oidc.
- [Cisco Identity Services Engine Outbound Rule API](https://apis.io/apis/cisco-ise/cisco-ise-outbound-rule-api/) — The Outbound Rule API from Cisco Identity Services Engine — 4 operation(s) for outbound rule.
- [Cisco Identity Services Engine PAN HA API](https://apis.io/apis/cisco-ise/cisco-ise-pan-ha-api/) — The PAN HA API from Cisco Identity Services Engine — 1 operation(s) for pan ha.
- [Cisco Identity Services Engine Patch API](https://apis.io/apis/cisco-ise/cisco-ise-patch-api/) — The Patch API from Cisco Identity Services Engine — 11 operation(s) for patch.
- [Cisco Identity Services Engine Patching API](https://apis.io/apis/cisco-ise/cisco-ise-patching-api/) — The Patching API from Cisco Identity Services Engine — 6 operation(s) for patching.
- [Cisco Identity Services Engine Portal API](https://apis.io/apis/cisco-ise/cisco-ise-portal-api/) — The portal API from Cisco Identity Services Engine — 5 operation(s) for portal.
- [Cisco Identity Services Engine Portalglobalsetting API](https://apis.io/apis/cisco-ise/cisco-ise-portalglobalsetting-api/) — The portalglobalsetting API from Cisco Identity Services Engine — 5 operation(s) for portalglobalsetting.
- [Cisco Identity Services Engine Portaltheme API](https://apis.io/apis/cisco-ise/cisco-ise-portaltheme-api/) — The portaltheme API from Cisco Identity Services Engine — 2 operation(s) for portaltheme.
- [Cisco Identity Services Engine Profiler Policy Management (Custom/Direct/ML -Rules) API](https://apis.io/apis/cisco-ise/cisco-ise-profiler-policy-management-custom-direct-ml-rules-api/) — The Profiler Policy Management (Custom/Direct/ML -Rules) API from Cisco Identity Services Engine — 7 operation(s) for profiler policy management…
- [Cisco Identity Services Engine Profilerprofile API](https://apis.io/apis/cisco-ise/cisco-ise-profilerprofile-api/) — The profilerprofile API from Cisco Identity Services Engine — 5 operation(s) for profilerprofile.
- [Cisco Identity Services Engine Prometheus Alertmanager API](https://apis.io/apis/cisco-ise/cisco-ise-prometheus-alertmanager-api/) — The Prometheus Alertmanager API from Cisco Identity Services Engine — 7 operation(s) for prometheus alertmanager.
- [Cisco Identity Services Engine Proxy API](https://apis.io/apis/cisco-ise/cisco-ise-proxy-api/) — The proxy API from Cisco Identity Services Engine — 1 operation(s) for proxy.
- [Cisco Identity Services Engine Pulldeploymentinfo API](https://apis.io/apis/cisco-ise/cisco-ise-pulldeploymentinfo-api/) — The pulldeploymentinfo API from Cisco Identity Services Engine — 2 operation(s) for pulldeploymentinfo.
- [Cisco Identity Services Engine pxGrid Cloud API](https://apis.io/apis/cisco-ise/cisco-ise-pxgrid-cloud-api/) — The pxGrid Cloud API from Cisco Identity Services Engine — 5 operation(s) for pxgrid cloud.
- [Cisco Identity Services Engine pxGrid Direct API](https://apis.io/apis/cisco-ise/cisco-ise-pxgrid-direct-api/) — The pxGrid Direct API from Cisco Identity Services Engine — 6 operation(s) for pxgrid direct.
- [Cisco Identity Services Engine pxGrid Direct Push APIs API](https://apis.io/apis/cisco-ise/cisco-ise-pxgrid-direct-push-apis-api/) — The pxGrid Direct Push APIs API from Cisco Identity Services Engine — 3 operation(s) for pxgrid direct push apis.
- [Cisco Identity Services Engine Pxgridnode API](https://apis.io/apis/cisco-ise/cisco-ise-pxgridnode-api/) — The pxgridnode API from Cisco Identity Services Engine — 4 operation(s) for pxgridnode.
- [Cisco Identity Services Engine Pxgridsettings API](https://apis.io/apis/cisco-ise/cisco-ise-pxgridsettings-api/) — The pxgridsettings API from Cisco Identity Services Engine — 3 operation(s) for pxgridsettings.
- [Cisco Identity Services Engine Radiusserversequence API](https://apis.io/apis/cisco-ise/cisco-ise-radiusserversequence-api/) — The radiusserversequence API from Cisco Identity Services Engine — 2 operation(s) for radiusserversequence.
- [Cisco Identity Services Engine RBAC Policy API](https://apis.io/apis/cisco-ise/cisco-ise-rbac-policy-api/) — The RBAC Policy API from Cisco Identity Services Engine — 2 operation(s) for rbac policy.
- [Cisco Identity Services Engine Reportconfig API](https://apis.io/apis/cisco-ise/cisco-ise-reportconfig-api/) — The reportconfig API from Cisco Identity Services Engine — 3 operation(s) for reportconfig.
- [Cisco Identity Services Engine Repository API](https://apis.io/apis/cisco-ise/cisco-ise-repository-api/) — The Repository API from Cisco Identity Services Engine — 3 operation(s) for repository.
- [Cisco Identity Services Engine Restidstore API](https://apis.io/apis/cisco-ise/cisco-ise-restidstore-api/) — The restidstore API from Cisco Identity Services Engine — 7 operation(s) for restidstore.
- [Cisco Identity Services Engine Restidstoreattribute API](https://apis.io/apis/cisco-ise/cisco-ise-restidstoreattribute-api/) — The restidstoreattribute API from Cisco Identity Services Engine — 2 operation(s) for restidstoreattribute.
- [Cisco Identity Services Engine Restidstoredeviceattribute API](https://apis.io/apis/cisco-ise/cisco-ise-restidstoredeviceattribute-api/) — The restidstoredeviceattribute API from Cisco Identity Services Engine — 2 operation(s) for restidstoredeviceattribute.
- [Cisco Identity Services Engine Restidstoregroup API](https://apis.io/apis/cisco-ise/cisco-ise-restidstoregroup-api/) — The restidstoregroup API from Cisco Identity Services Engine — 2 operation(s) for restidstoregroup.
- [Cisco Identity Services Engine Restidstorepredefinedregex API](https://apis.io/apis/cisco-ise/cisco-ise-restidstorepredefinedregex-api/) — The restidstorepredefinedregex API from Cisco Identity Services Engine — 3 operation(s) for restidstorepredefinedregex.
- [Cisco Identity Services Engine Restidstoresettings API](https://apis.io/apis/cisco-ise/cisco-ise-restidstoresettings-api/) — The restidstoresettings API from Cisco Identity Services Engine — 4 operation(s) for restidstoresettings.
- [Cisco Identity Services Engine Rule Flow API](https://apis.io/apis/cisco-ise/cisco-ise-rule-flow-api/) — The Rule Flow API from Cisco Identity Services Engine — 1 operation(s) for rule flow.
- [Cisco Identity Services Engine Rule Summary API](https://apis.io/apis/cisco-ise/cisco-ise-rule-summary-api/) — The Rule Summary API from Cisco Identity Services Engine — 1 operation(s) for rule summary.
- [Cisco Identity Services Engine Security Group Management API](https://apis.io/apis/cisco-ise/cisco-ise-security-group-management-api/) — The Security Group Management API from Cisco Identity Services Engine — 1 operation(s) for security group management.
- [Cisco Identity Services Engine Selfregportal API](https://apis.io/apis/cisco-ise/cisco-ise-selfregportal-api/) — The selfregportal API from Cisco Identity Services Engine — 2 operation(s) for selfregportal.
- [Cisco Identity Services Engine Service API](https://apis.io/apis/cisco-ise/cisco-ise-service-api/) — The service API from Cisco Identity Services Engine — 2 operation(s) for service.
- [Cisco Identity Services Engine Session API](https://apis.io/apis/cisco-ise/cisco-ise-session-api/) — The Session API from Cisco Identity Services Engine — 13 operation(s) for session.
- [Cisco Identity Services Engine Sessionservicenode API](https://apis.io/apis/cisco-ise/cisco-ise-sessionservicenode-api/) — The sessionservicenode API from Cisco Identity Services Engine — 7 operation(s) for sessionservicenode.
- [Cisco Identity Services Engine Sgacl API](https://apis.io/apis/cisco-ise/cisco-ise-sgacl-api/) — The sgacl API from Cisco Identity Services Engine — 7 operation(s) for sgacl.
- [Cisco Identity Services Engine Sgacls API](https://apis.io/apis/cisco-ise/cisco-ise-sgacls-api/) — The sgacls API from Cisco Identity Services Engine — 3 operation(s) for sgacls.
- [Cisco Identity Services Engine Sgmapping API](https://apis.io/apis/cisco-ise/cisco-ise-sgmapping-api/) — The sgmapping API from Cisco Identity Services Engine — 13 operation(s) for sgmapping.
- [Cisco Identity Services Engine Sgmappinggroup API](https://apis.io/apis/cisco-ise/cisco-ise-sgmappinggroup-api/) — The sgmappinggroup API from Cisco Identity Services Engine — 13 operation(s) for sgmappinggroup.
- [Cisco Identity Services Engine Sgt API](https://apis.io/apis/cisco-ise/cisco-ise-sgt-api/) — The sgt API from Cisco Identity Services Engine — 3 operation(s) for sgt.
- [Cisco Identity Services Engine Sgt Range Reservation API](https://apis.io/apis/cisco-ise/cisco-ise-sgtrangereservation-api/) — The SgtRangeReservation API from Cisco Identity Services Engine — 3 operation(s) for sgtrangereservation.
- [Cisco Identity Services Engine Sgtvnvlan API](https://apis.io/apis/cisco-ise/cisco-ise-sgtvnvlan-api/) — The sgtvnvlan API from Cisco Identity Services Engine — 7 operation(s) for sgtvnvlan.
- [Cisco Identity Services Engine Shared Mappings API](https://apis.io/apis/cisco-ise/cisco-ise-shared-mappings-api/) — The Shared Mappings API from Cisco Identity Services Engine — 1 operation(s) for shared mappings.
- [Cisco Identity Services Engine Smsprovider API](https://apis.io/apis/cisco-ise/cisco-ise-smsprovider-api/) — The smsprovider API from Cisco Identity Services Engine — 4 operation(s) for smsprovider.
- [Cisco Identity Services Engine Sponsoredguestportal API](https://apis.io/apis/cisco-ise/cisco-ise-sponsoredguestportal-api/) — The sponsoredguestportal API from Cisco Identity Services Engine — 2 operation(s) for sponsoredguestportal.
- [Cisco Identity Services Engine Sponsorgroup API](https://apis.io/apis/cisco-ise/cisco-ise-sponsorgroup-api/) — The sponsorgroup API from Cisco Identity Services Engine — 2 operation(s) for sponsorgroup.
- [Cisco Identity Services Engine Sponsorgroupmember API](https://apis.io/apis/cisco-ise/cisco-ise-sponsorgroupmember-api/) — The sponsorgroupmember API from Cisco Identity Services Engine — 4 operation(s) for sponsorgroupmember.
- [Cisco Identity Services Engine Sponsorportal API](https://apis.io/apis/cisco-ise/cisco-ise-sponsorportal-api/) — The sponsorportal API from Cisco Identity Services Engine — 2 operation(s) for sponsorportal.
- [Cisco Identity Services Engine Subscriber API](https://apis.io/apis/cisco-ise/cisco-ise-subscriber-api/) — The Subscriber API from Cisco Identity Services Engine — 4 operation(s) for subscriber.
- [Cisco Identity Services Engine Supportbundledownload API](https://apis.io/apis/cisco-ise/cisco-ise-supportbundledownload-api/) — The supportbundledownload API from Cisco Identity Services Engine — 3 operation(s) for supportbundledownload.
- [Cisco Identity Services Engine Supportbundlestatus API](https://apis.io/apis/cisco-ise/cisco-ise-supportbundlestatus-api/) — The supportbundlestatus API from Cisco Identity Services Engine — 2 operation(s) for supportbundlestatus.
- [Cisco Identity Services Engine Supportbundletriggerconfiguration API](https://apis.io/apis/cisco-ise/cisco-ise-supportbundletriggerconfiguration-api/) — The supportbundletriggerconfiguration API from Cisco Identity Services Engine — 2 operation(s) for supportbundletriggerconfiguration.
- [Cisco Identity Services Engine SXP API](https://apis.io/apis/cisco-ise/cisco-ise-sxp-api/) — The SXP API from Cisco Identity Services Engine — 3 operation(s) for sxp.
- [Cisco Identity Services Engine SXP Domains with mapping and devices counts API](https://apis.io/apis/cisco-ise/cisco-ise-sxp-domains-with-mapping-and-devices-counts-api/) — The SXP Domains with mapping and devices counts API from Cisco Identity Services Engine — 1 operation(s) for sxp domains with mapping and devices counts.
- [Cisco Identity Services Engine Sxpconnections API](https://apis.io/apis/cisco-ise/cisco-ise-sxpconnections-api/) — The sxpconnections API from Cisco Identity Services Engine — 7 operation(s) for sxpconnections.
- [Cisco Identity Services Engine Sxplocalbindings API](https://apis.io/apis/cisco-ise/cisco-ise-sxplocalbindings-api/) — The sxplocalbindings API from Cisco Identity Services Engine — 7 operation(s) for sxplocalbindings.
- [Cisco Identity Services Engine Sxpvpns API](https://apis.io/apis/cisco-ise/cisco-ise-sxpvpns-api/) — The sxpvpns API from Cisco Identity Services Engine — 7 operation(s) for sxpvpns.
- [Cisco Identity Services Engine Systemcertificate API](https://apis.io/apis/cisco-ise/cisco-ise-systemcertificate-api/) — The systemcertificate API from Cisco Identity Services Engine — 3 operation(s) for systemcertificate.
- [Cisco Identity Services Engine Tacacscommandsets API](https://apis.io/apis/cisco-ise/cisco-ise-tacacscommandsets-api/) — The tacacscommandsets API from Cisco Identity Services Engine — 3 operation(s) for tacacscommandsets.
- [Cisco Identity Services Engine Tacacsexternalservers API](https://apis.io/apis/cisco-ise/cisco-ise-tacacsexternalservers-api/) — The tacacsexternalservers API from Cisco Identity Services Engine — 3 operation(s) for tacacsexternalservers.
- [Cisco Identity Services Engine Tacacsprofile API](https://apis.io/apis/cisco-ise/cisco-ise-tacacsprofile-api/) — The tacacsprofile API from Cisco Identity Services Engine — 3 operation(s) for tacacsprofile.
- [Cisco Identity Services Engine Tacacsserversequence API](https://apis.io/apis/cisco-ise/cisco-ise-tacacsserversequence-api/) — The tacacsserversequence API from Cisco Identity Services Engine — 3 operation(s) for tacacsserversequence.
- [Cisco Identity Services Engine Tasks API](https://apis.io/apis/cisco-ise/cisco-ise-tasks-api/) — The tasks API from Cisco Identity Services Engine — 2 operation(s) for tasks.
- [Cisco Identity Services Engine Telemetry API](https://apis.io/apis/cisco-ise/cisco-ise-telemetry-api/) — The telemetry API from Cisco Identity Services Engine — 1 operation(s) for telemetry.
- [Cisco Identity Services Engine Telemetryinfo API](https://apis.io/apis/cisco-ise/cisco-ise-telemetryinfo-api/) — The telemetryinfo API from Cisco Identity Services Engine — 2 operation(s) for telemetryinfo.
- [Cisco Identity Services Engine Telemetryinformation API](https://apis.io/apis/cisco-ise/cisco-ise-telemetryinformation-api/) — The telemetryinformation API from Cisco Identity Services Engine — 3 operation(s) for telemetryinformation.
- [Cisco Identity Services Engine Threat API](https://apis.io/apis/cisco-ise/cisco-ise-threat-api/) — The threat API from Cisco Identity Services Engine — 1 operation(s) for threat.
- [Cisco Identity Services Engine Trustsec COA Push API](https://apis.io/apis/cisco-ise/cisco-ise-trustsec-coa-push-api/) — The Trustsec COA Push API from Cisco Identity Services Engine — 1 operation(s) for trustsec coa push.
- [Cisco Identity Services Engine Trustsec devices report API](https://apis.io/apis/cisco-ise/cisco-ise-trustsec-devices-report-api/) — The Trustsec devices report API from Cisco Identity Services Engine — 2 operation(s) for trustsec devices report.
- [Cisco Identity Services Engine Trustsec HTTPS Server API](https://apis.io/apis/cisco-ise/cisco-ise-trustsec-https-server-api/) — The Trustsec HTTPS Server API from Cisco Identity Services Engine — 2 operation(s) for trustsec https server.
- [Cisco Identity Services Engine Trustsec Integration Rule - Default Trustsec Integration Rule set API](https://apis.io/apis/cisco-ise/cisco-ise-trustsec-integration-rule-default-trustsec-integration-rule-set-api/) — The Trustsec Integration Rule - Default Trustsec Integration Rule set API from Cisco Identity Services Engine — 1 operation(s) for trustsec integration rule…
- [Cisco Identity Services Engine Trustsec Integration Rule - Dictionaries API](https://apis.io/apis/cisco-ise/cisco-ise-trustsec-integration-rule-dictionaries-api/) — The Trustsec Integration Rule - Dictionaries API from Cisco Identity Services Engine — 3 operation(s) for trustsec integration rule - dictionaries.
- [Cisco Identity Services Engine Trustsec Integration Rule - Dictionary Attributes API](https://apis.io/apis/cisco-ise/cisco-ise-trustsec-integration-rule-dictionary-attributes-api/) — The Trustsec Integration Rule - Dictionary Attributes API from Cisco Identity Services Engine — 6 operation(s) for trustsec integration rule - dictionary…
- [Cisco Identity Services Engine Trustsec Matrix API](https://apis.io/apis/cisco-ise/cisco-ise-trustsec-matrix-api/) — The Trustsec Matrix API from Cisco Identity Services Engine — 6 operation(s) for trustsec matrix.
- [Cisco Identity Services Engine TrustSec OpenAPI View API](https://apis.io/apis/cisco-ise/cisco-ise-trustsec-openapi-view-api/) — The TrustSec OpenAPI View API from Cisco Identity Services Engine — 2 operation(s) for trustsec openapi view.
- [Cisco Identity Services Engine Trustsec Settings API](https://apis.io/apis/cisco-ise/cisco-ise-trustsec-settings-api/) — The Trustsec Settings API from Cisco Identity Services Engine — 1 operation(s) for trustsec settings.
- [Cisco Identity Services Engine Upgrade API](https://apis.io/apis/cisco-ise/cisco-ise-upgrade-api/) — The Upgrade API from Cisco Identity Services Engine — 8 operation(s) for upgrade.
- [Cisco Identity Services Engine User Equipment API](https://apis.io/apis/cisco-ise/cisco-ise-user-equipment-api/) — The User Equipment API from Cisco Identity Services Engine — 6 operation(s) for user equipment.
- [Cisco Identity Services Engine Version API](https://apis.io/apis/cisco-ise/cisco-ise-version-api/) — The Version API from Cisco Identity Services Engine — 1 operation(s) for version.
- [Cisco Identity Services Engine Versionandpatch API](https://apis.io/apis/cisco-ise/cisco-ise-versionandpatch-api/) — The versionandpatch API from Cisco Identity Services Engine — 1 operation(s) for versionandpatch.
- [Cisco Identity Services Engine Virtual Network Management API](https://apis.io/apis/cisco-ise/cisco-ise-virtual-network-management-api/) — The Virtual Network Management API from Cisco Identity Services Engine — 5 operation(s) for virtual network management.
- [Cisco Identity Services Engine WebhookConfigurations Services API](https://apis.io/apis/cisco-ise/cisco-ise-webhookconfigurations-services-api/) — The WebhookConfigurations Services API from Cisco Identity Services Engine — 7 operation(s) for webhookconfigurations services.
- [Cisco Identity Services Engine Work Process Settings API](https://apis.io/apis/cisco-ise/cisco-ise-work-process-settings-api/) — The Work Process Settings API from Cisco Identity Services Engine — 1 operation(s) for work process settings.
- [Cisco Identity Services Engine Workload Connection API](https://apis.io/apis/cisco-ise/cisco-ise-workload-connection-api/) — The Workload Connection API from Cisco Identity Services Engine — 30 operation(s) for workload connection.
- [Cisco Identity Services Engine Guestsmtpnotificationconfiguration API](https://apis.io/apis/cisco-ise/cisco-ise-guestsmtpnotificationconfiguration-api/) — The guestsmtpnotificationconfiguration API from Cisco Identity Services Engine — 3 operation(s) for guestsmtpnotificationconfiguration.
- [Cisco Identity Services Engine Active Directory API](https://apis.io/apis/cisco-ise/cisco-ise-active-directory-api/) — The Active Directory API from Cisco Identity Services Engine — 29 operation(s) for active directory.
- [Cisco Identity Services Engine Ad Groups API](https://apis.io/apis/cisco-ise/cisco-ise-ad-groups-api/) — The Ad Groups API from Cisco Identity Services Engine — 1 operation(s) for ad groups.
- [Cisco Identity Services Engine Admin User API](https://apis.io/apis/cisco-ise/cisco-ise-admin-user-api/) — The Admin User API from Cisco Identity Services Engine — 11 operation(s) for admin user.
- [Cisco Identity Services Engine Custom Attributes API](https://apis.io/apis/cisco-ise/cisco-ise-custom-attributes-api/) — The Custom Attributes API from Cisco Identity Services Engine — 3 operation(s) for custom attributes.
- [Cisco Identity Services Engine Deployment Info API](https://apis.io/apis/cisco-ise/cisco-ise-deployment-info-api/) — The Deployment Info API from Cisco Identity Services Engine — 1 operation(s) for deployment info.
- [Cisco Identity Services Engine Endpoint Group API](https://apis.io/apis/cisco-ise/cisco-ise-endpoint-group-api/) — The Endpoint Group API from Cisco Identity Services Engine — 7 operation(s) for endpoint group.
- [Cisco Identity Services Engine Guest User API](https://apis.io/apis/cisco-ise/cisco-ise-guest-user-api/) — The Guest User API from Cisco Identity Services Engine — 29 operation(s) for guest user.
- [Cisco Identity Services Engine support Bundle API](https://apis.io/apis/cisco-ise/cisco-ise-support-bundle-api/) — The support Bundle API from Cisco Identity Services Engine — 1 operation(s) for support bundle.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### AsyncAPI (1)

Event-driven and webhook contracts.

- [Cisco Ise Webhooks](https://apis.io/asyncapis/cisco-ise/cisco-ise-webhooks/)

#### Overlays (32)

OpenAPI overlays, including conversational phrasing for each operation.

- [Cisco Ise Ers Open Api Ers Apis Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-ers-open-api-ers-apis-overlay/)
- [Cisco Ise Monitoring Open Api Monitoring Open Api Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-monitoring-open-api-monitoring-open-api-overlay/)
- [Cisco Ise Open Api 5G Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-5g-overlay/)
- [Cisco Ise Open Api Alarms Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-alarms-overlay/)
- [Cisco Ise Open Api Api Sgt Reservation Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-api-sgt-reservation-overlay/)
- [Cisco Ise Open Api Backuprestore Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-backuprestore-overlay/)
- [Cisco Ise Open Api Certificates Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-certificates-overlay/)
- [Cisco Ise Open Api Custom Attributes Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-custom-attributes-overlay/)
- [Cisco Ise Open Api Data Connect Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-data-connect-overlay/)
- [Cisco Ise Open Api Deployment Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-deployment-overlay/)
- [Cisco Ise Open Api Duo Identity Sync Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-duo-identity-sync-overlay/)
- [Cisco Ise Open Api Endpoint Replication Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-endpoint-replication-overlay/)
- [Cisco Ise Open Api Endpoints Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-endpoints-overlay/)
- [Cisco Ise Open Api Exim Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-exim-overlay/)
- [Cisco Ise Open Api Ipsec Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-ipsec-overlay/)
- [Cisco Ise Open Api Ise Profiler Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-ise-profiler-overlay/)
- [Cisco Ise Open Api Licensing Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-licensing-overlay/)
- [Cisco Ise Open Api Lsd Settings Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-lsd-settings-overlay/)
- [Cisco Ise Open Api Mfa Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-mfa-overlay/)
- [Cisco Ise Open Api Oidc Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-oidc-overlay/)
- [Cisco Ise Open Api Patch Hot Patch Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-patch-hot-patch-overlay/)
- [Cisco Ise Open Api Policy Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-policy-overlay/)
- [Cisco Ise Open Api Prometheus Alertmanager Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-prometheus-alertmanager-overlay/)
- [Cisco Ise Open Api Pxgrid Cloud Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-pxgrid-cloud-overlay/)
- [Cisco Ise Open Api Pxgrid Direct Overlay](https://apis.io/overlays/cisco-ise/cisco-ise-open-api-pxgrid-direct-overlay/)
- …and 7 more published on APIs.io

#### Security (4)

Authentication, trust centre, and vulnerability disclosure.

- [Cisco Ise Authentication](https://apis.io/security/cisco-ise/cisco-ise-authentication/)
- [Cisco Ise Domain Security](https://apis.io/security/cisco-ise/cisco-ise-domain-security/)
- [Cisco Ise Trust Center](https://apis.io/security/cisco-ise/cisco-ise-trust-center/)
- [Cisco Ise Vulnerability Disclosure](https://apis.io/security/cisco-ise/cisco-ise-vulnerability-disclosure/)

#### Plans and pricing (1)

Published plans, tiers and prices.

- [Cisco Ise Plans Pricing](https://apis.io/plans/cisco-ise/cisco-ise-plans-pricing/)

#### Rate limits (1)

Published request limits.

- [Cisco Ise Rate Limits](https://apis.io/rate-limits/cisco-ise/cisco-ise-rate-limits/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.cisco.com/site/us/en/products/security/identity-services-engine/index.html)
- [Documentation](https://developer.cisco.com/docs/identity-services-engine/latest/)
- [Getting started](https://developer.cisco.com/docs/identity-services-engine/latest/setting-up/)
- [API reference](https://developer.cisco.com/docs/identity-services-engine/latest/)
- [Pricing](https://www.cisco.com/c/en/us/products/collateral/security/identity-services-engine/guide-c07-656177.html)
- [Support](https://community.cisco.com/t5/network-access-control/bd-p/discussions-network-access-control)
- [Changelog](https://developer.cisco.com/docs/identity-services-engine/latest/changelog/)
- [Blog](https://blogs.cisco.com/tag/cisco-ise)
- [Security](https://sec.cloudapps.cisco.com/security/center/resources/security_vulnerability_policy.html)
- [Compliance](https://www.cisco.com/c/en/us/td/docs/security/ise/3-5/compatibility_doc/b_ise_sdt_35.html)
- [Terms of service](https://www.cisco.com/c/en/us/about/legal/terms-conditions.html)
- [Privacy policy](https://www.cisco.com/c/en/us/about/legal/privacy-full.html)
- [GitHub](https://github.com/CiscoISE)

## API Evangelist rating

**Kin Score 62.5** — strong · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 78.6 |
| Contract quality | 51.2 |
| Contract governance | 4.5 |
| Operational transparency | 65.8 |
| Developer ergonomics | 73.2 |
| Access clarity | 78.9 |

**Agent readiness 37.2** — agent-ready

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | — |
| Reversibility Documented | verified |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | verified |
| Rate Limit Signal | documented (partial credit) |
| Event Surface Described | yes |
| Agent Skills | derived (partial credit) |
| Well Known Catalog | — |
| Consent Identity | — |
| Agent Card | — |
| Dry Run Mode | — |
| Delegated Identity | — |
| Protected Resource Metadata | — |
| Dynamic Client Registration | — |
| Agentic Commerce | — |
| Pagination Ratio | — |
| Operation Distinctiveness | mostly |

**Regulatory alignment 35.3** — Horizontal (data, software, accessibility, platform)

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/cisco-ise/](https://apis.io/providers/cisco-ise/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for Cisco Identity Services Engine: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/cisco-ise/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
