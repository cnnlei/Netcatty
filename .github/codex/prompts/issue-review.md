# Review the current issue fix

Read `.codex-runtime/issue.json`, `.codex-runtime/verification.log`, and
`AGENTS.md`. Review only the current working-tree changes against `origin/main`.
Do not modify files.

Look for concrete correctness bugs, regressions, security or privacy problems,
broken edge cases, missing migration or compatibility handling, and tests that
do not actually protect the requested behavior. Respect the review boundaries
in `AGENTS.md`. Ignore subjective style preferences and minor cleanup.

Set `clean` to true only when there are no blocking or important findings and
the verification log says all checks passed. Every finding must state what can
go wrong, where it happens, and what must change. Return only the requested
structured result.
