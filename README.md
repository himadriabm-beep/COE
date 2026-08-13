# Building the Center of Excellence

A single self-contained `index.html` companion site to the white paper *"Building the Center of Excellence,"* covering all 13 sections end to end:

1. **The operating model triad** — Practice vs. GCC/GBS vs. Center of Excellence, how they work in tandem, and the benefits of a CoE.
2. **The CoE landscape** — technology, functional, and strategic CoE types, with AI/GenAI, Program & Portfolio Management, and Data & Analytics as running examples throughout.
3. **Setting up a CoE** — a vision statement template, key stakeholders, and signature deliverables per CoE.
4. **Resourcing the CoE** — four resourcing models and their trade-offs.
5. **Governance and cadence** — a tabbed view of the forum/frequency/purpose model for each of the three example CoEs.
6. **Core activities, OKRs/KPIs and reporting** — the six activities every CoE runs, and sample KPIs per CoE.
7. **Knowledge management** — explicit vs. tacit knowledge, and the five-stage knowledge lifecycle.
8. **Beyond the basics** — the Crawl/Walk/Run/Fly maturity model, funding models, anti-patterns, and the CXO value narrative.
9. **People management** — roles, time commitment, competency/career framework, and retention & succession.
10. **Change management** — the adoption curve and how to handle common resistance patterns.
11. **Building awareness** — an internal marketing campaign for the CoE: the awareness funnel, channel mix, and a sample 90-day launch plan.
12. **Scalability and adaptability** — scaling triggers, governing multiple CoEs, and resilience to organizational change.
13. **Closing perspective.**

No build step, no dependencies — plain HTML/CSS/JS (Google Fonts via CDN link, fine on GitHub Pages). Visually matches the design system used in the companion [Business User Journey Flow](https://github.com/himadriabm-beep/Business-User-Journey---Requirement-to-Prototype) site — same palette, type system (Space Grotesk / IBM Plex Sans / IBM Plex Mono), and card/chip/flow components — for a consistent look across projects.

## Publish on GitHub Pages

1. Add this `index.html` to the root of a repo (file name must be exactly `index.html`).
2. Repo → Settings → Pages → Source: "Deploy from a branch" → `main` / `(root)` → Save.
3. Live in about a minute at `https://<username>.github.io/<repo>/`.

## Editing content

Everything renders from JS data arrays inside the single `<script>` tag at the bottom of `index.html` — no HTML to hand-edit for content updates:

| Section | Data array | Notes |
|---|---|---|
| 01 Triad | `triad` | 3 cards: Practice, GCC/GBS, CoE |
| 01 Benefits | `benefits` | Chip row |
| 02 Landscape | `landscape` | 3 category cards |
| 03 Stakeholders | `stakeholders` | Chip row |
| 03 Deliverables | `deliverables` | 3 cards, one per example CoE |
| 04 Resourcing | `resourcing` | 4 model cards (how / fit / trade-off) |
| 05 Governance | `governance` | Object keyed by CoE name → array of `[forum, frequency, participants, purpose]` rows; renders as tabs |
| 06 Activities | `activities` | Chip row |
| 06 KPIs | `kpis` | 3 cards (objective + KPI list) |
| 07 Knowledge lifecycle | `kmFlow` | 5-stage flow with arrows |
| 08 Maturity | `maturity` | 4-stage tracker (Crawl/Walk/Run/Fly) |
| 08 Funding | `funding` | Chip row |
| 08 Anti-patterns | `antipatterns` | Objection-style cards |
| 09 Roles | `roles` | Table rows `[role, time commitment, responsibility]` |
| 10 Adoption curve | `adoption` | 3-stage tracker |
| 10 Resistance | `resistance` | Objection/response cards |
| 11 Awareness funnel | `funnel` | 4-stage flow with arrows |
| 11 Channels | `channels` | Table rows `[channel, cadence, best for]` |
| 11 90-day campaign | `campaign90` | 3-stage tracker |
| 12 Scaling triggers | `scaling` | Table rows `[signal, likely response]` |

The section navigation pills at the top (`sections` array) are generated automatically from the same 13-section list and highlight as you scroll.

Edit the relevant array and the page re-renders automatically — no other markup needs to change. The three-column card grids reflow to a single column below 900px automatically.


## About

Companion site to the white paper *"Building the Center of Excellence,"* covering the operating model triad (Practice / GCC-GBS / CoE), CoE types, setup, resourcing, governance, KPIs, knowledge management, maturity, people, change management, internal awareness campaigns, and scalability — with AI/GenAI, Program & Portfolio Management, and Data & Analytics CoEs as running examples throughout.
