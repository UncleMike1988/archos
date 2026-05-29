# CLAUDE.md — Archos
# Framework version: v3.0 (bumped 2026-05-28 — DETECTION-AND-RANKING REFACTOR. Position-sizing logic REMOVED (operator-owned); H8(b) end-market reformulated from a hard gate into a graded INFLECTION signal; H10-extended promoted to co-primary with the discovery hierarchy folded into the four-filter section; the two-pronged TRAP CHECK is now the SOLE hard-reject layer; scoring is Pattern Strength + Trap Risk + Bull/Base/Bear + analog + Δ + ranking (see SCORING_SYSTEM.md). Authorized by research/FRAMEWORK_OVERFIT_AUDIT.md + Sounding Board 2026-05-28. v2.1 trap-detection walls (H11, meme/squeeze, fraud/counterparty) PRESERVED.)

## What is this project?

Archos is a personal investment research system that DETECTS asymmetric,
mispriced equity opportunities, PATTERN-MATCHES them against the
reverse-engineered signatures of prior parabolic winners, RANKS them, and
flags the TRAPS. It is "the Sherlock Holmes of finding potential
opportunities" — it surfaces real opportunities, scores how closely each
matches the winner signature, names each one's strengths and weaknesses, and
separates the real companies from the manufactured ones.

Archos's job is **detection + pattern-matching + ranking + trap-detection.**
It produces a ranked, scored dossier for human review (see SCORING_SYSTEM.md:
Pattern Strength + Trap Risk + Bull/Base/Bear + closest analog + Δ + rank).

The system does NOT size positions, recommend entries or exits, or manage
risk — **the operator (Michael) owns ALL of that.** It is NOT a trading bot,
NOT an automated execution engine, and NOT a portfolio manager. (This is the
v3.0 reframe: position-sizing and rejection logic had crept into what should
be a pure detection system — the overfit the audit caught. See
research/FRAMEWORK_OVERFIT_AUDIT.md.)

## Governing principle — find the mispricing, not the flawless company

**This is the CENTERPIECE of the framework, not a caveat.** We are NOT
screening for flawless companies. A flawless sub-$1B company doesn't exist —
if it were clean, growing, contracted, and uncovered, it wouldn't still be
sub-$1B. **No company has a perfect score pre-breakout.** The winners had
clusters of signals WITH weaknesses, not flawless scorecards. The flaws ARE
the entry point. The job is to find a real, specific reason a company
re-rates materially, score how strongly it matches the winner pattern, and
hand the operator a ranked dossier — they size the bet.

The audit proved this directly: the framework's own flagship winners —
**AXTI (97x), SNDK (44x), POWL (38x), BE (16x), AEHR (12x), LITE (10x)** —
would ALL have been REJECTED at their pre-discovery lows by the old strict
gates (they were diluted, near-going-concern, or had the chokepoint as a
fastest-growing *minority* end-market). That is why the system must
**score-and-rank, not gate-and-reject.** Reject ONLY on a TRAP (fraud,
manufactured-promotion-around-a-hollow-core, counterparty insolvency,
going-concern-to-zero, the meme/squeeze anomaly — the two-pronged Trap Check
below). Almost nothing else is a hard reject; every other flag is a graded
weakness in the Pattern Strength score, not a veto. (The thesis-breaking
TRAPS vs magnitude-lowering flags split is the Flag Taxonomy below.)

## Strategy buckets (assign FIRST)

Assign the bucket BEFORE judging the candidate. Applying one bucket's
discipline to another is a category error — judging a Bucket 3 nanocap on
Bucket 1 LEAPS-timing rules is the VLN calibration miss. The per-bucket
"Expectation" and instrument figures below are **magnitude descriptors**
(the historical return shape by cap and instrument — genuine
reverse-engineered signal), NOT position-sizing prescriptions. Archos
describes the bucket, instrument availability, and magnitude; **the operator
sizes** (v3.0 — sizing is operator-owned).

- **Bucket 1 — Large-cap LEAPS:** >$5B compounder, down 35%+ on overdone
  fear, still growing, low IV. Instrument: LEAPS. Expectation: ~2x equity /
  3x+ option on a partial recovery to PT. Template: NOW / CRM.
- **Bucket 2 — Chokepoint LEAPS:** sub-$5B chokepoint pure-play with a real
  edge. Instrument: LEAPS or equity. Expectation: 3-5x equity / ~10x option.
  **The four-filter framework (H10/H8/H5/H11) governs here** — the chokepoint
  thesis, two-stage SCREEN-then-VET process, and four-filter sections below
  are all Bucket 2 detail. Template: CLSK.
- **Bucket 3 — Nanocap AI-adjacent:** sub-$1B with a credible AI tailwind,
  2-3 year horizon. Instrument: equity (LEAPS illiquid at this cap).
  Expectation: 5-10x, basket-sized, higher variance. Template: VLN.

## Core thesis (derived from Leopold Aschenbrenner's "Situational Awareness")

The AI buildout is a concentrated 4-7 year capital mobilization pulling
forward a multi-decade industrialization into a tight window (~2024-2030).
Physical constraints (power, photonics, memory, packaging, networking,
cooling) create chokepoints where demand dramatically exceeds supply.
Sub-$5B pure-play companies sitting at these chokepoints can re-rate
20-100x when the market recognizes the constraint.

## Two-stage process: SCREEN then VET

**Stage 1 — Four-filter framework → Pattern Strength (detection + scoring)**
Surfaces candidates and SCORES them (Pattern Strength 0-100, SCORING_SYSTEM.md).
Validated across 32 stocks, 3 research phases + N=61 universal.

**Stage 2 — Due diligence checklist → Trap Risk (adversarial vetting)**
Vets candidates and produces the Trap Risk verdict (Clear/Caution/Kill) via the
two-pronged trap check. 6 sections. Required BEFORE any capital decision.
See DUE_DILIGENCE_CHECKLIST.md.

Stage 2 includes a /last30days social signal sweep (Section 6) run as a Code
session. This surfaces paid promotion patterns, independent verification of bear
claims, management response quality, and whether an organic bull case exists from
credible independent capital — Prong B of the trap check.

A candidate is RANKED by its Stage 1 Pattern Strength and carries its Stage 2 Trap
Risk alongside (never blended — a high score with a Kill is a "high score with a
kill-switch," parked in the REJECT log). SHAZ would SURFACE and score in Stage 1 but
was a **6/6 Kill** in Stage 2 (counterparty insolvency, management self-dealing, DeFi
lender with insufficient capital, published short report with verified claims, IPO
underwriter selling shares while initiating coverage, zero organic social bull case
with confirmed paid promotion). This is the calibration case for why both stages
exist — Stage 1 alone would have surfaced it.

## The four-filter framework — the core SCORED signals (validated across 32 stocks + N=61 universal)

**v3.0 reframe:** the four filters are NO LONGER pass/fail GATES. They are the four
heaviest inputs to the **Pattern Strength** score (SCORING_SYSTEM.md). A weak filter
LOWERS the score; it does not veto. The ONLY veto-carrying conditions inside the
four are the two TRAP walls — **H11 going-concern-to-zero** and **H5 LOVED-EXTREME**
— which route to Trap Risk = Kill (see Flag Taxonomy + SCORING_SYSTEM.md). Everything
else the four filters surface is a graded weakness, named in the dossier.

**H10 — Chokepoint-specific bellwether fire (the sector-conditional FAMILY)**
H10 is the sector-conditional bellwether family from the top — there is no
"narrow-first, extended-as-addendum" ordering anymore (the audit showed a literal
narrow-first reading kills ~11 extended-lens winners — PATTERN_MATRIX 48% narrow vs
90% extended). The bellwether IDENTITY is sector-conditional; the chokepoint LOGIC
is universal:
- **AI-Infrastructure lens:** NVDA / TSMC / AVGO / Microsoft / Meta / AMD.
- **Defense/Space lens (H10-D), Nuclear (H10-N), Critical Minerals (H10-M),
  Pharma/GLP-1 (H10-P), Government-equity (H10-G):** the sector analogs in the
  "Sector-Conditional Bellwether Family" section below.

Two tiers, scored (SCORING_SYSTEM.md signal #1): **vendor-level** (bellwether names
the company or invests directly / a binding sector-anchor award) = +20, strongest;
**category-level** (bellwether names the chokepoint category) = +10.

**DISCOVERY HIERARCHY (v2.0, retained + folded in here):** the balance-sheet signal
layer (deferred-revenue spikes, customer-deposit first-time appearances, backlog
inflections) is the **PRIMARY discovery layer** — it is what SURFACES a name. The
H10 bellwether fire is the **CONFIRMATION layer that raises Pattern Strength, not a
gate that permits surfacing.** A candidate with a first-time chokepoint
deferred-revenue / customer-deposit signal >$10M SURFACES even without an H10 fire
(it scores on signals #4/#5 and goes on the ranked watchlist); when the H10 fire
arrives, signal #1 flips category→vendor and the score JUMPS (the biggest Δ-driver).
Empirical basis: balance-sheet signals lead bellwether mentions by 1-3 quarters
across the winner universe (SNDK, LEU, POWL, AEHR calibration cases).

**H8(a) — Cap geometry (magnitude descriptor + Pattern Strength signal #3).** Cap
brackets describe historical return MAGNITUDE by size (genuine reverse-engineered
signal: smaller = bigger re-rate). They are NOT sizing prescriptions — Archos does
not size (v3.0). Instrument availability is a fact (no liquid LEAPS sub-$500M), also
a descriptor, not a directive.
- **TIER 1 NANO: Sub-$500M.** Highest historical magnitude (16-100x). Equity only
  (no liquid LEAPS at this cap).
- **TIER 2 CATALYST: $500M-$2B.** Strong historical magnitude (5-20x). LEAPS often
  available.
- **TIER 3 COMPOUNDER: $2B-$5B.** Moderate historical magnitude (3-10x). LEAPS
  available.
- **TIER 4 SEGMENT: $5B-$15B parent** whose chokepoint-sector segment (a) is the
  inflecting majority of segment revenue from the chokepoint end-market AND (b) is
  growing >40% YoY. Parent cap waived; segment treated as a synthetic standalone.
  Lower historical magnitude (2-5x on parent, more on segment multiple expansion).

**H8(b) — End-market INFLECTION (Pattern Strength signal #4 — NOT a gate; CHANGE 3).**
The old hard ">50% of trailing revenue from a single AI-DC end-market" gate is
RETIRED — it scored the LEVEL and ignored the DERIVATIVE, and so rejected AXTI
(~15-25% AI-DC at low), SNDK (~13%), POWL (~15%), BE (~30%), AEHR (~10-15%), LITE
(telecom-majority) at their lows. Replaced with a GRADED inflection signal:

- The signal fires **STRONG** when the chokepoint SECTOR's anchor end-market is the
  **fastest-growing** end-market AND one of: (i) >X% of incremental/forward
  (next-2-quarter or contracted) revenue, OR (ii) a first-time chokepoint
  deferred-revenue / customer-deposit signal >$10M (the v2.0 PRIMARY discovery
  layer). It need NOT be >50% of trailing total.
- The "**inflecting toward dominance**" growth guardrail is REQUIRED — it is what
  distinguishes **AXTI-inflecting (STRONG, +16)** from **Anritsu/MIR/Sumitomo
  diluted-and-FLAT (WEAK, +0 to +6)**. A diluted end-market that is NOT the
  fastest-growing slice is a weak signal, **not a reject**.
- The end-market string is **the chokepoint SECTOR's anchor end-market** —
  generalized from "AI-DC" so nuclear/DOE (LEU), defense-gov (PL/RKLB),
  critical-minerals-strategic, AI-DC, and pharma all read on the right axis (H10 got
  sector-conditional treatment in v2.0; H8(b) now matches).

This is the highest-value Sherlock signal: small-but-inflecting chokepoint share +
balance-sheet confirmation. WOLF (>50% EV/auto, flat) is still correctly held — by
the growth guardrail AND independently by H11 going-concern; the inflection signal
catches no adversarial control on its own, so loosening the old gate costs zero
specificity.

**H5 — IGNORED / NEUTRAL sentiment (Pattern Strength signal #2, dose-response)**
Pre-move sentiment scored on a dose-response sub-scale: IGNORED-extreme +20 ·
IGNORED +16 · NEUTRAL +12 · PARTIAL-RECOVERING +8 · PARTIAL +6 · LOVED 0. More
extreme IGNORED → larger historical magnitude. **Only LOVED-EXTREME is a TRAP wall**
(parabolic, retail-driven, at or above the cap fundamentals justify → Trap Risk =
Kill / removed from the ranked field — the upside is gone). Plain LOVED and PARTIAL
are NOT rejects — they are graded, magnitude-lowering, scored not vetoed (the Wonik
calibration miss was treating an H5 PARTIAL as a reject).

**H5 PARTIAL-RECOVERING classification (v2.0, retained):** When a candidate
transitions from IGNORED/NEUTRAL to PARTIAL on a single identifiable catalyst
(contract announcement, bellwether mention, earnings beat), then retraces >25% from
the post-catalyst peak without a thesis-breaking event (no going concern, no fraud
disclosure, no contract cancellation), classify as PARTIAL-RECOVERING (signal #2 =
+8; magnitude expectation PARTIAL-tier 50-265% rather than IGNORED-tier 700-1,400%).
The catalyst has validated the thesis; the pullback has restored the entry window.
Re-score trigger: if the name retraces to within 10% of the pre-catalyst price with
thesis intact, reclassify back to IGNORED (+16). (Sizing off this classification is
the operator's call — Archos scores, does not size.)

**H11 — Balance-sheet survival (TRAP wall — preserved, do NOT loosen)**
Net debt / EBITDA < 5x, OR positive FCF runway > 18 months, OR no going-concern
qualification from auditors. **H11 going-concern-to-zero is the kill line** (Trap
Risk = Kill — EOSE, WOLF-pre). This is the one filter that independently catches an
adversarial control (WOLF-pre) and is audit-confirmed correct-strictness. Degrees of
balance-sheet quality SHORT of going-concern (some dilution, serial ATM, modest
leverage) are graded weaknesses, not vetoes.

## Sector-Conditional Bellwether Family (H10) — CO-PRIMARY (v3.0; was "extension" in v2.0)

**This IS the H10 definition (v3.0 — no longer an addendum below the four-filter
section).** The AI-infra list (NVDA/TSMC/AVGO/MSFT/META/AMD) is ONE lens of the
family, not the primary gate. A literal narrow-first reading killed ~11 extended-lens
winners (PL/RKLB/LEU/OKLO/SMR/USAR/NNE + biotech) at their lows; promoting the family
to co-primary admits NO adversarial control (the controls are AI-infra mega-caps,
unaffected by extended bellwethers — zero specificity cost). For parallel sector
lenses the bellwether analogs are:

**DEFENSE/SPACE — H10-D:** Binding contract award from DoD, NASA, DARPA, AFRL, Space Force, NRO, SDA, DIA, or named defense prime (Lockheed, Raytheon, Northrop, Boeing, L3Harris, General Dynamics) with disclosed dollar value. IDIQ ceiling alone does NOT qualify — funded task orders or firm-fixed-price awards required.

**NUCLEAR — H10-N:** NRC licensing milestone (construction permit, operating license, design certification), DOE Loan Programs Office commitment, or binding offtake from a utility/hyperscaler with disclosed MW and dollar value.

**CRITICAL MINERALS — H10-M:** DPA Title III designation, EXIM Board loan approval, DOE LPO commitment, DFARS deadline creating mandated domestic sourcing, or binding offtake from a defense prime or critical infrastructure operator.

**PHARMA/GLP-1 — H10-P:** FDA Breakthrough Therapy designation on a capacity-constrained modality, binding CDMO supply agreement with a top-10 pharma company, or Lilly/Novo/AstraZeneca named as customer with disclosed capacity commitment. (Biotech note: H10-P fires only for PRE-STAMPED designations/partners — CELC via FDA BT. Unpartnered Phase-3 winners like ABVX are a structurally uncatchable different-pattern binary-readout class; this is an ACCEPTED blind spot. Do NOT loosen H10-P to admit unpartnered names — it would admit clinical-microcap noise.)

**GOVERNMENT-EQUITY — H10-G:** a direct US-government equity stake / preferred investment / strategic anchor purchase (DoD preferred, DPA Title III equity, sovereign-fund stake) with disclosed dollar value. Established as its own class from the MP/government-equity lesson (INSIGHTS); the government-as-buyer-of-equity is a vendor-level-equivalent fire.

H8(a) cap geometry, H8(b) end-market inflection (sector-generalized — the anchor end-market is the chokepoint SECTOR's, not literally "AI-DC"), H5, and H11 apply identically across all lenses. Only the bellwether identity changes. The DD checklist is lens-agnostic and applies to all candidates regardless of sector.

Evidence basis: Phase 4 universal discovery (N=61) confirmed that extended bellwether fires for 90% of the winner universe vs 48% for narrow NVDA-list only. The chokepoint LOGIC is universal; the bellwether IDENTITY is sector-conditional.

## Flag Taxonomy — TRAPS (hard reject) vs magnitude-lowering (graded score input) (v3.0)

The governing principle made operational. Every flag is one of two kinds: it is
either a **TRAP** (hard reject → Trap Risk = Kill, removed from the ranked field) or
a **magnitude-lowering flag** (a graded weakness that LOWERS the Pattern Strength
score, never a veto). v3.0 NARROWS the hard-reject set to the traps ONLY — almost
nothing else is a reject. The TRAP check is the two-pronged authenticity/promotion
test (SCORING_SYSTEM.md + DD checklist).

**TRAPS → Trap Risk = Kill (the SOLE hard-reject layer):**
- Manufactured promotion AND hollow substance (the two-pronged Kill — SPAI/PPSI/SHAZ class)
- Counterparty insolvency or contract cancellation [SHAZ ESDS] — DD §2 RED
- Fraud / self-dealing / restatement — DD §1 RED
- Fabricated / non-existent chokepoint (hollow substance, Prong A)
- Meme/squeeze structural anomaly: float <20% + borrow >50% + zero bellwether + zero gov-contract + minimal revenue (SIGNAL_CLUSTERS Cluster 8 — RGC, SHAZ)
- Going-concern-to-zero / H11 fail [EOSE, INV, WOLF-pre]
- H5 LOVED-EXTREME: parabolic, retail-driven, at/above the cap fundamentals justify (magnitude veto — the upside is gone)

**MAGNITUDE-LOWERING → graded Pattern Strength input, NOT a reject:**
- **Diluted / flat chokepoint end-market — the OLD ">50% majority" fail. RETIRED as a veto (CHANGE 3): now a graded H8(b) inflection signal (+0 to +6 if not the fastest-growing slice), NOT a reject.** [Anritsu/Sumitomo/MIR — held at low rank, not deleted]
- Structural (not cyclical) revenue decline [NVO] — craters the inflection signals (#4/#6) and the winner-pattern match → near-floor Pattern Strength; it ranks at the bottom on its own, no separate veto needed
- Already ran / near 52-wk high with real runway left (H5 PARTIAL)
- Some dilution / serial ATM, absent going-concern
- Thin or near-PT analyst coverage
- One soft quarter, no thesis break
- Net insider selling — modal (killed-H3); at most a minor weakness, never a veto
- RED on DD §5 (valuation) only [AEHR]

**Rule:** reject ONLY on a TRAP. Otherwise flags set the Pattern Strength score →
the operator sizes off the score + Bet Shape + Trap Risk. Never pass on a *stack* of
magnitude-lowering flags — a pile of graded weaknesses is a LOW SCORE, not a Kill.
This NARROWS what counts as a reject; it removes zero traps (going-concern/H11, DD
§1/§2 RED, counterparty/fraud, meme/squeeze Cluster 8, LOVED-EXTREME all still Kill).

## Framework performance (backward-looking; corrected by the overfit audit 2026-05-28)

- **The old "12/12 = 100% sensitivity" claim does NOT hold and is RETIRED.** The
  overfit audit (research/FRAMEWORK_OVERFIT_AUDIT.md, N=25 winners scored cold at
  their pre-discovery lows) split the metric honestly:
  - **DISCOVERY sensitivity ~88%** — IGNORED + sub-cap + balance-sheet signals
    SURFACE ~88% of historical winners. The discovery engine is excellent.
  - **Old ACCEPT-track sensitivity 8-21%** — the strict gates then REFUSED to size
    them (8% literal / 21% intended). This is the overfit the v3.0 refactor fixes:
    the leak lived in the ACCEPT/SIZING gates, not the discovery engine.
  - **v3.0 scoring restores effective sensitivity to ~92%** (audit Reading C) by
    replacing the gates with graded signals (the H8 inflection signal alone recovers
    most of it) — without touching specificity.
- **Specificity unchanged: 0/10 false positives against adversarial controls (100%).**
  The trap walls (H11 going-concern, meme/squeeze Cluster 8, fraud/counterparty,
  LOVED-EXTREME) still reject all 10 controls; the v3.0 changes admit none of them.
- 1 known blind spot: legacy-industrial-capacity-pivot pattern (BW).
- Documented out-of-scope / different-pattern classes: sector pivot, M&A pivot,
  pre-revenue moonshot (caught via scoring, not gated out), geopolitical materials,
  AI services, and **unpartnered Phase-3 biotech** (binary-readout class — accepted
  blind spot; do NOT loosen H10-P).

## Key files

| File | Purpose |
|---|---|
| SCORING_SYSTEM.md | **The scorecard the operator reads (v3.0).** Pattern Strength (0-100, hit-rate-weighted) + Trap Risk (Clear/Caution/Kill) + Bull/Base/Bear + closest analog + Δ + ranking + canonical dossier format. |
| DUE_DILIGENCE_CHECKLIST.md | **MANDATORY** vetting. 6 sections (5 manual + 1 /last30days). Houses the two-pronged Trap Check + §7 re-scoring protocol. |
| CHOKEPOINT_TAXONOMY.md | The load-bearing asset. 10 chokepoints, 14 pure-plays. Refreshed quarterly. |
| CANDIDATE_UNIVERSE.md | Current screening output — the ranked, scored dossier (Pattern Strength + Trap Risk per candidate). Kills parked in the REJECT log. |
| ARCHOS_RESEARCH_TEMPLATE.md | Per-candidate research/publication template, aligned to the v3.0 dossier/scorecard format. |
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
- No predictions. No trade recommendations from Code. **No position sizing —
  the operator owns ALL sizing, entry, exit, and risk management (v3.0).** Code
  produces detection + Pattern Strength + Trap Risk + Bull/Base/Bear + ranking;
  the human makes ALL position decisions.
- All screening runs are backward-looking analysis or forward signal
  classification. Never forward price prediction.
- **Any candidate the operator considers for capital requires
  DUE_DILIGENCE_CHECKLIST.md first** — including the two-pronged Trap Check and the
  mandatory Section 6 (/last30days social sweep) Code session. The framework +
  Pattern Strength scoring finds and ranks candidates; the DD checklist runs the
  trap check that produces Trap Risk (Clear/Caution/Kill). SHAZ is the calibration
  case for why all three layers (framework + DD checklist + social signal) are
  non-negotiable — it scored high enough to surface but was a 6/6 Kill.
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
