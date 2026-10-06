# Testing and Release
TestSprite is supplemental, never the only test system.

Layers: unit (validation/quota/TruthGuard/cost); integration (DB/RLS/storage/provider mock/billing); Playwright E2E; TestSprite API/UI/negative path; security (IDOR/SSRF/upload/prompt injection/webhook replay/admin); operations (migrations/restore/retention/provider outage).

CI: format/lint/typecheck → unit → integration → Playwright → TestSprite when appropriate → security scans → build → staging → smoke → human approval → production.

Critical cases: Google login; Free rolling quota and daily cap; Free kill switch while paid remains; voucher caps; duplicate webhook; unsupported claim blocked; invalid model JSON; provider timeout; SSRF private IP; malicious upload; retention deletion; cross-user access denied; admin change audited; backup restore.
