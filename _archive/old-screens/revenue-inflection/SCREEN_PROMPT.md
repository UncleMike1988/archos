# SCREEN_PROMPT.md — Revenue Inflection Screen (v2)

## Version history

- **v1 (2026-05-21)** — total-company revenue only. Found WYFI
  (borderline; sustained growth, not first-time inflection). Surfaced
  SANM and PENG as having strong AI segment growth but failed both on
  H8 because the screen only looked at company-level revenue. SANM's
  Cloud/AI segment grew 3.78x YoY ($732M → $2.77B) inside a $13.8B
  parent. PENG's AI segment grew inside a $3.2B parent with -6% YoY
  total revenue. The v1 design **missed the segment-level inflection
  pattern entirely**.
- **v2 (2026-05-24)** — adds Level 2 segment-level extension. For
  companies $5-15B with disclosed AI-related segment growth, screen
  the segment as if it were a standalone company. Compute transition
  ETA — when the AI segment becomes >50% of total revenue, the company
  transitions from "mid-cap with AI exposure" to "AI pure-play" and
  may then re-pass H8.

## OBJECTIVE

Find sub-$5B companies where **quarterly revenue YoY growth exceeded
40% for the FIRST TIME** (Level 1, unchanged from v1), AND find
$5-15B mid-cap companies where an **AI-related segment** is growing
40%+ YoY with a credible path to becoming >50% of total revenue within
18 months (Level 2, NEW in v2).

The phase transition from "mid-cap with AI segment" to "AI pure-play"
**IS the re-rate catalyst**. IREN did exactly this: BTC miner → AI cloud.
The stock re-rated when the market saw AI revenue was about to dominate.
Finding companies where that transition is 6-12 months away is finding
the next IREN at the $3-5B stage instead of the $17B stage.

## METHOD

### LEVEL 1 — Total company revenue (same as v1)

#### Step 1.1 — Pull recent quarterly filings

Use `search_filings_full_text` to pull 10-Q filings from the last 90
days. Extract company, ticker, CIK, period, revenue current/prior/2YA.

#### Step 1.2 — Compute growth rates

```
yoy_growth = (current_q_rev - prior_year_q_rev) / prior_year_q_rev
prior_yoy_growth = (prior_year_q_rev - 2YA_q_rev) / 2YA_q_rev
```

#### Step 1.3 — Apply inflection filter

Keep only filings where:
- `yoy_growth > 0.40` (current quarter > 40% YoY growth)
- `prior_yoy_growth < 0.20` (year-ago quarter was < 20% YoY growth)
- Market cap < $5B (verified via live data, not XBRL)

#### Step 1.4 — Standard exclusions (same as v1)

- Biotech/pharma SIC 2830-2836
- Blank check / SPAC SIC 6770
- Already-known names (CANDIDATE_UNIVERSE.md, Phase 1/2/3 winners,
  Phase 2 controls)
- Sector-pivot blind-spot names (BTC-miner pivots, shell pivots)

#### Step 1.5 — Quick chokepoint + H5 + H11 indicators (same as v1)

Per surviving name, pull SIC, MD&A "Results of Operations", map to
CHOKEPOINT_TAXONOMY.md. Capture analyst count (H5 indicator), AI-ETF
inclusion (H5 indicator), balance-sheet snapshot (H11 indicator).

### LEVEL 2 — Segment-level analysis (NEW in v2)

#### Step 2.1 — Define the segment-level universe

Target companies between **$5B and $15B market cap** with disclosed
operating segments. Below $5B, Level 1 already catches them. Above
$15B, the segment-level signal is unlikely to produce the H8 transition
within 18 months — too much non-AI revenue to dilute.

#### Step 2.2 — Pull 10-Q segment disclosures

Use `search_filings_full_text` on 10-Q filings from the last 90 days:

```
form_type: 10-Q
date_range: last 90 days

queries (run separately):
  "segment" AND "data center"
  "segment" AND "artificial intelligence"
  "segment" AND "AI"
  "segment" AND "cloud" AND "growth"
  "segment" AND "high-performance computing"
  "segment" AND "HPC"
  "segment" AND "accelerat" (accelerated, accelerator, etc.)
```

Note: same boolean-AND-with-phrase-quotes limitation as v1 — use
single-phrase queries, triage manually.

#### Step 2.3 — Pull segment revenue tables

For each hit (or known candidates: SANM, PENG, and others surfaced
during the run), use `filing_section` with `note:` for the segment
disclosure XBRL tag, or read the relevant 10-Q MD&A and Notes to
Financials section.

Common XBRL segment tags to try:
- `note:SegmentReportingDisclosureTextBlock`
- `note:DisaggregationOfRevenueTableTextBlock`
- `note:ScheduleOfSegmentReportingInformationBySegmentTextBlock`
- `note:RevenueFromContractWithCustomerTextBlock`

Extract per segment:
- Segment name
- Segment revenue (current quarter)
- Segment revenue (year-ago quarter)
- Segment YoY growth rate
- Segment as % of total company revenue

#### Step 2.4 — Apply segment-level filter

Keep only segments where:
- Segment YoY growth > 40%
- Segment is AI/data-center/HPC-related (per the company's own
  disclosure language)
- Parent company market cap is $5-15B (verified live)
- Segment is at least 15% of total revenue today (below this, the
  transition timeline is too long to act on; above this, the
  transition is plausible within 18 months at >40% growth)

#### Step 2.5 — Compute transition ETA

For each surviving segment, compute the months until the AI segment
exceeds 50% of total revenue, assuming:
- AI segment grows at current YoY rate
- Non-AI segments grow at trailing rate (or 0% if declining)

```
months_to_majority = log(0.5 * (non_AI_rev / AI_rev) /
                          ((1 + non_AI_growth) / (1 + AI_growth))) /
                     log((1 + non_AI_growth) / (1 + AI_growth)) * 12

(simplified — use monthly projection in spreadsheet form for clarity)
```

If `months_to_majority` < 18, flag as **transition-imminent**.
If 18-36, flag as **transition-plausible**.
If > 36, flag as **transition-too-distant** (likely fails before
qualifying).

A transition-imminent flag means the company is the **next IREN**
candidate — when the market recognizes AI is the majority business,
H8 flips PASS and the candidate may rerate.

#### Step 2.6 — Mandatory verification of known patterns

Explicitly check these candidates from the v1 run:

- **SANM (Sanmina, $13.8B)** — Cloud/AI segment grew 3.78x YoY in
  Q2 FY26. What % of total revenue is the Cloud/AI segment? Path to
  >50%? Pull the Q2 FY26 10-Q segment table.
- **PENG (Penguin Solutions, $3.2B)** — Advanced Computing segment
  growing inside flat parent. Note: PENG is sub-$5B so it sits at
  the **boundary** between Level 1 and Level 2. Apply Level 2 logic
  to confirm segment-level inflection. If yes, this is a hybrid
  case: sub-$5B parent AND segment >40% growth = potential ACCEPT
  candidate after full 6-check.

Run `search_filings_full_text` on:
```
ciks: [SANM CIK, PENG CIK]
form_type: 10-Q
date_range: last 180 days
```

Read each 10-Q's segment disclosure note directly.

### LEVEL 3 — BTC-miner-to-AI-pivot scan (NEW in v2, contained scope)

The IREN/CLSK pattern: legacy BTC miner pivots to AI cloud, AI revenue
gradually overtakes BTC revenue. This is the **sector pivot blind spot**
the framework documents as out-of-scope, but a containment scan is
worth one cycle of attention because:

(a) IREN and CLSK are already in CANDIDATE_UNIVERSE Tier 2
(b) The pattern repeats — other small BTC miners may be 6-12 months
   away from their IREN moment
(c) The risk profile differs from a pure chokepoint pure-play, so
   any surfaces here go to a **separate** review queue, not the
   four-filter framework

#### Step 3.1 — Web search for current BTC-miner pivots

```
"bitcoin miner AI pivot 2026 small cap"
"BTC miner data center conversion 2026"
"hash rate AI hosting transition"
"crypto miner AI cloud 2026"
```

Surface names. For each candidate:
- Current market cap
- AI revenue (latest quarter, if any)
- BTC revenue (latest quarter)
- AI revenue as % of total (current vs. one year ago)
- Stated transition plan (8-K? Earnings call? Press release?)
- Hyperscaler / NVDA / AVGO partnerships announced?

#### Step 3.2 — Apply hybrid screen

A BTC-miner-pivot candidate is flagged for SEPARATE evaluation (NOT
the four-filter framework) if:

- Market cap < $5B
- Stated AI infrastructure pivot announced via 8-K or earnings
- AI revenue is growing as % of total, even if still <50%
- Power capacity (MW) is publicly disclosed
- Hyperscaler / NVDA / AVGO conversation is active

This is **not an ACCEPT signal** — it goes to a "BTC pivot watch list"
referenced in CANDIDATE_UNIVERSE Tier 2 logic. The framework does NOT
apply directly to these names.

## EXECUTION OPTIONS

Same as v1:
- **Option A** — Structured XBRL pull (preferred for top candidates)
- **Option B** — Filing-language search (first-pass discovery)
- **Option C** — Web-search hybrid (broadest net, fastest discovery)

**v2 RECOMMENDATION**: Run Option C first (web search for both Level
1 candidates and BTC-pivot names), then verify with Option A (segment
data via `filing_section` `note:` tags) for the top 3-5 from each
level.

## OUTPUT

Write the run report to:
`/Users/michaelturner/Desktop/Claude Builds/archos/screens/revenue-inflection/runs/{YYYY-MM-DD}-v2-run.md`

### Format

```markdown
# Revenue Inflection Screen v2 — {YYYY-MM-DD}

## Run parameters
- Date range: {YYYY-MM-DD} to {YYYY-MM-DD}
- Execution option(s) used: {A / B / C / hybrid}
- Level 1 universe size before filters: {N}
- Level 1 surviving: {N}
- Level 2 universe size before filters: {N}
- Level 2 surviving: {N}
- Level 3 (BTC pivot) candidates surfaced: {N}
- Time spent: {N} minutes

## Level 1 Results (total company revenue inflection, sub-$5B)

| Ticker | Company | Mkt Cap | Current Q Revenue | YoY Growth | Prior YoY | Sector | Flag? |
|--------|---------|---------|-------------------|------------|-----------|--------|-------|

## Level 2 Results (segment-level inflection, $5-15B)

| Ticker | Company | Mkt Cap | AI Segment Rev | AI Segment Growth | AI as % Total | Transition ETA | Flag? |
|--------|---------|---------|----------------|-------------------|---------------|----------------|-------|

## Level 3 Results (BTC-miner-to-AI pivot)

| Ticker | Company | Mkt Cap | AI Revenue | BTC Revenue | AI % Total | Pivot Catalyst | Separate Watch? |
|--------|---------|---------|------------|-------------|------------|----------------|-----------------|

## Top names (narrative, per level)

### Level 1 top names
1. {TICKER} — {one-line thesis}
   Revenue driver per MD&A: ...
   Quick H5/H11: ...
   Recommendation: ...

### Level 2 top names
1. {TICKER} — {one-line thesis on transition timing}
   AI segment context: ...
   Transition ETA: {N} months to >50%
   What flips when transition occurs: H8 PASS, mkt cap may rerate
   Recommendation: ...

### Level 3 top names (if any)
1. {TICKER} — {one-line pivot context}
   AI revenue trajectory: ...
   Separate watch (NOT framework ACCEPT): ...

## Refinement notes

- Query effectiveness
- Signal-to-noise ratio per level
- Tooling friction
- What to change before next run

## Cross-reference: retroactive validation

Spot-check tests:
- AXTI Q3 2024 10-Q (Level 1 — would the 40%/<20% threshold catch it?)
- POWL late 2023 10-Q (Level 1)
- AAOI Q4 2024 10-Q (Level 1)
- IREN's BTC-to-AI transition quarter (Level 2/3 — when did AI revenue
  inflect inside the BTC parent?)

## Mandatory v2 verification

Did v2 catch what v1 missed?

- **SANM** — was the segment-level inflection found and quantified?
  Result: {PASS / FAIL}
- **PENG** — was the segment-level inflection found and quantified?
  Result: {PASS / FAIL}

If yes: v2 segment-level extension validated.
If no: diagnose. Either (a) segment disclosure not parseable via
EdgarTools `filing_section` `note:` tags, (b) segment growth measured
on different basis than expected, (c) v2 threshold too strict for the
specific segment. Document for v3.
```

## TEST CASES (for retroactive validation)

Same as v1:
- **AXTI** — InP wafer ramp likely Q3-Q4 2024 10-Q (Level 1)
- **POWL** — Electrical infrastructure 2023 10-Qs (Level 1)
- **AAOI** — Hyperscale optical ramp 2023-2024 10-Qs (Level 1)
- **CRDO** — AECs / SerDes 2024 10-Qs (Level 1)

Plus v2-specific:
- **IREN** — was BTC-to-AI transition quarter identifiable from segment
  data 6-12 months before market rerate? (Level 2)
- **SMCI** — was AI-server segment inflection inside the parent
  identifiable 6-12 months before mega-rerate? (Level 2, retroactive)

If v1 caught 3 of 4 Level 1 test cases and v2 catches IREN at the
transition quarter via Level 2, the v2 design is validated.

## NEXT RUN

Run on the 15th of each month. If a major sub-$5B AI-infra name has
just filed a 10-Q with surprising results (or a $5-15B mid-cap files
with a segment-level beat), run sooner and append a delta.
