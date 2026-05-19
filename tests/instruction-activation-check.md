# Test: Instruction Activation Check

Use this to check whether standing instructions are active.

```markdown
Instruction activation check.

Before answering any project-specific question, tell me which standing instructions are currently active for this chat.

Do not summarize general Gemini policy.
Do not guess.
Do not infer instructions from this prompt alone.

Answer in this structure:

## Active standing instructions
List any persistent Notebook, Gem, saved, or workspace instructions currently affecting your behavior.

## Source of those instructions
For each instruction, identify whether it appears to come from:
- current chat
- Notebook instructions
- Gem instructions
- saved instructions
- saved information
- previous chats
- system/developer instruction
- cannot tell

## Project boundary rule
Do you currently have an instruction telling you not to mix information between unrelated projects?

Answer:
- yes, active
- no, not active
- cannot verify

## Information used
List what information you used for this answer.
```

## Passing behavior

Good signs:

- It identifies active instructions.
- It says the project-boundary rule is active if you installed one.
- It does not invent hidden tools or sources.

Warning signs:

- It says vague things like “background context” without explaining the source.
- It claims access to apps or chats you did not provide.
- It cannot identify any instruction even though you know one should be active.
