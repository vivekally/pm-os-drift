# Phase 2 — Market Deep Research: Recursive / Second-Brain AI Tools

**Prepared:** 2026-07-09 · **Analyst lens:** VC market analyst + product strategist (critical mode)
**Scope:** Tools that accumulate personal or org knowledge and improve with use — PKM, enterprise second brain, memory infra, AI-OS plays — evaluated as the competitive context for **PM OS**.
**Citation rules:** Every external figure carries a URL. `[Estimate]` = my derivation. `[Unverified]` = could not confirm from a primary/credible source. Notion sources cited as `[Notion: <page title>]` (links never written into this public repo, per project security policy).

---

## 1. Landscape map — four categories

### 1a. Personal second brain (PKM)

| Player | What it is | Status signal |
|---|---|---|
| **Mem** | AI note app, "self-organizing workspace" | $23.5M Series A led by OpenAI Startup Fund at $110M post (Nov 2022); ~$29M total ([TechCrunch](https://techcrunch.com/2022/11/10/ai-powered-note-taking-app-mem-raises-23-5m-openai/)) |
| **Rewind → Limitless** | Screen/audio capture "perfect memory"; pivoted to $99 pendant | $15M at $350M val (2023, NEA/a16z); **acquired by Meta, Dec 2025**, folded into Reality Labs ([Sacra](https://sacra.com/c/limitless/), [Crunchbase](https://www.crunchbase.com/organization/rewind-53b3)) |
| **Tana** | AI-native knowledge graph workspace | $25M total; $14M Series A at $100M post (Tola Capital, Feb 2025); 160K+ waitlist ([TechCrunch](https://techcrunch.com/2025/02/03/tana-snaps-up-25m-with-its-ai-powered-knowledge-graph-for-work-racking-up-a-160k-waitlist/)) |
| **Reflect** | Networked note app w/ AI | Small/bootstrapped-scale; no major round found `[Unverified]` |
| **LLM Wiki pattern (Karpathy)** | Not a product: 3-layer markdown wiki pattern (raw/ → wiki/ → schema), anti-RAG, "knowledge compounds" | Gist published Apr 2026, ~5K stars in days; multiple community implementations ([AI Builder Club](https://www.aibuilderclub.com/blog/karpathy-llm-wiki), [Level Up Coding](https://levelup.gitconnected.com/beyond-rag-how-andrej-karpathys-llm-wiki-pattern-builds-knowledge-that-actually-compounds-31a08528665e)) |

**Category read (critical):** Pure PKM is a graveyard for venture returns — Mem stalled after the OpenAI halo, Rewind exited small relative to hype via acqui-pivot, Evernote died before AI mattered. The pattern: *personal* memory alone doesn't monetize past prosumer price points, and platform owners (Notion, Meta, Anthropic/OpenAI memory features) absorb the feature. **Implication for PM OS: "second brain" as a horizontal consumer promise is a weak wedge; role-specific workflow value is the only defensible retail entry.**

### 1b. Enterprise second brain

| Player | What it is | Status signal |
|---|---|---|
| **Glean** | Enterprise search → work AI platform | $150M Series F at **$7.2B** (Jun 2025, Wellington) ([Glean](https://www.glean.com/blog/glean-series-f-announcement), [CNBC](https://www.cnbc.com/2025/06/10/glean-gen-ai-search-startup-raises-150-million-at-7-billion-value.html)); ARR reportedly $100M (early 2025) → ~$300M (May 2026) ([Teahose](https://www.teahose.com/guides/glean-valuation) — secondary source) |
| **Dust** | Multiplayer enterprise agents over a company context layer, 100+ connectors | $40M Series B (Sequoia + Abstract, May 2026), >$60M total; 3,000+ orgs, 300K agents deployed ([Sifted](https://sifted.eu/articles/dust-series-b-40m), [SiliconANGLE](https://siliconangle.com/2026/05/18/multiplayer-ai-startup-dust-swipes-40m-funding-help-enterprises-move-beyond-isolated-ai-assistants/)) |
| **Onyx** (ex-Danswer) | Open-source enterprise search/chat, self-hosted | YC W24; $10M seed co-led Khosla + First Round; Netflix, Ramp among users ([TechCrunch](https://techcrunch.com/2025/03/12/why-onyx-thinks-its-open-source-solution-will-win-enterprise-search/), [Onyx](https://onyx.app/blog/seed-round)) |
| **Viven** | Per-employee "digital twin" LLMs — query an unavailable coworker's knowledge | $35M seed from stealth (Khosla, Foundation Capital, Oct 2025); Eightfold founders; Genpact deployed ([TechCrunch](https://techcrunch.com/2025/10/15/eightfold-co-founders-raise-35m-for-viven-an-ai-digital-twin-startup-for-querying-unavailable-coworkers/)) |
| **Granola** | Meeting notes → "enterprise AI context" platform | $43M Series B at $250M (May 2025) → **$125M Series C at $1.5B (Mar 2026)**, explicitly repositioning from notetaker to enterprise context/memory ([TechCrunch](https://techcrunch.com/2026/03/25/granola-raises-125m-hits-1-5b-valuation-as-it-expands-from-meeting-notetaker-to-enterprise-ai-app/), [Bloomberg](https://www.bloomberg.com/news/articles/2026-03-25/ai-notetaker-granola-hits-1-5-billion-value-in-125-million-funding)) |
| **Notion** (incumbent) | Workspace + AI agents (Notion 3.0, Sep 2025) | 100M users (Aug 2024) ([Notion](https://www.notion.com/blog/100-million-of-you)); $500M+ ARR, >50% of ARR from AI-enabled customers ([CNBC](https://www.cnbc.com/2025/09/18/notion-launches-ai-agent-as-it-crosses-500-million-in-annual-revenue.html)) |
| **GBrain / Company Brain** | Open-source (MIT) agent memory: markdown-in-git → self-wiring knowledge graph; personal → company → hosted (gbrain.io) | OSS Apr 5, 2026 by Garry Tan; ~5K GitHub stars in 24h; 97.6% R@5 LongMemEval ([GitHub](https://github.com/garrytan/gbrain), [Digg](https://digg.com/ai/82u1xlg1), [Vectorize](https://vectorize.io/articles/what-is-gbrain)) |

**Category read (critical):** This is where the money is going, and it's crowding fast from *both* ends — Glean/Dust down from search/agents, Granola up from capture, Viven sideways from HR-tech, and Notion/Atlassian bundling it for free-ish. A generic "company brain" startup founded mid-2026 is late. **The open question Blomfield's RFS leaves — and your own Notion analysis lands on — is the vertical/role-scoped brain, where "what should happen" can be encoded.** `[Notion: Company Brain vs AI Operating System (YC RFS) + where gbrain fits]`

### 1c. Memory infrastructure

| Player | What it is | Status signal |
|---|---|---|
| **Mem0** | Memory API layer for AI apps/agents | $24M seed+Series A (Basis Set, Peak XV, **YC**, Oct 2025); 41K GitHub stars, 186M API calls Q3'25; AWS Agent SDK exclusive memory provider ([TechCrunch](https://techcrunch.com/2025/10/28/mem0-raises-24m-from-yc-peak-xv-and-basis-set-to-build-the-memory-layer-for-ai-apps/)) |
| **Supermemory** | Memory-as-a-service API ("universal memory") | $2.6–3M seed (Susa, Browder Capital; angels incl. Jeff Dean), Oct 2025 ([TechCrunch](https://techcrunch.com/2025/10/06/a-19-year-old-nabs-backing-from-google-execs-for-his-ai-memory-startup-supermemory/)) |
| **Letta** (MemGPT) | Agent runtime with self-editing memory | $10M seed at $70M post (Felicis, Sep 2024) ([BigDATAwire](https://www.hpcwire.com/bigdatawire/this-just-in/letta-emerges-from-stealth-with-10m-to-build-ai-agents-with-advanced-memory/)) |
| **Zep** | Temporal knowledge-graph memory for agents | YC W24; $3.3M raised ([Generational](https://www.generational.pub/p/memory-in-ai-agents)) |
| **GBrain (as infra)** | Free OSS engine incl. Postgres/pgvector hybrid retrieval + typed-edge graph | MIT; also runs your own /pm-brain substrate decision `[Notion: GBrain Ecosystem — Reference (Corrected)]` |

**Category read (critical):** Memory infra is being commoditized in real time — three funded APIs, one hyperscaler default (AWS→Mem0), and a free MIT engine from the YC CEO himself. **Do not build memory plumbing; your Notion decision to adopt a GBrain-class substrate is correct and now cheaper than ever to execute.** The corollary is uncomfortable: if the substrate is commodity, *none* of PM OS's defensibility can come from the brain engine.

### 1d. AI OS / role-based OS plays (the direct competitive set)

| Player | What it is | Status signal |
|---|---|---|
| **mySecond** (mysecond.ai) | "The PM Operating System" on Claude Code: context files + 70+ skills + MCP integrations + team browser dashboard | $39/seat/mo, 14-day trial; services from $5K; founder Ron Yang (ex-Aha!, scaled $2M→$100M ARR) + Maven course ([mySecond](https://mysecond.ai/), [Maven](https://maven.com/ron-yang/claude-code-os-product-managers)) |
| **ChatPRD** | AI CPO web app (PRDs → full PM platform) | Bootstrapped; claims 100K+ PMs, 750K+ docs (Jun 2026); $15/mo Pro, $29/seat Teams ([ChatPRD](https://www.chatprd.ai/), [Ry Walker research](https://rywalker.com/research/chatprd), [Every podcast](https://every.to/podcast/she-built-an-ai-product-manager-bringing-in-six-figures-as-a-side-hustle-e46be9bc-f426-424d-992d-5a71fd7ac5e4)) |
| **PM OS by Aakash Gupta** | $49 one-time Gumroad package: 103 md files, 41 workflows, 7 reviewers | Newsletter distribution (~large PM audience); no recurring product ([Gumroad](https://growthpioneer.gumroad.com/l/pmos)) `[Notion: PM-OS by Akash Gupta]` |
| **pm-brain by Paweł Huryn** | Free MIT PM second brain: markdown + git, provenance tags, /ingest //review | Research preview; companion pm-skills repo 11K+ stars ([GitHub](https://github.com/phuryn/pm-brain), [Product Compass](https://www.productcompass.pm/p/pm-brain-os)) `[Notion: PM Brain by Pawel]` |
| **Coconut** (coconut.dev) | "Shared context layer for AI agents" — governed org knowledge served via MCP | Early; positioning overlaps your Phase-1 context builder ([Coconut](https://www.coconut.dev/)) — funding `[Unverified]` |
| **Team OS (Hannah Stulberg, DoorDash) / Ramp "Glass"** | Internal company-brain implementations (shared repo + skills marketplace, ~350 skills at Ramp) | Not products — proof the pattern works at org scale ([Alex Lockey](https://www.alexlockey.com/writing/the-company-brain-four-builders-one-architecture/)) |

**Category read (critical):** The PM-specific lane is **already occupied at every price point**: $0 (Huryn, MIT), $49 one-time (Gupta), $15–29/mo (ChatPRD), $39/seat (mySecond). Your differentiation cannot be "PM skills on Claude Code" — that is now a commodity content category with three creators who each have bigger PM audiences than you. The unoccupied square is the one your Phase 2 defines: **a compounding, provenance-tagged PM memory that the skills read from and write back to** — mySecond has static context files, ChatPRD has doc history, Gupta has folders; none has a true brain with provenance, contradiction detection, and org-level federation. That gap is real but *narrow and closing* (Granola is building toward it top-down; mySecond can add it).

---

## 2. Market size — TAM / SAM / SOM

**Method:** top-down from category analyst reports, cross-checked bottom-up from PM population × observed price points. Category reports for "product management software" disagree wildly ($6B–$35B for 2025), so bottom-up is the load-bearing estimate; treat top-down as bounding.

### Top-down anchors
- Knowledge management software: **$20.15B (2024) → $62.15B (2033), 13.6% CAGR** ([Grand View Research](https://www.grandviewresearch.com/industry-analysis/knowledge-management-software-market-report)); alternate higher series: $34.99B (2024) → $92.45B (2033), 11.4% ([SkyQuest](https://www.skyquestt.com/report/knowledge-management-software-market)), and $33.5B (2025) → $97.7B (2035) ([MRFR](https://www.marketresearchfuture.com/reports/knowledge-management-software-market-4193)). Wide spread — use as ceiling for the *eventual role-agnostic OS vision*, not for PM OS today.
- Product management software: **$6.29B (2025) → $12.8B (2035), ~7.4% CAGR** ([WiseGuy](https://www.wiseguyreports.com/reports/product-management-software-market)); other reports up to $22.7B by 2034 ([Dataintelo](https://dataintelo.com/report/global-product-management-software-market)). Low-quality category; label all such figures `[Estimate — low-confidence analyst reports]`.

### Bottom-up (the sanity check that matters)
- PM population: **~850K active PMs globally** ([Corpwaters analysis](https://corpwaters.substack.com/p/how-many-product-managers-are-there)); up to **2.6M LinkedIn "Product Manager" title holders** ([LLCBuddy](https://llcbuddy.com/data/product-management-statistics/)). ~23K open PM roles worldwide, Apr 2025 ([Productify](https://productify.substack.com/p/2025-product-management-job-market)).
- Observed willingness to pay: $39/seat/mo (mySecond), $15–29/mo (ChatPRD), $49 one-time (Gupta). Take **$470/yr/seat** as the anchor ARPU. `[Estimate]`

| Layer | Definition | Math | Value |
|---|---|---|---|
| **TAM** | Every active PM globally on an AI PM-OS seat | 850K–2.6M PMs × $470/yr | **$0.4B–$1.2B/yr** `[Estimate]` — plus org-tier multiplier (dashboards, org brain, admin) plausibly 2–3× → **$1–3.5B**. Consistent with the low end of PM-software top-down ($6.3B total category, AI-OS as a 15–50% eventual share). |
| **SAM** | English-speaking, AI-forward PMs at tech companies reachable via creator/content GTM (the segment mySecond/ChatPRD fish in); ChatPRD's claimed 100K+ users is the live proxy for segment size | ~200–300K PMs × $470/yr | **$95–140M/yr** `[Estimate]` |
| **SOM** (24–36 mo) | Realistic capture for a new entrant with no distribution advantage, freemium onboarding, paid brain | 2K–8K paid seats (0.7–2.7% of SAM seats) × $470 | **$0.9M–$3.8M ARR** `[Estimate]` |

**Critical note on the deck-friendly version:** if the story is "role-based OS for every role" (PM → lawyers → …), TAM legitimately expands toward the knowledge-management ceiling ($20B+), but an investor will discount any TAM you haven't earned a wedge in. Lead with the honest $1–3.5B PM TAM and show the role-replication mechanism (skill/automation builders `[Notion: Direction]`) as the expansion story.

---

## 3. Competitor table

| Company | Category | Funding (cited above) | Stage | ICP | Wedge | Moat | Threat to PM OS (1–5) |
|---|---|---|---|---|---|---|---|
| Glean | Enterprise brain | $150M @ $7.2B | Late (F) | Large enterprise | Search → agents over all work data | Connectors, security, enterprise sales | 2 — different buyer (IT), too heavy for PM ICs |
| Dust | Enterprise brain | $40M B, >$60M total | Growth | Mid-market/enterprise teams | Multiplayer agents on context layer | 100+ connectors, usage depth (90% MAU) | 3 — a PM team could just use Dust |
| Onyx | Enterprise brain (OSS) | $10M seed, YC W24 | Seed | Self-hosting enterprises | Open-source Glean | OSS community + on-prem trust | 2 |
| Viven | Enterprise brain | $35M seed | Seed (big) | Enterprise | Per-person digital twins | Founder pedigree, privacy tech | 2 — top-down, HR-adjacent |
| Granola | Context capture → enterprise brain | $125M C @ $1.5B | Growth | Anyone in meetings → teams | Zero-friction capture at the source | Capture habit + data gravity | **4 — owns the highest-value PM input (meetings) and is moving into "enterprise context"** |
| Notion (AI) | Incumbent workspace | 100M users, $500M+ ARR | Public-scale private | Everyone | Bundled AI agents where docs already live | Distribution, data gravity | **4 — "good enough" org brain for free-ish** |
| Mem0 / Supermemory / Zep / Letta | Memory infra | $24M / ~$3M / $3.3M / $10M | Seed–A | Developers | Memory API | Dev adoption, benchmarks | 1 — suppliers, not competitors (potential substrate) |
| GBrain (OSS) | Memory substrate + pattern | n/a (MIT OSS) | n/a | Technical operators | Free, self-hosted, YC-CEO halo | Community velocity | 2 as competitor; **5 as commoditizer** of any brain-engine differentiation |
| mySecond | PM OS | Bootstrap/`[Unverified]` | Revenue | PM teams (non-technical OK) | Onboarding-first PM OS, team dashboard | Founder authority (ex-Aha!), Maven course GTM, first mover | **5 — your Phase 1 is their live product** |
| ChatPRD | PM AI platform | Bootstrapped, six-figure+ rev | Revenue | ICs → teams | Fast PRDs, web-native UX | 100K-user distribution, brand | **5 — owns the "AI for PMs" mindshare + web UX you plan to build** |
| Aakash Gupta PM OS | PM OS (content) | n/a ($49 product) | Revenue | His newsletter audience | Cheap, comprehensive package | Audience (newsletter/YouTube) | 3 — price anchor + audience, no compounding product |
| pm-brain (Huryn) | PM brain (OSS) | Free MIT | n/a | Technical PMs | Provenance-tagged markdown brain | 11K+ star skills repo audience | **4 — free version of your Phase 2, from a bigger audience** |
| Coconut | Context layer | `[Unverified]` | Early | AI-forward teams | Governed context via MCP | Unclear | 2–3 |

---

## 4. YC signal

**Both RFS texts verified** at [ycombinator.com/rfs](https://www.ycombinator.com/rfs) (Summer 2026 batch, ~15 categories; coverage: [TheVCCorner](https://www.thevccorner.com/p/yc-summer-2026-requests-for-startups-ideas), [Superframeworks](https://superframeworks.com/articles/yc-summer-2026-rfs-hard-tech-pivot)). Full screenshots preserved in `[Notion: Company Brain vs AI Operating System (YC RFS) + where gbrain fits]`.

**Company Brain — Tom Blomfield (exact language):**
> "The biggest blocker to AI automation of companies is no longer the models… Now the blocker is the domain knowledge." … "We need Garry's G-Brain, but for every business in the world. A system that pulls knowledge out of all these fragmented sources, structures it, keeps it current, and turns it into an executable skills file for AI." … "It's a living map of how a company works: how refunds get handled, how pricing exceptions are decided or how engineers respond to incidents." … "I think every company in the world is going to need one. If you're building this, you should apply to YC."

**The AI Operating System for Companies — Diana Hu (exact language):**
> "The best AI-native companies we're seeing have figured out something most haven't: they've made their entire company queryable." … "This turns a company from an open loop into a closed loop… the system monitors what's happening, compares it to what should be happening, and adjusts. I've seen teams that do this cut sprint time in half and ship twice as much." … "There's no product that connects all this context into a single intelligence layer that can reason across it, flag when engineering is building the wrong thing, or generate specs agents can execute on." … "Not another dashboard. The system that turns a company's own artifacts into a self-improving loop. If you're building this, we'd love to talk."

**YC-backed startups already in this space:** Mem0 (YC, memory layer — [TechCrunch](https://techcrunch.com/2025/10/28/mem0-raises-24m-from-yc-peak-xv-and-basis-set-to-build-the-memory-layer-for-ai-apps/)), Zep (W24), Onyx (W24 — [YC profile](https://www.ycombinator.com/companies/onyx)), Mem (early YC + OpenAI Fund). Plus the non-YC ecosystem YC's own partners point at: GBrain (Tan), Karpathy's LLM Wiki, Team OS, Ramp Glass ([Alex Lockey](https://www.alexlockey.com/writing/the-company-brain-four-builders-one-architecture/)).

**Signal read (critical):** YC has effectively declared the *category* open and the *substrate* solved (Tan gave it away MIT-licensed). The RFS is an invitation for the **loop and the vertical**, not another brain. Hu's examples of "should" are engineering-shaped (spec drift, sprint speed) — the PM function sits exactly at the intent layer she describes. That is genuine why-now evidence for PM OS **Phase 4's recursive-loop story**, but note the inversion: YC's language makes the *loop* the prize, while your roadmap defers the loop to last. Expect sophisticated investors to push on that.

---

## 5. Analyst's bottom line (pressure-test preview for Phase 3)

1. **Where you're right:** substrate-adoption decision (GBrain-class, don't build), provenance-tagged markdown brain (real gap vs mySecond/ChatPRD), role-vertical strategy (the only defensible posture vs Glean/Dust/Notion).
2. **Where the thesis is weakest:** (a) Phase 1 "onboarding-first" replicates a product (mySecond) that already exists at $39/seat with a stronger founder-brand and course-based GTM — replication without distribution is a losing race; (b) the free end of the market (Huryn MIT, Gupta $49) caps willingness-to-pay for exactly the artifact you'd charge for; (c) SOM math says this is a $1–4M ARR business in 3 years without a distribution unlock — fine for a bootstrap/consulting flywheel (which your `[Notion: Direction]` personal-branding plan implies), thin for a venture story unless the org-brain (Phase 3) or loop (Phase 4) arrives earlier.
3. **What would change the picture:** owning a proprietary input (mySecond doesn't capture meetings; Granola doesn't know PM frameworks), or collapsing Phase 2 into Phase 1 so the brain *is* the onboarding — full argument in Phase 3 (`strategy-eval.md`, pending your approval).
