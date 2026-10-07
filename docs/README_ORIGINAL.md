# TTRP Project Workspace

This repository is your persistent engineering workspace for the assigned project.

The same repository continues across all Backlogs assigned within this project. Existing accepted work becomes the baseline for subsequent work.

## Working References
- **Project Overview:** Refer to the project portal provided during onboarding.
- **Current Requirement:** Refer to your currently assigned Backlog.
- **Progress Communication:** Use the designated residency communication channel.
- **Submission:** Submit the exact Git commit SHA requested for evaluation.

## Repository Structure
- `src/` — project implementation
- `tests/` — tests and verification assets
- `docs/reflections/` — one reflection document for each Backlog
- `docs/DECISIONS.md` — significant engineering decisions
- `evidence/` — Backlog-specific screenshots or other requested evidence
- `.github/pull_request_template.md` — PR guidance when a PR is appropriate

## Working Principles
1. Treat the existing accepted repository state as the baseline for each new assignment.
2. Implement only the capability required by the current Backlog.
3. Do not add speculative capabilities that have not been requested.
4. Preserve accepted behaviour unless the current requirement explicitly changes it.
5. Keep Git history truthful and meaningful.
6. Never commit passwords, API keys, access tokens, credentials, or other secrets.
7. Add evidence only when relevant to the assigned work.

## Reflection
For each Backlog, copy `docs/reflections/REFLECTION_TEMPLATE.md` to `docs/reflections/<BACKLOG_ID>.md`.

Example: `docs/reflections/B000001.md`

Complete the reflection before submission.

## Evidence
When evidence is required, keep it under the corresponding Backlog ID, for example `evidence/B000001/`.

Use meaningful filenames. Do not create Backlog-specific folders inside `src/`; the implementation is one continuously evolving project.

