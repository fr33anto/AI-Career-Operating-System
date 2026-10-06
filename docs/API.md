# API Contract
All application endpoints are versioned `/api/v1`. Browser never calls model providers directly.

- Profile: GET/PATCH `/api/v1/profile`
- Career Passport: GET/POST/PATCH `/api/v1/career-passport`
- Documents: POST `/api/v1/documents`; GET/DELETE `/api/v1/documents/:id`
- Jobs: POST `/api/v1/jobs/ingest`; GET `/api/v1/jobs/:id`; POST `/api/v1/jobs/:id/analyze`
- Match: POST `/api/v1/applications/:id/match`
- CV: POST `/api/v1/applications/:id/cv`; PATCH `/api/v1/cv/:id/sections/:section`
- Cover letter: POST `/api/v1/applications/:id/cover-letter`
- Interview: POST `/api/v1/applications/:id/interview`
- Billing: GET `/api/v1/plans`; POST `/api/v1/purchases`
- Voucher: POST `/api/v1/vouchers/redeem`
- Admin: `/api/v1/admin/*`

Validate input/output; enforce auth, ownership, entitlement, quota, rate limits; use idempotency keys for money/credits; safe error codes; document schemas.
