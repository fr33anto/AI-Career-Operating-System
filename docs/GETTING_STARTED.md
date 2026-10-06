# Getting Started (Windows 10/11)
1. Install Cursor: https://cursor.com/
2. Install Git: https://git-scm.com/downloads
3. Install Node.js LTS: https://nodejs.org/
4. Install pnpm: https://pnpm.io/installation
5. Create/sign into GitHub: https://github.com/
6. Extract this ZIP to `C:\Projects\career-ai-os`.
7. Cursor → File → Open Folder → choose that folder.
8. Open Cursor Terminal and verify `git --version`, `node --version`, `pnpm --version`.
9. Initialize Git:
```powershell
git init
git add .
git status
git commit -m "chore: initialize AI Career OS specification"
```
If Git requests identity, set `git config user.name "Your Name"` and `git config user.email "you@example.com"` then retry.
10. Create a PRIVATE GitHub repository `career-ai-os`, add remote and push using GitHub's instructions.
11. Configure OpenCode using current official docs: https://opencode.ai/docs/ . Provider base URL `https://api.deepseek.com`, model `deepseek-flash`. Follow the current config schema; do not copy stale examples.
12. Use `docs/TASK_PROMPTS.md` for TASK-001 only. Stop for review after it.

Never paste API keys into chat/source files or commit `.env.local`. Do not use real CVs as test data. This archive is a scaffold, not a working SaaS yet.
