# Chrome and YouTube Notes

Chrome and YouTube are useful with Gemini, but they can blur source boundaries.

This guide does not try to replace Google’s documentation. Check current Google settings and help pages before relying on any specific behavior.

## Chrome

Gemini in Chrome may be able to use page or tab content depending on account, browser, product, and settings.

Recommended practice:

- Treat browser tabs as explicit sources.
- Do not assume a Chrome chat is current-chat-only.
- If possible, avoid sharing current tabs by default unless you want that behavior.
- Ask Gemini to list which tab, page, or source it used.
- Avoid using Chrome/page context for sensitive account pages unless necessary.

## YouTube

For ordinary YouTube video questions, the safest working rule is:

> Use only the specific video, link, transcript, or pasted content I provide.

Recommended practice:

- Ask for “based only on this video” when you want a source-faithful summary.
- Ask for “outside-the-video concerns” only when you want general reasoning beyond the video.
- Do not let YouTube History or account personalization become part of the answer unless you explicitly want that.
- Check that the answer ends with “provided source only” when that is what you requested.

## Good answer pattern

```markdown
## Information used
- Provided YouTube video/link/transcript

## Scope check
provided source only
```

## Suspect answer pattern

```markdown
## Information used
- Your prior chats
- Your projects
- Your preferences
- YouTube history
```

This may be fine if you asked for it. It is suspect if you only asked about one video.
