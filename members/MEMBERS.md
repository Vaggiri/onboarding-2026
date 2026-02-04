# Members — Add yourself

This file is the canonical list of people who have completed `task-00` (Repository onboarding and Git workflow). Add your details by submitting a pull request that adds a single entry following the format below.

Purpose
- Provide a simple, reviewable record of new members.
- Make it easy for reviewers to confirm completion of `task-00`.
- Keep personal information minimal and appropriate for a shared repository.

File format and rules (required)
- Add one entry per person.
- Use the YAML-like block shown in the example. Keep keys and spelling identical.
- Place your new entry under the existing entries. Entries should be separated by a single blank line.
- Do not remove or change other people's entries.
- Keep values short and factual.

Required fields
- `name` (string) — Full name as you prefer it to appear.
- `github` (string) — GitHub username (no URL).
- `role` (string) — Job title or role (brief).
- `start_date` (ISO date, YYYY-MM-DD) — Your official start date or onboarding date.
- `location` (string) — City and country (City, Country).
- `contact` (string | optional) — Preferred public contact (email or GitHub handle). Mark as `private` if you prefer not to share.
- `notes` (string | optional) — Short note about primary skills, interests, or preferred areas of contribution.

Optional fields
- `blog` (string | optional) — Link to an optional blog post or public portfolio item.
- `pronouns` (string | optional) — e.g. `they/them`, `she/her`, `he/him`.

Privacy and acceptable content
- Do not include personal identifiers beyond what is requested (no phone numbers, home addresses, national IDs).
- If you prefer not to publish your email, set `contact: private` and include an alternative contact method in your PR description.
- Keep notes professional and relevant.

Example entry (copy-paste and edit)
```yaml
- name: Josuke Higashikata
  github: josuke-h
  role: Research Associate
  start_date: 2026-02-01
  location: Morioh, Japan
  contact: josuke@speedwagonfoundation.com
  notes: "Stand: Crazy Diamond; interests in urban studies and community engagement."
  blog: "https://example.com/josuke-blog"
  pronouns: "he/him"
```

How to add yourself — step-by-step
1. Fork this repository to your GitHub account.
2. Clone your fork locally and configure `upstream` if you like:
   - `git clone git@github.com:<your-username>/onboarding-2026.git`
   - `cd onboarding-2026`
   - `git remote add upstream git@github.com:init-club/onboarding-2026.git` (optional)
3. Create a feature branch for your change. Use the naming convention:
   - `feat/task-00-add-member-<your-github>`
   - Example: `git checkout -b feat/task-00-add-member-josuke-h`
4. Edit `members/MEMBERS.md`:
   - Add a single entry using the exact field names shown above.
   - Do not modify other entries.
5. Commit with a clear message:
   - Example: `git add members/MEMBERS.md`
   - `git commit -m "feat(task-00): add member Josuke Higashikata (josuke-h)"`
6. Push the branch to your fork and open a Pull Request to `onboarding-2026:main`.
7. In the PR description:
   - Link to the task(s) you are completing (e.g. `task-00`).
   - State any assumptions you made (e.g. preferred contact set to `private`).
   - If your contact is `private`, indicate how reviewers should reach you (e.g. via GitHub).
8. Wait for review. If changes are requested, update the same branch and push additional commits.

Pull request expectations
- One logical change per PR (one member entry).
- PR title should follow the pattern: `feat(task-00): add member <Full Name> (<github>)`.
- PR description should be concise and reference the task number(s).
- Address reviewer feedback promptly in the same branch.

Validation checks reviewers will run
- Entry uses the required keys and valid date format.
- No other entries were altered or removed.
- Contact field is appropriate for public display (or explicitly `private`).
- Branch and commit message follow conventions.

Ordering and maintenance
- Entries are kept in insertion order. Reviewers may suggest alphabetical order in future PRs; do not reorder existing entries when adding yourself.
- If your details change (role, contact, location), submit a follow-up PR to update only your entry and explain the reason in the PR description.

Troubleshooting
- If you accidentally change other lines, create a new branch from `main` and re-apply only your entry.
- If you included sensitive information accidentally, open an issue or contact the onboarding reviewer to request removal; prefer the private contact route in future.

Contact for this repository
- For questions specific to the onboarding process, mention the Init Club reviewer group (Init Club, Amrita Vishwa Vidyapeetham, Coimbatore) in your PR or reach out to your onboarding buddy.
