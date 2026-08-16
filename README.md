# OERA — Organizational Entrepreneurial Readiness Assessment

A generic model — **Direction → Enable → Discover → Act → Learn & Scale** — for assessing whether an organization has the conditions to identify opportunities, experiment under uncertainty, learn from evidence, and scale successful change. Built for the Organizational Innovation course, RUNI MBA, and applied here to a real partner organization.

**Live tool:** enable GitHub Pages on this repo (Settings → Pages → Deploy from branch `main` / root) to get a shareable link, or just open `index.html` locally in a browser.

## What this is

Two ideas merged into one instrument:

1. **The generic OERA model** (5-stage model logic, Maturity/Importance-style dual rating, Priority = Importance × (5 − Maturity) scoring, polished assessment UI) — a reusable, organization-agnostic readiness framework.
2. **A tailored innovation-capacity model** for the assignment's partner organization, Israel Trauma Coalition (ITC), modeled on the mechanic behind [Idit Biton's Organizational Innovation Map](https://innovationmap.iditbiton.com) (current state vs. target state per question, gap-driven findings).

Rather than running two separate instruments, each of OERA's 5 generic stages is instantiated here by one applied, evidence-grounded capability:

| Stage | Applied capability | What it probes |
|---|---|---|
| **Direction** | Anticipatory Innovation | Whether leadership plans proactively for future demand shifts, or only reacts in crisis mode |
| **Enable** | Risk Tolerance & Psychological Safety | Whether the org can safely pilot and fail small — a precondition for any recommended change |
| **Discover** | Ecosystem Stability | Whether partnerships hold up under competitive pressure (e.g. post–Oct 7 funding surges/talent competition) |
| **Act** | Scalability ("Accordion") | Whether IT infrastructure and procedures can expand and contract rapidly during emergencies without breaking |
| **Learn & Scale** | Knowledge Management | Whether specialized trauma expertise is captured and transferred, not lost, as staff are rapidly re-tasked |

Each capability has 3 questions (15 total). Full question text lives in `index.html`.

This keeps the assignment's requirement to design and justify a custom model (drawing on INSA/the Innovation Map/other sources as inspiration, not adopting any one wholesale) while still being able to point to a defensible, general theoretical backbone.

## Scoring logic

- **Priority score per question/capability:** Target × (5 − Current) — high-target, low-current capabilities rise to the top (same logic as OERA's Importance × (5 − Maturity), translated into current/target terms)
- **Stakeholder divergence flag:** a spread of ≥ 1.5 points between HQ Leadership, Regional Field Coordinators, and Member NGO Leaders on the same capability — the "does leadership's story match the field's reality" check

## How to use it at the hackathon / with real respondents

1. Each respondent opens the page, selects their role, and rates all 15 questions (Current + Target).
2. On submit, the tool saves the response locally in the browser **and** downloads a JSON file — send that file to whoever is compiling results (e.g. the team's Evidence Lead).
3. On the **View Results & Compare** tab, upload everyone's exported JSON files together. The tool aggregates across all of them, computes per-dimension averages, gaps, and role-divergence, and renders the current-vs-target radar chart.

No data is transmitted anywhere — everything runs client-side in the browser. Nothing is stored on a server, which matters given the assignment's explicit instruction not to put confidential/clinical/personal information about ITC into public tools. (This isn't an AI tool at all — it's a static form — but the same caution applies to whatever respondents type into it.)

## AI use disclosure

This tool's structure, question set, and scoring logic were drafted with AI assistance (Claude) as part of the course's permitted AI use, then reviewed and adapted by the team. Full prompt/decision log lives in the assignment's AI Use Appendix, not in this repo.
