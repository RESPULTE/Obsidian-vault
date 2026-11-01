---
type: moc
domain: Knowledge Management
aliases: [Vault Home, Knowledge Graph Index]
status: active
updated: 2026-11-01
---

# Personal Knowledge Graph

Start here to navigate the vault through curated Maps of Content (MOCs):

- [[MOC - Computer Science]] — concepts and their subject hierarchy.
- [[MOC - Projects]] — active work and archived project history.

## Quick Access & Workflow

- [[_tasks|Active To-Do List (_tasks.md)]] — track priorities, follow-ups, and completed actions.
- [00_Inbox/](00_Inbox/) — capture raw thoughts, rough drafts, and meeting notes for subsequent processing (see [[_inbox-readme]]).
- [80_Templates/](80_Templates/) — use standardized templates when creating structured notes.

Capture in the inbox, distill actionable items into `_tasks.md`, organize durable knowledge in `20_Concepts/`, and record project context and decisions in `30_Projects/`. Link resulting notes through their relevant MOCs.

## Folder Taxonomy

| Folder | Purpose |
| --- | --- |
| `00_Inbox/` | Unprocessed captures, rough drafts, and meeting notes awaiting triage. |
| `10_MOCs/` | Navigation maps that organize concepts and projects. |
| `20_Concepts/` | Atomic, reusable notes about one idea or technique each. |
| `30_Projects/` | Project hubs connecting objectives, decisions, experiments, and concepts. |
| `80_Templates/` | Canonical templates for MOCs, concepts, projects, findings, decisions, and meetings. |
| `90_Archive/` | Superseded or deprecated material preserved for historical context. |

## Frontmatter Conventions

Use YAML frontmatter consistently:

- `type`: note kind, typically `moc`, `concept`, `project`, `finding`, `decision`, or `meeting`.
- `domain`: primary knowledge area (e.g., Computer Vision).
- `parent`: optional Obsidian link to the broader concept, project, or MOC, quoted in YAML (e.g., `"[[Image Segmentation]]"`).
- `aliases`: optional list of alternative names for a note.
- `status`: lifecycle state, such as `active`, `draft`, or `archived`.
- `updated`: date of the last substantive edit in `YYYY-MM-DD` format.

Prefer one concept per note, meaningful `[[wikilinks]]`, and MOCs for navigation. Link to existing notes when possible; unresolved links identify notes to create later.
