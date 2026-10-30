# MedAdvisor

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

MedAdvisor (MedAdvisor Solutions) is an Australian-founded, ASX-listed medication management and patient engagement technology company whose pharmacy workflow software runs in more than 95% of Australian community pharmacies and reaches over 4 million patients. Its clinician-facing platform - the web-based "MedAdvisor for Pharmacy" that replaced the long-running PlusOne desktop software - handles dispense workflow, medication adherence, appointment and service booking (vaccinations, health checks, scope-of-practice services), e-script (eScript) token handling, refill ordering, and omnichannel patient communication, alongside a consumer medication app. On the developer side MedAdvisor exposes a real, Swagger-documented HTTP REST surface, the Pharmacy Unified API, at pharmacy-unified.api.medadvisor.com.au, including a "3rd-Party Integration" family (partner login, pharmacy lookup, eScript status, and order notification into the pharmacy PlusOne inbox) for third-party widgets and eCommerce integrations. Authentication is a JWT bearer token obtained via a clientId/clientSecret plus Base64-encoded pharmacy credentials exchange; the surface is HL7/HTTP REST rather than HL7 FHIR - no public FHIR CapabilityStatement or SMART-on-FHIR configuration is served. Home market is Australia, positioned as the dominant community-pharmacy engagement layer sitting between dispense systems, pharmaceutical programs, and patients.

**Areas:** Healthcare · Australia · Pharmacy · Medication Management · Medication Adherence · e-Prescribing · eScript · Patient Engagement · Appointment Booking · Digital Health · Healthcare API

## MedAdvisor on APIs.io

Everything profiled for MedAdvisor is published on APIs.io rather than in this repository. Start at the provider page — **[apis.io/providers/medadvisor/](https://apis.io/providers/medadvisor/)** — or go straight to one of the APIs or properties below.

### APIs (14)

- [MedAdvisor 3rd-Party Integration API](https://apis.io/apis/medadvisor/medadvisor-3rd-party-integration-api/) — The 3rd-Party Integration API from MedAdvisor — 4 operation(s) for 3rd-party integration.
- [MedAdvisor Account API](https://apis.io/apis/medadvisor/medadvisor-account-api/) — The Account API from MedAdvisor — 1 operation(s) for account.
- [MedAdvisor Booking API](https://apis.io/apis/medadvisor/medadvisor-booking-api/) — The Booking API from MedAdvisor — 27 operation(s) for booking.
- [MedAdvisor Booking Service API](https://apis.io/apis/medadvisor/medadvisor-bookingservice-api/) — The BookingService API from MedAdvisor — 34 operation(s) for bookingservice.
- [MedAdvisor Calendar Setting API](https://apis.io/apis/medadvisor/medadvisor-calendarsetting-api/) — The CalendarSetting API from MedAdvisor — 6 operation(s) for calendarsetting.
- [MedAdvisor Clinic API](https://apis.io/apis/medadvisor/medadvisor-clinic-api/) — The Clinic API from MedAdvisor — 8 operation(s) for clinic.
- [MedAdvisor Communication API](https://apis.io/apis/medadvisor/medadvisor-communication-api/) — The Communication API from MedAdvisor — 6 operation(s) for communication.
- [MedAdvisor Config API](https://apis.io/apis/medadvisor/medadvisor-config-api/) — The Config API from MedAdvisor — 2 operation(s) for config.
- [MedAdvisor Head Office API](https://apis.io/apis/medadvisor/medadvisor-headoffice-api/) — The HeadOffice API from MedAdvisor — 6 operation(s) for headoffice.
- [MedAdvisor Inbox API](https://apis.io/apis/medadvisor/medadvisor-inbox-api/) — The Inbox API from MedAdvisor — 8 operation(s) for inbox.
- [MedAdvisor Logging API](https://apis.io/apis/medadvisor/medadvisor-logging-api/) — The Logging API from MedAdvisor — 1 operation(s) for logging.
- [MedAdvisor Pharmacist API](https://apis.io/apis/medadvisor/medadvisor-pharmacist-api/) — The Pharmacist API from MedAdvisor — 3 operation(s) for pharmacist.
- [MedAdvisor Pharmacy API](https://apis.io/apis/medadvisor/medadvisor-pharmacy-api/) — The Pharmacy API from MedAdvisor — 31 operation(s) for pharmacy.
- [MedAdvisor Refill Order API](https://apis.io/apis/medadvisor/medadvisor-refillorder-api/) — The RefillOrder API from MedAdvisor — 14 operation(s) for refillorder.

### Published properties

Each property below is a page on APIs.io carrying the machine-readable artifact and what it says.

#### MCP servers (1)

Model Context Protocol servers that expose the API to agents.

- [medadvisor-pharmacy-unified](https://apis.io/servers/medadvisor/medadvisor-pharmacy-unified/)

#### Agentic access (1)

Which operations an agent can call, which act, and which need a human in the loop.

- [Medadvisor Agentic Access](https://apis.io/agentic-access/medadvisor/medadvisor-agentic-access/)

#### Collections (2)

Postman and Open Collection request collections.

- [Pharmacy Unified API v1.0](https://apis.io/collections/medadvisor/open-medadvisor-pharmacy-unified/)
- [Pharmacy Unified API v2.0](https://apis.io/collections/medadvisor/open-medadvisor-pharmacy-unified-v2/)

#### Overlays (2)

OpenAPI overlays, including conversational phrasing for each operation.

- [Medadvisor Pharmacy Unified V1 Overlay](https://apis.io/overlays/medadvisor/medadvisor-pharmacy-unified-v1-overlay/)
- [Medadvisor Pharmacy Unified V2 Overlay](https://apis.io/overlays/medadvisor/medadvisor-pharmacy-unified-v2-overlay/)

#### Security (3)

Authentication, trust centre, and vulnerability disclosure.

- [Medadvisor Authentication](https://apis.io/security/medadvisor/medadvisor-authentication/)
- [Medadvisor Domain Security](https://apis.io/security/medadvisor/medadvisor-domain-security/)
- [Medadvisor Trust Center](https://apis.io/security/medadvisor/medadvisor-trust-center/)

## Where to find this API

Links to the company's own pages. This repository publishes no copy of their specifications — the canonical document is theirs and lives at the URLs below.

- [Website](https://www.medadvisor.com.au)
- [Documentation](https://support.medadvisor.com.au)
- [API reference](https://pharmacy-unified.api.medadvisor.com.au/swagger/)
- [Support](https://support.medadvisor.com.au)
- [Compliance](https://www.medadvisorsolutions.com/en-au/data-and-privacy)
- [Terms of service](https://www.medadvisorsolutions.com/terms-and-conditions)
- [Privacy policy](https://www.medadvisor.com.au/privacy)

## API Evangelist rating

**Kin Score 46.5** — developing · rubric 0.25.0 · scored 2026-10-23

| Facet | Score |
|---|---|
| Discoverability | 73.2 |
| Contract quality | 41.2 |
| Contract governance | 18.2 |
| Operational transparency | 0.0 |
| Developer ergonomics | 35.1 |
| Access clarity | 36.8 |

**Agent readiness 27.7** — agent-aware

| Agent-readiness dimension | Result |
|---|---|
| Spec Presence | yes |
| Agentic Access | derived (partial credit) |
| Reversibility Documented | documented (partial credit) |
| MCP Server | — |
| Auth Clarity | bearer (partial credit) |
| Idempotency | — |
| Error Semantics | verified |
| OpenAPI Examples | partial |
| Rate Limit Signal | — |
| Event Surface Described | — |
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

**Regulatory alignment 32.0** — Health

The rubric is published at [github.com/api-evangelist/kin-score](https://github.com/api-evangelist/kin-score). The per-check breakdown behind these numbers — which checks were earned, partial or missed — along with score history and how this provider compares to its peers, is available at [apis.io/providers/medadvisor/](https://apis.io/providers/medadvisor/).

## How this profile is made

API Evangelist profiles a company's public API surface the way a developer would find it: the website, developer portal and documentation, the specifications it publishes, its public repositories, and its pricing, status and changelog pages. From that it derives the properties above — contracts split per API, workflows, schemas, collections, governance rules, plans and rate limits — and scores them against the published [Kin Score rubric](https://github.com/api-evangelist/kin-score).

The artifacts are published on [APIs.io](https://apis.io), not in this repository. This repository is the public record for MedAdvisor: the place to say something is wrong, missing or out of date, and to ask for a re-score or a removal.

## Open an issue

- **Something about this listing** — a wrong description, a missing API, a stale artifact or a question about the rating: [open an issue on this repository](https://github.com/api-evangelist/medadvisor/issues/new).
- **A new API, or one that is not in the catalog yet** — [submit it on APIs.io](https://apis.io/add/).
- **Anything else** — [the APIs.io inbox](https://github.com/api-search/inbox/issues/new) or [info@apievangelist.com](mailto:info@apievangelist.com).
