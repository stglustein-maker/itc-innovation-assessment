# ITC Innovation Assessment

A tailored organizational innovation & change-capacity assessment tool built for the **Israel Trauma Coalition (ITC)** partner-organization project — Organizational Innovation course, RUNI MBA.

**Live tool:** enable GitHub Pages on this repo (Settings → Pages → Deploy from branch `main` / root) to get a shareable link, or just open `index.html` locally in a browser.

## What this is

Modeled on the mechanic behind [Idit Biton's Organizational Innovation Map](https://innovationmap.iditbiton.com) (the INSA-based assessment tool demonstrated in class): every question is rated twice — **Current state** and **Target state**, both 1–5 — so the gap between them becomes the actual finding, not just a raw score.

This version is scoped to a custom 5-dimension model built specifically for ITC, rather than the full 15-dimension INSA instrument, per the assignment's requirement to design and justify your own model (drawing on INSA/the Innovation Map as inspiration, not adopting them wholesale).

## The model

| Dimension | What it probes |
|---|---|
| **Ecosystem Stability** | Whether ITC's member-NGO partnerships hold up under competitive pressure (e.g. post–Oct 7 funding surges/talent competition) |
| **Scalability ("Accordion")** | Whether IT infrastructure and procedures can expand and contract rapidly during emergencies without breaking |
| **Knowledge Management** | Whether specialized trauma expertise is captured and transferred, not lost, as staff are rapidly re-tasked |
| **Anticipatory Innovation** | Whether leadership plans proactively for future demand shifts, or only reacts in crisis mode |
| **Risk Tolerance & Psychological Safety** | Whether the org can safely pilot and fail small, which determines whether any recommended Minimum Viable Change is actually feasible |

Each dimension has 3 questions (15 total). Full question text lives in `index.html`.

## Scoring logic

- **Innovation barrier flag:** a dimension's average Current score < 3.0, **or** its Current→Target gap ≥ 1.5
- **Stakeholder divergence flag:** a spread of ≥ 1.5 points between HQ Leadership, Regional Field Coordinators, and Member NGO Leaders on the same dimension — this is the "does leadership's story match the field's reality" check

## How to use it at the hackathon / with real respondents

1. Each respondent opens the page, selects their role, and rates all 15 questions (Current + Target).
2. On submit, the tool saves the response locally in the browser **and** downloads a JSON file — send that file to whoever is compiling results (e.g. the team's Evidence Lead).
3. On the **View Results & Compare** tab, upload everyone's exported JSON files together. The tool aggregates across all of them, computes per-dimension averages, gaps, and role-divergence, and renders the current-vs-target radar chart.

No data is transmitted anywhere — everything runs client-side in the browser. Nothing is stored on a server, which matters given the assignment's explicit instruction not to put confidential/clinical/personal information about ITC into public tools. (This isn't an AI tool at all — it's a static form — but the same caution applies to whatever respondents type into it.)

## AI use disclosure

This tool's structure, question set, and scoring logic were drafted with AI assistance (Claude) as part of the course's permitted AI use, then reviewed and adapted by the team. Full prompt/decision log lives in the assignment's AI Use Appendix, not in this repo.
