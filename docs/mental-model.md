# Mental Model

Think of Gemini context as several possible information layers.

Not every layer is available in every product mode or account. Product behavior changes. Check current Google settings and documentation.

## Possible information layers

| Layer | Plain meaning | Risk |
|---|---|---|
| Current chat | What you typed in this chat | Usually expected |
| Provided source | A file, link, video, image, page, or browser tab you gave Gemini | Expected if clearly provided |
| Notebook instruction | Rules for a specific Notebook | Useful for keeping a workspace focused |
| Notebook source | Files, notes, or sources attached to a Notebook | Useful, but source quality matters |
| Notebook chat history | Past chats inside the same Notebook | Useful if the Notebook is clean |
| Saved information | Durable facts or preferences Gemini may use | Risky if too broad or project-specific |
| Previous chats | Older Gemini chats outside the current chat | Useful but can create wrong-project mixing |
| Connected apps | Gmail, Drive, Docs, Calendar, YouTube, etc. | Powerful; should be deliberately invoked |
| Browser/tab context | Current tab or shared tabs in Chrome | Useful but easy to forget is active |
| Web/search | Public web information | May be stale, incomplete, or outside the intended scope |

## Recommended model

Use three levels of instruction:

1. Global instruction: short, neutral, and focused on one-off chat containment.
2. Notebook instruction: project-specific scope rules.
3. Task prompt: specific request and source limits for the current answer.

## Best default

For a new ordinary chat:

> Use only the current chat and what I clearly provide.

For a Notebook chat:

> Use this Notebook’s instructions and sources, not other Notebooks or unrelated projects.

For Chrome, YouTube, or page questions:

> Use only the provided page, video, link, transcript, or tab unless I ask for more.
