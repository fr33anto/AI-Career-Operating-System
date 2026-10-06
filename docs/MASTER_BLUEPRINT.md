# MASTER BLUEPRINT v1.0
Status: LOCKED MVP BASELINE. Date: 21 September 2026.

## Workflow
Google Login → Input Job → Explain Job → Match → Targeted CV → Cover Letter → Interview Preparation.

## Locked principles
Google-only login; Career Passport is source of truth; TruthGuard blocks unsupported claims; Application Pack is user-facing AI unit; No-LLM-first; all AI via AI Gateway; Modular Monolith; metered Free AI with Owner kill switch; temporary raw uploads; configurable commercial/operational settings; security is release gate.

## Initial commercial hypotheses
Free Rp0: 1 pack/30 days. One Pack Rp15k: 1. 5 Pack Rp59k: 5. 10 Pack Rp99k: 10. Job Hunter Rp99k/month: 10/month. Career Pro Rp179k/month: 25/month. Prices/entitlements stored in DB, never hard-coded; calibrate using actual costs.

## Free controls
Text-only at launch; 1 pack/user/rolling 30 days; private alpha 10–25 packs/day; global daily Free budget; concurrency 1 active AI job/user; Owner Free AI master switch; Paid budget reserve protected.

## Modules
auth, users, career-passport, documents, jobs, matching, applications, cv, cover-letter, interview, billing, credits, subscriptions, vouchers, notifications, analytics, admin.
AI: gateway, providers, router, prompts, schemas, cache, cost-control, quality-gate, truthguard, usage-ledger, evaluation.

## Storage
Career Passport structured data persistent while account active. Raw job images default delete within 24h. Processing files 1–6h. Generated files on-demand/default 7d if retained. Private buckets, short-lived signed URLs, content-hash dedupe.

## Security
OAuth/session security, privileged MFA, strict authorization/RLS, private storage, signed URLs, SSRF protection, prompt injection defense, upload validation/parser isolation/malware scanning, rate/concurrency limits, payment webhook verification/idempotency, audit logs, secret isolation, security headers, backup/restore and deletion lifecycle.
