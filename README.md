# Cumhuriyet Tarihi Archivist Agent

Turkish Republic history research skill for Manus, built with evidence-first workflow, provenance discipline, and multi-source verification.

Language support: Turkish + English (bilingual operation).

TR README: `README.tr.md`

## What This Project Does

- Routes each question to the right archive backbone (TBMM, Resmi Gazete, Devlet Arsivleri, etc.)
- Forces Evidence Card output with source metadata
- Requires triangulation for critical claims
- Handles contradictions via structured tickets
- Produces concise sourced synthesis and timeline
- Enforces direct source links for critical claims

## Bilingual Behavior

- If question is Turkish, output defaults to Turkish.
- If question is English, output defaults to English.
- If user asks for bilingual output, return Turkish + English.
- JSON schema keys remain English in all modes.

## Priority Source Spine

- Presidency State Archives of the Republic of Turkiye
- Grand National Assembly of Turkiye (TBMM)
- Official Gazette (Resmi Gazete)
- Turkish Historical Society (TTK)
- Ataturk Research Center
- National Library of Turkiye
- Ataturk Library
- SALT Research
- Foreign policy: NARA, TNA (UK), NATO Archives, UN Archives

## Project Structure

```text
cumhuriyet-tarihi-arsivci-skill-project/
├─ README.md
├─ README.tr.md
├─ LICENSE
├─ docs/
│  ├─ ANALIZ_GORUS_ONERILERI.md
│  ├─ GITHUB_METADATA.md
│  ├─ RELEASE_NOTES_EN.md
│  └─ RELEASE_NOTES_TR.md
├─ claude/
│  └─ CLAUDE_PROJECT_INSTRUCTIONS.md
├─ skill/
│  └─ cumhuriyet-tarihi-arsivci-ajani/
│     ├─ SKILL.md
│     ├─ agents/openai.yaml
│     └─ references/
└─ dist/
   ├─ *.zip
   └─ *.skill
```

## Install in Manus

1. Open Manus -> Skill upload.
2. Upload one file from `dist/` (`.skill` or `.zip`).
3. Confirm skill name appears as `cumhuriyet-tarihi-arsivci-ajani`.

## Build Package from Source

```powershell
$skillPath = ".\skill\cumhuriyet-tarihi-arsivci-ajani"
Compress-Archive -Path "$skillPath\*" -DestinationPath ".\dist\cumhuriyet-tarihi-arsivci-ajani.zip" -Force
Copy-Item ".\dist\cumhuriyet-tarihi-arsivci-ajani.zip" ".\dist\cumhuriyet-tarihi-arsivci-ajani.skill" -Force
```

## Claude Usage

Paste `claude/CLAUDE_PROJECT_INSTRUCTIONS.md` into Claude Project Instructions.

## Example Test Question

```text
What topics were discussed in TBMM in November 1924?
```

## GitHub Ready Metadata

See `docs/GITHUB_METADATA.md` for:

- ready-to-use repository description
- topic tags
- social/share snippets

Upload steps: `docs/GITHUB_UPLOAD_STEPS.md`

## Release Texts

- English release note: `docs/RELEASE_NOTES_EN.md`
- Turkish release note: `docs/RELEASE_NOTES_TR.md`

## Current Analysis Status

`docs/ANALIZ_GORUS_ONERILERI.md` now separates fixed items vs remaining items to avoid confusion.

## License

MIT (`LICENSE`).
