# Chrome and YouTube Use

Chrome and YouTube are common places where Gemini can be useful.

They are also common places where source boundaries become unclear.

## The simple rule

For Chrome, YouTube, page, video, or browser-tab questions:

> Use only the specific source I provide.

That source might be:

- a YouTube link
- a video transcript
- a webpage
- the current browser tab
- selected browser tabs
- a pasted excerpt
- an uploaded file

## Gemini in Chrome

Google’s Chrome help says Gemini in Chrome has permissions including:

- precise location
- microphone
- Share current tab by default
- Let Gemini browse for you

Official reference:

- https://support.google.com/chrome/answer/16283624

Suggested user actions:

- Review Gemini in Chrome settings.
- Consider turning off “Share current tab by default” if you want tab sharing to be deliberate.
- Treat the current tab as a source when Gemini uses it.
- Do not leave sensitive tabs open if you do not want them included.

## YouTube

Google’s Gemini help says Gemini uses public information from YouTube to help users find videos and understand video content. The same page says users can connect Gemini and YouTube for personalized experiences based on YouTube History.

Official reference:

- https://support.google.com/gemini/answer/16622858

Suggested user actions:

- For a normal video summary, provide the specific video link.
- Ask Gemini to use only that video/link/transcript.
- Avoid using YouTube History unless you intentionally want account-based personalization.
- Check that the answer says “provided source only.”

## Good prompt for YouTube

```markdown
Summarize this YouTube video.

Use only the video/link/transcript I provide. Do not use my YouTube History, Chrome history, Search history, previous chats, saved information, connected apps, or project context.

End with:

## Information used
List what you used.

## Scope check
Say one of:
- provided source only
- current chat only
- other project information may be relevant, but not used
- I may have used outside information
- I cannot verify
```

## Good follow-up prompt

```markdown
Based only on the provided video, what does the video say about risks or downsides?

Do not add outside concerns unless I ask for them.
```

## Separate outside analysis

If you want general reasoning beyond the video, say so explicitly:

```markdown
Now add a separate section called “Outside-the-video concerns.”

Use only general reasoning and official sources if needed. Do not use my projects, previous chats, saved information, YouTube History, Chrome history, Search history, or connected apps.
```

## Good scope labels

When Gemini used a provided video or page, the best label is:

```markdown
## Scope check
provided source only
```

Not:

```markdown
## Scope check
current chat only
```

The link, video, page, tab, file, or transcript is a source.
