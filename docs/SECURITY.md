# Security Baseline — Release Gate
- Google OAuth and secure sessions; privileged Owner/Admin MFA/passkeys; least privilege.
- Server-side authorization and RLS; test cross-user IDOR. Private buckets and short-lived signed URLs.
- Secrets server-only. No provider keys in browser or Git.
- SSRF: HTTP/HTTPS allowlist; reject localhost/private/loopback/link-local/metadata/reserved ranges; validate DNS results and every redirect; cap redirects/time/response size; defend DNS rebinding; use paste-text fallback.
- Prompt injection: CV/job/image/web text is untrusted data, not instruction authority.
- Uploads: extension/MIME/magic bytes/size/page/dimension checks; parser sandbox/time/memory limits; malware scan where practical; never execute uploads.
- Rate/concurrency limits; payment webhook signature verification/idempotency; privileged audit logs.
- Do not log raw CVs/full prompts/phone/address. Encrypt transit/at rest. Test backup restore and account deletion.
- Test SSRF, IDOR, RLS, malicious files, prompt injection, duplicate webhook, expired signed URL, unauthorized admin.
