# GitHub Upload Steps

Current environment note: automatic upload from this session is not possible because `git` and `gh` CLI are not installed.

## Option A - Git CLI (recommended)

```bash
git init
git add .
git commit -m "feat: release bilingual archive agent v1.1.0"
git branch -M main
git remote add origin https://github.com/<username>/cumhuriyet-tarihi-arsivci-ajani.git
git push -u origin main
```

## Option B - GitHub Web Upload

1. Create a new repo on GitHub.
2. Open repo page -> `Add file` -> `Upload files`.
3. Drag-drop all files from `cumhuriyet-tarihi-arsivci-skill-project`.
4. Commit as `Initial release v1.1.0`.
5. (Optional) Create Release and paste text from `docs/RELEASE_NOTES_EN.md` or `docs/RELEASE_NOTES_TR.md`.
