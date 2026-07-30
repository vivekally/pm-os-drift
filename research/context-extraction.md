# Phase 1 — Context Extraction from Vivek's Notion Sources

> **Access note (Phase 0):** All 6 Notion pages + subpages (2 levels), all 17 embedded
> diagram images, the LLMWiki Google Doc, the Karpathy gist, and the live site
> (https://vivekally.github.io/pm-os-landing/ — a React SPA; copy extracted from its JS
> bundle) were fetched successfully on 2026-07-09. **No access failures.**
>
> **Citation convention:** This repo is public. Per project security rules, Notion links
> are never written into this repo. Notion sources are cited as `[Notion: <page title>]`.

---

## 1. GBrain Ecosystem — Reference (Corrected) `[Notion: GBrain Ecosystem — Reference (Corrected)]`

- **GBrain is an open-source AI-agent memory system created by Garry Tan (President & CEO of Y Combinator), open-sourced April 5, 2026, MIT license.** It turns a markdown-in-git "brain" into a self-wiring knowledge graph an agent can search, write to, and reason over. GStack is the companion coding-workflow toolkit.
- **Correction to your prompt's definition:** GBrain is *not just* "a skill set for Claude Code." It ships in **four shapes** sharing one engine: (1) GBrain + GStack (code memory inside Claude Code), (2) Personal GBrain (full single-operator brain via Telegram/OpenClaw), (3) Company Brain (multi-user, OAuth-scoped federated sources), (4) gbrain.io (hosted, browser-only, commercial).
- Stack: markdown-in-git as source of truth → PGLite/Postgres+pgvector index → hybrid retrieval (HNSW vector + tsvector keyword + RRF fusion + backlink boost) → **self-wiring typed-edge knowledge graph with zero LLM calls per write** (worth +31.4 P@5 per its own benchmark).
- 60+ markdown skills (version-dependent); 30+ CLI=MCP operations; overnight 9-phase "dream cycle" (dedup, backlinks, synthesis, contradiction detection); Minions job queue; benchmarks BrainBench P@5 49.1% / LongMemEval R@5 97.6%.
- Cost profile: Personal ≈ $100–150/mo; Company ≈ $100/mo for ~25 people; gbrain.io pricing not public.
- Known limits `[Notion: 4 · Current Limitations & Known Issues]`: no end-user UI (CLI/MCP only), PGLite single-writer, onboarding friction requiring a "botmaster pattern" (pre-populate → wow flows → then grant access), no native mobile, young codebase with breaking changes.
- **Strategic read:** GBrain solved the engine, not the adoption. The missing UI + onboarding friction is exactly the gap PM OS Phase 1 targets.

## 2. Company Brain vs AI Operating System (YC RFS) `[Notion: Company Brain vs AI Operating System (YC RFS) + where gbrain fits]`

- Thesis: **Company Brain (Blomfield) is the noun (memory); AI OS (Hu) is the verb (control loop).** They are two layers of one stack; a real OS needs a Brain inside it.
- **Exact YC RFS language (from embedded screenshots of the YC RFS page):**
  - Tom Blomfield, "Company Brain": *"The biggest blocker to AI automation of companies is no longer the models… Now the blocker is the domain knowledge."* … *"We need Garry's G-Brain, but for every business in the world. A system that pulls knowledge out of all these fragmented sources, structures it, keeps it current, and turns it into an executable skills file for AI."* … *"It's a living map of how a company works: how refunds get handled, how pricing exceptions are decided or how engineers respond to incidents."* … *"I think every company in the world is going to need one. If you're building this, you should apply to YC."*
  - Diana Hu, "The AI Operating System for Companies": *"The best AI-native companies we're seeing have figured out something most haven't: they've made their entire company queryable."* … *"This turns a company from an open loop into a closed loop… the system monitors what's happening, compares it to what should be happening, and adjusts. I've seen teams that do this cut sprint time in half and ship twice as much."* … *"There's no product that connects all this context into a single intelligence layer… Not another dashboard. The system that turns a company's own artifacts into a self-improving loop."*
- gbrain implements the Company Brain RFS (Blomfield names G-Brain explicitly). Its loop closes on *the brain's own health*, not on company execution — the OS layer is unbuilt.
- Build order is forced: **Brain first** (the OS loop needs the brain as its reference model of "should"). Brain-first is also the better GTM (day-one value, data gravity, avoids "another dashboard").
- The moat is NOT the plumbing. It is: graph-structured relational knowledge, zero-upkeep freshness, trust (scoping/citations/honest gaps), and **encoding "what should happen" per vertical — the genuinely unsolved step**.
- Open question posed to you: *"What vertical or department do you know cold, where you could encode 'what should be happening' sharper than a generalist?"* → Your answer is PM.

## 3. LLMWiki `[Notion: LLMWiki]` + Google Doc + Karpathy gist

- **LLMWiki = your implementation of Andrej Karpathy's "LLM Wiki" pattern** (gist, ~Apr 2026, 5,000+ stars in days): a persistent, compounding, LLM-maintained markdown wiki, explicitly framed against RAG — *"synthesis happens once at ingest time; the wiki is a persistent, compounding artifact."*
- Your Google Doc ("LLM Wiki — Agentic Knowledge Base," 27KB): Claude in Cowork mode maintains a 3-layer architecture — `raw/` (immutable sources) → `wiki/` (LLM-owned interlinked markdown: domains/topics/entities/synthesis) → schema (project instructions). Operations: **ingest / query / lint**; contradiction preservation; wikilink integrity; Obsidian-native; scales to ~2K sources via `index.md` with no embeddings.
- Eval in the doc: 3/3 retrieval questions correct (incl. multi-hop) vs 1 hallucination for raw-document GPT-5.5; ~2 min ingest per article.
- `[Notion: LLMWiki vs SuperMemory]`: wiki = human-readable, compile-time structure; SuperMemory = API-first, agent-readable, automatic memory. Verdict recorded: for a general-purpose second brain, "most users don't actually want to maintain a wiki — they want an AI that remembers everything."
- `[Notion: Comparison with Other Tools]` (image): GBrain = multi-user *product/appliance* (server, embeddings, OAuth); LLM Wiki = single-user *pattern/recipe* (plain markdown + any agent). Lineage: Vannevar Bush's Memex — "LLM solves the maintenance problem."

## 4. PM OS `[Notion: PM OS]` — your concept and phase definitions

**Definitions** `[Notion: Direction]`:
- **Onboarding** = Context + Skills + Workflows + Automation
- **Brain** = Knowledge / memory
- **OS** = Onboarding + Brain + **Recursive Learning Loops**

**Refined one-liner (as requested):** *PM OS is a role-based AI operating system for product managers — guided onboarding (context, skills, workflows, automation) that becomes a provenance-tagged PM second brain, and eventually a recursive, self-learning OS that scales from one PM to the whole product org.*

**Phases (from the PM OS page mind-maps, verbatim intent):**
- **Phase 1 — PM Onboarding:** Replicate mysecond.ai (P0); take best from Paweł Huryn's PM Skills (P1), Aakash Gupta's PM_OS (P2), Coconut.dev (P3). "Don't reinvent the wheel — review and make the best package available on the internet." Keep it barebone and **free**; UI for non-technical PMs (if UI is a big investment, move it to Phase 2). Freemium: onboarding free, Brain paid. Start personal branding.
- **Phase 2 — PM Brain:** Take inspiration from Paweł Huryn's PM Brain, Garry's Personal GBrain, Akash's PM Brain, LLM Wiki, Coconut.dev. "Replicate best from existing PMBrain/Gbrains." UI showcases the power of the 2nd Brain.
- **Phase 3 — Improve 'PM Onboarding + PM Brain':** Double down on 2nd Brain; **expand from single PM to entire PM org** (company brain, per-source permissions).
- **Phase 4:** Recursive loops + self-learning → "true PM_OS or Self-Learning OS."

**Architecture** (mind-map): Onboarding (Context Builder + Context Health; Skills: existing library covering discovery/user research, strategy, prioritization, PRDs/specs, roadmapping + Skill Builder + orchestration; Workflows; Agents for automation & loops) · Brain (GBrain personal/company, PM Brain, LLMWiki, connectors to consolidate data) · OS (self-learning brain, recursive loops).

**Strategy notes** `[Notion: Direction]`, `[Notion: Summary]`:
- Progression path: *onboarding (one role) → personal brain (one role) → team/company brain → self-learning company OS.* Onboarding-first is explicitly justified as the stickiness/retention driver.
- Vision: role-agnostic OS; PM is the first test persona; lawyers next (law-os prototypes already exist).
- Current focus: **PM Onboarding + PM Brain + Personal Branding.** Personas: fractional PMs (technical & non-technical), solo founders. Personal-brand engine: LinkedIn content + "build AI engine to automate."
- "If we give skill and automation builders, we can replicate this for any role easily."

## 5. What to build next `[Notion: What to build next?]` (+ Direction, Summary)

- Direction tree: **User Onboarding & Stickiness** (Context Builder, Skill Builder, [Chained] Workflow Builder, Agent Builder, installable plugin packages) → **Personal Brain → Company Brain** → **Company OS** (learning loops, recursive learning).
- Summary page confirms the 3-phase roadmap wording: Phase 1 modeled on mysecond.ai with freemium (onboarding free, brain paid add-on); Phase 2 adds knowledge/memory layer; Phase 3 refines both. Strategic framing = the two YC RFS; "Garry Tan's open-source gbrain validates this approach. The moat comes from the loop, the vertical, and customer data, not the brain layer alone."
- Test strategy: build for PM first, use PM OS + PM Brain for personal branding and to attract consulting projects; then pick the next role to replicate.

## 6. AI Agentic Tooling Research `[Notion: AI Agentic Tooling Research]` (research hub)

- Hub covering: Claude Code + Couchto5k.ai, GStack workflow, GBrain ecosystem, GBrain security concerns, LLMWiki (+ security concerns PDF), SuperMemory, Hermes agent, OpenClaw cloud, Khoj, Glean Search, Shopify River/Aquifer.
- **Prior-art dossiers relevant to PM OS** `[Notion: Research/Notes]`:
  - **mysecond.ai (Ron Yang, ex-Aha!)** — "The PM Operating System." $39/seat/mo, 14-day trial. Two surfaces: Claude Code CLI (local-first markdown repo: CLAUDE.md, context/, 70+ skills, reviewer sub-agents) + browser app (shared context sync, context health, approvals, adoption/cost dashboards). MCP integrations: Linear/Jira/Confluence, PostHog/Amplitude/Mixpanel/Pendo, Slack/Notion, HubSpot/Salesforce/Intercom/Gong. **This is the Phase-1 pattern you cite.**
  - **PM-OS by Aakash Gupta** — $49 one-time Gumroad package: 103 markdown files, 41 workflows (400–700 lines each), 7 AI reviewers, 7 frameworks, 162k+ words; requires user's own Claude Pro/Max/API; claims ~15 hrs/week saved (vendor claim).
  - **PM Brain by Paweł Huryn** — free, MIT, open source. Plain markdown in local git, no vector DB/cloud/embeddings; 5-batch onboarding interview; /ingest with **provenance tagging (documented > verbal > intuition)**; /prep /ideate /risk /plan; weekly /review sweep; commits locally, never pushes. Companion pm-skills repo (11K+ stars). Internal eval 404/406 checks. **This is the Phase-2 pattern (and the pattern your current /pm-brain skill follows).**
  - **Coconut.dev** — model-agnostic "context layer": one governed source of knowledge any AI tool pulls via MCP; five context layers (Identity, Product, Process, Relationships, State) with auto-sync.
  - Convergence analysis: common-vs-unique component comparison across all PM OSes + web-traffic analysis + Lodestar landing prototype — "the synthesis layer that informs which features to prioritize."

## 7. Live site (Phase-4 input): https://vivekally.github.io/pm-os-landing/

- React/Vite SPA titled "PM OS — The operating system for product teams." Full copy extracted from JS bundle (site renders client-side; crawlers/SEO see only the `<title>` — flag for Phase 4).
- Hero: *"Your AI knows nothing about your product. PM OS fixes that: context, skills, workflows and automation for every PM, plus a [second brain] that remembers what your team learns. Onboard in minutes. Compound forever."* Sub: "plain markdown · no vector DB · commits locally, never pushes."
- Sections: The context tax (with/without PM OS) · Three phases (Phase 1 Skill Runner / PM Onboarding · Phase 2 Ask the Brain / PM Brain · Phase 3 Company Brain / scale to org · Phase 4 roadmap: recursive loops + self-learning) · The PM Brain (folder structure, provenance markers: documented/verbal/hunch/industry) · 3-step workflow (Capture → Orchestrate → Portable) · Skill layer (Teresa Torres OST, Amplitude North Star, Cagan four risks, Rumelt) · 13-screen clickable prototype CTA.

---

## Verified definitions (per your Phase-0 request)

| Term | Your definition | Verified against sources |
|---|---|---|
| GBrain | "Garry Tan's open-source second-brain skill set for Claude Code" | **Partially correct.** It's Garry Tan's open-source *agent memory system* (MIT, Apr 5 2026). The Claude Code skill set is one of four shapes; Personal/Company/hosted (gbrain.io) shapes are the fuller product. |
| LLMWiki | "as documented in my Notion page" | Karpathy's LLM Wiki *pattern* (compile-time knowledge, anti-RAG) as implemented in your Google Doc guide: Claude Cowork + raw/wiki/schema + ingest/query/lint. A pattern, not a product. |
| mysecond.ai | "onboarding-first second brain product" | **Correct pattern, wrong category emphasis:** it's an onboarding-first **PM OS** (context files + skills + MCP + team dashboard, $39/seat/mo). Its "brain" is context files; no compounding memory layer with provenance. That gap is your Phase-2 wedge. |
| PM OS | recursive self-learning OS for PMs | Confirmed + refined: Onboarding (context/skills/workflows/automation) → PM Brain (provenance-tagged memory) → org brain → recursive learning loops. Phases 1–4 as extracted above. |
