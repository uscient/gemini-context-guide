# The Problem

Personal AI workspaces are becoming useful because they can remember, summarize, connect, and personalize.

The problem is that personal work is rarely one clean stream. One person may use the same AI account for:

- work projects
- private planning
- research
- business or legal questions
- YouTube/video summaries
- browser-page questions
- family or personal admin
- coding help
- experiments with AI behavior

If the assistant can use saved information, past chats, Notebooks, browser tabs, uploaded files, connected apps, or video context, the user needs to know which information is being used.

The failure mode is not memory itself. The failure mode is information from the wrong place being silently used in the current answer.

## Common symptoms

- A new chat mentions an old project without being asked.
- A Notebook answer uses facts from another Notebook.
- A YouTube summary brings in unrelated personal or project context.
- Gemini says something like “from your work” but does not identify the source.
- A legal or business answer turns future possibilities into current obligations.
- A browser-tab answer uses more page/account context than expected.
- The answer is useful, but you cannot tell where the information came from.

## Goal

The goal is not to make Gemini forget everything.

The goal is to make context use more deliberate:

- separate spaces for separate work
- clear instructions for each space
- explicit source lists in important answers
- test prompts to check whether boundaries are working
- warning signs when the assistant appears to use the wrong information

## Key distinction

Helpful memory is not the same as governed memory.

Helpful memory tries to make answers better.

Governed memory asks:

- Is this the right information for this chat?
- Was this source allowed?
- Did this come from the current Notebook, another Notebook, a past chat, saved information, or a connected app?
- Should this information be used here at all?
