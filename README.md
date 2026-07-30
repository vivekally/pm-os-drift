# pm-os-drift

The weekly strategy drift report for Heads of Product, and the strategy behind it.

A Head of Product cannot tell, week to week, whether their team is building what
the strategy says they should be building. Documented intent sits in Notion and
goes stale in three weeks. Actual behavior lives in Linear/Jira, Slack threads,
and customer calls. Nobody reconciles the two, because reconciling them means
reading everything.

This repo holds the reconciliation: a weekly report that puts the documented bets
next to what actually shipped and got decided, then names the places those two
disagree, with every line cited back to a source.

## Status

**Pre-product.** No paying user, no named design partner yet. The design doc is
approved; the prototype is built and verified. The next step is not code, it is
one phone call. See [TODOS.md](TODOS.md).

## Relationship to PM OS with Second Brain

This is a re-sequencing of the original PM OS with Second Brain design, not a
replacement. The original repo is archived and private now; its full code and
history live on, unchanged, at
[pm-os-archive/second-brain](https://github.com/vivekally/pm-os-archive/tree/main/second-brain).
Four decisions changed here:

| | June 22 (old repo) | July 29 (this repo) |
|---|---|---|
| Buyer | PM individual contributor | Head of Product / CPO. IC seat eliminated |
| Wedge | Guided 12-minute context interview | Weekly drift report from auto-ingested sources |
| Pricing | $29-39/mo seats | Done-with-you install, payback as the anchor |
| Self-evolving brain | Phase 4, built last | A side effect of the Phase 1 review loop |

The guided `/pm-brain` interview is not dead. It demotes from product to internal
tooling: it is how the operator seeds a partner's brain before report #1.

## Contents

```
docs/
  design-2026-07-29-drift-report.md   approved design doc — premises, approaches, assignment
  whitespace-teardown.md              the structural reference model, decomposed
designs/
  drift-report/index.html             the report prototype (self-contained, no deps)
  drift-report/meta.json              build + verification record
DESIGN.md                             Workbench B tokens, provenance + drift severity colors
TODOS.md                              what to do next, and what gates what
```

## Open the prototype

```bash
open designs/drift-report/index.html
```

No build step, no server, no network dependency for the JavaScript. Resize the
window and text heights recompute through Pretext rather than CSS approximation.
Click any text to edit it and the layout re-measures on keystroke. Append
`?debug` to the URL to see per-block computed height and line count.

Content is fictional (Kestrel, a B2B expense platform) with realistic data. Swap
it for a real partner's Linear, roadmap doc, and call transcripts.

## The approach

Three phases, each gated on the previous one earning it.

1. **A — concierge, now.** Hand-build the weekly report for three Heads of
   Product. Paid. No product. This is the only phase that cannot be executed
   without a named buyer, which is why it is first.
2. **B — auto-ingest, on trigger.** MCP connectors for Linear/Jira, Notion, and
   transcripts feed a gbrain-class substrate. A weekly agent produces the report.
   A review surface turns every correction into a provenance-tagged decision.
   Trigger: a partner asks "can this run itself?"
3. **C — free exec brief, gated on B.** Zero-setup shareable artifact as
   top-of-funnel. Held until B's engine exists, so it demos a real product rather
   than capping willingness-to-pay on its own.

## Design system

Workbench B, dark. `#070A11` background, `#3DDC84` accent, Inter and JetBrains
Mono. Read [DESIGN.md](DESIGN.md) before any visual decision.

Green means on track. `--drift` coral means off track. Never mark a finding the
reader must act on in green — a skimming exec reads green as good news.
