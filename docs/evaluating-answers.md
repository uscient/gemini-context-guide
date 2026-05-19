# Evaluating Gemini Answers

This page explains how to decide whether a Gemini answer stayed within the intended scope.

## Good signs

An answer is more trustworthy when it:

- answers only the question asked
- lists the current chat, provided source, or Notebook sources it used
- does not mention unrelated projects
- does not infer private facts without source support
- says “I cannot verify” when appropriate
- separates source-based statements from general reasoning
- uses “provided source only” for a link, file, tab, or video
- flags possible outside context without importing it

## Warning signs

An answer is suspicious when it:

- mentions a project or personal detail you did not name
- imports terms from another project
- says “based on your previous work” without saying where that came from
- gives a confident answer while also saying it cannot tell the source
- treats a browser tab, connected app, or history source as available by default
- turns broad personalization into project facts
- mixes legal, personal, technical, and business contexts without being asked
- invents product settings or capabilities
- says a feature is isolated or guaranteed without official support

## Source labels to prefer

Use these labels when asking Gemini to report information sources:

- current chat
- provided link/video/page/file/tab
- Notebook instructions
- Notebook source
- Notebook chat history
- saved instruction
- saved information
- previous chat outside this Notebook
- connected Google app
- web/search
- cannot distinguish

## Interpreting common scope checks

| Scope check | Meaning | What to do |
|---|---|---|
| current chat only | Gemini claims it used only text in the current chat | Good for simple questions |
| provided source only | Gemini claims it used only a link, video, file, page, or tab you provided | Good for YouTube/page/file questions |
| other project information may be relevant, but not used | Gemini noticed possible relevance but says it did not import it | Usually good |
| I may have used outside information | Treat the answer as suspect | Run a source audit |
| I cannot verify | Source boundary is unclear | Do not rely on project-specific claims |

## Source audit prompt

Use this when an answer seems suspicious:

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

## What to do after a failed scope check

1. Save the suspicious answer.
2. Run the source audit prompt.
3. Identify which statement crossed the boundary.
4. Tighten the relevant instruction.
5. Move the work into the correct Notebook if needed.
6. Delete or avoid continuing the contaminated chat if it is no longer useful.
