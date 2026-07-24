---
name: Book a pharmacy clinical service
description: Find an available in-pharmacy service and time slot and create a patient booking (vaccination, health check, scope-of-practice).
api: openapi/medadvisor-pharmacy-unified-openapi.json
operations: [Account_LoginPharmacy, BookingService_RetrieveAvailableServices, BookingService_RetrieveAvailableTimeslots, Pharmacy_SearchPatients, BookingService_CreateEventBooking]
---

# Book a pharmacy clinical service

## Auth
Obtain and send a JWT bearer token as in the third-party integration skill (`Account_LoginPharmacy`).

## Steps
1. `GET /api/v1/bookingservice/pharmacy/services/available` (`BookingService_RetrieveAvailableServices`) - list bookable services.
2. `GET /api/v1/bookingservice/pharmacy/retrieveavailabletimeslots` (`BookingService_RetrieveAvailableTimeslots`) - find open slots.
3. `POST /api/v1/pharmacy/SearchPatients` (`Pharmacy_SearchPatients`) - resolve/confirm the patient.
4. `POST /api/v1/bookingservice/createeventbooking` (`BookingService_CreateEventBooking`) - create the booking.

## Rules
- Capture patient consent fields the booking model exposes (clinicalConsent, financialConsent) before creating.
- List responses carry `totalCount`; there is no cursor pagination. See conventions/medadvisor-conventions.yml.
