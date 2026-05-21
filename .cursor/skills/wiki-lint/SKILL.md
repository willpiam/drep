---
name: wiki-lint
description: Health-checks the DRep LLM wiki for contradictions, stale claims, orphan pages, missing cross-references, and index drift. Use when the user asks to lint the wiki, audit knowledge base health, or periodically maintain wiki quality.
disable-model-invocation: true
---

# Wiki Lint

Periodic health-check of the compounding wiki. Read [AGENTS.md](../../../AGENTS.md) for full schema.

## Workflow

```
Task Progress:
- [ ] Step 1: Load catalog
- [ ] Step 2: Scan pages for issues
- [ ] Step 3: Report findings
- [ ] Step 4: Fix clear issues (unless report-only)
- [ ] Step 5: Log and update index
```

### Step 1: Load catalog

Read `wiki/index.md` and `wiki/log.md` (recent entries). List all markdown under `wiki/` except `raw/`.

### Step 2: Scan for issues

Check each category:

| Check | What to find |
|-------|----------------|
| **Contradictions** | Conflicting claims across pages; note both and suggest resolution |
| **Stale claims** | Statements superseded by newer sources in `sources/` or `log.md` |
| **Orphans** | Pages with no inbound wikilinks from index or other pages |
| **Missing pages** | Important entities/concepts mentioned but without `entities/` or `concepts/` page |
| **Broken links** | Dead wikilinks, wrong paths |
| **Index drift** | Pages on disk not listed in `index.md`, or index entries for missing files |
| **Gaps** | Topics worth ingest or web search; suggest questions for `wiki-query` |

### Step 3: Report findings

Present a structured report:

```markdown
## Lint Report — YYYY-MM-DD

### Critical
- …

### Suggestions
- …

### Healthy
- …

### Suggested next steps
- …
```

### Step 4: Fix clear issues

Unless the user asked for report-only:

- Fix broken wikilinks
- Sync `index.md` with actual files
- Add inbound links to orphan pages where obvious
- Do **not** resolve contradictions without user input—flag them

### Step 5: Bookkeeping

1. Update `wiki/index.md` if pages were added/renamed
2. Append to `wiki/log.md`:
   ```
   ## [YYYY-MM-DD] lint | <one-line summary>
   ```

## Optional deep checks

- Compare `vote_context/markdown/` entries not yet reflected in wiki `sources/` or `proposals/`
- Review `overview.md` against latest `concepts/` and `proposals/`

## Do not

- Modify `wiki/raw/` or `vote_context/`
- Silently merge contradictory positions
