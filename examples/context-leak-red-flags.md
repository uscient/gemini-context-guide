# Example: Red Flags

These are examples of suspicious wording.

## Red flag examples

```text
Based on your work in another project...
```

```text
This connects to your broader architecture...
```

```text
From your previous discussions...
```

```text
Given your saved context...
```

```text
I know you prefer...
```

These are not always wrong. They are wrong when you did not ask Gemini to use that information.

## What to ask next

```markdown
What exact information source did you use for that statement?

Classify it as:
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

If you cannot tell, do not rely on it.
```
