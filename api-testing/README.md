# API Testing

Manual API testing using Postman across two public REST APIs, covering full CRUD operations, authentication flows, negative path testing, and status code validation.

## Collections

### Collection 1 — Restful Booker
A hotel booking API with token-based authentication.

**Covered:**
- GET all bookings (200)
- GET single booking by valid ID (200)
- GET single booking by invalid ID (404) — negative path
- POST create new booking (200)
- POST generate auth token — authentication flow

**Observation:** Restful Booker returns 200 on successful POST rather than the expected 201 Created — a minor API design inconsistency noted during testing.

### Collection 2 — JSONPlaceholder
A stable mock REST API used to demonstrate full CRUD sequence.

**Covered:**
- GET single post by valid ID (200)
- GET single post by invalid ID (404) — negative path
- POST create new post (201 Created)
- PUT update existing post (200)
- DELETE post (200)
- DELETE already-deleted post — returns 200 rather than expected 404, consistent with mock API behaviour (no persistence)

**Observation:** JSONPlaceholder correctly returns 201 on resource creation, unlike Restful Booker. Repeated DELETE returning 200 noted as mock API limitation rather than a defect.

## Key concepts demonstrated
- Happy path and negative path testing
- Status code validation (200, 201, 404, 403, 405)
- Token-based authentication
- Request body construction (raw JSON)
- Identifying API design inconsistencies across different implementations
