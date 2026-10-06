# PRD — AI Career OS
## Product
Personal AI Career Assistant that turns a job posting and verified career history into an application pack and interview preparation. Not a job board; no promise of hiring or ATS success.

## Users
Job seekers, fresh graduates, career switchers, and professionals preparing to change jobs.

## Core flow
1. Google sign-in and automatic member registration.
2. Create/review Career Passport from entered facts or allowed CV upload.
3. Paste job URL/text or upload plan-permitted file.
4. Normalize and explain role in Indonesian; preserve original language context.
5. Match requirements to verified candidate evidence.
6. Generate editable targeted CV with ATS-oriented structure.
7. TruthGuard blocks unsupported claims.
8. Generate editable cover letter.
9. Generate likely interview questions and STAR guidance.
10. Save Application Pack and download outputs.

## Functional requirements
Career Passport stores user-confirmed identity/contact (minimum necessary), summary, education, experience, skills, certifications, projects, languages, achievements/evidence, links, preferences. Job analysis distinguishes required/preferred criteria and never infers salary/deadline. UI language and document language are independent. User owns and edits outputs. Basic text mock interview and application tracker.

## Plans
Free text only; paid document/image inputs by plan/config. Pack capacity and prices configurable. Owner/Admin can manage plans, vouchers, AI routing, budgets, flags, retention, templates and announcements with RBAC/audit.

## Non-goals
No job board, auto-apply, covert live interview assistance, guaranteed hiring, model training on user CVs, voice/video analytics in MVP.

## NFR
Responsive, Indonesian default + English switch, secure personal-data handling, cost attribution per AI request, provider-failure UX, deletion lifecycle, tests for critical workflows.
