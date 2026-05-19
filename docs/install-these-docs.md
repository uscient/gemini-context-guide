# Installing This Docs Update

This folder contains replacement or additional Markdown files for the `uscient/gemini-context-guide` repository.

Suggested placement:

- `README.md` -> repository root
- `docs/how-to-use.md`
- `docs/settings-and-surfaces.md`
- `docs/usage-workflows.md`
- `docs/what-we-learned.md`
- `docs/evaluating-answers.md`
- `docs/notebooks-as-workspaces.md`
- `docs/chrome-and-youtube.md`

Suggested command from the repository root after extracting:

```bash
cp -R path/to/gemini-context-guide-docs-update/* .
git status
git diff
git add README.md docs/
git commit -m "Expand usage documentation"
git push
```

Review before committing. These files are intended as a starting point, not final doctrine.
