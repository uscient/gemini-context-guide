# Gemini Context Guide

Unofficial guidance for managing personal context, Notebook scope, saved information, browser/page context, and one-off chats when using Google Gemini.

This guide is for people who want useful AI continuity without letting unrelated projects, personal topics, research, browser pages, videos, or connected apps blend together silently.

## The short version

Modern AI assistants may use more than the words in the current prompt. Depending on settings and product features, Gemini may use saved instructions, past chats, Notebook sources, browser/page context, uploaded files, videos, or connected Google apps.

That can be useful. It can also make it hard to tell why an answer included a certain fact.

This guide provides practical instructions and tests for asking Gemini to:

- use only the intended information
- keep unrelated projects separate
- say what information it used
- avoid silently importing context from another chat, Notebook, app, or project
- handle YouTube, Chrome, browser tabs, and one-off chats more carefully

## What this does not do

This guide does **not** guarantee isolation inside Gemini.

It also does not replace Google’s settings, privacy controls, Workspace admin controls, or official documentation. Product behavior can change, and Gemini may still make mistakes.

This guide does not provide legal, privacy, security, or compliance advice.

## Start here

1. Read [How to use this guide](docs/how-to-use.md).
2. Review [Settings and surfaces to inspect](docs/settings-and-surfaces.md).
3. Add the general instruction in [`instructions/global-gemini-instruction.md`](instructions/global-gemini-instruction.md), if it fits your needs.
4. Add the Notebook instruction in [`instructions/notebook-boundary-instruction.md`](instructions/notebook-boundary-instruction.md) to important Notebooks.
5. Run [`tests/instruction-activation-check.md`](tests/instruction-activation-check.md) in a new chat.
6. Run [`tests/notebook-boundary-test.md`](tests/notebook-boundary-test.md) inside a Notebook.
7. Use [`tests/source-audit-prompt.md`](tests/source-audit-prompt.md) when an answer seems to use information from the wrong place.

## Common workflows

| Situation | Recommended workflow |
|---|---|
| Random question | Treat as a one-off chat |
| YouTube/video question | Use only the provided video/link/transcript |
| Browser-tab question | Treat the shared tab as an explicit source |
| Project work | Use a dedicated Notebook |
| Legal/business/research work | Use a dedicated Notebook with stricter instructions |
| A one-off becomes project-relevant | Move it into the right Notebook and run a scope check |
| Gemini mentions unexpected facts | Run a source audit prompt |

See [Usage workflows](docs/usage-workflows.md) for more detail.

## Core operating rules

1. Keep unrelated work in separate Notebooks or named workspaces.
2. Keep general instructions short and neutral.
3. Put project-specific rules inside the relevant Notebook, not global instructions.
4. Ask Gemini to list what information it used.
5. Treat browser tabs, YouTube videos, uploaded files, and connected apps as explicit sources.
6. Do not assume a new chat is isolated if personalization is enabled.
7. If a one-off chat becomes project-relevant, move it into the right Notebook and run a scope check.
8. Watch for information from the wrong project appearing in an answer.

## Key phrase

For longer answers, ask Gemini to include:

```markdown
## Information used
List what you used.

## Scope check
Say one of:
- current chat only
- provided source only
- other project information may be relevant, but not used
- I may have used outside information
- I cannot verify
```

This does not prove Gemini obeyed the boundary, but it makes the answer easier to inspect.

## Unofficial status

This project is unofficial and is not affiliated with, endorsed by, sponsored by, or approved by Google.

Google, Gemini, Google Workspace, Chrome, YouTube, Gmail, Drive, Docs, Calendar, and NotebookLM are trademarks or products of Google LLC.

## Official references to review

Google product behavior changes over time. Review current Google documentation before relying on any workflow here:

- Gemini Apps Privacy Hub: https://support.google.com/gemini/answer/13594961
- Gemini personalization overview: https://support.google.com/gemini/answer/16598623
- Gemini in Chrome: https://support.google.com/chrome/answer/16283624
- YouTube content in Gemini Apps: https://support.google.com/gemini/answer/16622858
- NotebookLM notebooks and sources: https://support.google.com/notebooklm/answer/16206563
- Google trademark rules: https://about.google/brand-resource-center/rules/

## Repository status

Early draft. Use carefully. Verify behavior yourself.
