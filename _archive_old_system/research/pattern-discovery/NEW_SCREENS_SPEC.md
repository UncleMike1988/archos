# NEW_SCREENS_SPEC.md — Draft Screen Prompts from Phase 3 Universal Discovery

**Date:** 2026-05-26
**Companion files:** WINNER_UNIVERSE.md, PATTERN_MATRIX_UNIVERSAL.md, SIGNAL_CLUSTERS.md, batch1-5_*.md

This document specifies the new screens that the Phase 3 universal pattern discovery surfaced. Each screen is mapped to a Phase 3 signal cluster, has its information gap defined, and includes a draft SCREEN_PROMPT structure ready for operationalization.

For format and integration conventions, see `archos/screens/SCREENS_README.md`.

---

## NEW SCREEN #7 — CUSTOMER DEPOSIT SPIKE SCREEN

**Status:** PROPOSED — highest priority new build
**Information gap closed:** balance-sheet demand-confirmation 1-3 quarters BEFORE the public earnings catalyst. Government contract prepayments, hyperscaler advance commitments, and Big Pharma milestone payments all surface as deferred revenue or customer-advances on the 10-Q balance sheet at least one quarter before they translate into recognized revenue.
**Source cluster:** Cluster 4 (Gov Contract Anchor) + cross-applies to Cluster 2 (Squeeze-Amplified Inflection)
**Hit rate basis:** 22/61 = 36% univ; 9/13 = 70% in DEF/SPACE/NUKE/QC
**Cadence:** Monthly (run on 20th — captures trailing 10-Q filings within the standard 45-day deadline window)
**Tooling:** EdgarTools `filing_section` on 10-Q balance sheet; XBRL extraction for "DeferredRevenue" + "AdvancesFromCustomers" + "ContractLiabilities"; parallel evaluation against the prior 4 quarters per filer

### Draft SCREEN_PROMPT

```
OBJECTIVE:
Surface sub-$5B US-listed companies where deferred revenue or
customer advances on the balance sheet increased >50% quarter-over-
quarter in the most recently filed 10-Q. The thesis: gov-contract
prepayments + hyperscaler/Apple advance commitments + Big Pharma
milestone payments surface on the balance sheet 1-3 quarters before
recognized revenue, giving a screen-able demand-confirmation signal.

METHOD:
1. UNIVERSE: Pull all 10-Q filings in the last 60 days with mkt cap < $5B
   (Alpha Vantage cross-check; EdgarTools XBRL stale).
2. EXTRACT: For each filer, pull the most recent 10-Q + the prior 4 10-Qs.
   Use XBRL tags: us-gaap:DeferredRevenueCurrent,
   us-gaap:DeferredRevenueNoncurrent, us-gaap:CustomerAdvancesCurrent,
   us-gaap:ContractWithCustomerLiabilityCurrent,
   us-gaap:ContractWithCustomerLiabilityNoncurrent.
3. CALCULATE: QoQ change for total deferred revenue + customer advances.
   Flag any filer with >50% QoQ increase.
4. CROSS-CHECK: For each flagged filer, scan 10-Q MD&A for the SOURCE of
   the increase. Acceptable sources:
   - Government contract advance / progress payment (DoD/DOE/NASA/etc.)
   - Hyperscaler capacity reservation (NVDA/MSFT/META/AMZN/GOOG/ORCL)
   - Strategic customer prepayment (Apple/Tesla/Big Pharma)
   - Multi-year contract advance (>$10M and >18-month term)
5. EXCLUDE: routine subscription/SaaS deferred revenue smoothing (where
   the increase is a function of new ARR, not chokepoint prepay).
6. SCORE: each hit on H10-extended (chokepoint bellwether named in MD&A?),
   H8 (sub-$5B?), H5 (sentiment IGNORED/NEUTRAL?), H11 (no going-concern?).

OUTPUT:
- Ticker, mkt cap, QoQ deferred-rev change %, source of spike, H10/H8/H5/H11 quick-score
- Route 4/4 passes to CANDIDATE_UNIVERSE.md WATCH
- Route 2-3/4 passes to next-cadence re-eval queue
- 0-1/4 passes auto-REJECT

TEST CASE:
LEU Q3 2024 10-Q: $189.8M deferred revenue + $32.8M customer advances —
the screen should fire CLEANLY and confirm via DOE bellwether mention in
MD&A. If LEU 2024 retroactive run DOES NOT fire, the screen logic needs
refinement.

OKLO Q1 2026 10-Q: Meta + Equinix prepayments — should fire as second
calibration case (also passes H10 extended via Meta vendor-level).

ATRO FY2024 10-K: record backlog $633.4M, book-to-bill 1.11x — should
fire on the contract-liability line item.
```

---

## NEW SCREEN #8 — DE-SPAC REANIMATION TIMING SCREEN

**Status:** PROPOSED
**Information gap closed:** entry-timing precision for the "abandoned de-SPAC reanimation" pattern. Once a de-SPAC clears its 24-month-post-merger window, sponsor lockup pressure resolves, PIPE warrants exit, and the chart bottom becomes "discoverable" — but ONLY survivors with growing gov/strategic backlog continue to re-rate.
**Source cluster:** Cluster 1 (Abandoned De-SPAC Reanimation)
**Hit rate basis:** 19/61 = 31% univ; 7-8/13 = 60%+ in DEF/SPACE/NUKE/QC
**Cadence:** Quarterly (run after 13F deadlines: 2/15, 5/15, 8/15, 11/15) — combine with Aschenbrenner 13F pull and bellwether sweep
**Tooling:** Maintain a master spreadsheet of all US-listed de-SPAC completions (sourced from S-4/F-4 effectiveness filings) with merger date, current ticker, current cap. EdgarTools for 10-Q + 10-K snapshots.

### Draft SCREEN_PROMPT

```
OBJECTIVE:
Surface US-listed de-SPACs at 24-36 months post-merger with sub-$2B
cap AND IGNORED-extreme sentiment AND government-contract or chokepoint-
bellwether catalyst within the last 6 months. The thesis: SPAC redemption
pressure has resolved, sponsor lockups expired, PIPE warrants shaken out
— this is the structural entry-timing window where chart-bottomed
de-SPACs with REAL gov/strategic momentum re-rate violently.

METHOD:
1. UNIVERSE: maintain a master list of US de-SPAC completions in the
   2021-2023 window (merger date 24-36 months ago relative to screen run).
   Source: S-4/F-4 effectiveness filings + Form 25 SPAC delisting +
   SPACInsider / SPACTrack archives.
2. FILTER: market cap < $2B as of screen run (Alpha Vantage live; EdgarTools
   XBRL stale).
3. SENTIMENT FILTER: stock trading below 50% of post-de-SPAC ATH; analyst
   coverage thin (<= 3 sell-side analysts) OR price-target consensus
   declining; 10-Q risk factor language not LOVED-narrative-heavy.
4. CATALYST CROSS-CHECK: scan 8-Ks in the trailing 180 days for any of:
   - Government contract award >$10M (any single contract OR cumulative
     across 12 months)
   - Bellwether-extended partnership announcement (NVDA/MSFT/GOOG/META/AMZN/
     ORCL/CoreWeave + DoD/NASA/DOE/Treasury/EXIM + Big Pharma + Apple/Tesla/
     Lockheed)
   - Strategic equity investment from same bellwether list
5. EXCLUDE: any de-SPAC with going-concern qualifier in most recent 10-K
   (H11 fail) OR any with auditor non-reliance language (H11 quality fail).
6. SCORE: each hit on H10-extended, H8, H5, H11. Score Customer Deposit
   Spike (Screen #7) overlay if recent 10-Q shows deferred-rev jump.

OUTPUT:
- Ticker, de-SPAC merger date, months-since-merger, current cap, trailing
  catalyst, H10/H8/H5/H11 quick-score, Customer Deposit overlay (Y/N)
- Triple-firers (H10ext + H8 + H5 + H11 + customer-deposit) → TIER 2 promotion
- Singles/doubles → WATCH for next-cycle re-eval

TEST CASES:
- RKLB at Aug 2024 (36 months post-Vector Acquisition merger): de-SPAC
  TIMING fires, sub-$2.5B at low, IGNORED narrative, SDA $515M + Space
  Force $816M = govt anchor — should be TIER 2 ACCEPT.
- QBTS at Apr 2024 (28 months post-DPCM merger): screen should fire with
  $300M cap + 14% SI + Carahsoft govt aggregator + CHIPS LOI.
- PL at Dec 2024 (36 months post-dMY-IV merger): should fire on NRO/NGA/
  NASA federal majority revenue.

EXCLUSION CASES:
- Sector-pivot blind-spot names (HIVE / BITF / CLSK / RIOT / KEEL / EVTV /
  AlphaTON / Bitzero / Axe Compute / Digi Power X / Alpha Compute Corp /
  K Wave Media / FABC / VWAV / VDTA / BSAI): rename-pivot de-SPACs without
  organic chokepoint capability — already in CANDIDATE_UNIVERSE.md REJECT
  log. Filter out by ticker exclusion list.
```

---

## NEW SCREEN #9 — SPINOFF / REORG CATALYST SCREEN

**Status:** PROPOSED
**Information gap closed:** corporate-event-driven setups (spinoff, Ch11 emergence, divestment-driven relisting, refi + new CFO/CEO at restructure event). These are the catalyst-structure leads, where the 8-K event RESETS the institutional float, analyst coverage, and risk-factor language — making the company "discoverable from scratch" 6-18 months before a chokepoint catalyst.
**Source cluster:** Cluster 3 (Spinoff / REORG Catalyst Structure) + cross-applies to Cluster 5 (Broken-IPO / Post-Failure Pivot)
**Hit rate basis:** 22/61 = 36% univ; cross-sector
**Cadence:** Monthly (run on 5th — captures trailing 30-day 8-K filings on Items 1.03, 2.01, 5.02)
**Tooling:** EdgarTools 8-K full-text search on Items 1.03 (bankruptcy), 2.01 (acquisition/disposition), 5.02 (officer change); Form 10-12B (spinoff registration); Form 25 (delisting → relisting); Form S-1/F-1 (new IPO post-spin).

### Draft SCREEN_PROMPT

```
OBJECTIVE:
Surface sub-$5B US-listed companies that completed a CORPORATE EVENT in
the trailing 18 months — specifically: spinoff, Ch11 emergence,
divestment-driven relisting, OR new CFO/CEO installed at a corporate
restructuring event. The thesis: the corporate event resets the
institutional float / analyst coverage / risk-factor language / business
focus, and combined with a chokepoint catalyst within the FOLLOWING 6-18
months, the market rerates from a clean slate.

METHOD:
1. EVENT DETECTION: scan trailing 18 months of:
   - Form 10-12B filings (spinoff registration) → identify spinoff completions
   - Form 8-K Item 1.03 (bankruptcy) + Item 5.02 + emergence press release →
     identify Ch11 emergence events
   - Form 25 (delisting) followed by Form 8-A/F-1/S-1 (relisting) → identify
     divestment-driven relistings (NBIS Yandex divest analog)
   - Form 8-K Item 5.02 (officer change) WHERE the change is CFO or CEO →
     identify governance-reset events (especially when concurrent with refi
     or debt restructuring 8-Ks)
2. FILTER: market cap < $5B at the event date (Alpha Vantage cross-check).
3. CHOKEPOINT CATALYST OVERLAY: scan the 6-month window AFTER the event for:
   - H10-extended bellwether mention (any sector)
   - Earnings inflection >40% YoY (first-time)
   - Major contract 8-K Item 1.01
4. SCORE: each hit on H10-extended, H8, H5, H11. Note WHICH corporate-event
   subtype was the lead.

OUTPUT:
- Ticker, event date, event type (spinoff/Ch11/relist/CEO-change), trailing
  catalyst, H10/H8/H5/H11 quick-score
- Spinoffs/Ch11/relistings: structurally high signal-quality — route to TIER 2
- CFO/CEO change alone: TIER 3 unless combined with chokepoint catalyst

TEST CASES:
- SNDK (Sandisk spinoff Feb 24 2025): screen should fire on Form 10-12B Aug
  2024 + spinoff completion Feb 2025. Then H10 NVDA HBM commentary +
  earnings inflection Sep 2025 → TIER 2.
- NBIS (Yandex divest Jul 2024 + name change Aug 2024 + Nasdaq relist Oct
  2024): screen should fire on Form 25 + 8-A relisting. Then NVDA $700M PIPE
  Dec 2024 → TIER 2.
- WOLF (Ch11 emergence Sep 29 2025): screen should fire on Item 1.03 + 5.02
  + emergence 8-K. Then new CEO Feurle (May 1 2025) + CHIPS Act renegotiation
  → TIER 2 post-emergence (different pattern class).
- BE (CFO Berenbaum Apr 29 2024 + refi May 2024): screen should fire on
  Item 5.02 + concurrent refi 8-K. Then AEP 1GW Nov 2024 → TIER 2.

EXCLUSION CASES:
- Routine CFO/CEO turnover without restructuring context (no refi, no debt
  workout, no business-focus change) — these are governance noise, not
  catalyst structure.
- Mega-cap spinoffs (above $5B at event) — these don't get the discoverable-
  from-scratch micro-cap dynamic.
```

---

## NEW SCREEN #10 — REVERSE-SPLIT-RECOVERY / POST-FAILURE-PIVOT SCREEN (biotech-focused)

**Status:** PROPOSED — biotech-specific extension
**Information gap closed:** biotech reverse-split recovery pattern + asset-pivot pattern. Biotech micro-caps with reverse-split-recovery within 12 months AND FDA designation OR Phase 3/Phase 2 catalyst OR commercial inflection on an in-licensed asset.
**Source cluster:** Cluster 5 (Broken-IPO / Post-Failure Pivot)
**Hit rate basis:** 12-15/61 = 20-25% univ; 5-6/11 = 45-55% in biotech
**Cadence:** Monthly (Form 4 + Form S-3 + 8-K Item 1.01 with reverse-split filings)
**Tooling:** EdgarTools 8-K full-text search on "reverse stock split"; cross-reference Form S-1/S-3 reverse-split disclosures; FDA designation registry; ClinicalTrials.gov for Phase 2/3 catalysts.

### Draft SCREEN_PROMPT

```
OBJECTIVE:
Surface sub-$500M biotech / clinical-stage / commercial-pharma companies
that EITHER executed a reverse split in the trailing 24 months OR avoided
one by recovering above the Nasdaq compliance threshold via catalyst. The
thesis: the dollar-stock geometry (sub-$1 to sub-$5) creates leveraged
upside on positive Phase 2/3 readout or FDA designation, especially when
combined with asset-pivot or restructuring.

METHOD:
1. EVENT DETECTION:
   - EdgarTools 8-K full-text search "reverse stock split" + filtered to
     SIC codes 2834 (pharmaceuticals), 2836 (biological products), 8731
     (commercial research).
   - Cross-reference Form S-3 / S-1 for proposed reverse splits NOT yet
     executed (e.g., RLMD's avoided reverse split Jul 2025).
   - Cross-reference Nasdaq compliance deficiency notice 8-Ks.
2. FILTER: sub-$500M market cap; sub-$5 stock price; clinical-stage or
   commercial-stage pharma.
3. CATALYST OVERLAY:
   - FDA designation in trailing 12 months (Breakthrough Therapy / Fast
     Track / Orphan Drug / Priority Review)
   - Phase 2 or Phase 3 trial readout in trailing 12 months (positive)
   - Big Pharma licensing or partnership amendment in trailing 12 months
     (Roche/Merck/Pfizer/BMS/AbbVie/Lilly/Sanofi/AZ/Novartis/JNJ/Viatris)
   - Asset in-license (new pipeline reset via outside license)
4. SCORE: H10-extended via Big-Pharma-partner OR FDA-designation; H8 sub-$500M
   (tighter than the AI-infra H8); H5 IGNORED (post-failure narrative); H11
   balance-sheet survival (going-concern allowed if recently raised PIPE).
5. EXCLUDE: pure clinical-stage with no Phase 2/3 catalyst within 12 months;
   chronic-dilution micro-caps without asset pivot (e.g., 5+ reverse splits
   without underlying program reset).

OUTPUT:
- Ticker, reverse-split date (or avoided-date), ratio, catalyst type,
  H10ext/H8/H5/H11 score, specialist-fund 13F overlay
- 4/4 passes → TIER 2
- Specialist healthcare fund (BVF / Frazier / Deerfield / Baker Bros) overlay
  upgrades to TIER 1 if cluster buy or PIPE participation

TEST CASES:
- SLGL: 10-for-1 reverse split May 2 2025 + Twyneo/Epsolay commercial
  inflection (Viatris licensee). Should fire on reverse-split + commercial
  bellwether.
- RLMD: Avoided reverse split Jul 2025 + NDV-01 Phase 2 92% ORR data + FDA
  Type B feedback. Should fire on avoided-reverse + FDA-designation overlay.
- PVLA: Reverse merger Dec 2024 + Phase 3 SELVA met Feb 2026 + BVF/Frazier
  PIPE anchor. Should fire on reverse-merger (functional equivalent of
  reverse split) + Phase 3 + specialist-fund overlay.

NEW DIMENSION — specialist healthcare fund 13F:
Track BVF Partners, Frazier Life Sciences, Deerfield Management, Baker
Bros, Bain Life Sciences, RTW Investments, Avoro Capital — these are the
BIOTECH-equivalent of Vanguard/BlackRock/State Street first-13F appearance.
Add as Dim 17' for biotech screen specifically.
```

---

## NEW SCREEN OVERLAY — SHORT INTEREST AMPLIFIER (not standalone)

**Status:** PROPOSED — overlay on existing screens
**Information gap closed:** magnitude expectation upgrade. SI >15% with rising trajectory in last 90 days, combined with an H10-passing candidate, signals squeeze-fuel amplification of the eventual rerate from +200% to +1000%.
**Source cluster:** Cluster 2 (Squeeze-Amplified Inflection)
**Hit rate basis:** 18/61 = 30% univ
**Cadence:** Apply at point of candidate evaluation, NOT as standalone screen
**Tooling:** Fintel / S3 Partners / Ortex API or web scrape for short interest %; Nasdaq SI reports (semi-monthly).

### Draft OVERLAY_PROMPT

```
OBJECTIVE:
For any candidate that passes H10-extended + H8 + H5 + H11, check short
interest as a MAGNITUDE AMPLIFIER. The overlay upgrades the magnitude
expectation when SI is elevated, not the thesis itself.

METHOD:
1. For each H10-extended-passing candidate, pull short interest:
   - Most recent semi-monthly Nasdaq SI report OR Fintel current SI %
   - Trajectory over trailing 90 days (rising / flat / falling)
   - Borrow fee (Ortex / S3 / Fintel)
2. SCORING:
   - SI <10%, flat or falling: BASELINE (no amplifier, expect +200-500%
     magnitude if H10/H8/H5/H11 all pass)
   - SI 10-15%, flat or rising: MILD AMPLIFIER (+500-1000% magnitude
     expectation)
   - SI 15-25%, rising: STRONG AMPLIFIER (+1000-2500% magnitude expectation)
   - SI 25-40%, rising + borrow >25% annualized: VIOLENT AMPLIFIER
     (+2500-10000% magnitude possible — but H11 must be CLEAN)
3. SI >50% OR borrow >100% annualized: SUSPICIOUS — re-check if candidate
   is meme/squeeze structural anomaly (Cluster 8 REJECT zone).

OUTPUT:
Annotate each candidate's CANDIDATE_UNIVERSE.md entry with:
- SI % at evaluation
- 90-day SI trajectory
- Borrow fee
- Amplifier tier (BASELINE / MILD / STRONG / VIOLENT)
- Expected magnitude range

TEST CASES:
- NVTS at Apr 2025 SI 28% + NVDA partnership coming → VIOLENT amplifier,
  realized +738% (within range).
- AAOI at Aug 2024 SI 24% + AVGO 800G fire → VIOLENT amplifier, realized
  +1500% (within range).
- BTDR at 2024 SI 35% + NVDA H100 deploy → VIOLENT amplifier, realized
  +1500%.
- RGC at Feb 2025 borrow 188% annualized → SUSPICIOUS, route to Cluster 8
  REJECT.
```

---

## NEW SCREEN — FOREIGN-FILER DISCOVERY (specialty path)

**Status:** PROPOSED — specialty / quarterly
**Information gap closed:** US-listed 6-K/20-F filers (Korean, Japanese, Israeli, Canadian, European, Singaporean) are systematically under-followed by US analyst pool. When H10 fires, the discovery friction creates an amplifier effect.
**Source cluster:** H19 — Foreign Filer Discovery Friction Amplifier
**Hit rate basis:** 9/61 = 15% — but high-amplitude when fires
**Cadence:** Quarterly (synchronize with foreign-listing annual report cycles: Stockholm April, TSE March, HKEX May, Tel Aviv May, Toronto March)
**Tooling:** EdgarTools 6-K + 20-F search; TSE EDINET; HKEX HKEXnews; LSE RNS; cross-reference NYSE/Nasdaq listed ADRs.

### Draft SCREEN_PROMPT

```
OBJECTIVE:
Surface sub-$5B US-listed foreign issuers (6-K or 20-F filers) with
H10-extended bellwether mention or Big-Pharma partnership in trailing 6
months. The thesis: foreign filers have US-analyst-coverage friction (no
Form 4 → no insider visibility; no US 13F per US managers → no specialist-
mandate visibility; foreign primary listing → US retail unaware). This
creates a structural discovery friction amplifier on the catalyst.

METHOD:
1. UNIVERSE: pull all US-listed foreign filers (sources: SEC list of 6-K
   filers + Foreign Private Issuer registrations). Filter to sub-$5B.
2. CATALYST DETECTION: scan trailing 6-month 6-K and 20-F filings for
   H10-extended bellwether mentions OR Big Pharma partnership amendments
   OR Treasury/DoD/EXIM mentions OR strategic-customer LOIs.
3. US-COVERAGE FILTER: low US analyst coverage (<= 3 active US sell-side
   analysts in trailing 12 months). Low US options activity (LEAPS
   minimal volume).
4. SCORE: H10-extended + H8 + H5 + H11. Flag the foreign-filer status
   explicitly as a discovery-friction amplifier on top of normal scoring.

OUTPUT:
- Ticker (and primary listing), home exchange, mkt cap USD, 6-K catalyst
  date, H10ext/H8/H5/H11 score, US analyst count
- Foreign filers passing 4/4 → TIER 2 with foreign-amplifier annotation
- Track parallel home-exchange filings (TSE EDINET, HKEX, RNS) since US
  EdgarTools coverage is partial for these names

TEST CASES:
- BTDR (Singapore, Cayman 6-K): pre-AI-Cloud inflection with NVDA H100/H200
  deployment disclosures + low US analyst coverage → should fire as
  high-amplifier candidate.
- ABVX (France, FR ADR): pre-Phase 3 readout July 2025 + low US analyst
  coverage + sub-$300M cap → should fire on Big Pharma extension (FDA
  primary endpoint met).
- 3778.T Sakura Internet (Japan TSE — currently in WATCH): Microsoft
  Japan vendor-level partnership 2026-04-03 → should fire on MSFT
  bellwether + foreign-filer amplifier (already in CANDIDATE_UNIVERSE.md).
- SIVEF (Sweden — currently in WATCH): pending FY2025 annual report.

EXCLUSION: Foreign filers without H10-extended or Big-Pharma catalyst —
discovery friction alone is not a thesis.
```

---

## NEW REJECT CRITERIA — Meme/Squeeze Microstructure Pattern

**Status:** PROPOSED — add to DISCOVERY_PROMPT.md as automatic REJECT criteria
**Information gap closed:** screening OUT structural microstructure anomalies (RGC pattern) that produce massive returns but are uninvestable on a thesis basis.
**Source cluster:** Cluster 8 (Meme / Squeeze Structural Anomaly REJECT)

### REJECT criteria block to add to DISCOVERY_PROMPT.md

```
PRE-SCREEN AUTOMATIC REJECT — Meme/Squeeze Microstructure Pattern

Before running the 6-check evaluation on any candidate, apply this
PRE-SCREEN. If ALL of the following conditions are met, AUTO-REJECT
the candidate as Cluster 8 microstructure anomaly. Do not pursue.

CONDITION 1: Free float < 20% of shares outstanding (CEO/founder
  ownership > 80% OR insider+restricted blocks > 80%).
CONDITION 2: Annualized borrow fee > 50% (Ortex / Fintel / S3 reading).
CONDITION 3: NO H10-extended bellwether mention in trailing 12 months
  (no NVDA/MSFT/META/AMZN/GOOG/TSMC/AVGO/AMD, no DoD/NASA/DOE/Treasury/
  EXIM, no Big Pharma, no Apple/Tesla/Lockheed).
CONDITION 4: NO government contract >5% of TTM revenue.
CONDITION 5: TTM revenue < $10M OR pre-revenue.

If 5/5 → AUTO-REJECT. Document in REJECT log with "Cluster 8 microstructure
pattern (RGC analog)" rationale.

If 4/5 → ELEVATED-FLAG. Manual review required before proceeding to
6-check.

If 3/5 or fewer → no action; proceed to standard 6-check.

CALIBRATION CASES:
- RGC: ALL 5 conditions met → AUTO-REJECT (correctly).
- SHAZ: passed Stage 1 framework via NCP cert, but met 3/5 conditions →
  flagged for elevated review; correctly REJECTED at Stage 2 DD.
- BTDR: passes condition 1 (founder 25-35%), but H10 vendor-level fires
  (NVDA H100/H200) → does NOT meet condition 3 → proceeds to standard
  6-check (correct outcome: BTDR is a real BTC-pivot candidate).
```

---

## INTEGRATION WITH EXISTING SCREENS

The 4 new screens + 2 overlays integrate with existing Archos screens as follows:

| Existing screen | Integration with new screens |
|---|---|
| **revenue-inflection** | Add Screen #7 Customer Deposit Spike as a v3 enhancement — same balance-sheet read, complementary signal |
| **supplier-mapping** | No direct overlap; supplier-mapping is one-degree/two-degree customer disclosure, Customer Deposit Spike is balance-sheet line items |
| **insider-buying-weakness** | Already documented Phase 1 H3 KILLED finding cross-confirmed. No changes. |
| **master-screen** | Sub-screens 1-5 retained. Add Sub-Screen 6 (Customer Deposit Spike) and Sub-Screen 7 (De-SPAC Reanimation) for next quarter's v2. |
| **patent-cluster** | Still PLANNED — Phase 3 confirmed patent-acceleration is conceptually sound but USPTO baseline tooling not yet built |
| **conference-presenter** | Still PLANNED — no new data from Phase 3 |
| **bellwether sweep (existing)** | Extend bellwether list per H14: + DoD/DOE/NASA/AFRL/DARPA/EXIM/Treasury/Apple/Tesla + Big Pharma. Already drifting this direction; codify. |

---

## RECOMMENDED PRIORITY ORDER FOR BUILD

1. **Customer Deposit Spike Screen (#7)** — HIGHEST PRIORITY. Direct balance-sheet read; 70% hit rate in target sector; minimal new tooling required (EdgarTools XBRL extraction).
2. **De-SPAC Reanimation Timing Screen (#8)** — HIGH PRIORITY. Requires master spreadsheet of de-SPACs (one-time build then monthly maintenance). 60%+ hit rate in target sector.
3. **Short Interest Amplifier Overlay** — MEDIUM PRIORITY. No standalone screen; cross-applies to existing screens. Requires SI data source (Fintel / Ortex / S3 — assess access).
4. **Spinoff / REORG Catalyst Screen (#9)** — MEDIUM PRIORITY. EdgarTools 8-K item-filter-based; modest new tooling.
5. **Meme/Squeeze REJECT Pre-Screen** — MEDIUM-HIGH PRIORITY for risk management. Quick to implement; integrate into DISCOVERY_PROMPT.md.
6. **Reverse-Split-Recovery Biotech Screen (#10)** — MEDIUM PRIORITY. Specialty screen; only applies to biotech batch.
7. **Foreign-Filer Discovery Screen** — LOWER PRIORITY. Specialty; requires non-US filing aggregator integration.

---

## OPEN QUESTIONS FOR SOUNDING BOARD

1. **Sector-lens H10 codification.** Should CHOKEPOINT_TAXONOMY.md be refactored to a sector-conditional bellwether registry (NVDA-list for AI-infra, DoD-list for defense, Big-Pharma-list for biotech, etc.)? This is the deepest framework refactor surfaced by Phase 3.
2. **H8 sub-$5B vs sub-$2B.** Universe-wide 80% of winners started sub-$2B (not sub-$5B). Should H8 tighten? Or keep $5B for AI-infra and tighten to $2B for biotech / defense / critical minerals?
3. **REORG cluster as a recognized pattern variant.** WW / WOLF / BW post-petition-equity are a real winner pattern but pre-petition holders are wiped. How should the framework formally treat REORG candidates — separate pattern variant per H12 (sector pivot proposal) or hard-rejected on H11?
4. **De-SPAC timing window precision.** 24-36 months post-merger appears to be the discoverable window. Should be tested forward across the 2022-2023 de-SPAC cohort (most reanimating now) for hit-rate validation before committing to the screen.
5. **Specialist healthcare fund 13F integration.** Add BVF / Frazier / Deerfield / Baker Bros / Bain / RTW / Avoro as biotech-equivalent of Vanguard/BlackRock/State Street first-appearance signal in DISCOVERY_PROMPT.md? Phase 3 evidence is strong (PVLA, NBTX, ABVX, CELC, RLMD).
6. **Foreign-filer infrastructure investment.** Worth building TSE EDINET / HKEX HKEXnews / LSE RNS / Stockholm OMX parallel-feed scraping? Phase 3 surfaced 9/61 foreign filers including IREN, NBIS, BTDR, ABVX, NBTX, SLGL, POET, CNL, ASM. Material discovery gap if not addressed.

---

End of NEW_SCREENS_SPEC.md. Phase 3 complete.
