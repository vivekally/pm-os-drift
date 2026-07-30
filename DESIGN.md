# DESIGN.md — PM OS Design System

Design system for PM OS / PMBrain. Read this before any visual or UI decision.
Full project design doc: [docs/design-pm-os-second-brain.md](docs/design-pm-os-second-brain.md).

---

## Theme: Workbench B

Dark terminal aesthetic. Electric green accent. No decorative chrome.

## Colors

```
--bg:        #070A11   /* page background */
--surface:   #0F1420   /* card / panel */
--surface-2: #141B29   /* elevated surface */
--border:    #1E2D45   /* subtle divider */
--accent:    #3DDC84   /* primary CTA, active state, green dot */
--code:      #7FE8B0   /* code text, secondary green */
--text:      #E2E8F0   /* primary text */
--muted:     #64748B   /* secondary / placeholder */
```

## Provenance Tag Colors

Every load-bearing claim in the brain carries one of four provenance tags.
Use these exact colors — never reuse them for other meaning.

```
--doc:      #7FE8B0   /* documented  — highest trust: interview, data, survey */
--verbal:   #5BC0EB   /* verbal       — said in a meeting, not yet written */
--hunch:    #C9A227   /* hunch        — "I think", "I bet", gut feeling */
--industry: #8A93A6   /* industry     — benchmark, best practice, category norm */
```

Trust hierarchy: `documented > verbal > hunch > industry`

## Drift Severity Colors

The one status color outside the accent. Used ONLY to mark drift severity in
reports — never for provenance, never for general UI state.

```
--drift:      #FF6B5B   /* high severity — contradicted decision, documented bet broken */
--drift-soft: #8C4A45   /* medium / low severity — same hue, damped */
```

Same hue at two strengths, deliberately: a second hue would collide with
`--hunch` amber or `--verbal` blue and pollute the provenance vocabulary.

Rule: `--accent` green means **on track**. `--drift` means **off track**. Never
use green to mark a finding the reader needs to act on — a skimming exec reads
green as good news.

## Typography

```
UI / body:   Inter            (system weight: 400 regular, 500 medium, 600 semibold)
Code / data: JetBrains Mono   (all terminal output, file paths, commands, metrics)
```

No serif fonts. No display fonts. Type is functional, not decorative.

## Spacing

Base unit: `4px`. Common increments: `4 8 12 16 24 32 48`.

## Component Patterns

**Brain file output** — markdown with provenance pills:
```
## knowledge/users.md
- activation drops at day 3  [documented]
- SMB segment churns faster  [verbal]
- enterprise will pay more   [hunch]
```

**Command prompt** — JetBrains Mono, `#` or `/` prefix, dark surface bg:
```
/discover → brainstorm-ideas → identify-assumptions → ...
```

**Skill chain pipeline** — horizontal steps with `→` arrows, each step transitions
`none → running → done` with the accent green dot on active.

**Context file bar** — slim bar showing which brain files are loaded, provenance
color dot per file.

## States

- Active / selected: `--accent` left border or background tint
- Loading / running: pulsing `--accent` dot
- Done / complete: static `--accent` checkmark or dot
- Muted / empty: `--muted` text, dashed border

## What Not To Do

- No blue primary actions — accent is always `#3DDC84` green
- No stark white backgrounds — minimum `#0F1420`
- No rounded cards over `8px` radius — keep edges tight
- No emoji in UI chrome — only in brain content if user-authored
- Do not reuse provenance tag colors for status indicators or other UI elements
