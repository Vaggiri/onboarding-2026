# Task 01 — Local development environment setup

Objective

This task verifies that you can create a working local development environment suitable for the onboarding tasks and common day-to-day work. You will install or confirm essential tools, clone your fork, and provide evidence (logs or screenshots) showing the environment is functioning.

Why this task matters

- Ensures everyone has a reproducible baseline for future tasks.
- Confirms your ability to capture and present evidence for reviewers.
- Reduces friction when reviewers try to reproduce your steps.

Prerequisites

- A GitHub account and a fork of this repository (see `task-00`).
- Basic familiarity with your operating system (macOS, Linux or Windows).
- Internet access to download tools.

Recommended minimum tooling

- Git (2.20+ recommended)
- Visual Studio Code (or another code editor)
- A terminal (Terminal.app, iTerm2, Windows Terminal, or equivalent)
- Optionally: Node.js/npm (for simple tooling), Python 3 (for scripting)

Estimated time

30–90 minutes depending on your OS and whether the tools are already installed.

Directory layout for this task

- `task-01/README.md` — this file
- `task-01/logs/` — place command logs here (plain text)
- `task-01/screenshots/` — place screenshots here (PNG or JPG)
- `task-01/writeup.md` — short write-up describing your steps and any issues

Step-by-step instructions

Follow the steps below. Where appropriate, choose the commands that match your operating system.

1. Confirm or install Git

- macOS (Homebrew):
```onboarding-2026/task-01/README.md#L1-4
brew update
brew install git
git --version
```

- Ubuntu / Debian:
```onboarding-2026/task-01/README.md#L5-8
sudo apt update
sudo apt install -y git
git --version
```

- Windows (Git for Windows)
  - Download and run the installer from https://git-scm.com/.
  - Then in Powershell / Windows Terminal:
```onboarding-2026/task-01/README.md#L9-12
git --version
```

Save the output of `git --version` to `task-01/logs/git-version.txt` (copy-and-paste the terminal output).

2. Install Visual Studio Code (recommended) or confirm your editor

- macOS (Homebrew Cask):
```onboarding-2026/task-01/README.md#L13-16
brew install --cask visual-studio-code
code --version
```

- Linux (deb):
```onboarding-2026/task-01/README.md#L17-20
# Example for Debian/Ubuntu using the VS Code repo
wget -qO- https://packages.microsoft.com/keys/microsoft.asc | gpg --dearmor > microsoft.gpg
sudo install -o root -g root -m 644 microsoft.gpg /usr/share/keyrings/
# Follow official instructions: https://code.visualstudio.com/docs/setup/linux
code --version
```

- Windows
  - Download from https://code.visualstudio.com/ and run the installer.
  - Verify in a terminal:
```onboarding-2026/task-01/README.md#L21-24
code --version
```

Save the output of `code --version` to `task-01/logs/code-version.txt`.

3. Clone your fork and set upstream (use the method you prefer: SSH or HTTPS)

```onboarding-2026/task-01/README.md#L25-32
# SSH example (recommended if you have SSH keys)
git clone git@github.com:<your-username>/onboarding-2026.git
cd onboarding-2026

# Add upstream to keep your fork in sync
git remote add upstream git@github.com:init-club/onboarding-2026.git
git fetch upstream
git branch -a
```

Save the terminal transcript to `task-01/logs/clone-log.txt`. If you used HTTPS, replace the clone URL accordingly.

4. Run a few basic Git commands to demonstrate everything is working

```onboarding-2026/task-01/README.md#L33-40
# Show remotes and branches
git remote -v
git status

# Create and switch to a temporary branch to demonstrate commit workflow
git checkout -b tmp/task-01-verify
git commit --allow-empty -m "chore(task-01): verify local git environment"
git log --oneline -n 3
```

Save the output to `task-01/logs/git-commands.txt`.

5. Capture evidence

- Logs: Place the saved text files in `task-01/logs/` and ensure they contain relevant outputs.
- Screenshots: For GUI steps (e.g. VS Code opening the repository) add screenshots in `task-01/screenshots/`.
- Write-up: Create `task-01/writeup.md` with a short summary (200–400 words) describing:
  - which OS you used,
  - which tools you already had vs installed,
  - any issues you encountered and how you resolved them,
  - what you would do differently next time.

Example `writeup.md` structure
- Environment: macOS 12.4, Git 2.39.0, VS Code 1.76.0
- Steps performed: list of commands you ran
- Problems and solutions: short notes
- Next steps / follow-up: items to address (optional)

Expected deliverables

- `task-01/logs/git-version.txt`
- `task-01/logs/code-version.txt`
- `task-01/logs/clone-log.txt`
- `task-01/logs/git-commands.txt`
- `task-01/screenshots/` (one or two relevant screenshots)
- `task-01/writeup.md`

Place all files under `task-01/` in your branch before opening a PR.

Submission and evaluation criteria

Submission

1. Create a feature branch from `main`: use the branch naming convention:
   - `feat/task-01-setup-local-env` or `feat/task-01-<your-shortname>`.
2. Add the files listed in Expected deliverables to `task-01/`.
3. Commit using conventional-style commit messages:
```onboarding-2026/task-01/README.md#L41-44
git add task-01/
git commit -m "docs(task-01): add environment logs and setup write-up"
```
4. Push the branch to your fork and open a Pull Request to `onboarding-2026:main`.

Evaluation criteria

- Completeness: all required deliverables are present in `task-01/`.
- Evidence: logs and screenshots clearly show the tools are installed and functional.
- Clarity: `writeup.md` explains what was done and any issues encountered.
- Process: branch naming and commit messages follow the repository conventions.
- Reproducibility: a reviewer can follow your steps to reach the same state.

Reviewers will check the logs, open a sample of the files, and, if necessary, run a quick verification (for example, cloning your branch and opening VS Code).

Optional extensions (recommended for learning)

- Add a small verification script `task-01/check-env.sh` (or `.ps1` on Windows) which prints `git --version`, `code --version`, `node --version` (if installed). Make sure to document how to run it in `writeup.md`.
- Provide brief notes on how to set up SSH keys with GitHub and link to the official documentation.
- Add editor configuration recommendations (`.editorconfig`, recommended VS Code extensions in a `task-01/vscode-extensions.txt`).
- Explain how to enable autosave, recommended extensions, or workspace settings for accessibility.

Troubleshooting and common issues

- Permission denied (SSH) when cloning:
  - Check your SSH key is added to GitHub, or use HTTPS for cloning.
- `git` not found:
  - Ensure your PATH includes the `git` binary or reinstall Git.
- `code` not recognised:
  - On macOS and Windows, ensure the `code` CLI is installed/enabled:
    - In VS Code: Command Palette → “Shell Command: Install 'code' command in PATH”.
- If you get merge conflicts when creating branches, rebase or merge `upstream/main` into your local `main`, recreate a clean branch and reapply your changes.

Assumptions

- This task assumes access to the internet and administrative rights to install software.
- It assumes a fairly recent OS release; commands may differ on older systems.
- If you cannot install software (e.g. restricted machine), document the restriction in `task-01/writeup.md` and provide screenshots of what you could accomplish.

Reviewer verification checklist

- [ ] Confirm presence of the required log files in `task-01/logs/`.
- [ ] Confirm at least one screenshot in `task-01/screenshots/`.
- [ ] Read `task-01/writeup.md` and ensure it documents the environment and any issues.
- [ ] Branch and commit naming conform to `CONTRIBUTING.md`.
- [ ] Evidence is sufficient for acceptance, or reviewer gives targeted feedback.

Final notes

Be explicit in your write-up about any deviations from the instructions and include the exact commands you ran — reviewers value reproducibility. When in doubt, add more context rather than less.

Good luck — once this task is approved you may continue to `task-02`.
