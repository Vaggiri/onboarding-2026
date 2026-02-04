# Task 04 — Small technical implementation

Objective

Implement a small, well-documented programme or script that demonstrates basic problem-solving, separation of logic and presentation, and adherence to minimal coding standards. This task assesses your ability to write clear, maintainable code and provide sufficient instructions for others to run and review it.

Prerequisites

- Completion of `task-00` and `task-01` recommended.
- A working local development environment with:
  - Git
  - An interpreter or runtime for your chosen language (examples below use Python 3.8+)
  - A text editor or IDE (e.g. VS Code)
- Basic familiarity with running commands in a terminal

Scope and constraints

- Keep the implementation small: one module/library and one CLI or invocation entry point.
- Keep dependencies minimal — prefer standard library where feasible.
- Demonstrate separation of concerns:
  - Core logic in a module (e.g. `src/` or `lib/`)
  - CLI or runnable wrapper in `bin/` or at repository root
  - Tests in `tests/`
- Provide clear documentation and examples for running and testing the code.

Suggested project ideas (pick one)

- A command-line CSV summariser: compute column means, counts, and basic statistics.
- A small HTTP healthcheck script that queries a URL and returns structured JSON with timing.
- A configuration validator: read a simple YAML/JSON file and report missing or invalid fields.
- A short data transformer: read JSON input and output a filtered, reformatted JSON.

Directory layout (recommended)

- `task-04/`
  - `README.md` (this file)
  - `src/` — source code (module(s))
  - `bin/` — executable wrapper(s) or entrypoint scripts
  - `tests/` — unit tests
  - `examples/` — example input and expected output
  - `requirements.txt` or `pyproject.toml` (if needed)
  - `LICENSE` (optional)

Step-by-step instructions (beginner-friendly)

1. Choose language and minimal dependencies

   - Recommended: Python 3.8+ (standard library), or a single-file Bash script, or Node.js (small package.json).
   - If you use external packages, document them in `requirements.txt` or `package.json`.

2. Create a new branch for the task

```onboarding-2026/task-04/README.md#L1-4
git checkout -b feat/task-04-<short-desc>
```

3. Implement core logic in `src/`

   - Keep functions small and pure where possible.
   - Add docstrings or comments that explain intent and parameters.
   - Ensure the module exposes a clear API (one or two public functions).

Example: minimal Python module structure

```onboarding-2026/task-04/README.md#L5-14
# src/summary.py
def summarize_numbers(numbers):
    \"\"\"Return a dict with count, sum, mean.\"\"\"
    if not numbers:
        return {"count": 0, "sum": 0, "mean": None}
    count = len(numbers)
    total = sum(numbers)
    mean = total / count
    return {"count": count, "sum": total, "mean": mean}
```

4. Provide a CLI or small wrapper in `bin/` or at project root

   - The CLI should accept input as arguments or read from a file/stdin.
   - Provide helpful `--help` text.

Example: a simple CLI invocation

```onboarding-2026/task-04/README.md#L15-22
# bin/run-summary (executable script)
# Usage: python -m task04.summary --input examples/numbers.txt
# or: ./bin/run-summary examples/numbers.txt
```

5. Add tests in `tests/`

   - Use a minimal test framework (Python `unittest` or `pytest`) and include 3–5 small tests covering normal and edge cases.
   - Keep tests deterministic and fast.

Example: a minimal test case

```onboarding-2026/task-04/README.md#L23-30
# tests/test_summary.py
def test_summarize_numbers_empty():
    assert summarize_numbers([])["count"] == 0

def test_summarize_numbers_basic():
    assert summarize_numbers([1, 2, 3])["mean"] == 2
```

6. Add examples and usage instructions in `task-04/examples/`

   - Include at least one sample input file and the expected output or a simple script demonstrating the expected output.

7. Document how to run and test

   - Add run instructions to `task-04/README.md` (this file). Use command examples and expected output.

Run and test examples (Python)

```onboarding-2026/task-04/README.md#L31-44
# From repository root (example)
git checkout feat/task-04-<short-desc>
python -m venv .venv
source .venv/bin/activate
pip install -r task-04/requirements.txt   # if requirements exist
python -m src.summary --input task-04/examples/numbers.txt
# Run tests
pytest task-04/tests
```

Expected deliverables

- Source code for the implementation under `task-04/src/` (or `lib/`).
- Executable wrapper(s) under `task-04/bin/` or clear `python -m` entrypoint.
- Unit tests in `task-04/tests/` with instructions to run them.
- Example files in `task-04/examples/` demonstrating input and expected output.
- A short `task-04/IMPLEMENTATION.md` (or include a section in this README) describing:
  - design choices,
  - separation of logic and I/O,
  - any external dependencies,
  - how to run and test locally.
- A pull request that follows branch and commit message conventions.

Submission and evaluation criteria

- Submit work as a pull request from your fork to `main` following the branch conventions in `CONTRIBUTING.md`.
- The PR should include:
  - A clear title (e.g. `feat(task-04): add CSV summariser tool — <Your Name>`).
  - A PR description that lists deliverables and any assumptions.
  - Links to key files in your branch.
- Reviewers will evaluate:
  - Correctness: does the programme behave as described and produce expected output for the provided examples?
  - Structure: is logic separated from I/O and are modules small and focused?
  - Tests: are there tests that cover typical and edge cases?
  - Documentation: are run instructions clear and sufficient for reproducibility?
  - Code quality: readability, consistent naming, brief comments/docstrings, no obvious security issues.
  - Adherence to conventions: branch name and commit messages follow `CONTRIBUTING.md`.
- Passing criteria:
  - The repository contains the expected files and examples.
  - Tests pass locally and are easy for reviewers to run.
  - The PR description documents any notable decisions or deviations.

Examples of acceptable minimal commit sequence

```onboarding-2026/task-04/README.md#L45-52
git add task-04/src task-04/bin task-04/tests task-04/examples
git commit -m "feat(task-04): add initial CSV summariser implementation and tests"
git push -u origin feat/task-04-csv-summariser
```

Best practices and coding standards

- Use clear, descriptive function and variable names.
- Keep line length reasonable (~80–100 chars).
- Include docstrings for public functions and a brief module header comment describing purpose.
- Handle invalid input gracefully and provide helpful error messages.
- Avoid committing large binary files; keep examples small.
- Use a linter or formatter if available (e.g. `black` / `flake8` for Python) and include configuration if used.

Optional extensions (for bonus learning)

- Add continuous integration (GitHub Actions) that runs tests on PRs.
- Provide a Dockerfile to run the tool in a container (useful for consistent runtimes).
- Add argument validation and richer output formats (CSV, JSON).
- Add a brief performance test if the input may be large (document expected behaviour).
- Provide a simple bench or profiling note in `IMPLEMENTATION.md`.

Accessibility, security and privacy notes

- Do not include real personal data in example files.
- If your tool reads network endpoints or private files, document how to supply safe test endpoints or mock data.
- Make error messages user-friendly and avoid leaking sensitive information (e.g. stack traces).

Learning outcomes

- You will practice designing a small but maintainable codebase.
- You will learn how to separate logic and I/O for testability.
- You will show ability to document and test your work for a reviewer.
- You will become familiar with writing small, reviewable PRs that follow project conventions.

Assumptions and notes

- This task assumes the reviewer will run tests locally and that the environment is typical (Python 3.8+, or the runtime you choose).
- If any requirement is ambiguous, include an explicit `Assumptions` section in `task-04/IMPLEMENTATION.md` and document why you chose a particular approach.
- Keep the implementation self-contained so that reviewers can verify quickly.

Reviewer checklist (quick)

- [ ] Code present in `task-04/src/` and runnable.
- [ ] Executable wrapper documented and present.
- [ ] Tests present, runnable and passing.
- [ ] Examples showing expected behaviour.
- [ ] Implementation notes and run instructions included.
- [ ] PR follows branch and commit naming conventions.

If you are ready, create the branch, implement the small programme as described, add tests and examples, and open a PR describing your work. Good implementations are small, well-documented and easy to verify.