## MANDATORY — READ BEFORE ANYTHING ELSE

Read these files IN FULL before doing anything:

1. /Users/michaelturner/Desktop/Claude Builds/_master_docs/WORKING_PHILOSOPHY.md
2. /Users/michaelturner/Desktop/Claude Builds/archos/CLAUDE.md
3. /Users/michaelturner/Desktop/Claude Builds/archos/CANDIDATE_UNIVERSE.md
4. /Users/michaelturner/Desktop/Claude Builds/archos/CHOKEPOINT_TAXONOMY.md
5. /Users/michaelturner/Desktop/Claude Builds/archos/INSIGHTS.md

Confirm by stating the LAST LINE of WORKING_PHILOSOPHY.md.
Do not run any commands or make any changes until confirmed read.

---

## SESSION TYPE

THIS IS A TARGETED OPTIONS SCREEN — finding $2-15B companies with real AI/defense/nuclear tailwinds where implied volatility is LOW, meaning LEAPS are cheap relative to the potential catalyst-driven upside.

---

## CONTEXT

The Archos portfolio strategy is built around LEAPS on companies with identifiable catalysts. The best risk/reward comes when:
1. The company has a real fundamental catalyst (binding contract, government relationship, revenue inflection)
2. The options market HASN'T priced in the catalyst (low IV = cheap premium)
3. Jan 2028 LEAPS exist with reasonable liquidity (tight bid-ask spreads)

High IV names (WYFI at 107%, CRML at 117%) eat the upside even when the thesis is right. Low IV names give you leveraged exposure to the catalyst at a fraction of the cost.

The scan inverts the normal Archos discovery process: instead of finding the company first and checking options second, we find cheap options first and validate the company second.

---

## TOOLS AVAILABLE

You have access to Massive Market Data MCP which provides:
- Option Chain Snapshot: GET /v3/snapshot/options/{underlyingAsset} — returns full chain with IV, Greeks, bid/ask, open interest for every contract
- Option Contract Snapshot: GET /v3/snapshot/options/{underlyingAsset}/{optionContract} — detailed single contract data
- All Contracts: GET /v3/reference/options/contracts — index of all options contracts
- Store results as SQL tables via store_as parameter, then query with SQL via query_data

You also have web search for fundamental validation.

---

## TASK: LOW-IV LEAPS CATALYST SCREEN

### PHASE 1 — Build the Universe (30 min)

We need a list of $2-15B companies in AI-adjacent sectors to screen for IV. Build the universe from three sources:

**Source A — Archos sector keywords via web search:**
Search for lists of companies in these sectors, $2-15B market cap:
- "AI infrastructure stocks $2 billion to $15 billion market cap 2026"
- "defense technology stocks mid cap 2026"
- "nuclear energy stocks mid cap 2026"
- "semiconductor equipment stocks mid cap 2026"
- "data center stocks mid cap 2026"
- "cybersecurity stocks mid cap 2026"
- "cloud infrastructure stocks mid cap 2026"
- site:stockanalysis.com screener results for $2-15B technology/industrials

Collect ~50-80 tickers across these sectors.

**Source B — Archos existing universe:**
Pull every ticker from CANDIDATE_UNIVERSE.md and CHOKEPOINT_TAXONOMY.md that is between $2-15B. These are names we already know have fundamental merit.

**Source C — ETF holdings mining:**
Pull top holdings from sector ETFs and filter for $2-15B:
- HACK (cybersecurity), ITA/PPA (defense), SOXX/SMH (semiconductors), NUKZ/NLR (nuclear), SKYY/WCLD (cloud)
- Filter each for $2-15B market cap names

Deduplicate across all three sources. Target: 60-100 unique tickers.

### PHASE 2 — Pull IV Data (45 min)

For each ticker in the universe, use Massive Market Data to pull the options chain snapshot:

GET /v3/snapshot/options/{ticker}

Store each result. For each ticker, extract:
- Current stock price (from underlying asset data)
- Jan 2028 LEAPS availability (do they exist?)
- If Jan 2028 LEAPS exist, find the ATM or slightly OTM call (strike closest to 120-130% of current price)
- Record: ticker, stock price, strike, bid, ask, IV, delta, theta, open interest, volume

Store all results in a SQL table for ranking.

IMPORTANT: Massive Market Data may rate-limit. If so, batch the requests (10-15 at a time with pauses). Prioritize Source B (Archos universe) tickers first since those have known fundamental merit.

### PHASE 3 — Rank by IV (15 min)

Query the stored data to rank all tickers by implied volatility (ascending — lowest IV first).

Filter criteria:
- Jan 2028 LEAPS must exist
- IV < 60% (below the median for growth stocks — this is the "cheap" threshold)
- Open interest > 100 on the specific contract (minimum liquidity)
- Bid-ask spread < 15% of midpoint (tradeable)
- Stock price $10-200 range (practical for LEAPS sizing)

Output: ranked list of tickers sorted by IV ascending, with all options data attached.

### PHASE 4 — Fundamental Validation (30 min)

For the top 20 lowest-IV names that pass Phase 3 filters, run a quick fundamental check via web search:

For each ticker:
1. What does the company do? Which Archos sector lens applies?
2. Revenue growth rate (TTM YoY) — is it >20%?
3. Is there an identifiable catalyst in the next 12-18 months? (New product cycle, government contract, regulatory milestone, earnings inflection, M&A, sector tailwind)
4. H5 sentiment check — is this name IGNORED/NEUTRAL or LOVED? (Analyst count, recent coverage)
5. Any RED flags? (Going concern, insider selling, SEC investigation, paid promotion)

Classify each as:
- TIER 1 STRONG: Real catalyst + low IV + revenue growth >25% + IGNORED/NEUTRAL sentiment
- TIER 2 MODERATE: Real catalyst + low IV + revenue growth 10-25% OR sentiment PARTIAL
- TIER 3 WATCH: Sector tailwind but no specific catalyst identified
- REJECT: No catalyst, or RED flag found, or revenue declining

### PHASE 5 — LEAPS Pricing Analysis (15 min)

For every TIER 1 and TIER 2 candidate, calculate:
- Cost of 1 ATM-ish Jan 2028 LEAPS contract (ask price × 100)
- Breakeven price at expiry
- Return on LEAPS if stock doubles (2x)
- Return on LEAPS if stock goes up 50%
- Return on equity if stock doubles (for comparison)
- The "LEAPS advantage crossover" — at what stock price does LEAPS beat equity?
- Dollar amount to control 1,000 shares via LEAPS vs equity

This gives a direct comparison of capital efficiency across all candidates.

---

## OUTPUT

Write results to:
/Users/michaelturner/Desktop/Claude Builds/archos/weekly-scan/runs/2026-05-28-low-iv-leaps-screen.md

Format:

# Low-IV LEAPS Catalyst Screen — 2026-05-28

## Universe
- Total tickers screened: X
- With Jan 2028 LEAPS: X
- Passing IV < 60% filter: X
- Passing liquidity filter: X

## Top 20 Lowest-IV Names with LEAPS

| Rank | Ticker | Price | Mkt Cap | Sector | IV | Strike | Ask | Breakeven | OI | Spread% | Rev Growth | Catalyst | Tier |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|

## TIER 1 STRONG Candidates (low IV + real catalyst + growth)

[Full profile for each: company, catalyst, revenue trajectory, IV context, LEAPS pricing analysis, return scenarios]

## TIER 2 MODERATE Candidates

[Same format, briefer]

## Best Risk/Reward Rankings

| Rank | Ticker | IV | LEAPS Cost (1 contract) | Return if 2x | Return if +50% | Catalyst | Conviction |
|---|---|---|---|---|---|---|---|

## Capital Efficiency Comparison

"For $20,000 deployed, here is what you control and what you make at various price targets across the top 5 candidates"

Update CANDIDATE_UNIVERSE.md with any TIER 1 candidates not already tracked.

---

## SESSION END

No git push. No framework changes beyond candidate additions.

Output summary to chat:
- How many tickers screened
- How many had Jan 2028 LEAPS with IV < 60%
- Top 5 lowest-IV names with real catalysts
- Best risk/reward LEAPS trade identified
- Any names already in Archos universe that have cheap LEAPS (conviction upgrade)
- Recommended position(s) with sizing

STOP after summary.
