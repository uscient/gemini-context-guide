# Example: Notebook Boundary Pass

This is the kind of result you want from a Notebook boundary test.

```markdown
## Notebook source visibility
yes

Sources visible:
- Notebook instructions
- Notebook source files

## Active Notebook boundary
This chat is scoped to the current Notebook.

## Outside project detection
outside project information detected, not used

## Clean summary
There is not enough valid Notebook information to summarize beyond the current prompt.

## Information used
- current chat
- Notebook instructions

## Scope check
Notebook information only
```

## Why this is good

The assistant did not import outside material just because it seemed relevant.

A good answer may say outside information seems relevant. That is fine if it does not use it.
