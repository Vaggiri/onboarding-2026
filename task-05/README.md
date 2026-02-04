# Task 05 — Open-source style contribution

Objective

This task simulates a real open-source contribution workflow. You will locate a small issue or improvement in this repository, implement a clear and tested change, and submit a professional pull request that demonstrates good collaboration practices: issue discussion, focused commits, clear documentation and responsiveness to review.

Why this task matters

- Practises the end-to-end contribution flow used in most open-source projects.
- Reinforces skills in issue triage, minimal-but-meaningful changes, and clear PR communication.
- Demonstrates your ability to work in a collaborative review-driven environment.

Prerequisites

- Completion of `task-00` (forking, branching and PR basics) recommended.
- Familiarity with Git and the pull request workflow.
- A working local environment (`task-01`) to run any tests or linters.
- Read `CONTRIBUTING.md` and the top-level `README.md` before starting.

Selecting an issue or improvement

You may choose one of the following approaches:

- Pick an open issue in this repository labelled `good first issue` or `help wanted`.
- Implement a small documentation improvement (typos, examples, formatting).
- Improve a README, add missing examples, or correct a small workflow inconsistency.
- Add a simple automated check (e.g. a formatting or markdown linter) if you are comfortable with CI.

If no issues exist, propose an improvement via a new issue first. Provide a short description and wait a short period for maintainers to confirm it is acceptable to work on.

Scope and constraints

- Keep the change small and focused: one logical change per PR.
- Avoid large refactors or adding heavy dependencies.
- Avoid adding proprietary or sensitive information.
- Prefer improvements that are easy for reviewers to validate quickly.

Step-by-step instructions

1. Find or create an issue
   - Search issues, or create a new issue describing the problem and the proposed fix.
   - If you open a new issue, include:
     - A concise title.
     - A short description of the problem.
     - Proposed approach and deliverables.

2. Create a feature branch
   - Branch naming convention example:
```onboarding-2026/task-05/README.md#L1-8
git checkout -b feat/task-05-fix-typo-<your-github>
```
   - Keep the branch focused on the issue.

3. Implement the change
   - Make minimal, well-scoped code or documentation changes.
   - Add or update tests if the change affects behaviour.
   - Run any relevant linting or test commands locally before committing.

4. Write clear commits
   - Use conventional commit style and concise messages:
```onboarding-2026/task-05/README.md#L9-16
feat(task-05): improve README example for CSV summariser

- Clarify command usage with example input/output
- Fix minor grammar and British English spelling
```
   - Keep commits small and logical; use interactive rebase to tidy history if necessary.

5. Push and open a pull request
   - Push your branch to your fork and open a PR to `onboarding-2026:main`.
   - Use the PR template (suggested example below) and reference the issue number if applicable:
```onboarding-2026/task-05/README.md#L17-40
Title: feat(task-05): <short description>

Description:
- Task: task-05 — Open-source style contribution
- Summary of changes:
  - files changed: list key files
  - brief explanation of what was changed and why
- Deliverables:
  - link to files changed in branch
  - tests or verification steps
- Assumptions:
  - list any assumptions made
- How to verify:
  1. Steps to run tests or commands
  2. Expected output or behaviour

References:
- Issue: #NN (if applicable)
```

6. Engage in review
   - Respond promptly and professionally to reviewer comments.
   - Make changes in the same branch and push updates.
   - Explain decisions where trade-offs were made.

7. After merge
   - If requested, follow any post-merge steps (for example: delete branch on your fork).
   - Add a short note to your onboarding task record (if required).

Expected deliverables

- A pull request implementing a small, meaningful repository improvement.
- The PR must:
  - Be focused on one issue or improvement.
  - Follow branch and commit naming conventions.
  - Include tests or a clear verification method if relevant.
  - Contain a clear PR description and reference the issue (or explain why no issue exists).
- Files changed should be limited to those required by the change.

Submission and evaluation criteria

Your submission will be evaluated on:

- Correctness: The change addresses the issue and does not introduce regressions.
- Scope: The PR is focused and does not contain unrelated changes.
- Documentation: The PR description and in-code comments explain what changed and why.
- Testing: Tests (if applicable) exist and pass or clear verification steps are provided.
- Process: Branch naming, commit messages and PR etiquette follow `CONTRIBUTING.md`.
- Collaboration: You respond constructively to review feedback and iterate as necessary.

Reviewers will ask for a rework if the PR is too large, lacks explanation, or fails to meet repository conventions.

Optional extensions (for additional learning)

- Add a simple GitHub Action that runs a linter or unit tests for the part of the repository you touched.
- Provide a short performance or accessibility note if the change affects end users.
- Draft a changelog entry or release note summarising the improvement.
- Prepare a short (2–3 minute) screencast demonstrating the before-and-after behaviour.

Examples of good PR descriptions

- Short, descriptive title and a bulleted description.
- Link to the exact files changed (use GitHub UI links).
- Clear verification steps the reviewer can run in 5–10 minutes.

Common pitfalls and troubleshooting

- PR contains unrelated changes: create a new clean branch and cherry-pick the intended commits.
- Large diffs: break the work into smaller, sequential PRs.
- Tests failing on CI but passing locally: check runtime versions, environment variables, and ensure deterministic tests.
- Sensitive data inadvertently committed: contact a maintainer immediately and follow repository escalation procedures.

Assumptions and notes

- You may work from your fork; all reviewed submissions must be via GitHub PRs to this repository.
- If a chosen issue is ambiguous, document your assumptions in the issue and the PR description.
- Maintain British English spelling in documentation and commit messages when writing prose.

Reviewer checklist

- [ ] Is the PR focused and small?
- [ ] Does the PR reference an issue or include a clear reason why none exists?
- [ ] Are commit messages clear and conventional?
- [ ] Is the change documented and testable?
- [ ] Did the contributor respond to review comments appropriately?

If you need help selecting an issue or want feedback on your proposed approach before coding, open a short discussion in a draft issue and tag the onboarding reviewers. I will help you think through options and suggest improvements — and once you’re ready, you can implement the change and submit the PR for formal review.

Good luck — this task mirrors real open-source collaboration and is excellent practice for working on shared code and documentation.