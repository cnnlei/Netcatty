# Fix the latest review findings

Read `.codex-runtime/issue.json`, `.codex-runtime/review-latest.json`,
`.codex-runtime/verification.log`, and `AGENTS.md`. Fix every actionable finding
without expanding the issue's scope. If verification failed, diagnose and fix
that failure even when the review findings are empty. Keep or add focused
regression tests.

Do not edit anything under `.github/`, `AGENTS.md`,
`scripts/issue-triage.cjs`, or `.codex-runtime/`. Do not commit, push, open a
pull request, or communicate with GitHub. Run the relevant checks before
finishing; the workflow will independently verify and review the result again.
