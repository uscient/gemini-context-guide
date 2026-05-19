# Settings and Surfaces to Inspect

This page lists Gemini-related surfaces that can affect what information may be used in a chat.

Google product behavior changes over time. Always review the current official settings and help pages.

## Gemini Apps Activity / Keep Activity

Gemini Apps Activity controls important retention and improvement settings.

Google’s Privacy Hub says Gemini Apps Activity lets users review and delete activity, change the auto-delete period, and control whether data is used to improve Google AI. It also says some reviewed data may be retained separately for longer than deleted account activity.

Official reference:

- https://support.google.com/gemini/answer/13594961

Suggested user action:

- Review Gemini Apps Activity.
- Set the auto-delete period intentionally.
- Do not treat auto-delete as a complete privacy or isolation guarantee.

## Saved information and instructions

Gemini personalization can involve preferences and instructions about how you want Gemini to respond.

Official reference:

- https://support.google.com/gemini/answer/16598623

Suggested user action:

- Keep global instructions short and general.
- Do not put project-specific facts in global instructions.
- Put project-specific rules in the relevant Notebook or workspace instead.

## Past chats

Gemini personalization may use memory of past Gemini chats when available and enabled.

Official reference:

- https://support.google.com/gemini/answer/16598623

Suggested user action:

- Do not assume a new chat is isolated if personalization is enabled.
- Use project-specific Notebooks for project work.
- Ask Gemini to identify whether it used previous chats.

## Connected Google apps

Gemini may use connected Google apps when available and when you ask for that kind of help.

Official reference:

- https://support.google.com/gemini/answer/13594961

Suggested user action:

- Do not ask Gemini to use Gmail, Drive, Docs, Calendar, Photos, YouTube History, Search history, or other connected app data unless you intend to expose that source to the current chat.
- For sensitive work, avoid broad requests like “check my files” or “look at my emails.”
- Prefer specific requests with a named item, source, or scope.

## Gemini in Chrome

Gemini in Chrome can involve browser context.

Google’s Chrome help page lists permissions including precise location, microphone, “Share current tab by default,” and “Let Gemini browse for you.”

Official reference:

- https://support.google.com/chrome/answer/16283624

Suggested user action:

- Review Gemini in Chrome permissions.
- Consider turning off “Share current tab by default” if you want tab context to be explicit.
- Treat any shared tab as a source you intentionally gave Gemini.

## YouTube

Gemini can find and answer questions about YouTube content. Google says Gemini uses public information from YouTube to help users find videos and understand video content. The same help page notes that users can connect Gemini and YouTube for personalized experiences based on YouTube History.

Official reference:

- https://support.google.com/gemini/answer/16622858

Suggested user action:

- For normal video summaries, ask Gemini to use only the provided YouTube link or transcript.
- Do not use YouTube History unless you intentionally want personalization from watch history or account activity.
- In the scope check, prefer “provided source only” instead of “current chat only” when Gemini used a video link.

## Notebooks / NotebookLM

NotebookLM notebooks use user-provided sources and instructions to generate answers and outputs. Google’s help page says users can add and remove sources in a notebook, and that NotebookLM answers and outputs are generated based on user-provided sources and instructions.

Official reference:

- https://support.google.com/notebooklm/answer/16206563

Suggested user action:

- Use separate Notebooks for separate projects or topics.
- Add clear Notebook instructions.
- Keep Notebook sources clean.
- Do not mix unrelated projects in the same Notebook unless the purpose is comparison.
- When sharing notebooks, remember that viewers may still be able to access underlying sources and artifacts even when Chat View hides them.

## Temporary chats

If Temporary Chat is available to you, it may be useful for sensitive one-off work. If it is not available, use global one-off containment instructions and avoid connected app sources.

Suggested user action:

- Do not assume Temporary Chat exists in every Gemini surface.
- If it is unavailable, rely on careful instructions, source limits, and manual deletion where appropriate.

## Practical rule

Before a serious chat, ask:

1. What source do I want Gemini to use?
2. What source do I not want Gemini to use?
3. Is this a one-off chat or a Notebook/project chat?
4. Should this answer include an “Information used” section?
5. Would I be comfortable if this prompt were retained or reviewed under the applicable product settings?
