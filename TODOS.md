# TODOS

From the /office-hours session on 2026-07-29. Full context:
[docs/design-2026-07-29-drift-report.md](docs/design-2026-07-29-drift-report.md).

## P1 — gates everything

- [ ] **T1 — Get one Head of Product to grant read access, then hand-build one report.**
  - Read access to their Linear or Jira, their roadmap or bets doc, and their last
    three customer call transcripts.
  - Hand-build the weekly drift report. Send it Monday morning.
  - **The metric is the forward.** Did they send it to someone senior to them? A
    compliment is not a forward.
  - Do not demo, do not explain the brain, do not mention provenance tags, do not
    send a guided interview. Send the artifact.
  - **Kill criterion:** three Heads of Product read the report, call it
    interesting, and none forward it. The wedge is not the wedge and the drift
    thesis stops.

- [ ] **T2 — Capture three numbers on that first call, before any report exists.**
  1. How long their last exec update took to assemble, in hours.
  2. One bet the team drifted off without anyone noticing, and what it cost.
  3. Whether they will connect a transcript export. Ask live. A no here weakens
     the whole spine and is better known in week one.

- [ ] **T3 — Ask the cold-start question on intake.**
  Does a written bets doc exist, and when was it last updated? Section 01 of the
  report is impossible without one. If it does not exist, report #1 becomes "here
  is what your team did" with no argument. This is the first thing that breaks.

## P2 — same workstream

- [ ] **T4 — Instrument context-to-output traceability from report #1.**
  Log which source fed which finding. This is what makes the review loop
  measurable, and it is the only way to tell good brain evolution from bad later.
  Carried forward from the old repo; now load-bearing rather than nice to have.

- [ ] **T5 — Own-store plus per-object scope field, before design partner #2.**
  Cheap insurance. Retrofitting access-scoping is the classic painful rewrite even
  inside a single-product, multi-team deployment.

- [ ] **T6 — Encryption at rest and a context read/write audit log, before partner #2.**
  Reading a company's Linear, Slack, and customer calls is a different security
  conversation than reading one PM's notes. This moved up from "deferrable legal
  bundle" the moment the buyer changed.

## Deferred, with triggers

| Item | Trigger to start |
|---|---|
| Approach B: connectors, drift agent, review surface | A partner asks "can this run itself?", or one report costs more than a day |
| Approach C: free exec brief funnel | B's engine runs unattended for one partner |
| Plain-text email version of the report | First partner's mail client mangles the HTML |
| Web review UI beyond the report | A partner asks to correct in-place instead of by reply |
| Skill library / marketplace | Not planned. Commodity, and never the moat |

## Open questions

1. Cost of the status quo is still unquantified. T2 gets the number.
2. Does the report survive being wrong? Three findings where two are wrong
   destroys trust faster than a stale doc. Confidence and provenance display is a
   trust design problem, not a model problem.
3. Cold start per customer: how many weeks of history and how many transcripts
   before report #1 is worth forwarding?
4. Transcript access is the weakest link in the whole spine.
5. The PM-to-lawyer transferable core is still unnamed, but there is finally a
   candidate: the documented-intent-versus-actual-behavior reconciliation loop.
   Legal equivalent would be matter-intent versus filed-work. Hypothesis only.

## Constraint

Path D (consulting) stays capped at roughly 20% of the week, and every engagement
must dogfood the product. Under the done-with-you delivery model the install *is*
the consulting, so A and D stop competing for hours.
