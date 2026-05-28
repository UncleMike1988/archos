# SCREEN_PROMPT.md — Insider Buying Into Weakness Screen (v1)

## Version history

- **v1 (2026-05-24)** — Initial build. Different signal class from
  the killed H3 hypothesis: this screen looks for executives buying
  THEIR OWN STOCK with open-market dollars AFTER a 25-40% drawdown,
  not founders/execs grinding option grants ahead of inflection.
  H3 was killed because Phase 1 winners (AXTI, NVTS, etc.) had
  insiders SELLING into the rerate. This screen captures a different
  pattern: insiders accumulating during pessimism / distraction.

## CRITICAL CONTEXT — what this screen IS and IS NOT

**This is NOT a resurrection of H3.** H3 hypothesized that Form 4
buying was a leading signal for the 12 confirmed 20x+ winners.
PATTERN_MATRIX_v2 killed H3 at 0/12 leading because those insiders
either (a) sold into strength, (b) acquired via grants/exercises
that compound silently, or (c) had no Form 4 activity at all.

**This IS a different signal class.** It is a contrarian add-on
filter for ALREADY-identified candidates: when a CEO/CFO commits
$100K+ of personal liquid cash to open-market BUYS while their
stock is 25-40% below its 52-week high, they are betting against
the consensus that just sold them down. Cross-referenced with any
chokepoint, AI-infrastructure, or revenue-inflection exposure,
this is a high-conviction confirmation overlay — not an entry
signal in isolation.

The risk to manage: insider buying can be (a) optic creation by
management dumping through other channels, (b) genuine conviction
in a turnaround, (c) noise from a director topping up a stake for
non-economic reasons (family office, estate planning, etc.). The
H11 balance-sheet survival check is non-negotiable on hits because
of (a).

## OBJECTIVE

Find sub-$10B AI-infrastructure-adjacent companies where insiders
(CEO / CFO / COO / board director) bought open-market shares
(Form 4 transaction code P) with **aggregate purchases >$100K** in
the **trailing 90 days** while the stock was **>25% below its
52-week high** at the time of purchase.

Cross-reference against:
- CHOKEPOINT_TAXONOMY.md (highest priority if maps to a chokepoint)
- Current WATCH list in CANDIDATE_UNIVERSE.md (upgrades conviction)
- Output of revenue-inflection screen (cross-screen hits = highest
  priority — see Step 4)
- Output of supplier-mapping screen (same)
- Output of weekly bellwether sweep (same)

## METHOD

### Step 1 — Find insiders buying into weakness

Identify all qualifying Form 4 BUY transactions across a candidate
universe. A "qualifying" purchase meets ALL of:

a) Transaction code = **P** (open-market purchase). Reject:
   - **A** = grant
   - **M** = exercise of option (cashless)
   - **F** = withholding for taxes
   - **G** = gift
   - Anything else that is not an open-market BUY with the
     insider's own cash
b) Net purchase value aggregated across all insiders at the same
   company in the trailing 90 days > **$100K**
c) Buyer's role is one of:
   - **CEO** (President + CEO combinations count)
   - **CFO**
   - **COO**
   - **Director** (board member, not 10% holder)
   - Reject 10% beneficial owners (different signal — those are
     fund accumulators) and external advisors
d) Stock was **>25% below 52-week high** at the time of the BUY.
   For cluster buys spanning a week+, use the median trade date
   stock price.

### Step 2 — Filter for AI-infrastructure or chokepoint exposure

For each candidate that passes Step 1:

a) **Live market cap < $10B** (this screen runs wider than $5B
   because Step 1's signal is rarer and the conviction overlay
   reduces the H8 false-positive risk somewhat). Verify via
   Alpha Vantage / Massive Market Data, not XBRL.

b) **Chokepoint cross-reference** against CHOKEPOINT_TAXONOMY.md:
   - **HIGH PRIORITY** if the company maps to one of the 10
     active chokepoints
   - **MEDIUM PRIORITY** if the company has AI-infrastructure,
     defense, space, or critical-technology exposure not yet in
     the taxonomy
   - **LOW PRIORITY** if no AI-infra link can be drawn — note
     for the rejection log

c) **Quick H5 sentiment indicator** — what is the rough
   sentiment posture?
   - IGNORED / NEUTRAL → good (insiders see what market doesn't)
   - PARTIAL → ok (entry window may still be open)
   - LOVED → bad (insiders buying at the top of a narrative is
     a red flag — see "optic creation" risk above)

d) **Quick H11 balance sheet check** — is the company solvent?
   - Net debt / EBITDA < 5x → PASS
   - Positive FCF runway > 18 months → PASS
   - No going-concern qualification → PASS
   - If ANY of these fail → flag as **H11 FLAG**. Optic-creation
     risk multiplies when insiders are buying into a balance
     sheet that may not survive — they may be unloading via
     shelf offerings while individually buying small stakes
     to create a confidence narrative.

### Step 3 — Compute conviction metrics

Build a row per candidate with these fields:

| Field | Description |
|---|---|
| Ticker | |
| Company | |
| Insider(s) | Name + title for each buyer |
| Trade dates | All P transaction dates in the 90-day window |
| Cluster? | YES if >1 insider purchased within 14 days |
| Total $ purchased (90 day) | Aggregate across all insiders |
| Largest single trade | Single biggest P transaction $ |
| Stock price at purchase (median) | |
| Current stock price | For drawdown-since-purchase context |
| % below 52wk high (at purchase) | |
| % below 52wk high (currently) | |
| Mkt cap (current, live) | |
| Chokepoint mapping | Or "none yet documented" |
| H5 indicator | IGNORED / NEUTRAL / PARTIAL / LOVED |
| H11 indicator | PASS / FLAG |
| 1st-time buyer flag | YES if no prior P purchases by this insider in 2+ years |
| Cross-screen flag | If also in revenue-inflection or supplier-mapping or bellwether sweep |

### Conviction ranking factors (apply after Step 3 is complete)

The ranking is qualitative — there is no closed-form score. Weight
by these dimensions (descending importance):

1. **CEO > CFO > COO > Director.** The CEO knows the most; a
   buying CEO has the strongest information signal. A director
   buying $5M can still beat a $200K CFO buy if the director is
   widely known to be the company's largest individual holder.
2. **Cluster buying > solo.** Two or more insiders within 14 days
   = the information is being shared inside the executive team,
   which is a higher-confidence read than a single insider's
   private idiosyncratic bet.
3. **Larger absolute $ > smaller.** $500K+ in a single trade is
   meaningful even for highly compensated insiders. $100K is the
   floor; below that the signal-to-noise collapses.
4. **Deeper drawdown > shallower.** 40%+ below 52-week high =
   strongest contrarian signal. 25-40% = moderate. <25% does
   not qualify.
5. **First buy in 2+ years > regular buyer.** A change in behavior
   is the actual signal; a director who buys $50K every quarter
   is doing portfolio management, not signaling.
6. **Chokepoint mapping > no map.** A chokepoint-mapped name with
   insider buying is the highest-priority class.
7. **Cross-screen hit > standalone.** If the name also appeared
   in revenue-inflection or supplier-mapping or bellwether sweep
   = highest priority for full DD.

### Step 4 — Cross-reference with other screens

For each surviving candidate, check whether the ticker also
appears in:

- **Revenue-inflection screen** (latest run) — revenue accelerating
  AND insiders buying = strongest possible confirmation. Flag as
  **CROSS-SCREEN TIER 1**.
- **Supplier-mapping screen** (latest run) — hidden bellwether
  supplier AND insiders buying = second-strongest. Flag as
  **CROSS-SCREEN TIER 2**.
- **Bellwether sweep** (last 60 days) — recent partnership
  announced AND insiders bought the dip = third-strongest. Flag
  as **CROSS-SCREEN TIER 3**.

A CROSS-SCREEN TIER 1 candidate should be promoted to ACCEPT-pending
full 6-check immediately. CROSS-SCREEN TIER 2/3 to WATCH with
upgraded priority for next 6-check cadence.

### Step 5 — Mandatory exclusions

Filter out, regardless of insider activity:

- **Sector-pivot blind-spot names** — bitcoin-miner pivots, shell
  pivots (HIVE, BITF, CLSK, RIOT, KEEL, EVTV, AlphaTON, Bitzero,
  Axe Compute, Digi Power X, Alpha Compute Corp, K Wave Media).
  H3 was a documented blind spot — insider buying at these does
  not change the framework's rejection.
- **Biotech / pharma SIC 2830-2836** — outside framework scope.
- **Blank check / SPAC SIC 6770** — outside framework scope.
- **AI services not AI infrastructure** (INOD pattern) — out of
  scope per CLAUDE.md.
- **Pre-revenue moonshot blind spot** (LWLG / IPWR / OKLO pattern)
  — H8 cannot apply.
- **M&A pivot blind spot** (SEI pattern) — chokepoint acquired,
  not built.
- **Geopolitical materials** (MP / UUUU pattern) — parallel
  framework, not this one.
- **DD-rejected names** — SHAZ (6/6 RED). Do not re-surface even
  if insider buying appears post-DD-reject.

## EXECUTION OPTIONS

### Option A — EdgarTools `search_filings_full_text` over Form 4

**Risk:** Form 4 XML structure is highly programmatic. The
`search_filings_full_text` index may not handle Form 4 transaction
codes natively. Expected to return noise or zero results.

Attempt:
```
form_type: 4
date_range: last 90 days

queries (single-phrase, per INSIGHTS.md boolean limitation):
  "P" (transaction code — likely too noisy)
  "purchased shares"
  "open market purchase"
  "open market purchases"
```

If this returns useful results: use as primary source. If not:
fall through to Option B / C.

### Option B — Targeted universe + EdgarTools `insider_activity`

EdgarTools `insider_activity` works company-by-company. Build a
targeted universe:

1. **WATCH list** from CANDIDATE_UNIVERSE.md (currently: SIVEF,
   3778.T, WYFI, ICHR, UCTT). Each gets an insider_activity pull
   for the trailing 90 days.
2. **All 14 cataloged chokepoint pure-plays** in CHOKEPOINT_TAXONOMY.md
   (AXTI, POET, SNDK, ONTO, AEHR, NVTS, POWL, HPS.A, APLD, IREN,
   NBIS, AAOI, CRDO, LITE, BE, PSIX). Several are too large now
   ($10B+) but check for completeness.
3. **Broader sub-$10B AI-infrastructure universe** — pull from a
   web-search-derived list of names mentioned in recent (last 60
   day) AI-DC press, supplier disclosures, or 8-K filings. Cap
   the broader universe at ~50 names per run to keep within time
   budget.

For each company, pull insider transactions and filter by:
- transaction_code = P
- date range = last 90 days
- aggregate $ > $100K
- buyer role = CEO/CFO/COO/Director

### Option C — Web-aggregator hybrid (broadest net)

**Primary source:** OpenInsider.com top-buy lists, filtered to
cluster buys and large dollar amounts.

```
web_fetch: http://openinsider.com/top-insider-purchases-of-the-month
web_fetch: http://openinsider.com/insider-cluster-buys
```

OpenInsider exposes pre-filtered cluster-buy and large-purchase
feeds for the trailing 30-90 days. Each entry includes transaction
date, ticker, insider name, title, P/A/M code, share count, and
$ value. This is the cheapest fastest path to a candidate list.

**Secondary sources:**
- WhaleWisdom insider activity feed
- GuruFocus insider buying screener
- Targeted web search: `"insider buying small cap AI 2026"`,
  `"CEO buying stock semiconductor 2026"`, `"insider purchase
  data center 2026"`, `"director buys stock photonics 2026"`

**Verification:** for each candidate surfaced, cross-check with
EdgarTools `insider_activity` to confirm the transaction code,
aggregate dollar value, and insider role. OpenInsider scraping
can lag the SEC by 24-48 hours but is more accessible than the
raw EDGAR API.

**v1 RECOMMENDATION**: Run Option C first (OpenInsider for the
candidate list), then verify with Option B (EdgarTools per name)
for the top 5-10 hits. Skip Option A unless time allows — Form 4
full-text search is expected to be low-yield.

## OUTPUT

Write the run report to:
`/Users/michaelturner/Desktop/Claude Builds/archos/screens/insider-buying-weakness/runs/{YYYY-MM-DD}-run.md`

### Format

```markdown
# Insider Buying Into Weakness Screen — {YYYY-MM-DD}

## Run parameters
- Date range scanned: {YYYY-MM-DD} to {YYYY-MM-DD}
- Execution option(s) used: {A / B / C / hybrid}
- Raw insider buys surveyed: {N}
- After role filter (CEO/CFO/COO/Director): {N}
- After $ threshold filter (>$100K): {N}
- After drawdown filter (>25% below 52wk high): {N}
- After market cap filter (<$10B): {N}
- After exclusion list: {N}
- Final candidates with AI-infra exposure: {N}
- Cross-screen hits: {N}
- Time spent: {N} minutes

## Raw hits (Step 1 output, before AI-infra filter)

| Insider | Title | Company | Ticker | Trade $ | Date | Stock price | % below 52wk high |
|---------|-------|---------|--------|---------|------|-------------|-------------------|

## Filtered candidates (Step 2 output)

| Ticker | Company | Mkt Cap | Insider(s) | Total $ | Largest single | Cluster? | % below high | Chokepoint? | H5 | H11 | Cross-screen? | Priority |
|--------|---------|---------|------------|---------|----------------|----------|--------------|-------------|----|----|---------------|----------|

## Conviction ranking (top 3-5)

### 1. {TICKER} — {one-line thesis fragment}
- Insider(s): {name + title}
- Trade dates: {all P transactions in window}
- Total $ committed: ${N}
- Largest single trade: ${N}
- Cluster: {YES/NO — count and time window}
- Stock at purchase / current: ${N} / ${N}
- % below 52wk high (at purchase): {N}%
- Chokepoint: {map to CHOKEPOINT_TAXONOMY.md or "none"}
- H5: {indicator + reasoning}
- H11: {PASS / FLAG + reasoning}
- 1st-time buyer flag: {YES/NO}
- Cross-screen flag: {TIER 1 / 2 / 3 or "none"}
- Recommendation: {full 6-check / WATCH / pass}

### 2. ...

### 3. ...

## Cross-screen hits (named explicitly)

If any candidate appears in:
- Revenue-inflection latest run (date)
- Supplier-mapping latest run (date)
- Bellwether sweep last 60 days

Document the overlap and the implied priority upgrade.

## Excluded candidates (with reason)

| Ticker | Why excluded |
|--------|--------------|

## Refinement notes

- Query / data source effectiveness
- Signal-to-noise ratio
- Tooling friction (Form 4 access, OpenInsider availability,
  EdgarTools `insider_activity` quirks)
- What to change before next run
```

## TEST CASES (for retroactive validation when feasible)

The framework is forward-looking; full retroactive backtest of
this signal is out of scope for v1. But spot-check tests against
known patterns:

- **CRDO** during 2023 drawdown (post-IPO trough $7.20, May 2023)
  — did the CEO or any director file Form 4 P buys at the low?
  If yes, this screen would have caught CRDO at the inflection.
- **NBIS** post-IPO Q4 2024 (pre-NVDA $700M PIPE) — did insiders
  buy ahead of the PIPE announcement?
- **APLD** during 2024 Q2 weakness (pre-NVDA $160M Sept 2024 stake)
  — did insiders accumulate?
- **AEHR** during 2023 fiscal Q3 inventory write-down weakness —
  did insiders buy the drawdown?

A successful retroactive backtest on 2-of-4 of these = v1 design
validated for monthly cadence. If none of these had Form 4 P buys
at the inflection lows: screen yields mostly noise / out-of-scope
hits, downgrade cadence to quarterly and reconsider design.

## NEXT RUN

Monthly cadence — run on the 1st of each month. Form 4 must be
filed within 2 business days of transaction, so a monthly sweep
catches the prior month's window cleanly.

Sooner if:
- A name on CANDIDATE_UNIVERSE.md WATCH list takes a >20% drawdown
  within a week (manual trigger — pull insider activity on that
  specific name immediately)
- A weekly bellwether sweep surfaces a new sub-$10B partnership
  AND the partner stock is in drawdown (insider buying could
  confirm the bellwether partnership's significance)
