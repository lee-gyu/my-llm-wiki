---
name: research
description: Investigate a topic with external evidence and save a provenance-tracked synthesis under research/. Use when the user asks to research, investigate, survey, compare, or gather authoritative material about a topic, including follow-up research on an existing topic. Do not use for answering only from existing wiki content, ingesting files from raw/, or automatically promoting findings into wiki/.
---

# Research

Perform the LLM Wiki's **research** operation. Treat research as an evidence-gathering
workspace, not as a shortcut for adding unreviewed claims to `wiki/`.

## Before starting

Read the repository's `CLAUDE.md` first. It is the authoritative schema for directory
layout, hard rules, naming, logging, and commits. If this skill disagrees with it,
follow `CLAUDE.md` and flag the discrepancy to the user.

Keep these constraints throughout the operation:

- Store agent-conducted research only under `research/<topic-slug>/`; never write it to
  `raw/`.
- Cite the topic's source ledger for every substantive factual claim.
- Preserve conflicting findings instead of silently replacing earlier evidence.
- Do not promote findings into `wiki/` unless the user requests that separate operation.

## Workflow

### 1. Identify the topic

Read `research/index.md` first if it exists. Choose a short, stable, kebab-case ASCII
slug, and reuse an existing topic directory for follow-up research instead of creating
a near-duplicate.

Record the user's original request and define a focused scope. If the topic is broad,
state the boundaries and research questions before gathering evidence.

### 2. Gather evidence

Search for current external evidence. Prefer primary and authoritative sources, and use
multiple independent sources for consequential claims. Distinguish sourced facts from
your synthesis or inference.

Maintain `research/<topic-slug>/sources.md` as the source ledger while researching.
Assign stable IDs (`S1`, `S2`, ...); never renumber existing IDs. For each source,
record:

- title
- author or publisher
- publication date, when known
- URL
- access date
- the finding or claim it supports

Put useful source-specific details in `notes/`, clearly marking quotations and
paraphrases. Keep quotations brief and never copy an entire copyrighted work into the
repository.

### 3. Write the synthesis

Create or update `research/<topic-slug>/README.md`. Read the existing file first during
follow-up work and preserve earlier findings when new evidence disagrees.

Include:

- original request
- scope and research questions
- research date and status
- synthesized findings
- conflicts in the evidence
- limitations
- open questions

Cite source IDs inline for every substantive factual claim, using `[S1]` or
`[S1, S3]`. Describe disagreements explicitly and leave them unresolved unless the
available evidence clearly supports an adjudication.

### 4. Update project bookkeeping

Update `research/index.md` with one line for the topic containing its link,
discriminating summary, status, and last-researched date. Append a `research` entry to
`wiki/log.md` describing what was created or updated; never edit past log entries.

Before finishing, verify that every inline source ID exists in `sources.md`, every
ledger entry used by the synthesis is cited, and the index and log match the files.

### 5. Commit and report

Create one commit for the completed operation with message `research: <topic-slug>`.
Commit only after the topic files, research index, and wiki log form a consistent
snapshot.

Report:

```markdown
## Researched: <topic>
- Topic: research/<topic-slug>/README.md
- Scope: <one-line scope>
- Sources: <count; note primary/secondary mix>
- Key findings: <brief bullets>
- Conflicts or limitations: <brief list or "none">
- Open questions: <brief list or "none">
- Wiki promotion: not performed
```

If the user asks to incorporate findings into `wiki/`, handle it as a separate
operation using the normal source-page, provenance, contradiction, index, log, and
commit rules from `CLAUDE.md`.
