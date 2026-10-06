# Architecture
## Proposed stack for TASK-001 confirmation
Next.js App Router + TypeScript; Tailwind; Supabase managed PostgreSQL/Google OAuth/private Storage; Zod; Vitest; Playwright; TestSprite supplemental; pnpm. Cursor IDE; OpenCode in Cursor terminal for direct DeepSeek API agent access.

## Pattern
Modular Monolith. No microservices/Kubernetes/Kafka for MVP.
Browser → `/api/v1` → auth/authorization → domain use case → deterministic validation/quota → AI Gateway (only if needed) → policy/cost/cache/router → provider adapter → schema validation → TruthGuard → persistence.

## Layers
`src/modules`: domain use cases. `src/ai`: gateway/providers/router/prompts/schemas/cost/quality/truthguard. `src/infrastructure`: database/storage/queue/telemetry. `src/shared`: types/errors/config/utils. `supabase/migrations`: schema/RLS. `tests`: unit/integration/e2e/security.

## Rules
Provider SDKs only in adapters. Server-only secrets. Development/staging/production credentials separate. CI → staging → smoke/security → human approval → production.
