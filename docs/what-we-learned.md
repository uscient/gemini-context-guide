# What We Learned While Creating This Guide

This page summarizes practical lessons discovered while testing Gemini context behavior and writing this guide.

These are workflow observations, not guarantees about Gemini internals.

## 1. The problem is not memory. The problem is uncontrolled memory.

Useful continuity is valuable.

The issue is when information from another chat, project, source, app, or saved preference appears in an answer without clear permission or source labeling.

A better goal is:

> Use helpful context only when it belongs to the current task.

## 2. Project boundaries need plain instructions

Instructions work better when they are simple and direct.

Less helpful:

> Avoid context contamination.

More helpful:

> Do not use information from other projects unless I name that project.

Gemini-facing instructions should use ordinary language.

## 3. Global instructions should stay neutral

Global instructions apply broadly, so they should not contain project-specific facts.

Good global instruction:

> For chats that are not inside a specific Notebook, Gem, or named project, treat the chat as separate.

Bad global instruction:

> Always apply my legal/business/product doctrine from Project X.

## 4. Notebook instructions should define the local boundary

A Notebook can be used like a project workspace when its instructions say what belongs there and what does not.

A useful Notebook instruction says:

- treat this Notebook as the active scope
- use Notebook sources when relevant
- do not use other projects unless asked
- if another project seems relevant, mention that without importing it
- list what information was used

## 5. Similarity tests are stronger than simple tests

A simple test asks Gemini not to use another project.

A stronger test gives Gemini a synthetic project that is similar to a real project and checks whether it imports real-project context.

Good result:

> similarity detected, not imported

Bad result:

> Gemini silently imports terms, goals, plans, or assumptions from the real project.

## 6. “Information used” is useful, but not proof

Asking Gemini to list sources helps users inspect answers.

It does not prove Gemini only used those sources.

Treat the source list as a helpful audit clue, not a technical guarantee.

## 7. “Provided source only” is better than “current chat only” for links and videos

If Gemini summarizes a YouTube video, webpage, uploaded file, or browser tab, the answer did not use only the current text prompt.

Better scope label:

> provided source only

This makes it clearer that a video, page, file, or tab was used.

## 8. Chrome and YouTube need special care

Chrome and YouTube are useful because they can provide page or video context.

They also create ambiguity if users do not know whether Gemini used:

- the current tab
- selected tabs
- a provided video link
- YouTube History
- Chrome history
- Search history
- account personalization

For video/page questions, ask Gemini to use only the specific provided source.

## 9. Moving a chat into a Notebook should be treated as a transition

If a one-off chat later gets moved into a Notebook, do not assume it was Notebook-scoped from the beginning.

After moving, ask Gemini to confirm the active Notebook scope and sources.

## 10. Legal, privacy, security, and compliance answers need triage

When Gemini gives legal, privacy, security, or compliance suggestions, it may turn future possibilities into current obligations.

Use triage categories such as:

- required now
- required before public launch
- required only if a feature enters scope
- strategic but optional
- watchlist only
- professional review recommended

This keeps advice useful without making every possible future risk sound urgent.

## 11. A good guide should not overpromise

This guide should avoid saying that prompts or Notebooks guarantee isolation.

Better wording:

> These workflows can make context use more visible and deliberate. They do not prove technical isolation.
