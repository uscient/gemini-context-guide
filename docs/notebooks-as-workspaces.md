# Using Notebooks as Workspaces

A Notebook can be used as a workspace for a project, topic, research area, or recurring kind of work.

This is a practical workflow, not a guarantee of technical isolation.

## When to use a Notebook

Use a dedicated Notebook when you want Gemini to work with a stable set of sources or rules over time.

Good Notebook use cases:

- one project
- one legal or business topic
- one research area
- one class or study topic
- one recurring workflow
- one client or account, if appropriate

Avoid using one giant Notebook for everything important.

## What belongs in a Notebook

A Notebook should contain:

- sources that belong to that topic
- local instructions for that topic
- relevant chat history
- summaries or notes that belong to that topic

Do not add unrelated projects or mixed private material just because it might be useful later.

## Notebook boundary instruction

Each important Notebook should include a local instruction like:

```markdown
This Notebook is a workspace for this topic only.

Use only:
- this chat
- this Notebook’s instructions
- this Notebook’s sources
- information I clearly provide in this chat

Do not use information from other Notebooks, other projects, previous chats outside this Notebook, saved information, Gmail, Drive, Docs, Calendar, Chrome history, YouTube History, Photos, Search history, or other connected apps unless I clearly ask.

If information from another project may be relevant, say:
“Information from another project may be relevant, but I did not use it.”

For longer answers, end with:

## Information used
List what you used.

## Scope check
Say one of:
- clean Notebook context
- provided source only
- other project information may be relevant, but not used
- I may have used outside information
- I cannot verify
```

## Source hygiene

A Notebook is only as clean as its sources.

If a source mixes multiple projects, Gemini may correctly use that source while still producing mixed-context answers.

Before adding a source, ask:

- Does this source belong in this Notebook?
- Does it contain unrelated project information?
- Does it contain private data that should not be in this workspace?
- Should it be summarized or redacted before adding?

## Testing a Notebook

After creating or updating a Notebook, run:

1. `tests/instruction-activation-check.md`
2. `tests/notebook-boundary-test.md`
3. `tests/similarity-stress-test.md`

These tests help check whether Gemini sees the instructions and can resist importing outside context.

## Moving chats into a Notebook

If a one-off chat is moved into a Notebook later, treat the move as a transition.

Run:

```markdown
This chat has been moved into this Notebook.

From this point forward:
- use this Notebook’s instructions
- use this Notebook’s sources only when relevant
- do not use information from other Notebooks or projects unless I clearly ask

Please confirm the active Notebook scope and list what information you are using now.
```

## Sharing a Notebook

Be careful when sharing notebooks.

Google’s NotebookLM help says Chat View can hide some materials for a focused experience, but viewers may still be able to access underlying sources and artifacts. Do not share notebooks that contain material you do not intend recipients to access.

Official reference:

- https://support.google.com/notebooklm/answer/16206563
