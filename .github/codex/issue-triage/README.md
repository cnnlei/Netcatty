# Automated issue triage

This workflow classifies every valid new issue into one of five outcomes:

1. `bug_ready` - implement, verify, review, and open a pull request.
2. `bug_needs_info` - ask for specific evidence and wait for a maintainer.
3. `feature_quick_win` - implement, verify, review, and open a pull request.
4. `feature_defer` - leave a concise reply and wait for a maintainer.
5. `other` - copy the issue into the matching Discussion category and close it.

Low-confidence results are never allowed to start source changes. Review and fix
runs stop after three review passes; unresolved work is opened as a draft pull
request and marked for human attention.

## Required repository secrets

- `OPENAI_API_KEY`: API key used by the official Codex GitHub Action.
- `TRIAGE_GITHUB_TOKEN`: fine-grained personal access token with Contents and
  Pull requests read/write access for this repository. Using a separate token
  ensures the pull request triggers the repository's normal CI workflows.
- `SLACK_WEBHOOK_URL`: Slack incoming webhook for progress notifications.

## Optional repository variable

- `CODEX_TRIAGE_DAILY_LIMIT`: maximum automatic runs per UTC day for reports
  from people without repository access. Defaults to `10`.

## Manual retry

Run **Issue triage and auto-fix** from the Actions page and enter an issue
number. Manual runs bypass format and daily-limit checks, but keep every other
safety check.
