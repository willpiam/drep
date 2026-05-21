---
name: wiki-ingest
description: Ingests a new raw source into the DRep LLM wiki—creates source summaries, updates entities/concepts/proposals, and maintains index and log. Use when the user adds a file to wiki/raw/, asks to ingest/process a source, or wants vote context compounded into the wiki.
disable-model-invocation: true
---

# Wiki Ingest

Process one raw source into the compounding wiki. Read [AGENTS.md](../../../AGENTS.md) for full schema.

## Prerequisites

- Source file exists in `wiki/raw/` (or user will add it now)
- `vote_context/` is read-only legacy raw—ingest from it, never edit

## Workflow

```
Task Progress:
- [ ] Step 1: Read source
- [ ] Step 2: Discuss takeaways (if user is present)
- [ ] Step 3: Write source summary page
- [ ] Step 4: Update entity/concept/proposal pages
- [ ] Step 5: Update index, log, overview if needed
```

### Step 1: Read source

Read the full file in `wiki/raw/`. If images matter, read `wiki/raw/assets/` references separately.

### Step 2: Discuss takeaways

Summarize key points for the user. Ask what to emphasize if unclear. One source at a time unless user requests batch.

### Step 3: Source summary page

Create `wiki/sources/<slug>.md` using the template in AGENTS.md:

- Link to raw file
- Summary + key points
- List wiki pages updated

### Step 4: Cross-wiki updates

Touch all relevant pages (typically 5–15):

| Type | Path | Action |
|------|------|--------|
| Entity | `wiki/entities/<slug>.md` | Create or update |
| Concept | `wiki/concepts/<slug>.md` | Create or update |
| Proposal | `wiki/proposals/<slug>.md` | Create or update; add **DRep position** if vote context |

Use wikilinks. Flag contradictions with older content; do not silently overwrite.

### Step 5: Bookkeeping

1. Update `wiki/index.md` — add every new/changed page with one-line summary
2. Append to `wiki/log.md`:
   ```
   ## [YYYY-MM-DD] ingest | <source title>
   ```
3. Update `wiki/overview.md` only if synthesis materially changed

## Slug rules

- Lowercase, hyphens, no spaces: `token2049-sponsorship-2026`
- Match raw filename when sensible

## Do not

- Modify files in `wiki/raw/` or `vote_context/`
- Skip `index.md` updates
- Create duplicate pages for the same entity/concept
