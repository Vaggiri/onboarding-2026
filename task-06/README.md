# Task 06 — Learning reflection (optional blog)

Objective

- Encourage reflective technical writing: articulate what you learned during onboarding, how you approached problems, and what you would do next.
- Build a public-facing artefact that demonstrates communication skills and consolidates learning.
- This task is optional and not required for formal evaluation; it may be used for mentoring or portfolio purposes.

Why this task matters

- Reflection improves retention and helps others learn from your experience.
- A well-written blog post is useful evidence of growth and can be shared with colleagues or included on your profile.
- Practising public technical writing improves concision, clarity and accessibility.

Prerequisites

- Completion of earlier onboarding tasks (recommended) so you have concrete experiences to reflect on.
- Basic Markdown skills and a platform to publish (GitHub, GitHub Pages, dev.to, Medium, personal blog).
- Optional: basic image editing for screenshots, and familiarity with including metadata (YAML front matter) if you publish to a static site.

Scope and expectations

- Pick a topic closely related to your onboarding: a technical concept you implemented, lessons from working with Git and reviews, a walkthrough of a small implementation, or a reflective summary of your first weeks.
- Keep the post focused — one main idea with 2–4 supporting sections.
- Length: aim for ~600–1,200 words for a substantive post; shorter vignettes (~300–500 words) are acceptable.
- Use inclusive, accessible language and British English spelling.

Suggested topics

- "How I resolved my first merge conflict — a walkthrough"
- "Setting up a reproducible local dev environment for onboarding"
- "Design decisions in my small implementation (task-04): why I separated logic from I/O"
- "What I learned about open-source collaboration from task-05"
- "A reflective summary: three improvements I'd make to my workflow"

Step-by-step instructions

1. Choose your topic
   - Pick something you found interesting, challenging or instructive during onboarding.

2. Draft the post locally
   - Prefer Markdown for portability.
   - Include a short title, a 1–2 line summary, headings, code or command snippets where helpful, and one concluding reflection.

3. Add images or screenshots (optional)
   - Keep images small and add descriptive alt text.
   - Avoid publishing sensitive or personal data.

4. Publish
   - Option A (recommended for visibility): add a Markdown file to `task-06/<your-github>/POST.md` in your fork and open a PR linking to it.
   - Option B: publish externally (dev.to, Medium, personal blog) and include the public URL in a PR or comment.

5. Share and optionally request feedback
   - In your PR, ask reviewers for feedback on clarity and accuracy if you want reviewer comments.

Expected deliverables

You may choose one of the following delivery options:

A. Repository-based (recommended)
   - `task-06/<your-github>/POST.md` — the blog post in Markdown.
   - Optional: `task-06/<your-github>/images/` — any screenshots used (include alt text in the post).
   - Optional: a short `task-06/<your-github>/SUMMARY.md` listing the specific onboarding tasks referenced.

B. External
   - A public URL to your published post (dev.to, Medium, personal site).
   - In your PR or submission note, include the URL and a short summary.

Submission and evaluation criteria

- This task is optional and not part of formal evaluation. However:
  - If you add the post to the repository, open a PR for visibility and informal feedback.
  - Reviewers may provide editorial suggestions focused on clarity and accuracy.
  - The blog will not replace evaluated task submissions — ensure all evaluated tasks are submitted via GitHub PRs as required.

Recommended PR contents (if adding to the repo)

- PR title: `docs(task-06): add reflection post — <Your Name>`
- PR description:
  - Short summary of the post.
  - Which onboarding tasks you referenced.
  - Link to rendered Markdown file in your branch.
  - Any requests for feedback (e.g. "Please review clarity of the merge-conflict section").

Blog post template

Use the template below as a starting point. Create `task-06/<your-github>/POST.md` and paste the template, then fill it in.

```onboarding-2026/task-06/README.md#L1-60
# Title: <Concise, descriptive title>

Summary
A one- or two-sentence summary of the post and its audience.

Introduction
Short paragraph explaining why this topic matters and your context (which onboarding tasks this relates to).

What I did
- Bullet list of concrete actions you took (e.g. completed task-02 rebase, implemented CSV summariser in task-04).

Key lessons
1. Lesson one — explanation, short example or command snippet if relevant.
2. Lesson two — explanation and how it changed your approach.
3. Lesson three — brief actionable tip.

Example / Walkthrough (optional)
- Provide a minimal, runnable example or command sequence.
- Show expected output.

Reflection
- How this will change your practice going forward.
- Things you would do differently next time.

Further reading and references
- Links to documentation, blog posts or official references.

Acknowledgements (optional)
- People who helped or reviewed your work.

Metadata (optional)
- Tags: onboarding, git, documentation, <your-tags>
- Date: YYYY-MM-DD
```

Publishing options and tips

- GitHub (in-repo): create `task-06/<your-github>/POST.md` and open a PR. Advantages: permanent, easy to link from your profile.
- GitHub Pages: use if you maintain a personal site and want a polished page.
- dev.to: quick, supports Markdown and metadata, good discoverability.
- Medium: widely used but consider paywall and content ownership.

Accessibility and privacy

- Add alt text for all images.
- Avoid posting proprietary or sensitive data (snippets that include internal endpoints, secrets, or personal identifiable information).
- If discussing interactions with colleagues, get their permission before naming them or quoting private messages.

Quality checklist before publishing

- [ ] Title is descriptive and concise.
- [ ] Summary and introduction clearly state purpose and audience.
- [ ] Post follows British English spelling.
- [ ] Code snippets are minimal and tested (where applicable).
- [ ] Images include alt text and are optimised for size.
- [ ] No sensitive information is included.
- [ ] If added to the repository, PR follows branch and commit conventions.

Optional extensions (for learning)

- Turn your post into a short slide deck or screencast.
- Convert your Markdown to a blog post with a static site generator (Jekyll, Hugo) and document the process.
- Add a short rubric evaluating the post for clarity and reproducibility.

Assumptions and notes

- This task is explicitly optional: it is designed for learning and portfolio development, not for formal scoring.
- If you add your post to the repository, treat the PR as a request for informal feedback rather than an evaluation.
- Keep posts technical, constructive and focussed on learning outcomes.

If you want feedback from reviewers, include a note in your PR describing what kind of feedback you want (clarity, technical correctness, grammar). We welcome well-made posts and will provide constructive comments where possible.