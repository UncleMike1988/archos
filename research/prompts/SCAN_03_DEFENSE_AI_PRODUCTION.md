## MANDATORY — READ BEFORE ANYTHING ELSE

Read these files IN FULL before doing anything:

1. /Users/michaelturner/Desktop/Claude Builds/_master_docs/WORKING_PHILOSOPHY.md
2. /Users/michaelturner/Desktop/Claude Builds/archos/CLAUDE.md
3. /Users/michaelturner/Desktop/Claude Builds/archos/CHOKEPOINT_TAXONOMY.md
4. /Users/michaelturner/Desktop/Claude Builds/archos/CANDIDATE_UNIVERSE.md
5. /Users/michaelturner/Desktop/Claude Builds/archos/INSIGHTS.md
6. /Users/michaelturner/Desktop/Claude Builds/archos/DUE_DILIGENCE_CHECKLIST.md

Confirm by stating the LAST LINE of WORKING_PHILOSOPHY.md.
Do not run any commands or make any changes until confirmed read.

---

## SESSION TYPE

THIS IS A TARGETED DISCOVERY SCAN — identifying defense AI companies crossing the threshold from development/R&D/SBIR into production procurement. Uses the newly codified H10-D bellwether extension (2026-05-27 framework evolution).

---

## CONTEXT

The 2026-05-27 framework evolution formally codified the Defense/Space bellwether analog:

H10-D = Binding contract award from DoD, NASA, DARPA, AFRL, Space Force, NRO, SDA, DIA, or named defense prime (Lockheed, Raytheon, Northrop, Boeing, L3Harris, General Dynamics) with disclosed dollar value. IDIQ ceiling alone does NOT qualify — funded task orders or firm-fixed-price awards required.

The nano-cap scan (2026-05-26) found that 7 of 14 candidates (50%) were defense AI. The weekly master scan found CTM, MNTS, ODYS as defense candidates. AISP passed full DD. The defense AI sector is the densest source of Archos-shaped candidates right now — but most prior scans focused on the sub-$100M nano-cap tier.

This scan targets the $100M-$2B tier — defense companies large enough to have real contracts and revenue but small enough for asymmetric upside. The specific signal: a company transitioning from SBIR/STTR grants and R&D contracts into PRODUCTION procurement (firm-fixed-price, LRIP, FRP, OTA production awards). This transition is the defense equivalent of a neocloud signing its first hyperscaler lease.

Known defense AI candidates already in the universe: CTM (unblocked, $65M), MNTS (unblocked, $35-75M), AISP (DD complete, $88M), ODYS ($74M, flagged), SPAI (downgraded), EXYN (rejected). This scan looks ABOVE the nano-cap tier for larger, more established defense companies at the production transition inflection.

---

## TASK: DEFENSE AI PRODUCTION TRANSITION SCAN

### PHASE 1 — 8-K Production Contract Discovery (Primary — 45 min)

**Step 1: EdgarTools 8-K full-text search for production awards**
Run these single-phrase queries against 8-K filings from the last 90 days. Use single-phrase queries only (boolean AND is broken in EdgarTools — confirmed 4x).

Production-signal phrases:
- "firm fixed price"
- "full rate production"
- "low rate initial production"
- "production contract"
- "production order"
- "OTA production"
- "indefinite delivery indefinite quantity" (then cross-filter for disclosed FUNDED amounts)
- "task order" AND defense context (run "task order" alone, filter snippets)

Agency-specific phrases (run each separately):
- "Department of Defense"
- "NAVAIR"
- "Army Contracting Command"
- "Space Force"
- "Space Development Agency"
- "Missile Defense Agency"
- "SOCOM" OR "Special Operations"
- "DARPA" (filter for Phase 3 / production transition, not Phase 1 R&D)

For each hit: real-time market cap verification. Filter to $100M-$2B. Read the 8-K to classify:
- PRODUCTION (firm-fixed-price, LRIP, FRP, OTA production) = H10-D PASS
- DEVELOPMENT (SBIR, STTR, Phase 1/2, CRADA, study contract) = H10-D FAIL (too early)
- IDIQ CEILING ONLY (no funded task order disclosed) = H10-D FLAG (per CTM DD lesson — headline backlog without funded decomposition is misleading)

**Step 2: Defense prime subcontract discovery**
Many sub-$2B defense companies win production work as subcontractors to primes. Search for:
- "subcontract" AND "Lockheed" (run "subcontract" alone, filter)
- "subcontract" AND "Raytheon"
- "subcontract" AND "Northrop"
- "subcontract" AND "L3Harris"
- "subcontract" AND "General Dynamics"
- "subcontract" AND "Boeing defense"
- "teaming agreement" AND defense context

For subcontracts: verify the PRIME contract is production (not R&D). A subcontract on a production program is more valuable than a prime contract on an SBIR.

**Step 3: AI-specific defense vocabulary**
- "autonomous" AND "production" (in 8-K)
- "artificial intelligence" AND "contract award" (in 8-K)
- "machine learning" AND "Department of Defense" (in 8-K)
- "computer vision" AND "defense" (in 8-K)
- "sensor fusion" AND "contract" (in 8-K)
- "counter-UAS" OR "counter-drone" (in 8-K — hot defense AI subcategory)
- "predictive maintenance" AND "military" OR "defense" (in 8-K)
- "ISR" OR "intelligence surveillance reconnaissance" (in 8-K)
- "electronic warfare" AND "AI" OR "machine learning" (in 8-K)

### PHASE 2 — Web Search Discovery (30 min)

**Step 1: Defense AI company landscape**
- "defense AI company stock small cap 2026"
- "defense technology IPO 2025 2026"
- "defense AI startup public Nasdaq NYSE"
- "counter drone company stock"
- "autonomous defense company publicly traded"
- "NDAA onshoring defense technology small cap"
- site:stockanalysis.com defense AI market cap under 2B

**Step 2: Contract award databases**
- "defense contract award May 2026" site:defense.gov
- "DoD contract announcement" May 2026
- USAspending.gov top-level search for AI/autonomous/UAS awards >$5M in last 90 days (if accessible via web)
- "Pentagon AI budget 2026 2027" (macro context for TAM)

**Step 3: Defense AI ETF holdings as discovery vector**
- Pull holdings of defense/aerospace ETFs: ITA, PPA, XAR, DFEN
- Filter for sub-$2B holdings
- Cross-reference against Archos candidate universe — any names NOT already tracked?

### PHASE 3 — Revenue Inflection Cross-Check (15 min)

For every candidate found in Phases 1-2 with market cap $100M-$2B:

**Step 1: Revenue trajectory**
- Pull TTM revenue from most recent 10-Q
- Compare to prior year — is this company showing FIRST-TIME >40% YoY growth?
- Is growth driven by production contract conversion (not just R&D grants)?

**Step 2: Backlog quality (per DD v2.0 Check 5.5)**
- If the company reports "backlog" — decompose: funded vs unfunded vs IDIQ ceiling vs priced options
- Funded-to-total ratio <20% = misleading (CTM lesson: 4.8% funded)
- Backlog growing while revenue declining = paper not converting (CYCU lesson)

**Step 3: Deferred revenue / customer deposits**
- Any first-time deferred revenue appearance?
- Government contract progress billing patterns?
- Per discovery hierarchy: balance-sheet signal qualifies for TIER 2 WATCH even without bellwether fire

### PHASE 4 — Insider Activity Overlay (15 min)

For the top 5-8 candidates from Phases 1-3:
- Pull EdgarTools insider_activity for each
- Flag any with CEO/CFO/Director BUYING into weakness (the AISP pattern)
- Flag any with heavy insider SELLING post-award (the extraction pattern)
- Cross-reference with the H3-contrarian-inverse finding: insider buying is rare (38/39 names sell); when a defense CEO is buying, it's a high-conviction signal

---

## CANDIDATE EVALUATION

For each candidate, apply the defense-specific framework check:

| Check | Defense-specific criteria |
|---|---|
| H10-D | Funded production contract (FFP, LRIP, FRP, funded task order) with disclosed dollar value from DoD/NASA/DARPA/prime. IDIQ ceiling alone = FLAG. SBIR/CRADA = FAIL |
| H8 (tiered) | Sub-$500M = Tier 1 Nano. $500M-$2B = Tier 2 Catalyst |
| H5 | IGNORED or NEUTRAL. Defense AI is getting hotter — check if name has already been "discovered" by defense FinTwit |
| H11 | Going concern + defense company = HIGH RISK (defense contracts don't save insolvent companies — EXYN lesson). Clean balance sheet required |
| Revenue mix | >50% government/defense revenue = H8-D analog. Mixed commercial/defense = weaker signal |
| Contract type | FFP > CPFF > T&M > IDIQ ceiling. Production > development. Prime > sub |
| ITAR/CFIUS | Foreign-origin defense companies face CFIUS risk (SPAI lesson). Flag any non-US-origin |
| Cluster match | Cluster 1 (de-SPAC defense company at 24-36mo), Cluster 4 (gov-anchor concentration), Cluster 5 (broken-IPO defense) |

Do NOT run full DD in this session. Flag candidates for DD queue only.

---

## OUTPUT

Write results to:
/Users/michaelturner/Desktop/Claude Builds/archos/weekly-scan/runs/2026-05-27-defense-ai-production-scan.md

Update CANDIDATE_UNIVERSE.md with any new WATCH candidates.

---

## SESSION END

No git push. No framework changes beyond candidate additions.

Output summary to chat:
- Total candidates found at $100M-$2B tier
- How many have PRODUCTION contracts (H10-D PASS) vs only R&D/SBIR
- Backlog quality assessment (funded % for each)
- Any with insider buying signal (the AISP pattern)
- Any with first-time revenue inflection >40% YoY
- DD queue recommendations (priority ordered)
- Defense AI sector macro assessment: how hot is this space getting? Is H5 IGNORED still realistic or is the sector transitioning to PARTIAL?

STOP after summary.
