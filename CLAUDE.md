# CLAUDE.md — Archos
# Framework version: v2.0 (bumped 2026-05-27 — adds discovery hierarchy, tiered H8, PARTIAL-RECOVERING H5, sector-conditional H10-extended)

## What is this project?

Archos is a personal investment research system that identifies sub-$5B
AI-infrastructure chokepoint stocks before the market discovers them.

The system is NOT a trading bot, NOT an automated execution engine, and
NOT a portfolio manager. It is a discovery and screening engine that
produces a ranked candidate list for human review and decision-making.

## Core thesis (derived from Leopold Aschenbrenner's "Situational Awareness")

The AI buildout is a concentrated 4-7 year capital mobilization pulling
forward a multi-decade industrialization into a tight window (~2024-2030).
Physical constraints (power, photonics, memory, packaging, networking,
cooling) create chokepoints where demand dramatically exceeds supply.
Sub-$5B pure-play companies sitting at these chokepoints can re-rate
20-100x when the market recognizes the constraint.

## Two-stage process: SCREEN then VET

**Stage 1 — Four-filter framework (signal classification)**
Finds candidates. Validated across 32 stocks, 3 research phases.

**Stage 2 — Due diligence checklist (adversarial vetting)**
Vets candidates. 6 sections. Required BEFORE any capital allocation.
See DUE_DILIGENCE_CHECKLIST.md.

Stage 2 includes a /last30days social signal sweep (Section 6) run
as a Code session. This surfaces paid promotion patterns, independent
verification of bear claims, management response quality, and whether
an organic bull case exists from credible independent capital.

A candidate must ACCEPT from Stage 1 AND CLEAR from Stage 2.
SHAZ passed all four filters in Stage 1 but scored 6/6 RED in
Stage 2 (counterparty insolvency, management self-dealing, DeFi
lender with insufficient capital, published short report with
verified claims, IPO underwriter selling shares while initiating
coverage, zero organic social bull case with confirmed paid
promotion). This is the calibration case for why both stages exist.

## The four-filter framework (validated across 32 stocks, 3 research phases)

Every candidate must pass ALL FOUR filters:

**H10 — Chokepoint-specific bellwether mention**
The stock's chokepoint was explicitly mentioned by NVDA / TSMC / AVGO /
Microsoft / Meta / AMD in the last 18 months. Two tiers:
- Vendor-level (bellwether names the company or invests directly) = strongest
- Category-level (bellwether names the chokepoint category) = screening trigger

**DISCOVERY HIERARCHY (added 2026-05-27, Framework v2.0):** The balance-sheet signal layer (deferred revenue spikes, customer deposit first-time appearances, backlog inflections) is the PRIMARY discovery layer. The bellwether mention (H10) is the CONFIRMATION layer that upgrades conviction tier, not the gate that permits entry. A candidate showing first-time deferred revenue buildup >$10M from a chokepoint-adjacent end-market qualifies for TIER 2 WATCH even without an H10 bellwether fire, provided H8 + H5 + H11 pass. The H10 fire upgrades it to TIER 1 / ACCEPT-track. This reflects the empirical finding that balance-sheet signals lead bellwether mentions by 1-3 quarters across the winner universe (SNDK, LEU, POWL, AEHR calibration cases).

**H8 (tiered, v2.0 — added 2026-05-27) — Market cap AND >50% AI-infrastructure revenue. Tiered by magnitude expectation:**
- **TIER 1 NANO: Sub-$500M.** Highest asymmetry (16-100x historical). Equity only (no liquid LEAPS at this cap). Position size $3-5K.
- **TIER 2 CATALYST: $500M-$2B.** Strong asymmetry (5-20x historical). LEAPS preferred where available. Position size $5-15K.
- **TIER 3 COMPOUNDER: $2B-$5B.** Moderate asymmetry (3-10x historical). LEAPS preferred. Position size $10-25K.
- **TIER 4 SEGMENT: $5B-$15B parent with an AI-infrastructure segment that is (a) >50% of segment revenue from AI-DC end-market AND (b) growing >40% YoY.** Parent cap waived; segment treated as synthetic standalone. Lower magnitude expectation (2-5x on parent, more on segment multiple expansion). LEAPS on parent. Position size per Tier 3 rules.

More than 50% of revenue must come from a single AI-infrastructure chokepoint end-market. The end-market test (not just product-line) remains — WOLF failed end-market (>50% EV/auto) despite passing product (100% SiC).

**H5 — IGNORED / NEUTRAL sentiment**
Pre-move sentiment classified as IGNORED-extreme, IGNORED, or NEUTRAL.
Dose-response: more extreme IGNORED → larger expected return magnitude.
PARTIAL = lower-magnitude candidate. LOVED = reject.

**H5 PARTIAL-RECOVERING classification (added 2026-05-27, Framework v2.0):** When a candidate transitions from IGNORED/NEUTRAL to PARTIAL on a single identifiable catalyst (contract announcement, bellwether mention, earnings beat), then retraces >25% from the post-catalyst peak without a thesis-breaking event (no going concern, no fraud disclosure, no contract cancellation), reclassify as PARTIAL-RECOVERING. This classification permits entry at reduced position size (50% of tier standard) with the understanding that magnitude expectation is PARTIAL-tier (50-265%) rather than IGNORED-tier (700-1,400%). The catalyst has validated the thesis; the pullback has restored the entry window. Re-eval trigger: if the name retraces to within 10% of pre-catalyst price with thesis intact, reclassify back to IGNORED and apply full position sizing.

**H11 — Balance-sheet survival**
Net debt / EBITDA < 5x, OR positive FCF runway > 18 months, OR no
going-concern qualification from auditors.

## Sector-Conditional Bellwether Extension (H10-extended) — added 2026-05-27 (Framework v2.0)

The four-filter framework's H10 bellwether list (NVDA/TSMC/AVGO/MSFT/META/AMD) applies to the AI Infrastructure lens. For parallel sector lenses, the following bellwether analogs apply:

**DEFENSE/SPACE — H10-D:** Binding contract award from DoD, NASA, DARPA, AFRL, Space Force, NRO, SDA, DIA, or named defense prime (Lockheed, Raytheon, Northrop, Boeing, L3Harris, General Dynamics) with disclosed dollar value. IDIQ ceiling alone does NOT qualify — funded task orders or firm-fixed-price awards required.

**NUCLEAR — H10-N:** NRC licensing milestone (construction permit, operating license, design certification), DOE Loan Programs Office commitment, or binding offtake from a utility/hyperscaler with disclosed MW and dollar value.

**CRITICAL MINERALS — H10-M:** DPA Title III designation, EXIM Board loan approval, DOE LPO commitment, DFARS deadline creating mandated domestic sourcing, or binding offtake from a defense prime or critical infrastructure operator.

**PHARMA/GLP-1 — H10-P:** FDA Breakthrough Therapy designation on a capacity-constrained modality, binding CDMO supply agreement with a top-10 pharma company, or Lilly/Novo/AstraZeneca named as customer with disclosed capacity commitment.

H8, H5, and H11 apply identically across all lenses. Only the bellwether identity changes. The DD checklist is lens-agnostic and applies to all candidates regardless of sector.

Evidence basis: Phase 4 universal discovery (N=61) confirmed that extended bellwether fires for 90% of the winner universe vs 48% for narrow NVDA-list only. The chokepoint LOGIC is universal; the bellwether IDENTITY is sector-conditional.

## Framework performance (backward-looking, as of 2026-05-21)

- 12/12 sensitivity within design-intent universe (100%)
- 0/10 false positives against adversarial controls (100% specificity)
- 1 known blind spot: legacy-industrial-capacity-pivot pattern (BW)
- 5 out-of-scope patterns documented (sector pivot, M&A pivot,
  pre-revenue moonshot, geopolitical materials, AI services)

## Key files

| File | Purpose |
|---|---|
| DUE_DILIGENCE_CHECKLIST.md | **MANDATORY** post-ACCEPT vetting. 6 sections (5 manual + 1 /last30days). |
| CHOKEPOINT_TAXONOMY.md | The load-bearing asset. 10 chokepoints, 14 pure-plays. Refreshed quarterly. |
| CANDIDATE_UNIVERSE.md | Current screening output. ACCEPT / WATCH / REJECT per candidate. |
| ARCHOS_RESEARCH_TEMPLATE.md | Per-candidate research template used during DD. |
| INSIGHTS.md | Compound knowledge. What worked, what didn't, pattern updates. |
| weekly-scan/runs/ | One .md per weekly master scan, dated. Raw output. Future runs land here. |
| research/pattern-discovery/ | Universal pattern discovery artifacts (Phase 4 winner universe + signal clusters + 25-dimension matrix). |
| research/bottleneck-phases/ | Pointer (README.md) to original 3-phase research canonically stored in _master_docs/bottleneck-asymmetry-research/. |
| content/ | Drafts and published essays / write-ups. Currently empty; ready for future use. |
| due-diligence/ | DD work per candidate. Includes last30days/ subfolder for social sweeps. |
| trades/ | One .md per position (when/if opened). Entry thesis, exit rules, post-mortem. |
| _archive/ | Obsolete or superseded files preserved for traceability (old screens/, old screening/, duplicate Builds nest, DISCOVERY_PROMPT.md). Not deleted. |

## Research lineage

All foundational research lives in:
`_master_docs/bottleneck-asymmetry-research/`

Key files (READ BEFORE any framework modification):
- PATTERN_MATRIX_v2.md — signal × stock matrix (8 winners, Phase 1 + Phase 3)
- CONTROL_MATRIX_v1.md — anti-pattern controls (10 non-winners, Phase 2)
- FRAMEWORK_STRESS_TEST.md — 2x2 synthesis with sensitivity/specificity
- EXPANDED_WINNERS_v1.md — Phase 3 expanded universe (12 new winners)
- TAXONOMY_UPDATE_v1.md — Phase 3 chokepoint taxonomy expansion
- HYPOTHESIS_EVOLUTION.md — full audit trail of H1-H13 across all phases

## Screening cadence

| Frequency | Action |
|---|---|
| Quarterly (after NVDA/TSMC/AVGO/MSFT/META/AMD earnings) | Re-parse transcripts. Update CHOKEPOINT_TAXONOMY.md. |
| Quarterly (after 13F deadlines: 2/15, 5/15, 8/15, 11/15) | Pull Situational Awareness LP 13F + specialist watchlist. |
| Monthly | Refresh sentiment state per candidate. ETF inclusion check. |
| Weekly | EdgarTools 8-K full-text search on candidate universe. |
| Daily (lightweight) | Market-cap monitor — flag if candidate breaches $5B. |

## Governance

- This project follows WORKING_PHILOSOPHY.md and DEBUGGING_PHILOSOPHY.md.
- Framework modifications require evidence from a structured research run
  (autoresearch pattern), not ad-hoc changes.
- No predictions. No trade recommendations from Code. Code produces
  signal classification; human makes position decisions.
- All screening runs are backward-looking analysis or forward signal
  classification. Never forward price prediction.
- **Every ACCEPT requires DUE_DILIGENCE_CHECKLIST.md before capital.**
  The four-filter framework finds candidates. The DD checklist vets them.
  Section 6 (/last30days social sweep) is a mandatory Code session per
  ACCEPT candidate. SHAZ is the calibration case for why all three
  layers (framework + DD checklist + social signal) are non-negotiable.
- **Real-time data verification is MANDATORY before writing any market
  cap, stock price, or valuation metric to a project file.** EdgarTools
  XBRL market caps are stale (confirmed multiple times — AXTI showed
  $273M when real was $4.5B). Training-data prices are often months or
  years old. Before any price, market cap, P/S ratio, or "sub-$5B"
  classification is committed to a .md file, the session MUST verify
  via Alpha Vantage, live web search, or equivalent real-time source.
  A file with stale pricing is worse than no file — it creates false
  confidence in outdated classifications. This rule applies to:
  CHOKEPOINT_TAXONOMY.md, CANDIDATE_UNIVERSE.md, all DD reports, all
  screening run outputs, and any file that references a company's
  current market cap or stock price.

## Tech stack

| Tool | Purpose |
|---|---|
| EdgarTools MCP (Pro tier) | 8-K/10-K/10-Q full-text search, insider Form 4, company briefs |
| LLMQuant MCP | 13F institutional holdings (when API is up; EdgarTools as fallback) |
| Alpha Vantage MCP | Live market cap cross-check (EdgarTools XBRL is stale) |
| Web search | Bellwether transcripts, analyst PTs, sentiment checks, ETF holdings |
| LunarCrush MCP | Social sentiment on micro-caps (coverage is thin; augment manually) |
| /last30days (Code skill) | Social signal sweep for DD Section 6. Covers Reddit, X, YouTube, TikTok, Instagram, Substack, HN. |
| Filesystem | Read/write project files on Mac |
