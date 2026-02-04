# Task 00 — Repository onboarding and Git workflow

Objective
- Ensure every new member can perform the basic Git and GitHub operations required by the Init Club at Amrita Vishwa Vidyapeetham, Coimbatore.
- Demonstrate ability to:
  - Fork a repository,
  - Create and push a feature branch,
  - Add a single member entry to the `members/` directory,
  - Open a pull request (PR) with a clear description and appropriate commit message.

Why this task matters
- Confirms you can use the collaboration workflow we rely on.
- Provides reviewers with a simple artefact to verify your account, branch and PR skills.
- Serves as the first checkpoint in the onboarding process.

Prerequisites
- A GitHub account.
- Git installed locally (version 2.20+ recommended).
- Basic familiarity with the command line (terminal).
- Optional: an SSH key configured for GitHub (HTTPS is acceptable if you prefer).

Estimated time
- 10–30 minutes.

Expected deliverables
- A pull request on this repository adding one entry for you to `members/MEMBERS.md` (or `members/members.yml` if you prefer YAML).
- Branch name following the convention described below.
- A small, focused commit with an appropriate conventional-style commit message.
- PR description that references `task-00` and documents any assumptions (for example, `contact: private`).

Directory and file to edit
- `members/MEMBERS.md` (primary)
- Alternatively: `members/members.yml` (if you prefer YAML; ensure you follow the example format in `members/MEMBERS.md`)

Step-by-step instructions (beginner-friendly)

1. Fork the repository on GitHub
- Open the repository in your web browser.
- Click the "Fork" button in the top-right and choose your personal account.

2. Clone your fork locally
- Replace `<your-username>` in the commands below with your GitHub username.

  (Example — clone via SSH)
      git clone git@github.com:<your-username>/onboarding-2026.git
      cd onboarding-2026

  (Example — clone via HTTPS)
      git clone https://github.com/<your-username>/onboarding-2026.git
      cd onboarding-2026

3. (Optional) Add the upstream remote
- This makes it easy to pull updates from the original repository later.

      git remote add upstream git@github.com:init-club/onboarding-2026.git
      git fetch upstream

4. Create a feature branch for this task
- Branch names must be descriptive and follow the project convention. For `task-00` use:

      git checkout -b feat/task-00-add-member-<your-github>

- Example:

      git checkout -b feat/task-00-add-member-josuke-h

5. Add your entry to `members/MEMBERS.md` (or `members/members.yml`)
- Open `members/MEMBERS.md` in your editor.
- Add one new entry following the example format in that file.

- Required fields (Markdown list format):
  - `name` — Full name
  - `github` — GitHub username
  - `role` — Role title (brief)
  - `start_date` — ISO date in `YYYY-MM-DD` format
  - `location` — City, Country
  - `contact` — public contact (email or `private`)

- Example (markdown list format):

  - **name**: Josuke Higashikata
    **github**: josuke-h
    **role**: Research Associate
    **start_date**: 2026-02-01
    **location**: Morioh, Japan
    **contact**: josuke@speedwagonfoundation.com
    **notes**: "Stand: Crazy Diamond; interests in urban studies and community engagement."


- If you prefer YAML, create or edit `members/members.yml` and use the YAML example in `MEMBERS.md`.

6. Stage and commit your change
- Use a conventional-style commit message. Keep the message short and imperative.

      git add members/MEMBERS.md
      git commit -m "feat(task-00): add member Josuke Higashikata (josuke-h)"

Commit message guidance
- Use `type(scope): short summary` format (e.g. `feat(task-00): add member <name>`).
- Keep the subject line ≤ 72 characters.
- If you need a longer explanation, add a commit body.

7. Push your branch to your fork
- Push the branch to GitHub:

      git push -u origin feat/task-00-add-member-josuke-h

8. Open a pull request (PR)
- On GitHub, open a PR from your fork/branch to `onboarding-2026:main`.
- PR title example:

  feat(task-00): add member Josuke Higashikata (josuke-h)

- PR description should include:
  - The task being completed: `task-00`.
  - Which file you changed (link to the file in your branch).
  - Any assumptions (for example: `contact: private`).
  - Any notes the reviewer may need.

PR description template (copy-paste and adapt)
- Task: `task-00` — Repository onboarding and Git workflow
- Summary: Added entry to `members/MEMBERS.md`
- Deliverables:
  - `members/MEMBERS.md` (one new entry)
- Assumptions:
  - `contact: private` (if you set this)
- How to verify:
  1. Confirm the PR touches only `members/MEMBERS.md` (or `members/members.yml`).
  2. Confirm the entry uses required fields and valid date format.

Evaluation criteria
- The PR adds exactly one member entry.
- The entry uses the required fields and correct formatting.
- Branch name and commit message follow project conventions.
- PR description references `task-00` and documents any assumptions.
- No unrelated changes are present in the branch.
- Reviewer confirms the work and merges the PR.

Common mistakes and troubleshooting
- Accidentally modifying other entries:
  - Undo changes, rebase or reapply only your addition on a clean branch and re-open a PR.
- Invalid date format:
  - Use `YYYY-MM-DD`. Example: `2026-02-01`.
- Sensitive information included:
  - If you mistakenly add sensitive data, contact a reviewer immediately and create a follow-up PR to remove it.
- Branch contains unrelated commits:
  - Create a new branch from up-to-date `main` and cherry-pick or reapply only the relevant change.

What reviewers will check
- Single, focused change (one member entry).
- Entry format and completeness.
- Naming and commit conventions.
- Presence of assumptions (if any).
- Clean git history for the branch (no unrelated or large binary files).

Optional extensions (not required for completion)
- Add a short public portfolio link in `blog` or `notes`.
- Provide a short screenshot of the PR page as evidence (useful for records).
- Add a brief note in the PR about how you plan to approach subsequent tasks.

Learning outcomes
- You will gain confidence using GitHub forks, branches and pull requests.
- You will practise making small, reviewable changes and writing clear PR descriptions.
- You will understand the project's standards for branch and commit naming.

Assumptions documented for reviewers
- If any task instruction is ambiguous, the contributor should include a short "Assumptions" section in the PR description. Reviewers will accept reasonable assumptions when they are made explicit.

Support
- If you need help, mention the maintainers in your PR or reach out to your onboarding buddy.
- For urgent issues (e.g. accidentally publishing private data), contact the repository maintainers directly.

Good luck — once your PR for `task-00` is approved and merged you may proceed to `task-01`.
