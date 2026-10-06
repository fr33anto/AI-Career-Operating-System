# Database Design
PostgreSQL; UUID IDs; timestamps; foreign keys/unique constraints; migrations only; RLS for user data; binary files in private object storage.

Logical tables:
- Identity: users, profiles, user_roles.
- Career: career_passports, career_passport_versions, experiences, educations, skills, certifications, projects, languages, evidences.
- Documents/jobs: documents, document_versions, document_processing_jobs, jobs, job_sources, job_requirements, job_snapshots, job_analysis.
- Applications: applications, application_versions, generated_cvs, cover_letters, interviews, interview_questions, interview_answers, interview_feedback.
- Billing: subscription_plans, plan_features, subscriptions, purchases, payments, invoices, wallets, credit_ledger, credit_reservations.
- Promotion: vouchers, voucher_redemptions.
- AI ops: ai_requests, ai_usage, model_registry, routing_rules, prompt_versions, ai_failures, ai_evaluations.
- System: feature_flags, system_settings, notifications, audit_logs.

Every user-owned record has ownership enforcement. Application stores exact Career Passport version used. Credit reservations/payment webhooks/voucher redemptions are idempotent and transactional. AI ledger stores metadata/cost, not raw CV by default.
