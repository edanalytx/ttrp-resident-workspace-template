# TTRP Resident Guide

This guide remains available while you rewrite `README.md` for your actual project. Keep it in the repository for future backlogs. The original template README is also preserved in [docs/README_ORIGINAL.md](docs/README_ORIGINAL.md); use this guide for the updated process.

## 1. Create your project workspace

Create a repository from this template under the GitHub profile you supplied during onboarding. Use the same repository for all backlogs within the assigned project. Its owner must match your registered profile, and it must be accessible to TTRP's verification and evaluation process. The current POC verifies public repositories.

Clone your own repository, replacing the placeholders:

```sh
git clone https://github.com/<YOUR_GITHUB_USERNAME>/<YOUR_PROJECT_REPOSITORY>.git
cd <YOUR_PROJECT_REPOSITORY>
```

Read your project overview, assigned backlog and acceptance criteria in TTRP. Existing accepted work is the baseline for subsequent assignments. Preserve that behaviour unless a new requirement explicitly changes it.

## 2. Use a branch for each backlog

Start from the latest accepted project baseline. If `main` holds that baseline:

```sh
git switch main
git pull --ff-only origin main
git switch -c backlog/<EXACT_ASSIGNED_BACKLOG_CODE>
```

Replace the example branch suffix with the exact assigned code, for example `BL-P001-000005`. If accepted work is on another branch, start from that branch instead. Do not automatically treat unreviewed work as accepted or start from an unrelated template again.

Keep the implementation in the project's normal structure. Do not create a separate project inside `src/` for every backlog.

## 3. Work and commit

Implement the assigned scope, verify it and make meaningful commits. Review what you stage and exclude secrets, generated files and unrelated changes.

```sh
git status
git diff
git add <FILES_YOU_REVIEWED>
git diff --cached
git commit -m "Describe the concrete change"
git push -u origin backlog/<EXACT_ASSIGNED_BACKLOG_CODE>
```

Use real paths in place of the examples. Commit working increments as useful; there is no required commit count. Report progress through Daily Scrum in TTRP. Scrum history is separate from the final backlog reflection.

## 4. Complete the backlog reflection

Copy [REFLECTION_TEMPLATE.md](docs/reflections/REFLECTION_TEMPLATE.md) to `docs/reflections/<EXACT_ASSIGNED_BACKLOG_CODE>.md`. For example:

```sh
cp docs/reflections/REFLECTION_TEMPLATE.md docs/reflections/BL-P001-000005.md
```

Answer the reflection questions in that file, replacing all placeholders. Cover implementation, verification, decisions, problems, limitations and relevant assistance. Be specific and honest. If a section does not apply, explain that briefly. Preserve earlier reflections.

The submission page uses a checklist; the detailed answers live in the committed reflection file rather than being entered twice.

## 5. Maintain engineering decisions

Record significant decisions with lasting project implications in [docs/DECISIONS.md](docs/DECISIONS.md), using its template and a stable decision ID. Link to that entry from the backlog reflection instead of copying the same explanation into both files.

Routine backlog-specific choices belong in the reflection. No new decision entry is required when no lasting decision was introduced. Keep existing entries; if a later decision changes one, add a superseding entry and explain the relationship.

## 6. Update the project README

Before submission, rewrite or update `README.md` for the actual project and completed task. Include its purpose, implemented behaviour, prerequisites, configuration, setup, run instructions, verification commands and known limitations. Link the current backlog reflection.

Keep useful documentation for previously accepted functionality. The README describes the continuing project, not only the latest task. Remove unused template placeholders. The permanent guide and original README reference remain available separately.

## 7. Prepare the final reference

Commit and push the implementation, reflection, README, relevant decisions and any required evidence together before taking the final reference.

```sh
git status
git push origin backlog/<EXACT_ASSIGNED_BACKLOG_CODE>
git rev-parse HEAD
```

Copy the full commit SHA returned by the last command. Confirm that the commit is visible on GitHub in your submitted repository and branch. A branch name can move as you continue working; the commit SHA identifies the exact version submitted for evaluation. Avoid amending or force-pushing away the submitted commit. Later changes do not silently replace the submitted version.

A pull request is optional unless the assignment requires one. Do not merge unreviewed work merely to submit it.

## 8. Submit through TTRP

Provide your verified repository URL, branch name, exact commit SHA and optional PR URL. Complete the submission checklist:

- [ ] Implementation and documentation are committed and pushed.
- [ ] The reflection for the exact assigned backlog code is complete.
- [ ] The README contains current setup, run and verification instructions.
- [ ] Significant project decisions are recorded where applicable.
- [ ] Acceptance criteria have been reviewed and known limitations disclosed.

Submit through the TTRP workspace; pushing a commit alone does not submit the backlog. After successful submission, your work is queued for evaluation and Daily Scrum for that backlog closes. The confirmation email will explain the next step; your next backlog will be allocated once evaluation is complete.

These instructions describe the agreed submission design. The live TTRP form remains the authority for the fields currently enabled while the design is being implemented.

## 9. Continue after evaluation

Follow the evaluation result and any requested changes. Keep the submitted commit and reflection available. Use the accepted project state as the starting point for the next backlog; retain earlier code, documentation, decisions and reflections.

## Evidence and credentials

Only add separate evidence when relevant or requested by the backlog, under `evidence/<EXACT_ASSIGNED_BACKLOG_CODE>/`. There is no additional daily screenshot or activity-proof requirement. Never commit passwords, tokens, private keys or personal credentials.
