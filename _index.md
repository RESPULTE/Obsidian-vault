---
type: moc
domain: Knowledge Management
aliases: [Vault Home, Knowledge Graph Index]
status: active
updated: 2026-10-31
---

# Personal Knowledge Graph

Start here to navigate the vault through curated Maps of Content (MOCs):

- [[MOC - Computer Science]] — concepts and their subject hierarchy.
- [[MOC - Projects]] — active work and archived project history.

## Folder Taxonomy

| Folder | Purpose |
| --- | --- |
| `10_MOCs/` | Navigation maps that organize concepts and projects. |
| `20_Concepts/` | Atomic, reusable notes about one idea or technique each. |
| `30_Projects/` | Project hubs connecting objectives, decisions, experiments, and concepts. |
| `90_Archive/` | Superseded or deprecated material preserved for historical context. |

## Frontmatter Conventions

Use YAML frontmatter consistently:

- `type`: note kind, typically `moc`, `concept`, or `project`.
- `domain`: primary knowledge area (e.g., Computer Vision).
- `parent`: optional Obsidian link to the broader concept or MOC, quoted in YAML (e.g., `"[[Image Segmentation]]"`).
- `aliases`: optional list of alternative names for a note.
- `status`: lifecycle state, such as `active`, `draft`, or `archived`.
- `updated`: date of the last substantive edit in `YYYY-MM-DD` format.

Prefer one concept per note, meaningful `[[wikilinks]]`, and MOCs for navigation. Link to existing notes when possible; unresolved links identify notes to create later.
