# DRep LLM Wiki — Agent Schema

This repository maintains a **persistent, compounding wiki** for Cardano governance and DRep voting. Read [llm-wiki.md](llm-wiki.md) for the general pattern. This file is the schema: conventions, structure, and workflows.

## Three layers

| Layer | Location | Who writes |
|-------|----------|------------|
| **Raw sources** | `wiki/raw/` (+ legacy `vote_context/`) | Human curates; **never modify** |
| **Wiki** | `wiki/` | LLM maintains |
| **Schema** | This file (`AGENTS.md`) | Human + LLM co-evolve |

## Directory layout

```
wiki/
├── raw/              # Immutable sources (articles, proposals, clips)
│   └── assets/       # Local images (Obsidian download target)
├── entities/         # Orgs, people, committees
├── concepts/         # Topics (NCL, treasury tax, constitution, …)
├── sources/          # One summary page per ingested raw file
├── proposals/        # Governance actions (cross-linked)
├── analysis/         # Filed comparisons and query outputs
├── index.md          # Catalog — update on every change
├── log.md            # Append-only timeline
└── overview.md       # High-level synthesis
```

**Legacy raw (read-only):** `vote_context/markdown/` and `vote_context/*.jsonld` are published vote artifacts. Ingest from them but do not edit.

## Page conventions

### Frontmatter (optional, for Obsidian Dataview)

```yaml
---
tags: [entity | concept | source | proposal | analysis]
updated: YYYY-MM-DD
sources: []
---
```

### Wikilinks

Use relative wikilinks: `[[concepts/ncl]]`, `[[entities/cardano-foundation]]`.

### Source pages (`wiki/sources/`)

Filename: slug from raw filename, e.g. `token2049-sponsorship-2026.md`.

Structure:

```markdown
# <Title>

**Raw:** [../raw/<file>](../raw/<file>)
**Ingested:** YYYY-MM-DD

## Summary
…

## Key points
- …

## Wiki updates
- Updated [[entities/…]]
- Updated [[concepts/…]]
```

### Entity / concept pages

Lead with a one-paragraph definition, then sections that accrue over ingests: **Position**, **History**, **Related votes**, **Open questions**.

### Vote alignment

When ingesting vote context, link to the proposal page and note vote (yes / no / abstain) without overwriting neutral entity descriptions—use a **DRep position** subsection on proposal pages.

## Operations

Use the project Cursor skills (invoke by name or attach):

| Skill | Purpose |
|-------|---------|
| `wiki-ingest` | Process new raw source into wiki |
| `wiki-query` | Answer questions; file insights back |
| `wiki-lint` | Health-check the wiki |

## Ingest workflow

1. Confirm source is in `wiki/raw/` (or ask user to add it).
2. Read the source; discuss key takeaways with the user if they are present.
3. Create or update `wiki/sources/<slug>.md`.
4. Update relevant `entities/`, `concepts/`, `proposals/` pages (expect 5–15 files).
5. Update `wiki/index.md` and append to `wiki/log.md`:
   `## [YYYY-MM-DD] ingest | <title>`
6. Revise `overview.md` if the synthesis materially changed.

## Query workflow

1. Read `wiki/index.md` to locate relevant pages.
2. Read those pages (and raw sources only if wiki is insufficient).
3. Synthesize an answer with citations to wiki pages.
4. **File insights back:** valuable comparisons, connections, or analyses become new pages under `wiki/analysis/` (or updates to existing pages). Update `index.md` and append to `log.md`:
   `## [YYYY-MM-DD] query | <question slug>`
   `## [YYYY-MM-DD] filing | <new page title>` (when filing)

## Lint workflow

1. Read `wiki/index.md` and scan all wiki pages.
2. Report: contradictions, stale claims, orphan pages, missing entity/concept pages, broken wikilinks, gaps worth a web search.
3. Fix clear issues (broken links, index drift) unless user prefers report-only.
4. Append `## [YYYY-MM-DD] lint | <summary>` to `log.md`.

## Index and log

- **index.md** — Content catalog; read first for navigation.
- **log.md** — Chronological; entries prefixed `## [date] type | title` for grep.

## Domain context

- **Agenda:** Keep Cardano viable for generations to come.
- **Published vote flow:** `vote_context/markdown/` → GitHub → Twitter; wiki compounds separately.
- **Template:** [vote_context/markdown/template.md](vote_context/markdown/template.md)

## Rules

- Never modify `wiki/raw/` or `vote_context/` content during ingest (read-only).
- Prefer updating existing pages over duplicating.
- Note contradictions explicitly; do not silently overwrite.
- Keep `index.md` in sync with every new or renamed page.
