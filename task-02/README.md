# Task 02 — Git fundamentals and collaboration

Objective

Build practical confidence with common Git workflows used in collaborative projects:
- create and manage branches,
- synchronise work with the upstream repository using merge and rebase,
- resolve a simple merge conflict cleanly,
- produce a clean, reviewable pull request that demonstrates correct history and process.

Prerequisites

- Completion or familiarity with Task 00 (forking, branching, opening PRs).
- Git installed locally (version 2.20+ recommended).
- A fork of this repository on GitHub and the fork cloned locally.
- Basic command-line experience.

Estimated time

30–90 minutes, depending on familiarity with Git.

What this task involves

- Making a meaningful branch-based change.
- Simulating or resolving a merge conflict with upstream.
- Choosing an appropriate method to integrate upstream changes (merge or rebase).
- Creating a pull request with a tidy history and a README inside the task folder that explains the commands you used.

Step-by-step instructions

1. Prepare your fork and local repository

- Ensure your fork is cloned and you have an `upstream` remote configured:

```onboarding-2026/task-02/README.md#L1-6
git clone git@github.com:<your-username>/onboarding-2026.git
cd onboarding-2026
git remote -v
# If upstream not present, add it:
git remote add upstream git@github.com:init-club/onboarding-2026.git
git fetch upstream
```

2. Create a feature branch for this task

- Use the branch naming convention and keep the work focused:

```onboarding-2026/task-02/README.md#L7-10
git checkout -b feat/task-02-git-collab-<your-shortname>
```

3. Make a small change to demonstrate typical work

- Edit or add a file in `task-02/` (for example `task-02/NOTES.md`) with a short sentence. Commit with a conventional commit message:

```onboarding-2026/task-02/README.md#L11-16
echo "Initial notes by <your-github>." > task-02/NOTES.md
git add task-02/NOTES.md
git commit -m "feat(task-02): add initial notes for git collaboration task"
```

4. Simulate upstream activity (how reviewers may test conflict resolution)

- To practise conflict resolution, either:
  - Wait for a genuine upstream change to the same file; OR
  - Simulate by creating a conflicting change in the upstream repository (in a controlled environment) or ask a teammate to make a small edit; OR
  - If you cannot modify upstream, simulate a conflict locally by creating two branches and merging to reproduce the steps (document this clearly in your README).

5. Bring your branch up to date — two common approaches

- Option A — Merge from upstream (preserves history, records a merge commit):

```onboarding-2026/task-02/README.md#L17-24
# Ensure local main is up to date
git checkout main
git fetch upstream
git merge upstream/main
git push origin main

# Back on your feature branch
git checkout feat/task-02-git-collab-<your-shortname>
git merge main
# Resolve conflicts if any, then:
git add <files-with-conflicts-resolved>
git commit
```

- Option B — Rebase onto upstream (produces a linear history; preferred when your branch hasn't been published to others):

```onboarding-2026/task-02/README.md#L25-32
# Update local main
git checkout main
git fetch upstream
git rebase upstream/main
git push origin main

# Rebase your feature branch onto updated main
git checkout feat/task-02-git-collab-<your-shortname>
git rebase main
# Resolve conflicts during rebase as they arise (instructions below), then
git rebase --continue
# If necessary, force-push your branch to your fork:
git push --force-with-lease origin feat/task-02-git-collab-<your-shortname>
```

6. Resolve a simple merge conflict (illustrative example)

- When Git reports a conflict, open the conflicted file(s) and look for conflict markers:

```onboarding-2026/task-02/README.md#L33-40
<<<<<<< HEAD
Your local changes here.
=======
Upstream or other branch changes here.
>>>>>>> upstream/main
```

- Resolve by choosing the correct content (or combining both), then remove the markers:

```onboarding-2026/task-02/README.md#L41-46
# After editing the file to resolve conflicts:
git add path/to/conflicted-file.md
# If using merge:
git commit -m "fix(task-02): resolve merge conflict in path/to/conflicted-file.md"
# If using rebase:
git rebase --continue
```

Notes:
- If rebasing and you need to abort: `git rebase --abort`
- If merging and you wish to abort merge: `git merge --abort`

7. Push your branch and open the pull request

- After resolving conflicts and ensuring the branch is in the desired state:

```onboarding-2026/task-02/README.md#L47-52
git push origin feat/task-02-git-collab-<your-shortname>
# Open a PR on GitHub from your fork/branch into onboarding-2026:main
```

- In the PR description:
  - State whether you used merge or rebase to synchronise with upstream.
  - Explain the conflict and how you resolved it.
  - Include links to key files changed and to your `task-02/README.md` inside your branch.

Expected deliverables

- `task-02/README.md` (this file is the task instruction) remains as-is.
- `task-02/NOTES.md` (or similar) demonstrating your changes.
- `task-02/PROCESS.md` — a new file you must add that documents:
  - the exact commands you ran,
  - whether you used merge or rebase (and why),
  - the conflict markers you resolved and the decision you made,
  - any screenshots or terminal transcripts (optional) demonstrating the conflict and resolution.
- A pull request from your fork/branch to `onboarding-2026:main` containing the files above.

Submission and evaluation criteria

- PR must target `main` of this repository.
- The branch name and commit messages must follow the repository conventions.
- Deliverables must include `task-02/PROCESS.md` documenting the full sequence of commands and the rationale for merge vs rebase.
- Reviewer will inspect:
  - That the PR history is tidy and appropriate for the chosen strategy:
    - If you rebased, the branch history should be linear and you likely used a force-push.
    - If you merged, the merge commit should be clear and intentional.
  - That conflicts were resolved correctly and no conflict markers remain.
  - That the `PROCESS.md` accurately reflects the commands run.
- The PR will be accepted once the reviewer is satisfied with the technical correctness, clarity of documentation and adherence to conventions.

Best practices and guidance

- Use `rebase` for local, unpublished branches to keep history linear and simple.
- Use `merge` if your branch has been shared or if you prefer to preserve exact history.
- When rebasing, prefer `git rebase --interactive` for cleaning up commits, and `--force-with-lease` when pushing to avoid overwriting someone else's work.
- Keep commits small and focused; use descriptive conventional commit messages:
  - `feat(task-02): implement X`
  - `fix(task-02): resolve conflict in Y`
  - `docs(task-02): add PROCESS.md describing rebase steps`

Troubleshooting and common pitfalls

- I accidentally committed sensitive data
  - Stop, create a new branch, remove the sensitive file from history using tools like `git filter-branch` or `git filter-repo` (ask maintainers for assistance), and contact a reviewer.
- Rebase is complicated and you are mid-rebase
  - `git rebase --abort` returns you to the pre-rebase state.
- Force-push required after rebase
  - Use `git push --force-with-lease origin <branch>` to reduce risk of overwriting remote changes.
- Merge conflicts are noisy
  - Resolve conflicts in a text editor, run the test or lint checks you normally use, and add a commit explaining the resolution.

Optional extensions / learning outcomes

- Demonstrate an interactive rebase to squash minor fix commits and explain why you squashed them.
- Add a short script `task-02/rebase-vs-merge.sh` that demonstrates the difference on a toy repository (document clearly).
- Create a short screencast or terminal recording that shows the conflict and the resolution steps.

Assumptions

- The reviewer will have access to the upstream repository and can verify the PR.
- If you cannot create a real upstream conflict, document clearly how you simulated a conflict and why the simulation is equivalent for the learning goals.

Reviewer checklist

- [ ] PR targets `main` and follows branch naming conventions.
- [ ] `task-02/PROCESS.md` present and accurate.
- [ ] No conflict markers remain in committed files.
- [ ] Commit history is appropriate and explained: linear (if rebased) or contains merge commit (if merged).
- [ ] Clear explanation in PR body of merge vs rebase choice and steps taken.

Good luck — mastering these workflows will significantly improve your confidence working on team projects and open-source contributions. When you submit, be explicit about your choices and include precise command transcripts in `task-02/PROCESS.md` so reviewers can reproduce and verify your steps.
