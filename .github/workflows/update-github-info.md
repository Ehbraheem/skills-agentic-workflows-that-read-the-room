---
name: update-github-info
description: Draft website updates for Mona's GitHub Info site from official GitHub sources.
model: gpt-5-mini
on:
  workflow_dispatch:
  schedule:
    - cron: '17 9 * * *'
safe-outputs:
  create-pull-request:
    title-prefix: '[mona] '
    draft: true
    fallback-as-issue: false
tools:
  edit:
  web-fetch:
network:
  allowed:
    - github.com
    - github.blog
    - awesome-copilot.github.com
---

# Update Mona's GitHub Info website

Read `notes/mona-notes.md` before making changes.

Use the following sources as the basis for site updates:

- `notes/mona-notes.md`
- GitHub Blog: https://github.blog/latest/
- GitHub Changelog: https://github.blog/changelog/
- Awesome Copilot workflows: https://awesome-copilot.github.com/workflows/

Read external public guidance with web-fetch, especially the latest GitHub Blog, GitHub Changelog, and Awesome Copilot workflow updates. When repository guidance or reference files are needed, use GitHub repository API tools instead of terminal, CLI, or sandboxed commands.

Update `site/content/github-info.md` with concise, practical content for developers learning GitHub faster. Mention the source whenever content comes from the GitHub Blog, GitHub Changelog, or Awesome Copilot workflows.

Open a pull request for Mona to review. Use `safe-outputs` with `create-pull-request` so the agent can propose changes without writing directly to `main`.

Do not write directly to `main`; rely on `safe-outputs` and `create-pull-request` to open a `pull request` for Mona.
