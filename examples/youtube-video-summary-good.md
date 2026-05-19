# Example: Good YouTube Scope Behavior

This example shows the pattern to look for when asking Gemini about one video.

## Good signs

- The answer summarizes the provided video.
- It does not mention unrelated projects.
- It does not use personal history or saved information.
- It ends with source and scope sections.

## Example ending

```markdown
## Information used
- Provided YouTube video transcript and metadata

## Scope check
provided source only
```

## Small correction to watch for

If Gemini says:

```markdown
## Scope check
current chat only
```

but it used the video transcript or metadata, ask it to use:

```markdown
provided source only
```

That is more accurate.
