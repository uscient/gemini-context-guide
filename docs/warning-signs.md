# Warning Signs

Use this page when an answer feels helpful but suspicious.

## Possible wrong-source behavior

Watch for:

- The answer mentions a project you did not name.
- The answer uses terminology from another Notebook or project.
- The answer refers to your preferences, history, role, or work without identifying the source.
- The answer says “based on your context” but does not say which context.
- The answer imports old decisions as if they are current.
- The answer mixes personal, business, legal, coding, or research topics without being asked.
- The answer gives confident advice from unclear sources.

## Browser and video warning signs

Watch for:

- A YouTube answer uses your watch history when you only wanted the provided video.
- A Chrome answer appears to use a tab you did not intend to share.
- A page summary uses account, history, or project context beyond the page itself.
- Gemini says it used “the page” but not which page.

## Notebook warning signs

Watch for:

- A Notebook answer uses terms from another Notebook.
- A Notebook answer cannot identify whether a source came from this Notebook.
- A Notebook source contains mixed material from multiple projects.
- A moved chat is treated as if it always had access to the Notebook.

## What to do

Run the source audit prompt:

```markdown
Context audit this answer.

Identify every statement that may have come from outside this chat or Notebook.

For each one, classify the likely source:
- current chat
- provided source
- Notebook instruction
- Notebook source
- Notebook chat history
- saved information
- previous chat outside this Notebook
- connected app
- browser/page context
- web/search
- cannot tell

Do not defend the answer. Audit it.
```
