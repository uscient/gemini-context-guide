# Gemini Context Guide

Unofficial guidance for managing personal context, Notebook scope, saved information, browser/page context, and one-off chats when using Google Gemini.

This guide is for people who want useful AI continuity without letting unrelated projects, personal topics, research, browser pages, videos, or connected apps blend together silently.

## What this helps with

- Keeping unrelated work in separate Gemini Notebooks or named workspaces
- Writing clear Notebook instructions
- Keeping one-off chats separate unless you intentionally move them later
- Asking Gemini to say what information it used
- Testing whether instructions are active
- Watching for context from the wrong project or source
- Handling Chrome, YouTube, browser-tab, and video questions more carefully

## What this does not do

- It does not guarantee isolation inside Gemini.
- It does not replace Google’s settings, privacy controls, or official documentation.
- It does not provide legal, privacy, security, or compliance advice.
- It does not prove what Google stores, reviews, trains on, or deletes.
- It does not make personal Gemini equivalent to a managed enterprise environment.

## Quick start

1. Read [`docs/problem.md`](docs/problem.md).
2. Add [`instructions/global-gemini-instruction.md`](instructions/global-gemini-instruction.md) to your general Gemini instructions if it fits your needs.
3. Add [`instructions/notebook-boundary-instruction.md`](instructions/notebook-boundary-instruction.md) to each important Notebook.
4. Run [`tests/instruction-activation-check.md`](tests/instruction-activation-check.md) in a new chat.
5. Run [`tests/notebook-boundary-test.md`](tests/notebook-boundary-test.md) inside a Notebook.
6. Use [`tests/source-audit-prompt.md`](tests/source-audit-prompt.md) whenever an answer seems to pull information from the wrong place.

## Core idea

Modern AI assistants may use more than the words in the current prompt. Depending on product settings and features, they may use saved information, past chats, Notebook sources, browser tabs, uploaded files, videos, or connected apps.

That can be useful. It can also cause unrelated work to blend together.

This guide treats context as something that should be scoped, named, and checked.

## Basic operating rules

1. Keep unrelated work in separate Notebooks or named project spaces.
2. Keep global instructions short and neutral.
3. Put project-specific rules inside the relevant Notebook, not global instructions.
4. Ask Gemini to list what information it used.
5. Treat browser tabs, YouTube videos, uploaded files, and connected apps as explicit sources.
6. Do not assume a new chat is isolated if personalization is enabled.
7. If a one-off chat becomes project-relevant, move it into the right Notebook and run a scope check.
8. Watch for information from the wrong project appearing in an answer.

## Unofficial status

This project is unofficial and is not affiliated with, endorsed by, sponsored by, or approved by Google.

Google, Gemini, Google Workspace, Chrome, YouTube, Gmail, Drive, Docs, Calendar, and NotebookLM are trademarks or products of Google LLC.

## Official references to review

Google product behavior changes over time. Review current Google documentation before relying on any workflow here:

- Gemini Apps Privacy Hub: https://support.google.com/gemini/answer/13594961
- Gemini personalization overview: https://gemini.google/overview/personalization/
- Gemini in Chrome: https://support.google.com/gemini/answer/16283624
- YouTube content in Gemini Apps: https://support.google.com/gemini/answer/16622858
- Google trademark rules: https://about.google/brand-resource-center/rules/

## Suggested repo status

Early draft. Use carefully. Verify behavior yourself.
