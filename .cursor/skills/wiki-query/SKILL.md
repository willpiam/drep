---
name: wiki-query
description: Answers questions using the DRep LLM wiki (index-first navigation, cited synthesis) and files valuable insights back into wiki/analysis or related pages. Use when the user asks questions about governance, voting history, entities, concepts, or wants analysis that should compound in the knowledge base.
disable-model-invocation: true
---

# Wiki Query

Search the wiki, synthesize an answer, and **file insights back** so explorations compound. Read [AGENTS.md](../../../AGENTS.md) for full schema.

## Workflow

```
Task Progress:
- [ ] Step 1: Navigate via index
- [ ] Step 2: Read relevant pages
- [ ] Step 3: Synthesize answer with citations
- [ ] Step 4: File insights into wiki
- [ ] Step 5: Update index and log
```

### Step 1: Navigate via index

Read `wiki/index.md` first. Identify pages under entities, concepts, sources, proposals, analysis.

If the index is insufficient, grep or search `wiki/` for keywords. Read `wiki/raw/` only when wiki pages lack needed detail.

### Step 2: Read relevant pages

Read all pages likely to answer the question. Follow wikilinks to related pages.

Legacy vote context: `vote_context/markdown/` when wiki lacks a specific vote rationale.

### Step 3: Synthesize answer

Respond with:

- Direct answer to the question
- **Citations** as wikilinks or paths: `[[concepts/ncl]]`, `wiki/proposals/...`
- Gaps or uncertainties called out explicitly

Output format follows the question: markdown, table, or brief prose. Do not let valuable analysis die in chat only.

### Step 4: File insights back

**Required when** the answer includes any of:

- A comparison across proposals or entities
- A new connection not yet on a wiki page
- A reusable analysis the user may ask again
- A refined position or synthesis

**Actions:**

| Insight type | Where to file |
|--------------|---------------|
| New standalone analysis | `wiki/analysis/<slug>.md` |
| Extends existing topic | Update `wiki/concepts/` or `wiki/proposals/` |
| Updates big picture | `wiki/overview.md` |

Analysis page template:

```markdown
# <Title>

**From query:** YYYY-MM-DD
**Question:** <original question>

## Answer
…

## Sources
- [[sources/…]]
- [[proposals/…]]
```

### Step 5: Bookkeeping

1. Update `wiki/index.md` for new/changed pages
2. Append to `wiki/log.md`:
   ```
   ## [YYYY-MM-DD] query | <short question label>
   ## [YYYY-MM-DD] filing | <page title>   # if new analysis page
   ```

## Do not

- Answer only from chat without checking the wiki first
- Skip filing when the analysis would be useful later
- Edit `wiki/raw/` or `vote_context/`
