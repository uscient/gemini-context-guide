# Usage Workflows

This page gives practical workflows for common Gemini use cases.

## Workflow 1: One-off chat

Use this for ordinary questions that are not part of a project.

1. Start a normal Gemini chat.
2. Ask the question.
3. Rely on the global instruction to keep the chat separate.
4. For longer answers, check the “Information used” and “Scope check” sections.
5. If the answer mentions another project or outside information, run the source-audit prompt.

Good scope check:

```markdown
## Information used
- Current chat

## Scope check
current chat only
```

## Workflow 2: YouTube or video summary

Use this when asking Gemini about a specific YouTube video.

1. Provide the video link or transcript.
2. Ask Gemini to summarize or analyze the video.
3. Require Gemini to use only the provided video/link/transcript.
4. Check that the scope says “provided source only.”

Good scope check:

```markdown
## Information used
- Provided YouTube video/link/transcript

## Scope check
provided source only
```

Suspicious behavior:

- Gemini references your projects without being asked.
- Gemini mentions your YouTube History.
- Gemini says “current chat only” even though it used a video source.
- Gemini fills gaps with unrelated web or account information.

## Workflow 3: Chrome/browser-tab question

Use this when Gemini in Chrome is looking at a page or tab.

1. Confirm whether tab sharing is intentional.
2. Ask about the current tab or selected tabs.
3. Treat the tab as an explicit source.
4. Avoid asking broad questions that might pull in history or other tabs unless intended.

Good scope check:

```markdown
## Information used
- Provided browser tab/page

## Scope check
provided source only
```

## Workflow 4: Project Notebook

Use this for ongoing work on a project, research topic, legal topic, or recurring workstream.

1. Create or open the relevant Notebook.
2. Add only relevant sources.
3. Add the Notebook boundary instruction.
4. Run the Notebook boundary test.
5. Use the Notebook for that project only.
6. If another project is relevant, ask Gemini to flag it without importing it.

Good scope check:

```markdown
## Information used
- Current chat
- Notebook instructions
- Notebook sources

## Scope check
clean notebook context
```

## Workflow 5: Similarity stress test

Use this when two projects are similar and you want to know whether Gemini is mixing them.

1. Create a synthetic project inside the Notebook or chat.
2. Make it similar to another project.
3. Tell Gemini not to import outside project information.
4. Ask for a clean-room answer.
5. Check whether it says the similar project was detected but not used.

Good answer:

```markdown
## Similarity check
similarity detected, not imported

## Scope check
clean notebook context
```

Bad answer:

- It names the outside project.
- It imports terminology from the outside project.
- It says it cannot verify but still relies on the outside information.

## Workflow 6: Moving a one-off chat into a Notebook

Use this when a loose chat becomes useful enough to organize.

1. Move the chat into the relevant Notebook if the product supports it.
2. Run the moved-chat scope check.
3. Treat the move as a transition point.
4. From that point forward, use Notebook instructions and sources.

Prompt:

```markdown
This chat has been moved into this Notebook.

From this point forward:
- use this Notebook’s instructions
- use this Notebook’s sources only when relevant
- do not use information from other Notebooks or projects unless I clearly ask

Please confirm the active Notebook scope and list what information you are using now.
```

## Workflow 7: Auditing a suspicious answer

Use this when Gemini appears to know something it should not have used.

1. Copy the suspicious answer.
2. Run the source-audit prompt.
3. Ask Gemini to classify each suspicious statement.
4. Do not let it defend the answer. Ask it to audit the answer.

Prompt:

```markdown
Context audit this answer.

Identify every statement that may have come from outside the current chat, source, Notebook, or project.

For each one, classify the likely source:
- current chat
- Notebook instruction
- Notebook source
- Notebook chat history
- saved instruction
- saved information
- previous chat outside this Notebook
- connected app
- web/search
- cannot distinguish

Do not defend the answer. Audit it.
```
