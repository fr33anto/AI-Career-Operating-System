# Repository Structure
```text
career-ai-os/
├── .cursor/rules/
├── .github/workflows/
├── docs/ (PRD, ARCHITECTURE, DATABASE, ERD, API, AI_ARCHITECTURE, COST_CONTROL, SECURITY, UI_UX, BILLING, TESTING, ROADMAP, TASKS, ADRs)
├── prompts/{job,matching,cv,cover-letter,interview}/
├── public/
├── src/
│   ├── app/
│   ├── modules/{auth,users,career-passport,documents,jobs,matching,applications,cv,cover-letter,interview,billing,credits,subscriptions,vouchers,notifications,analytics,admin}/
│   ├── ai/{gateway,providers,router,prompts,schemas,cache,cost-control,quality-gate,truthguard,usage-ledger}/
│   ├── infrastructure/{database,storage,queue,telemetry}/
│   └── shared/{config,errors,types,utils}/
├── supabase/migrations/
├── tests/{unit,integration,e2e,security}/
├── AGENTS.md
├── .env.example
└── README.md
```
Folders are placeholders. Do not implement all modules in TASK-001.
