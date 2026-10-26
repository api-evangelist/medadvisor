# MedAdvisor (medadvisor)

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

MedAdvisor (MedAdvisor Solutions) is an Australian-founded, ASX-listed medication management and patient engagement technology company. Its pharmacy workflow software runs in more than 95% of Australian community pharmacies and reaches over 4 million patients. The web-based "MedAdvisor for Pharmacy" platform (which replaced the long-running PlusOne desktop software) handles dispense workflow, medication adherence, appointment and clinical-service booking, e-script (eScript) handling, refill ordering, and omnichannel patient communication, alongside a consumer medication app. Home market: Australia.

**APIs.json:** [https://raw.githubusercontent.com/api-evangelist/medadvisor/refs/heads/main/apis.yml](https://raw.githubusercontent.com/api-evangelist/medadvisor/refs/heads/main/apis.yml)

## API Posture

MedAdvisor exposes a real, machine-readable **Pharmacy Unified API** documented with a live Swagger UI. It is an HTTP REST API (Swagger 2.0), **not** HL7 FHIR — no FHIR CapabilityStatement or SMART-on-FHIR configuration is served. Authentication is a JWT bearer token obtained via a MedAdvisor-issued `clientId`/`clientSecret` plus Base64-encoded pharmacy credentials (`POST /api/v1/account/3rdpartylogin`). The Swagger reference is publicly viewable, but access is gated behind a partner/integrator arrangement.

- **Developer reference (Swagger UI):** [https://pharmacy-unified.api.medadvisor.com.au/swagger/](https://pharmacy-unified.api.medadvisor.com.au/swagger/)
- **OpenAPI (harvested):** [openapi/medadvisor-pharmacy-unified-openapi.json](openapi/medadvisor-pharmacy-unified-openapi.json) — Swagger 2.0, 107 paths / ~112 operations, from `/swagger/docs/v1`

## Tags

- Healthcare
- Australia
- Pharmacy
- Medication Management
- Medication Adherence
- e-Prescribing
- eScript
- Patient Engagement
- Appointment Booking
- Digital Health
- Healthcare API

## Timestamps

- **Created:** 2026-07-24
- **Modified:** 2026-07-24

## APIs

### Pharmacy Unified API — 3rd-Party Integration

The publicly documented third-party integration surface — partner login, pharmacy lookup, eScript status by token, and order notification into the pharmacy PlusOne inbox — for external widgets and eCommerce platforms.

- **Reference:** [https://pharmacy-unified.api.medadvisor.com.au/swagger/](https://pharmacy-unified.api.medadvisor.com.au/swagger/)
- **Base URL:** `https://pharmacy-unified.api.medadvisor.com.au`

### Pharmacy Unified API — Booking Service

Appointment and clinical-service booking — available services and time slots, event bookings, event resources and staff calendars, and patient/booking search. Supports in-pharmacy vaccination, health-check, and scope-of-practice services.

### Pharmacy Unified API — Refill Order

Medication refill and order management — pending/completed orders, sending eScript tokens, line items, patient-initiated actions, order completion, refunds, reminders, and return-to-stock.

### Pharmacy Unified API — Inbox

The pharmacy PlusOne inbox — main, sent, completed, scheduled, and ready-to-collect queues, adding scripts, sending scheduled messages, and dismissing items.

### Pharmacy Unified API — Communication

Patient-communication and group-messaging — creating/editing patient groups, managing membership, and targeted patient outreach.

### Pharmacy Unified API — Head Office

Head-office (banner / multi-pharmacy) operations — managing services across a group, listing pharmacies, and pushing services with deadlines to member stores.

### Pharmacy Unified API — Pharmacy

Pharmacy account, settings, and administration — pharmacy details and module/feature settings, patient search, registration and activation, electronic-prescribing settings, SMS reminders, and change requests.

## Common Properties

- [Website](https://www.medadvisor.com.au)
- [Company Website](https://www.medadvisorsolutions.com/)
- [API Reference](https://pharmacy-unified.api.medadvisor.com.au/swagger/)
- [Support](https://support.medadvisor.com.au)
- [Privacy Policy](https://www.medadvisor.com.au/privacy)
- [Contact](https://www.medadvisorsolutions.com/contact)

## Maintainers

**FN:** Kin Lane
**Email:** kin@apievangelist.com
