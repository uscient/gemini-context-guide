# Test: Source Audit Prompt

Use this when an answer seems to include information from the wrong place.

```markdown
Context audit this answer.

Identify every statement that may have come from outside this chat, outside this Notebook, or outside the source I provided.

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

If you used information from outside the intended scope, say so directly.

Then provide a corrected answer using only the allowed information.
```
