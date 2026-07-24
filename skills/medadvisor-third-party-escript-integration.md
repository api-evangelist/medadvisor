---
name: Third-party eScript & order integration
description: Authenticate a partner widget, look up a pharmacy, check an eScript token, and notify the pharmacy of an eCommerce order into its PlusOne inbox.
api: openapi/medadvisor-pharmacy-unified-openapi.json
operations: [Account_LoginPharmacy, Pharmacy_PharmacyDetail, Drug_RetrieveEPrescription3rdParty, Pharmacy_NotifyPharmacyOfECommerceOrder]
---

# Third-party eScript & order integration

Use this flow to connect an external widget or eCommerce platform to a MedAdvisor pharmacy.

## Auth
1. Obtain a JWT: `POST /api/v1/account/3rdpartylogin` (`Account_LoginPharmacy`) with your
   issued `clientId` + `clientSecret` and Base64-encoded (UTF-8) pharmacy credentials.
2. Send `Authorization: Bearer {token}` on every subsequent request. On 401, re-run step 1.

## Steps
1. `GET /api/v1/pharmacy/{id}` (`Pharmacy_PharmacyDetail`) - resolve the target pharmacy's public detail.
2. `GET /api/v1/drug/escript/{token}` (`Drug_RetrieveEPrescription3rdParty`) - retrieve eScript status/details by token.
3. `POST /api/v1/pharmacy/notify` (`Pharmacy_NotifyPharmacyOfECommerceOrder`) - push the order into the pharmacy PlusOne inbox.

## Rules
- Errors return an `OperationResult` envelope (`result`, `resultMessage`, `errorData`); check `result` before trusting `data`. See errors/medadvisor-problem-types.yml.
- No idempotency-key support - do not blindly retry `notify` on timeouts; reconcile first.
