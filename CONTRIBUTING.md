# Contributing

Thank you for contributing to the Onboarding 2026 repository. This document explains how to add yourself, the branching strategy, commit message style, pull request (PR) rules, review expectations and how self-onboarding via PR works.

Please follow these conventions to make reviews fast, consistent and fair.

---

## Table of contents

- Purpose
- Quick start
- Branching strategy
- Commit message conventions
- Pull request rules
- PR description template (suggested)
- Review process and expectations
- Self-onboarding via PR (task-00)
- Working with upstream changes
- Tests and verification
- Adding or updating tasks
- Code of conduct and etiquette
- Contact

---

## Purpose

This repository is both a learning resource and an evaluation point for new members. Contributors should aim for clarity, reproducibility and small, focused changes. All evaluated work must be submitted via GitHub PRs following the rules below.

---

## Quick start

1. Fork the repository on GitHub.
2. Clone your fork locally:
   ```sh
   git clone git@github.com:<your-username>/onboarding-2026.git
   cd onboarding-2026
   ```
3. Add the upstream remote (optional but recommended):
   ```sh
   git remote add upstream git@github.com:init-club/onboarding-2026.git
   git fetch upstream
   ```
4. Create a branch for the task you are working on (see Branching strategy).
5. Make focused commits and push to your fork.
6. Open a PR from your fork/branch to `onboarding-2026:main`.

---

## Branching strategy

We use short-lived feature branches. Branch names must be descriptive and follow these patterns:

- Feature (task work): `feat/task-0N-short-description`  
  Example: `feat/task-01-setup-local-env`
- Fix: `fix/task-0N-short-description`  
  Example: `fix/task-02-merge-conflict-example`
- Documentation: `docs/task-0N-short-description`  
  Example: `docs/task-03-markdown-skill`
- Chore: `chore/<short-description>` for repository maintenance

Guidelines:
- Always branch from `main` (ensure your local `main` is up to date).
- Keep branches focused on a single task or logical change.
- Delete branches from your fork after the PR is merged.

---

## Commit message conventions

Use concise, conventional commit-style messages:

Format:
```
<type>(<scope>): <short summary>
```

- `type` should be one of: `feat`, `fix`, `docs`, `chore`, `test`
- `scope` is optional but useful (e.g. `task-01`, `members`)
- Keep the subject line ≤ 72 characters.
- If more detail is required, separate the body with a blank line and explain the why.

Examples:
```
feat(task-00): add member entry for josuke-h

- Added entry to members/MEMBERS.md
- Confirmed branch naming and PR description
```

Good commit hygiene:
- Make small, atomic commits.
- Amend or squash local commits when cleaning up history before opening a PR.
- Do not include personal or sensitive information in commits.

---

## Pull request rules

A pull request is the official submission mechanism for evaluated tasks.

Required for every PR:
- Title follows pattern: `<type>(task-0N): short summary` (type examples: `feat`, `fix`, `docs`).
  Example: `feat(task-00): add member Josuke Higashikata (josuke-h)`
- Description that summarises the change, references the task number, and lists deliverables included.
- Evidence as required by the task README (screenshots, logs, code, or links).
- Branch name and commits follow the conventions above.
- Target branch: `main` of this repository.

Checklist (ensure these are present before requesting review):
- [ ] PR is focused (one logical change per PR).
- [ ] All required files and evidence are included.
- [ ] No unrelated changes are present.
- [ ] The PR description states any assumptions made.
- [ ] Members additions modify only `members/MEMBERS.md` or `members/members.yml` as instructed by `MEMBERS.md`.

Merging:
- PRs are merged by project maintainers or reviewers after all checks and requested changes are addressed.
- Do not merge your own PR unless explicitly permitted by a reviewer.
- Squash-and-merge may be used for simplicity; maintainers will indicate merging strategy per PR.

---

## PR description template (suggested)

You can use the following template when creating PRs. It helps reviewers accelerate their checks.

Title: feat(task-0N): short summary

Description:
- Task: `task-0N` — short task title
- Summary of changes:
  - Bullet list of files changed and what was added
- Deliverables attached:
  - e.g. `task-01/setup-log.txt`, screenshots in `task-01/screenshots/`
- Assumptions:
  - any assumptions you made while completing the task
- How to verify:
  - step-by-step verification instructions for a reviewer

Example:
```
Task: task-01 — Local development environment setup

Summary:
- Added `task-01/README.md` with setup notes
- Added `task-01/logs/setup-log.txt` containing terminal output

Deliverables:
- `task-01/README.md`
- `task-01/logs/setup-log.txt`

Assumptions:
- User is on macOS or Linux; Windows notes provided where applicable.

How to verify:
1. Open `task-01/README.md`.
2. Confirm logs demonstrate successful `git` and `code` (VS Code) installation.
```

---

## Review process and expectations

- Reviewers check for completeness, clarity and adherence to instructions in the task README.
- Typical checks:
  - Required deliverables are present and runnable.
  - Documentation is clear and free of spelling errors (British English).
  - Branch and commit conventions followed.
  - No sensitive data included.
- If changes are requested, update the same branch and push additional commits. The reviewer will re-check.
- Be responsive to review comments; reviewers may re-run verification steps.

Timings:
- Review turnaround depends on availability; if you need expedited review, note this in the PR description and tag the relevant reviewer or group.

---

## Self-onboarding via PR (task-00)

`task-00` is mandatory as the first active step for new members. It demonstrates you can use GitHub, branches and PR workflows.

What `task-00` requires:
- Add a single entry to `members/MEMBERS.md` or `members/members.yml` using the required format in `members/MEMBERS.md`.
- Create a branch using the naming convention (e.g. `feat/task-00-add-member-yourusername`).
- Commit with a conventional message (see Commit message conventions).
- Open a PR to `onboarding-2026:main` with the PR description stating this is `task-00`.
- Include any notes about private contact preferences.

PR reviewers will check:
- The entry uses the required fields and valid date format.
- Only your entry was added/changed.
- Branch and commit messages follow conventions.

If you make a mistake, update the branch or open a new PR referencing the previous one and explain why.

---

## Working with upstream changes

To keep your fork up to date:

```sh
# On your local main
git checkout main
git fetch upstream
git merge upstream/main
# or prefer rebase
git rebase upstream/main
git push origin main
```

When your branch diverges from `main`, rebase or merge upstream `main` into your branch to handle conflicts locally before opening or updating a PR. When resolving conflicts, prefer the simplest, least risky resolution and explain the choice in the PR.

---

## Tests and verification

- Many tasks require simple manual verification (screenshots, logs). Follow the task README for exact expectations.
- If you add scripts or code, include brief instructions on how to run them and include expected output.
- Keep test artefacts small and readable.

---

## Adding or updating tasks

If you identify an improvement to a task:
- Open an issue describing the proposed change.
- Work in a branch named `feat/docs-task-0N-change-short-desc`.
- Update the task README and any templates; keep changes minimal and well explained.
- Link the PR to the issue and explain the rationale for the change.

---

## Code of conduct and etiquette

- Be respectful in PR descriptions and review comments.
- Provide constructive feedback and avoid gatekeeping.
- If you are unsure about feedback, ask clarifying questions.
- Do not include proprietary or sensitive data in this public repository.

---

## Contact

For process questions or urgent help with onboarding, mention the Init Club reviewer group  in your PR or contact your onboarding buddy. For technical issues with this repository, open an issue and tag the maintainers.

Thank you for following these guidelines — they help us keep onboarding consistent and efficient.
