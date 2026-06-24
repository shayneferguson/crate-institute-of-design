# Brand Wiki Schema
**The Crate Institute of Design**

This document defines the structure, conventions, and workflows for this brand wiki. Read it before any operation.

---

## Purpose

A living brand intelligence system for The Crate Institute of Design. Rather than a static PDF guide, this wiki evolves as new material is ingested. The LLM handles bookkeeping; the human handles judgment.

---

## Directory Structure

```
/
├── schema.md          ← this file; read first
├── index.md           ← catalog of every article
├── log.md             ← chronological change record
├── sources/           ← raw immutable source material
├── identity/          ← who we are, what we stand for
├── audience/          ← who we serve and why they hire us
├── offers/            ← services, pricing philosophy, process
├── voice/             ← tone, language, copy examples
├── proof/             ← testimonials, case studies, results
├── market/            ← competitive landscape, positioning
├── strategy/          ← goals, growth bets, direction
└── frameworks/        ← proprietary tools and methodologies
```

---

## Source Types

When ingesting a new source, classify it first:

| Type | Examples | Primary categories updated |
|---|---|---|
| Founder reflection | journal entries, interviews, voice memos | identity, strategy, voice |
| Client call transcript | discovery, feedback, or sales calls | audience, proof, offers |
| Testimonial / review | written or video testimonials | proof, audience |
| Existing copy | website, proposals, social posts | voice, offers, identity |
| Research / reference | competitor analysis, market reports | market, strategy |
| Case study | project summaries, before/after | proof, offers, frameworks |

---

## Conventions

- Every article begins with a `# Title` and a one-line `> Summary` blockquote.
- Articles link to related articles using `[[article-name]]` notation.
- Contradictions are flagged with `⚠️ CONFLICT:` inline.
- Stale or unverified claims are marked `[unverified]`.
- Each article ends with `_Last updated: YYYY-MM-DD | Sources: [list]_`

---

## Workflows

### First Read
Before any query or ingest, consult:
1. `schema.md` (this file)
2. `index.md` (what exists)
3. `log.md` (what changed recently)

### Ingest
1. Place source file in `sources/` with a descriptive name and date prefix (e.g. `2026-06-23-client-call-abc-corp.md`)
2. Classify the source type
3. Extract intelligence and update relevant wiki articles
4. Update `index.md` and append to `log.md`
5. Weight newer sources more heavily than older ones

### Query
1. Identify which categories are relevant
2. Synthesize answer from wiki articles
3. If a valuable new insight emerges, create a new article and update index + log

### Lint (run periodically)
- Scan for contradictions between articles
- Flag stale content (no update in 90+ days)
- Identify thin articles that need more source material
- Verify all index entries match actual files

### Export
Generate `exports/brand-context.md` — a 3,000–5,000 word synthesis of the wiki for sharing with other AI systems or stakeholders. Regenerate whenever major updates occur.

---

## Weighting Rules

- Newer sources supersede older ones
- Founder voice supersedes third-party interpretation
- Repeated patterns across multiple sources = high confidence
- Single-source claims should be marked `[unverified]`
