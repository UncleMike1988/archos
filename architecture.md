# architecture.md — Archos
# Framework version: v2.1 (bumped 2026-05-28 — multi-strategy buckets + flag taxonomy + over-rejection guardrail; validated four-filter logic unchanged)

## System overview

Archos is a human-in-the-loop discovery engine. It screens for sub-$5B
AI-infrastructure chokepoint stocks using a four-filter framework
validated across 32 stocks in three research phases. **As of Framework
v2.0 (2026-05-27), the discovery hierarchy has been flipped: balance-sheet
signals (deferred revenue, customer deposits, backlog inflections) are the
PRIMARY discovery layer; bellwether mentions (H10/H10-extended) are the
CONFIRMATION layer that upgrades conviction tier.**

**Multi-strategy system (Framework v2.1, 2026-05-28):** Archos now spans three
strategy buckets — Bucket 1 (large-cap LEAPS), Bucket 2 (sub-$5B chokepoint
pure-plays), Bucket 3 (sub-$1B nanocap AI-adjacent); see CLAUDE.md → Strategy
buckets + Flag Taxonomy. **The discovery-engine data flow below describes
Bucket 2.** Buckets 1 and 3 share the governing principle (reject only on
thesis-breakers; flags set magnitude → magnitude sets size) and the Flag
Taxonomy, but use different discovery inputs and sizing. The diagram is
unchanged.

```
Bellwether Transcripts ──→ CHOKEPOINT_TAXONOMY.md (quarterly refresh; H10-extended per sector lens)
                                    │
                                    ▼
                           ┌─────────────────┐
                           │  Universe Build  │
                           │  (all sub-$15B   │
                           │   tiered: NANO/  │
                           │   CATALYST/      │
                           │   COMPOUNDER/    │
                           │   SEGMENT)       │
                           └────────┬────────┘
                                    │
                                    ▼
                  ┌─────────────────────────────────┐
                  │  PRIMARY DISCOVERY (v2.0)        │
                  │  Screen 3 — Customer Deposits /  │
                  │  Deferred Revenue (10-Q)         │
                  │  Threshold: >50% QoQ OR          │
                  │             absolute >$10M       │
                  └────────────────┬─────────────────┘
                                   │
                                   ▼
                  ┌─────────────────────────────────┐
                  │  CONFIRMATION OVERLAY (H10)      │
                  │  Screen 1 — Material Agreement   │
                  │  (8-K Item 1.01) cross-checked   │
                  │  against Screen 3 hits           │
                  │  H10-extended: H10/H10-D/H10-N/  │
                  │                H10-M/H10-P       │
                  └────────────────┬─────────────────┘
                                   │
                                   ▼
                           ┌─────────────────┐
                           │  4-Filter Gate   │
                           │  H8-tiered → H5  │
                           │       → H11      │
                           │  (PARTIAL-       │
                           │   RECOVERING     │
                           │   re-entry path) │
                           └────────┬────────┘
                                    │
                  ┌─────────────────┼─────────────────┐
                  ▼                 ▼                 ▼
            ACCEPT-track    WATCH (multi-tier)    REJECT
              (H10 fires      TIER 1/2/3 NANO/
              on Screen 3      CATALYST/COMPOUNDER
              candidate)       + TIER 4 SEGMENT
                  │                 │
                  ▼                 ▼
              CANDIDATE_UNIVERSE.md (tiered sections per Framework v2.0)
                        │
                        ▼
              ┌─────────────────┐
              │  Confirmation   │
              │  Signals (H1',  │
              │  H7, H9)        │
              └────────┬────────┘
                       │
                       ▼
              ┌─────────────────┐
              │  DD Checklist   │
              │  (6 sections;   │
              │  lens-agnostic) │
              └────────┬────────┘
                       │
                       ▼
              Human decision
              (Sounding Board)
                       │
                       ▼
              trades/{ticker}.md
```

## Data flow

### Input layer (external data → project files)

1. **Bellwether transcripts** → parsed quarterly → CHOKEPOINT_TAXONOMY.md
   - Sources: NVDA, TSMC, AVGO, MSFT, META, AMD earnings calls
   - Tool: web search + manual review
   - Output: chokepoint additions, removals, or modifications

2. **EdgarTools 8-K/6-K full-text search** → weekly → weekly-scan/runs/{date}.md
   - Query: capacity expansion / design win / record backlog / supply
     constrained / qualified supplier / production ramp / long-term
     agreement / strategic partnership
   - Filter: sub-$5B market cap (cross-check with Alpha Vantage)
   - Output: new candidate alerts

3. **13F filings** → quarterly → weekly-scan/runs/{date}-13f.md
   - Sources: Situational Awareness LP, specialist watchlist (Hood River,
     William Blair, Baillie Gifford, Sculptor, Slate Path, Caption,
     Bridgeway, Kennedy, Acadian, Alyeska, Point72)
   - Tool: EdgarTools search_filings_full_text on 13F-HR; LLMQuant as
     secondary when available
   - Output: new specialist positions in chokepoint universe

4. **Sentiment refresh** → monthly → appended to CANDIDATE_UNIVERSE.md
   - Checks: analyst coverage count, AI-ETF inclusion (AIQ, BOTZ, ROBO,
     SOXX, SMH), FinTwit/Reddit volume, consensus PT vs price
   - Tool: web search, LunarCrush

### Processing layer (filters applied to candidates — Framework v2.0)

Each candidate is evaluated against the 6-check discovery prompt
(methodology preserved in _archive/DISCOVERY_PROMPT.md; embedded into
the weekly-scan workflow). The checks now map to the v2.0 filter set:

| Check | Filter | Tool | Notes |
|---|---|---|---|
| 0. Balance-sheet primary discovery (NEW v2.0) | DISCOVERY HIERARCHY | EdgarTools 10-Q Screen 3 | Deferred rev / customer deposits — Screen 3 runs FIRST per WEEKLY_SCAN_PROMPT.md execution order; balance sheet leads, bellwether confirms |
| 1. Chokepoint mapping | H10 / H10-extended | CHOKEPOINT_TAXONOMY.md + web search | H10 (AI Infra: NVDA/TSMC/AVGO/MSFT/META/AMD); H10-D (Defense); H10-N (Nuclear); H10-M (Critical Minerals); H10-P (Pharma) |
| 2. Structural filter | H8 (tiered v2.0) | Alpha Vantage + web search | TIER 1 NANO sub-$500M / TIER 2 CATALYST $500M-$2B / TIER 3 COMPOUNDER $2B-$5B / TIER 4 SEGMENT $5B-$15B parent w/ qualifying AI segment |
| 3. Sentiment state | H5 (with PARTIAL-RECOVERING) | Web search + LunarCrush | PARTIAL-RECOVERING re-entry path added v2.0: post-catalyst >25% retrace without thesis-break = entry at 50% tier sizing |
| 4. 8-K/6-K confirmation | H1' (supplementary) | EdgarTools | Confirmation overlay on Screen 3 primary candidates |
| 5. Specialist 13F upgrade | H7 (supplementary) | EdgarTools / LLMQuant | |
| 6. PT-lag cross-check | Contrarian sanity | Web search | |

### Output layer (project files → human decision)

- CANDIDATE_UNIVERSE.md: master list with ACCEPT / WATCH / REJECT
- weekly-scan/runs/: raw scan run output (one file per run, dated)
- research/: pattern discovery and foundational research artifacts
- due-diligence/: per-candidate DD (incl. last30days/ social sweeps)
- trades/: position records (entry thesis, exit rules, post-mortem)
- content/: drafts and published essays / write-ups
- INSIGHTS.md: compound knowledge accumulating across scan runs
- _archive/: preserved obsolete files (old screens/, old screening/, DISCOVERY_PROMPT.md)

## Known framework limitations

1. **Legacy-industrial-capacity-pivot blind spot** (BW pattern): legacy
   industrials with repurposable manufacturing capacity have no leading
   signal until the anchor-customer LOI fires. Documented, not fixable
   without exploding false positives.

2. **Adjacent opportunity classes out of scope**: sector pivots (CIFR),
   M&A pivots (SEI), pre-revenue moonshots (LWLG), geopolitical
   materials (MP/UUUU). These require parallel frameworks.

3. **H10 taxonomy staleness**: if a new chokepoint emerges in bellwether
   discourse and the taxonomy isn't updated within 90 days, the
   framework will miss candidates on that chokepoint.

4. **Small sample**: N=12 design-intent winners, N=10 controls. Hit
   rates are directional, not statistically rigorous.

5. **Tool-stack gaps**: LLMQuant API intermittent; no first-class
   earnings-transcript MCP; LunarCrush thin on micro-caps; no
   automated ETF-inclusion check; foreign filers use 6-K not 8-K.

## Database

None. All data is markdown files on the local filesystem. No
PostgreSQL hub for this project — the data volume doesn't justify it.
If Archos scales to automated daily screening, reconsider.
