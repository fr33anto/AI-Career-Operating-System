# Cost Control
Application Pack is the user-facing unit; internally meter every AI request by user/application/feature/provider/model/tokens/cost/latency/status.

Before each call: auth/ownership → plan entitlement → per-user quota → concurrency → request token budget → Free/Paid daily budget → global emergency budget → provider health/rate limit.

Free baseline: 1 pack/rolling 30 days; text-only; private alpha 10–25 packs/day; one active AI job/user; Owner kill switch; paid reserve separate.

Modes: NORMAL, SAVING, RESTRICTED, EMERGENCY, CRITICAL. Max 3 section regenerations/application initially. Cache normalized job and deterministic parsing; never share personalized outputs across users. Alert at 70/85/95%. Measure actual provider usage; never treat estimates as production guarantees.
