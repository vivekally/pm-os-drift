# pm-os-drift

The weekly strategy drift report for Heads of Product, and the strategy behind it.

## Live links

Everything below is published and clickable. No signup, no build step.

**Current site** — `vivekally.github.io/pm-os-drift/`

| Link | What it is |
|---|---|
| [Weekly drift report](https://vivekally.github.io/pm-os-drift/) | The artifact. Week of Jul 28, showing a correction from the previous week closing |
| [Report #1](https://vivekally.github.io/pm-os-drift/report-1/) | The previous week, kept so the correction above can be checked against what was actually flagged |
| [Setup flow](https://vivekally.github.io/pm-os-drift/onboarding/) | Four-source connection flow |
| [Forum Ventures deck](https://vivekally.github.io/pm-os-drift/forum-deck/) | 13 slides, companion to the studio founder memo |
| [/drift-report-w2/](https://vivekally.github.io/pm-os-drift/drift-report-w2/) | Redirect, kept so previously shared links keep working |

**v2 rebuild** — the product surface rebuilt around the correction loop

| Link | What it is |
|---|---|
| [Landing page](https://vivekally.github.io/pm-os-drift/v2/) | One entry point into the prototype |
| [Weekly report](https://vivekally.github.io/pm-os-drift/v2/report/index.html) | Findings measured only against confirmed commitments, each correctable inline |
| [Commitment ledger](https://vivekally.github.io/pm-os-drift/v2/ledger/index.html) | What we think you committed to. Confirm, correct or dismiss |
| [Assumption ledger](https://vivekally.github.io/pm-os-drift/v2/assumptions/index.html) | What the roadmap takes on faith, ranked by evidence weakness times age times dependents |
| [Sources](https://vivekally.github.io/pm-os-drift/v2/setup/index.html) | Capture-first setup. No strategy document required |

**Earlier work** — separate repos, still live

| Link | What it is |
|---|---|
| [pm-os-landing](https://vivekally.github.io/pm-os-landing/) | Landing page for the previous strategy |
| [pm-os-deck](https://vivekally.github.io/pm-os-deck/) | Investor deck for the previous strategy |
| [pm-os-prototype](https://vivekally.github.io/pm-os-prototype/) | 13-screen clickable prototype, three phases |
| [PM-OS-with-Second-Brain](https://vivekally.github.io/PM-OS-with-Second-Brain/) | Original second-brain designs |

> The three "earlier work" sites describe a different buyer ($39/seat, PM
> individual contributor) than this repo does. That is a known inconsistency,
> not an oversight. See the table below for what changed.

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
  site/index.html                     the current weekly report (published at /)
  site/report-1/index.html            the previous week, kept for verification
  site/onboarding/index.html          four-source setup flow
  site/drift-report-w2/index.html     redirect stub for a previously shared link
  v2/index.html                       v2 landing page
  v2/report|ledger|assumptions|setup  the v2 prototype, four screens
  forum-deck/index.html               Forum Ventures studio deck
DESIGN.md                             Workbench B tokens, provenance + drift severity colors
TODOS.md                              what to do next, and what gates what
```

## Open the prototype

```bash
open designs/site/index.html
```

Or the v2 rebuild:

```bash
open designs/v2/index.html
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
