# How to Use This Guide

This guide helps you use Gemini more deliberately when you have multiple kinds of work in the same Google account.

The goal is not to make Gemini forget everything.

The goal is to make Gemini use the right information in the right place.

## The basic problem

Gemini can be useful because it may work with more than the current prompt: saved instructions, previous chats, Notebook sources, browser tabs, uploaded files, YouTube videos, or connected Google apps.

That same usefulness can create a problem:

> An answer may include information from the wrong chat, project, source, app, or saved preference.

This guide gives you reusable instructions and tests for reducing that risk.

## Step 1: Decide what kind of chat this is

Before using Gemini, classify the chat.

| Chat type | Use this approach |
|---|---|
| One-off question | Keep it separate; use only the current chat and provided sources |
| YouTube/video/page question | Use only the specific video, page, transcript, or tab you provide |
| Project work | Use a dedicated Notebook |
| Legal/business/research work | Use a dedicated Notebook and require source/scope checks |
| Personal/private question | Be extra cautious; avoid connected app data unless intentional |

## Step 2: Use the right instruction layer

Use global instructions only for general behavior.

Use Notebook instructions for project-specific boundaries.

| Instruction layer | What belongs there | What does not belong there |
|---|---|---|
| Global Gemini instructions | General containment and source-check rules | Project-specific details |
| Notebook instructions | Rules for one project or topic | Rules for unrelated projects |
| Chat prompt | Temporary task-specific rules | Long-term facts you do not want reused broadly |

## Step 3: Ask for “Information used” and “Scope check”

For important answers, ask Gemini to end with:

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

This is not a guarantee. It is an inspection aid.

If the answer says “provided source only,” check whether that is true. If the answer mentions facts from another project, run a source audit.

## Step 4: Test before trusting

Use the tests in the `tests/` directory:

- `instruction-activation-check.md`
- `notebook-boundary-test.md`
- `similarity-stress-test.md`
- `youtube-scope-test.md`
- `source-audit-prompt.md`
- `moved-chat-scope-check.md`

The best test is not whether Gemini says the rule exists.

The better test is whether Gemini follows the rule when it would be tempting to use outside information.

## Step 5: Watch for suspicious answers

An answer is suspicious when it:

- mentions a project you did not name
- uses facts you did not provide
- says “your work” or “your prior discussion” without explaining the source
- combines two unrelated projects
- uses a browser tab, app, file, video, or history source you did not intend
- gives a confident answer while saying it cannot tell where information came from

When this happens, use `tests/source-audit-prompt.md`.

## Step 6: Move useful one-off chats carefully

If a one-off chat becomes useful for a project, move it into the relevant Notebook if Gemini supports that workflow.

After moving it, run the moved-chat scope check:

```markdown
This chat has been moved into this Notebook.

From this point forward:
- use this Notebook’s instructions
- use this Notebook’s sources only when relevant
- do not use information from other Notebooks or projects unless I clearly ask

Please confirm the active Notebook scope and list what information you are using now.
```

Treat the move as a transition point. Do not assume the chat had Notebook context before it was moved.

## A realistic expectation

These instructions reduce confusion. They do not create a hard security boundary.

You are asking Gemini to behave more carefully and to show its work. You are not proving technical isolation.
