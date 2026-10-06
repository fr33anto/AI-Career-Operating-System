# AI Architecture
Every model call: domain use case → AI Gateway → entitlement/quota/token/daily-budget checks → cache → router → provider adapter → provider → schema validation → TruthGuard/quality gate → usage ledger.

Initial provider: DeepSeek. Model ID `deepseek-flash`; OpenAI-compatible base URL `https://api.deepseek.com`. Verify live docs/pricing before production.

No LLM for validation, metadata, hashing, quota, billing, sorting, pagination, file limits, retention, rendering. DeepSeek Flash for job explanation, matching, CV, cover letter, interview questions. Escalate only if evaluation proves necessary.

Version prompts and schemas. Reject malformed output. Bounded retries. Treat job/CV/web content as untrusted data. Minimize personal context. Never invent candidate facts.
