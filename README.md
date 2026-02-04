<div align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/init-club/.github/main/assets/logo-dark.svg">
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/init-club/.github/main/assets/logo-light.svg">
    <img alt="Init Club Logo"
         src="https://raw.githubusercontent.com/init-club/.github/main/assets/logo-light.svg"
         width="300">
  </picture>
    <h1>Onboarding Tasks for Init Club Members - 2026</h1>
</div>

Welcome — this repository contains the official onboarding tasks for new members joining the Init Club at Amrita Vishwa Vidyapeetham, Coimbatore in 2026. Its purpose is to give you a clear, practical path from first contact to working confidently with our code, tools and processes.

This top-level README explains:
- what the repository is for,
- the available tasks and a short description of each,
- how you should approach and submit work,
- evaluation expectations,
- the basic GitHub workflow we expect you to follow.

If you are editing files here, please also read `CONTRIBUTING.md` for the full contribution process and branch rules.

---

## Purpose

This repo is a single place for structured onboarding tasks. Each task is self-contained inside its own directory (`task-00/`, `task-01/`, ... `task-06/`) and includes a detailed `README.md` that covers the objective, prerequisites, step-by-step instructions, expected deliverables, and evaluation criteria.

Use this repo to:
- learn our Git/GitHub workflow,
- practise local development setup,
- demonstrate basic technical skills,
- contribute small improvements to a shared repository,
- optionally write a reflective blog post of your learning.

All evaluated tasks must be submitted via GitHub pull requests. Blogging or personal write-ups are optional but encouraged for your portfolio.

---

## Repository structure

At the top level you will find:

- `README.md` — this file (overview and workflow).
- `CONTRIBUTING.md` — contribution rules, branching strategy and PR guidelines.
- `members/` — a directory containing `members.yml` (or `members.md`) where you add your personal details via PR.
- `task-00/` through `task-06/` — each task folder contains a `README.md` and any sample files or templates required.

All task folders follow the naming convention: `task-0N` where `N` is the task number with leading zero for consistent sorting (e.g. `task-00`, `task-01`, ...).

---

## Task list (short descriptions)

- `task-00` — Repository onboarding and Git workflow  
  Objective: Fork the repository, create a feature branch, add your details to `members/`, and open a PR.

- `task-01` — Local development environment setup  
  Objective: Install required tools, clone your fork, and demonstrate a working local setup with logs/screenshots.

- `task-02` — Git fundamentals and collaboration  
  Objective: Use branches, rebase or merge from upstream, and resolve a simple merge conflict; submit a clean PR.

- `task-03` — Documentation and Markdown skills  
  Objective: Produce a clear, structured README explaining a technical concept using headings, code blocks and lists.

- `task-04` — Small technical implementation  
  Objective: Implement a small script or configuration demonstrating problem-solving and coding standards.

- `task-05` — Open-source style contribution  
  Objective: Pick an issue or improvement in this repo, make a meaningful change and submit an approved PR.

- `task-06` — Learning reflection (optional blog)  
  Objective: Write a blog post or markdown article explaining what you learned. Optional; not required for evaluation.

Each task directory includes full, beginner-friendly instructions. Start with `task-00` and proceed in order; you may complete tasks in parallel if you prefer.

---

## How you should approach tasks

1. Read the task `README.md` in full before starting.
2. Make a small, focused change per pull request. Keep PRs atomic and well described.
3. Follow the branch naming and commit message conventions below.
4. Include evidence required by the task (screenshots, logs, small programmes, or markdown write-ups).
5. If something is unclear, add a short note in your PR describing the assumption you made — reviewers value transparency.
6. Keep accessibility and clarity in mind when writing documentation.

---

## Evaluation expectations

- All evaluated tasks must be submitted through GitHub pull requests to this repository (your fork → main repository).
- Pull requests should include:
  - A descriptive title and summary,
  - Link(s) to relevant files in your branch,
  - Evidence of work (screenshots, logs, or runnable examples),
  - A brief explanation of any assumptions or deviations.
- Reviewers from the Init Club will comment on technical correctness, clarity and process adherence.
- Blogs are optional and will not substitute GitHub submission. A blog is a showcase, not a submission channel.

---

## Quick start — fork, clone, branch, PR

Use the GitHub UI to fork this repository to your account. Then run these commands locally (example):

```onboarding-2026/README.md#L1-12
# Replace <your-username> and <repo> as needed
git clone git@github.com:<your-username>/onboarding-2026.git
cd onboarding-2026
git remote add upstream git@github.com:init-club/onboarding-2026.git
git fetch upstream
```

Create a feature branch (branch naming conventions below) and make changes:

```onboarding-2026/README.md#L13-24
# Create and switch to a new branch
git checkout -b feat/task-00-add-member-yourname

# Make your edits (e.g. add entry to members/members.yml), then
git add members/members.yml
git commit -m "feat(task-00): add member entry for Your Name (email@example.com)"
git push -u origin feat/task-00-add-member-yourname
```

Then open a Pull Request from your fork/branch into `main` of the upstream repository using the GitHub website. Use the PR template if present.

---

## Branch naming and commit message conventions

Branch names:
- Feature branches: `feat/task-0N-short-desc` (e.g. `feat/task-02-resolve-merge-conflict`)
- Fix branches: `fix/task-0N-short-desc`
- Docs branches: `docs/task-0N-short-desc`

Keep names short, lowercase and hyphen-separated.

Commit messages:
- Use conventional style: `type(scope): short summary`  
  Example: `feat(task-01): document local setup steps`  
- Use `type` values such as `feat`, `fix`, `docs`, `chore`, `test`.
- Keep the summary under 72 characters; add a longer body if necessary.

---

## Pull request checklist

When you open a PR, ensure:
- [ ] The PR title is descriptive and follows project conventions.
- [ ] The PR description explains what you changed and why.
- [ ] All required files for the task are present (evidence, write-ups, code).
- [ ] The branch contains only related commits (squash if necessary).
- [ ] You added yourself to `members/` as required by `task-00`.
- [ ] You responded to CI or reviewer comments in a timely manner.

---

## Adding yourself to `members/`

The `members/` directory contains `members.yml` (or `members.md`) with a clear format. Add one entry per person. Example entry format (use the file in `members/` as the authoritative template):

```onboarding-2026/README.md#L40-51
# Example member entry (YAML)
- name: Your Full Name
  github: your-github-username
  email: your.email@example.com
  role: Research Associate
  start_date: 2026-02-01
  location: City, Country
  notes: "Short note about interests or primary skills"
```

When you submit your PR for `task-00`, include a link to your fork/branch and a short note confirming you've read the CONTRIBUTING guidelines.

---

## Support and review

- Reviewers will aim to provide feedback within a reasonable timeframe; if you need urgent help, mention the relevant contact in your PR or reach out to your onboarding buddy.
- For questions about evaluation criteria, direct them to the Init Club reviewer group.

---

## Accessibility and inclusivity

Write documentation and code samples that are accessible and considerate:
- Avoid unnecessarily complex language.
- Use clear, descriptive headings and alt text for images.
- Prefer inclusive examples and names.

---

If you are ready, start with `task-00` and follow its `README.md`. Best of luck — we look forward to reviewing your first pull request.
