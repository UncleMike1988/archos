## MANDATORY — READ BEFORE ANYTHING ELSE

Read these files IN FULL before doing anything:

1. /Users/michaelturner/Desktop/Claude Builds/_master_docs/WORKING_PHILOSOPHY.md
2. /Users/michaelturner/Desktop/Claude Builds/archos/CLAUDE.md
3. /Users/michaelturner/Desktop/Claude Builds/archos/CHOKEPOINT_TAXONOMY.md
4. /Users/michaelturner/Desktop/Claude Builds/archos/CANDIDATE_UNIVERSE.md
5. /Users/michaelturner/Desktop/Claude Builds/archos/INSIGHTS.md
6. /Users/michaelturner/Desktop/Claude Builds/archos/research/pattern-discovery/SIGNAL_CLUSTERS.md

Confirm by stating the LAST LINE of WORKING_PHILOSOPHY.md.
Do not run any commands or make any changes until confirmed read.

---

## SESSION TYPE

THIS IS A TARGETED CHOKEPOINT DISCOVERY SCAN — two related hardware-layer chokepoints that scale linearly with GPU deployment and have NOT been screened by Archos before.

---

## CONTEXT

The AI infrastructure buildout has priced the obvious layers: GPUs (NVDA $5.2T), HBM (MU $1T), networking (AVGO $2T). The next chokepoint layer forming — but not yet priced — sits INSIDE the data center at two levels:

**Chokepoint A: CXL Memory Expansion**
Compute Express Link (CXL) allows memory to be pooled and shared across GPUs/CPUs over a fabric rather than soldered onto each chip. This solves "not enough HBM per GPU" without waiting for HBM4/HBM5 supply to catch up. CXL 2.0/3.0 is going from spec to deployment in 2026-2027. Most CXL controller IP is inside Marvell and Broadcom (too large), but there may be sub-$500M pure-plays making CXL expander modules, controllers, switches, or test equipment.

Why this is a chokepoint: every GPU rack deployed at scale will eventually need CXL-attached memory pooling to optimize memory utilization and reduce cost-per-inference. Without it, GPUs sit idle waiting for memory bandwidth. The economics of inference at scale REQUIRE memory disaggregation.

**Chokepoint B: Rack-Level Power Delivery**
Everyone talks about megawatts to the data center (building level — POWL caught this at 30x). Nobody talks about power delivery INSIDE the rack. Each B200/Vera Rubin rack draws 120-140kW. Power must be converted (AC-DC-point-of-load), distributed (busbars, power shelves), and managed (intelligent PDUs, thermal-aware power balancing) at the rack level. This layer scales LINEARLY with every GPU rack shipped.

Why this is a chokepoint: you can have infinite megawatts at the building and still bottleneck at the rack if the power conversion and distribution can't keep up with GPU density. The move from 40kW/rack (2023) to 140kW/rack (2026) to 250kW+/rack (2028) is a 6x increase that rack power infrastructure wasn't designed for.

---

## TASK: DUAL CHOKEPOINT SCAN

### PHASE 1 — CXL Memory Expansion (45 min)

**Step 1: EdgarTools 10-K full-text search**
Run these single-phrase queries against 10-K filings, sub-$2B market cap:
- "Compute Express Link"
- "CXL memory"
- "CXL controller"
- "CXL expander"
- "memory pooling"
- "disaggregated memory"
- "memory fabric"
- "CXL switch"

For each hit: verify market cap via web search (EdgarTools XBRL is stale — MANDATORY real-time verification per CLAUDE.md governance rule). Filter to sub-$2B. Read the snippet to determine if CXL is core product or just a mention.

**Step 2: Web search for CXL pure-plays**
- "CXL memory company IPO 2025 2026"
- "CXL startup public Nasdaq NYSE"
- "Compute Express Link stock small cap"
- "CXL memory expander manufacturer publicly traded"
- "CXL consortium members public company"
- "memory disaggregation company stock"

**Step 3: Supplier mapping from NVIDIA CXL specs**
NVIDIA's Grace Hopper and Vera Rubin platforms support CXL. Search for:
- NVIDIA CXL partner or supplier names in recent GTC presentations
- Any sub-$2B company named in CXL Consortium press releases
- Companies making CXL validation/test equipment (the AEHR analog for CXL)

**Step 4: Cross-reference with deferred revenue**
For any CXL company found in Steps 1-3, pull most recent 10-Q and check:
- First-time deferred revenue appearance?
- Customer deposit or prepayment language?
- Balance-sheet signal per the new discovery hierarchy (leads bellwether by 1-3 quarters)

### PHASE 2 — Rack-Level Power Delivery (45 min)

**Step 1: EdgarTools 10-K full-text search**
Run these single-phrase queries against 10-K filings, sub-$2B market cap:
- "power distribution unit"
- "rack power"
- "48 volt"
- "busbar" AND "data center" (run separately, cross-filter in post)
- "power shelf"
- "point of load converter"
- "rack PDU"
- "intelligent PDU"
- "power conversion" AND "GPU" (run separately, cross-filter)
- "liquid cooled power"

For each hit: real-time market cap verification. Filter to sub-$2B. Determine if data center power delivery is core product or peripheral mention.

**Step 2: Web search for rack power pure-plays**
- "data center rack power delivery company stock"
- "48V power conversion data center publicly traded"
- "GPU rack power distribution manufacturer"
- "high density rack PDU company Nasdaq NYSE"
- "data center power shelf manufacturer small cap"
- "NVIDIA rack power supplier"
- site:stockanalysis.com "power distribution" "data center" market cap

**Step 3: Supplier mapping from NVIDIA rack power specs**
NVIDIA publishes rack-level power requirements for DGX/HGX platforms. Search for:
- Named power delivery suppliers in NVIDIA DGX SuperPOD documentation
- OEM rack power partners for Dell, HPE, Supermicro GPU server lines
- Companies making the AC-DC or DC-DC conversion stages specifically for AI racks

**Step 4: POWL supply chain extension**
POWL caught switchgear at the building level. Who supplies components TO rack-level power systems? Run the two-degree supplier mapping:
- POWL — who are POWL's component suppliers?
- Vertiv (too large) — who supplies Vertiv's rack PDU product line?
- Delta Electronics, Lite-On, Murata — are any sub-$2B subsidiaries or divisions publicly traded?

**Step 5: Cross-reference with deferred revenue**
Same as Phase 1 Step 4 — for any rack power company found, check balance sheet for leading signals.

---

## CANDIDATE EVALUATION

For each candidate surfaced, run the quick framework check:

| Check | Criteria |
|---|---|
| H10 (or balance-sheet lead) | Bellwether named the chokepoint category, OR first-time deferred revenue >$10M from chokepoint-adjacent end-market |
| H8 (tiered) | Sub-$500M = Tier 1 Nano; $500M-$2B = Tier 2 Catalyst |
| H5 | IGNORED or NEUTRAL sentiment (check analyst coverage count, ETF inclusion, FinTwit volume) |
| H11 | No going concern, positive FCF or >18mo runway |
| Cluster check | Does it match any of the 7 signal clusters? (Cluster 1 de-SPAC, Cluster 2 squeeze, Cluster 3 spinoff, Cluster 4 gov-anchor, Cluster 5 broken-IPO) |

Do NOT run full DD in this session. Flag candidates for DD queue only.

---

## OUTPUT

Write results to:
/Users/michaelturner/Desktop/Claude Builds/archos/weekly-scan/runs/2026-05-27-cxl-rack-power-scan.md

Update CANDIDATE_UNIVERSE.md if any candidate passes the quick framework check (add to appropriate WATCH tier).
Update CHOKEPOINT_TAXONOMY.md if a new chokepoint surface is confirmed (add to Active or Monitor).

---

## SESSION END

No git push. No framework changes beyond taxonomy/candidate additions.

Output summary to chat:
- How many CXL companies found (public vs private)
- How many rack power companies found
- Any TIER 1/TIER 2 candidates flagged for DD
- Taxonomy recommendations
- Is CXL investable today or still 12-18 months from having a public pure-play?
- Is rack power a real chokepoint surface or is it too fragmented?

STOP after summary.
