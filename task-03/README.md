# Task 03 — Documentation and Markdown skills

Objective

This task develops your ability to write clear, structured technical documentation using Markdown. You will produce a well-written `README.md` that explains a technical concept, demonstrates Markdown features (headings, lists, tables, code blocks, links and images), and follows the project's style and accessibility expectations.

Prerequisites

- Completion of `task-00` (repository basics) and `task-01` (local environment) is recommended.
- Basic familiarity with Markdown (if you are new, this task will guide you).
- An editor that can edit plain text (VS Code recommended).

What this task involves

- Selecting a concise technical topic appropriate for a short README (examples below).
- Writing a structured document that teaches or documents the topic.
- Using Markdown features correctly and consistently.
- Providing examples, code snippets and at least one table or checklist.
- Including a short self-review section that explains your editorial choices and any assumptions.

Suggested topics (pick one)

- A simple explanation of Git branching strategies (feature branch vs main).
- How to create and use a Python virtual environment.
- A short guide to setting up a developer-friendly VS Code workspace.
- Explaining a small script you wrote for `task-04` (if you plan to complete both tasks).

Deliverable

- `task-03/README.md` — a Markdown document that:
  - Is at least 300 words, structured with headings and subheadings.
  - Contains at least one fenced code block showing a practical command or snippet.
  - Includes at least one table and one checklist.
  - Uses British English spelling and follows clear, inclusive language.
  - Has no spelling or obvious formatting errors.

Step-by-step instructions

1. Choose your topic
   - Pick a focused topic that can be explained clearly in a short README. Avoid overly broad or highly specialised subjects.

2. Create the document structure
   - At minimum include:
     - Title
     - Objective
     - Prerequisites
     - Step-by-step instructions or explanation
     - Examples (code blocks where appropriate)
     - Expected outcomes / deliverables
     - Self-review or reflection
   - Use headings to break content into logical sections.

3. Write the content
   - Be concise and precise. Use short paragraphs and bullet lists for readability.
   - Use code formatting for filenames and short commands: e.g. `git status`, `README.md`.
   - When including longer command sequences or code, use a fenced code block.

4. Include a table and a checklist
   - Tables are useful for quick comparisons or configuration summaries.
   - Checklists help reviewers and readers verify steps.

5. Add examples and runnable commands
   - Provide at least one minimal, runnable example or command sequence the reviewer can copy and paste.
   - Where appropriate, show both the command and expected output.

6. Self-review
   - Add a short section titled `Self-review` describing editorial choices, any assumptions, and a short note about accessibility (e.g. alt text for images, clear link text).

7. Commit and submit
   - Create a branch named `docs/task-03-<short-desc>` and commit your `task-03/README.md`.
   - Open a pull request that references `task-03` and includes a brief summary of the deliverable.

Markdown examples and templates

- Example inline code and filenames:
  - Use backticks for inline code: `python -m venv venv` or `README.md`.

- Fenced code block (command sequence):
```onboarding-2026/task-03/README.md#L301-320
# Example: create and activate a Python virtual environment (macOS / Linux)
python3 -m venv .venv
source .venv/bin/activate
pip install --upgrade pip
pip install -r requirements.txt
```

- Example table (configuration summary):

| Setting | Typical value | Notes |
|---|---:|---|
| Python | `3.10` | Use the project `.python-version` if present |
| Virtual env | `.venv/` | Local to the repository |
| Editor | `VS Code` | Recommended: install workspace settings |

- Example checklist (for the reader to verify):

- [ ] I have Python 3.8+ installed.
- [ ] I created and activated a virtual environment.
- [ ] I installed required packages from `requirements.txt`.

A recommended README template

Copy, fill and adapt this template for your submission. Provide the filled template as `task-03/README.md` in your branch.

```onboarding-2026/task-03/README.md#L321-420
# Title: <Short descriptive title>

## Objective
A short statement of what this README explains and who it is for.

## Prerequisites
- Itemised list of required software or knowledge (versions where relevant).

## Quick summary
A one-paragraph summary that gives the reader the gist in a sentence or two.

## Step-by-step instructions
1. Step one with command or example:
   - `command --example`
2. Step two with notes.

## Example (runnable snippet)
# Paste minimal, runnable example here
echo "Hello, world"

## Table: quick reference
| Key | Value | Notes |
|---|---|---|
| example | value | short note |

## Checklist (for readers)
- [ ] Task verified
- [ ] Example ran successfully

## Self-review
Explain your assumptions, editorial choices, and any accessibility considerations.

```

Best practices and style guidance

- Use British English spelling (e.g. organisation, initialise, behaviour).
- Keep sentences short and paragraphs compact.
- Use meaningful headings that reflect content.
- Use accessible link text: avoid 'click here' — prefer descriptive text.
- Add alt text for images: `![Screenshot of VS Code opening the workspace](screenshots/vscode-workspace.png)`.
- Prefer unordered lists for items without inherent order and ordered lists for step sequences.

Evaluation criteria

Your submission will be reviewed against the following:

- Completeness (the `README.md` meets the deliverable checklist above).
- Clarity (content is easy to follow and logically ordered).
- Markdown correctness (code fences, lists, tables render correctly).
- Adherence to conventions (branch name, commit message formatting per `CONTRIBUTING.md`).
- Quality of examples (runnable where applicable) and accuracy of expected outputs.
- Use of British English and absence of obvious spelling mistakes.
- Inclusion of a `Self-review` section describing assumptions.

Grading rubric (informal)

- Excellent: clear, concise, includes runnable examples, table and checklist, self-review present.
- Good: mostly complete but minor issues in clarity or missing small examples.
- Needs improvement: missing expected elements (table, checklist, examples) or poor organisation.

Submission checklist (for your PR)

- [ ] Branch named `docs/task-03-<short-desc>` and pushed to your fork.
- [ ] `task-03/README.md` is present and follows the template above.
- [ ] Commit messages follow conventional style, e.g. `docs(task-03): add README about X`.
- [ ] PR description references `task-03` and lists deliverables and assumptions.

Optional extensions (for learning)

- Add screenshots in `task-03/screenshots/` with appropriate alt text.
- Provide a short `CONTRIBUTING` subsection explaining how others can improve your README.
- Create a small example repository or gist and link to it for longer samples.
- Create a short accessibility checklist and run it against your document.

Notes and assumptions

- This task assumes the reader can run basic shell commands. If you cannot, provide screenshots and clear descriptions of actions taken.
- If your topic requires platform-specific commands, provide both macOS/Linux and Windows examples when feasible.
- If any instruction is ambiguous, document your assumption in the `Self-review` section of your README.

If you are ready, create `task-03/README.md` using the template, commit it on a correctly named branch and open a pull request for review. Good documentation is as important as working code — take the time to make your README helpful to a newcomer.