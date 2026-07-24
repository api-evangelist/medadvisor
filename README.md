# MedAdvisor (medadvisor)

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
