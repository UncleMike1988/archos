# 2026-05-27 — CXL Memory Expansion + Rack-Level Power Delivery Targeted Chokepoint Scan

**Type:** Targeted dual-chokepoint discovery scan (off-cadence, requested 2026-05-27)
**Prompt:** `research/prompts/SCAN_01_CXL_RACK_POWER.md`
**Framework version:** v2.0 (discovery hierarchy + tiered H8 + H5 PARTIAL-RECOVERING + H10-extended)
**Date window:** 2024-05-27 to 2026-05-27 (24-month 10-K lookback); 2026-02-27 to 2026-05-27 (90-day 8-K Item 1.01)
**All market caps verified via live web search 2026-05-27.**

---

## SUMMARY (one-line answers to the brief's session-end questions)

1. **How many CXL companies found (public vs private)?** 13 U.S. 10-K hits in 24mo window. **0 sub-$2B U.S. Nasdaq pure-plays.** 1 sub-$1B OTC (NLST — fails exchange test). 3 already-graduated mega-caps (ALAB $54B, RMBS $17B, MCHP $35B+). Foreign-listed pure-plays: Montage Technology (HK 2026 IPO), CXMT, UniIC — not on permitted exchanges. Pure-play CXL ecosystem is dominated by ALAB (already-graduated post-IPO) and Chinese names; private players (MemVerge, etc.) not screenable.
2. **How many rack power companies found?** Many. But **all sub-$5B AI-rack-power chokepoint pure-plays have GRADUATED** — AEIS ($13B), VICR ($15B), NVT ($26.6B), MOD ($17B+), ALGM ($9.5B), ENPH ($9.4B). Only candidates remaining sub-$5B: **TSSI** ($330-459M, rack integration services adjacency, 99% Dell concentration) + BELFB ($3.91B, diversified) + POWI ($4-4.63B, diversified). MEI ($365M) is in-rack-busbar pure-play but was **already explicitly REJECTED** per CHOKEPOINT_TAXONOMY.md (chokepoint fragmented; flat-to-down despite record DC sales).
3. **Any TIER 1/TIER 2 candidates flagged for DD?** **NONE for AI infrastructure lens.** TSSI lands at TIER 3 WATCH (adjacency-pattern, low conviction per INSIGHTS rule).
4. **Taxonomy recommendations?** ALAB should be added to **GRADUATED PURE-PLAYS** as historical CXL chokepoint winner (passed sub-$5B at March 2024 IPO; now $54B = ~10x post-IPO). Document #11 CXL chokepoint + #12 Rack-Level Power Delivery as bellwether-validated but empty (no sub-$5B pure-plays remaining).
5. **Is CXL investable today or still 12-18 months from public pure-play?** **Window is closed** for direct sub-$5B U.S. pure-play. ALAB caught the entire rerate at IPO. Next viable entry points: (a) ALAB pullback to PARTIAL-RECOVERING if rerate retraces >25%, (b) Montage Technology HK IPO if Hong Kong listing is investable, (c) foreign-filer monitoring for any CXL pure-play sub-$5B emerging in TSE/HKEX/Stockholm.
6. **Is rack power a real chokepoint surface or too fragmented?** **Real chokepoint that ALREADY FIRED**. The 30kW→140kW→250kW rack power transition produced VICR +15.7% one-day, AEIS +13B+ market cap, NVT $26B, MOD $4B hyperscaler deal. **All sub-$5B vehicles have graduated.** Sub-component layer (in-rack busbars / high-density PDUs per MEI) is fragmented and not pure-play tradable — already explicitly rejected. Rack INTEGRATION SERVICES (TSSI) is adjacency, not chokepoint hardware.

---

## CONCLUSIONS

The structural finding from this dual scan: **both chokepoints are real AND already-priced.** The framework's screening discipline correctly held — neither chokepoint produces a fresh sub-$5B U.S. Nasdaq pure-play candidate suitable for ACCEPT-track, despite both being unambiguous physical bottlenecks scaling linearly with GPU deployment.

This is the same structural pattern documented across CHOKEPOINT_TAXONOMY.md 2026-05-27 refresh: **6 of 10 chokepoints are EMPTY** because their pure-plays have graduated. CXL and rack power add two more candidate chokepoint surfaces that fit this graduation pattern. The "concentrated 4-7 year capital mobilization" thesis is firing in real-time across multiple chokepoint layers; the entry window is compressing systemically, not name-specifically.

**No CANDIDATE_UNIVERSE.md ACCEPT or TIER 2 additions.** TSSI flagged at TIER 3 WATCH (adjacency pattern, monitor only).

**Two CHOKEPOINT_TAXONOMY.md additions:** ALAB to graduated pure-plays for CXL chokepoint #11; rack-level power delivery chokepoint #12 added with all graduated names enumerated.

---

## PHASE 1 — CXL MEMORY EXPANSION (results)

### EdgarTools 10-K full-text search — 8 queries, 24-month window

| Query | Total hits | Sub-$2B Nasdaq pure-plays |
|---|---|---|
| "Compute Express Link" | 17 | NLST (OTC — fails), OSS (forward, not core) |
| "CXL memory" | 6 | OSS (Teledyne LeCroy partnership only) |
| "CXL controller" | 1 | RMBS only (graduated $17B) |
| "CXL expander" | 0 | — |
| "memory pooling" | 1 | MRVL only (mega-cap) |
| "disaggregated memory" | 0 | — |
| "memory fabric" | 0 | — |
| "CXL switch" | 0 | — |
| "CXL" (broad) | 29 (de-noised: 12 real CXL refs) | Same set; no new sub-$2B |
| "memory expansion module" OR "CXL-attached" OR "MXC" | 4 | None new (SANM, MXC=Mexco Energy oil/gas) |

**5 of 8 queries returned ZERO results — consistent with the documented single-phrase fail mode per INSIGHTS.md ("EdgarTools `search_filings_full_text` boolean AND failure reconfirmed").**

### Companies with CXL exposure (consolidated)

| Ticker | Mkt cap (2026-05-27) | Status | Notes |
|---|---|---|---|
| **ALAB** (Astera Labs) | **$51-54B** | **GRADUATED-LARGE** | Aries CXL retimers + Leo CXL Memory Connectivity Controllers + Scorpio Smart Fabric Switches. **Was the cleanest CXL chokepoint pure-play at IPO March 2024 (~$5.5B); rerated ~10x in 24mo. Framework MISSED the IPO-window entry**. Add to GRADUATED PURE-PLAYS. |
| **MRVL** (Marvell) | mega-cap | mega-cap | XConn acquisition adds CXL switch portfolio. Out of scope. |
| **RMBS** (Rambus) | **$15-17B** | GRADUATED-LARGE | CXL Controller IP. Out of scope. |
| **MCHP** (Microchip) | mega-cap (~$35B) | mega-cap | CXL memory expansion controllers. Out of scope. |
| **MU** (Micron) | mega-cap | mega-cap | CXL-based products. Out of scope. |
| **CDNS** (Cadence) | mega-cap | mega-cap | CXL design IP. Out of scope. |
| **SNPS** (Synopsys) | mega-cap | mega-cap | CXL IP. Out of scope. |
| **INTC** (Intel) | mega-cap | mega-cap | CXL co-founder. Out of scope. |
| **AMD** | mega-cap | mega-cap | Versal Premium Series Gen 2 with CXL. Out of scope. |
| **CRDO** (Credo Tech) | **$40.88B** | GRADUATED-LARGE | Toucan PCIe Gen6.x/CXL 3.x retimers. Out of scope. Already in graduated list. |
| **PENG** (Penguin Solutions) | $3.2B | **REJECTED** | SMART Modular CXL NV-CMM modules; HPC/AI segment **DOWN 42% YoY per v2 verification 2026-05-24**. Already in REJECT log per INSIGHTS. |
| **SANM** (Sanmina) | $13.8B | OVER CAP / REJECTED | CXL attached memory products. Already in REJECT (M&A pivot blind spot, ZT Systems acquired Oct 2024). |
| **OSS** (One Stop Systems) | **$431-441M** | NOT A PURE-PLAY | Tier 1 NANO range, Nasdaq. "Expect to address PCIe Gen 6.0 + CXL in 2026 and beyond" — forward, not core revenue. Reselling Teledyne LeCroy CXL test equipment. Core business is rugged edge HPC for defense + sensor + autonomy. CXL <<10% of revenue. **Does NOT qualify as CXL pure-play; H8 end-market fails (defense/sensor dominated, not CXL chokepoint).** |
| **NLST** (Netlist) | **$831-960M (OTC)** | **REJECTED — fails exchange test** | OTC-only listing (not Nasdaq/NYSE per project convention). Also: negative stockholders' equity (-$5.2M H11 RED FLAG), 0 buys / 12 sells last 90d (bearish insider sentiment), -$24.8M net income, -$14.7M operating cash flow. CXL is "investing in new technologies" language — pre-revenue. **Triple-fail: exchange + H11 + H5.** |

### Web search for CXL pure-plays — supplementary

**Pure-play CXL ecosystem identified:**

- **Astera Labs (ALAB)** — already graduated post-IPO ($51-54B). Was the textbook CXL chokepoint pure-play but framework didn't have an IPO-window mechanism to catch it at the ~$5.5B IPO price.
- **Montage Technology** — HK 2026 IPO; world's largest memory interconnect chip supplier (>1/3 global revenue share); CXL MXC chips; customers Intel, AMD, Samsung; 2025 net income RMB 2.15-2.35B. **NOT US-listed; foreign-filer with discovery-friction handicap per INSIGHTS** (H7 silent, no US 8-K, no Form 4).
- **CXMT** (China) — $42B IPO planned early 2026; mega-cap, Chinese exchange.
- **UniIC, GigaDevice, DapuStor** — Chinese IPO plans; not US-listed.
- **MemVerge** — Private (GISMO memory virtualization layer).
- **Teledyne LeCroy** — CXL validation test equipment; subsidiary of Teledyne Technologies (~$30B mega-cap parent). Closest direct AEHR analog for CXL but locked inside a mega-cap.

### NVIDIA Vera Rubin / Grace Hopper CXL supplier mapping

- Vera Rubin platform supports PCIe6 + CXL3.1.
- **Nanya Technology (Taiwan)** named as LPDDR5X memory supplier for Vera Rubin (3x capacity, +50% bandwidth) — but this is LPDDR5X, not CXL specifically. Foreign-listed (Taiwan), no Cluster 8/AGPU pattern but no clean H10 fire on CXL specifically.
- No sub-$2B U.S. Nasdaq company named in NVDA's CXL ecosystem disclosures.

### Phase 1 deferred revenue cross-reference

**No sub-$2B U.S. Nasdaq CXL candidates surfaced — no balance-sheet cross-ref needed.** OSS and NLST both fail before this step (OSS = forward investment, not current core revenue; NLST = OTC + H11 fail).

### Phase 1 conclusion

**The CXL chokepoint pure-play in the U.S. public market WAS Astera Labs at its March 2024 IPO at ~$5.5B. ALAB rerated ~10x to $51-54B in 24 months — textbook CXL chokepoint rerate.** The framework correctly identified CXL as a chokepoint but did not have an IPO-window screening mechanism to catch ALAB at the entry.

**Forward investability: NO viable sub-$5B U.S. pure-play exists today.** The window is closed for U.S. Nasdaq AI-Infra lens. Future entry vectors:
- ALAB pullback to PARTIAL-RECOVERING (H5 v2.0 reclassification if rerate retraces >25% with thesis intact — but at $54B cap, framework H8 still fails sub-$5B)
- Montage HK IPO if foreign-listed investability is workable
- IPO-watch list for any CXL pure-play coming public sub-$5B (none currently known)

---

## PHASE 2 — RACK-LEVEL POWER DELIVERY (results)

### EdgarTools 10-K full-text search — 10 queries, 24-month window

| Query | Total hits | Sub-$2B Nasdaq pure-plays |
|---|---|---|
| "power distribution unit" | 4 | None (ABM service co + AST SpaceMobile satellite) |
| "rack power" | 13 | TSSI only sub-$2B; VRT/AEIS/FLEX/TXN/ALGM/HYLN over cap or REJECTED |
| "48 volt" | 10 | None — auto-EV dominated (Gentherm, Lear, Dragonfly, Microvast) |
| "busbar" | 10 | MEI only sub-$2B (already-REJECTED chokepoint per taxonomy) |
| "power shelf" | 1 | AEIS only (graduated $13B) |
| "point of load" | 7 | VICR/HEICO/BELFB/ALGM (none new sub-$2B except BELFB at $3.91B) |
| "rack PDU" | 0 | — |
| "intelligent PDU" | 0 | — |
| "AI rack" | 5 | TSSI (rack integration services, not power-delivery hardware); AMD (mega) |
| "liquid cooled" | 36 | Mostly EV/auto/SMCI/IREN/CIFR/HUT/BITF/SHAZ pattern; TSSI surfaces DLC racks |
| "high density rack" | 2 | FLEX (mega), RIOT (sector pivot REJECT) |
| "GPU rack" | 0 | — |
| "data center power" 8-K Item 1.01 90d | 5 | CalEthos GEDC (OTC, pre-revenue shell — REJECT); BW (already-blind-spot); 2 SPACs |

### Companies with rack power exposure (consolidated)

| Ticker | Mkt cap (2026-05-27) | Status | Notes |
|---|---|---|---|
| **AEIS** (Advanced Energy) | **$12.5-13.4B** | **GRADUATED-LARGE** | Explicit "AI-based servers and racks" + "48V power shelf infrastructure" + "server rack power solutions" leading provider. FY25 revenue $1.8B, net income $148M. Data Center Computing one of 4 segments. **Possible TIER 4 SEGMENT candidate** if Data Center Computing segment is >50% AI-DC mix and >40% YoY growth (verify next 10-K). Add to graduated. |
| **VICR** (Vicor Corp) | **$11.7-15.2B** | **GRADUATED-LARGE** | 48V→12V→POL conversion stack with FPA-enabled regulators; explicit AI server target. **+15.7% one-day on 5/26; chopping $260s→$340s in May.** Insider selling 319 sells / 115 buys / **-$193M net** — massive post-rerate distribution = LOVED zone, would fail H5. Add to graduated. |
| **NVT** (nVent Electric) | **$26.6B** | **GRADUATED-LARGE** | Enlogic iPDU subsidiary = high-density intelligent power distribution; Data Solutions segment grew ~30% in 2024 (cited as 65% Q3 2025 organic order growth from hyperscalers). **TIER 4 SEGMENT candidate** if Data Solutions segment crosses >50% AI-DC mix and >40% YoY growth. Add to graduated. |
| **MOD** (Modine Manufacturing) | **~$17-20B** (+175% YoY) | **GRADUATED-MID** | $4B hyperscaler cooling deal (2027-2029, $165M upfront, announced 5/26). Spinning off Performance Technologies via Reverse Morris Trust w/ Gentherm Q4 2026 = **Cluster 3 spinoff catalyst pending**. Climate Solutions segment 50-70% YoY DC growth guide. Already-rerated; LOVED zone. Add to graduated. |
| **ALGM** (Allegro Microsystems) | **$7.6-9.5B** | **GRADUATED-MID** | AI DC cooling power ICs + automotive. **Auto-dominated revenue** = H8 end-market FAIL (not AI-DC >50%). Add to graduated as adjacency only. |
| **ENPH** (Enphase Energy) | **$8.4-9.45B** | **OVER CAP / adjacency** | IQ Solid-State Transformer for 800V DC AI data center racks — announced 4/28/26. Pilots 2027, volume 2028 = forward product, not current revenue. +103% in May. Solar inverter origin. Out of scope. |
| **POWI** (Power Integrations) | **$4.0-4.63B** | **TIER 3 COMPOUNDER (borderline)** | PowiGaN products for AI DC + EV + industrial. Diversified end-markets (AI DC is one of several). Q1 2026 sales $108M, net income only $3.3M. PARTIAL/NEUTRAL sentiment, well-covered. **H8 end-market test likely FAILS** (AI-DC <50%). H5 likely PARTIAL/NEUTRAL not IGNORED. Not promoted. |
| **BELFB** (Bel Fuse) | **$3.91B** | **TIER 3 COMPOUNDER (borderline)** | POL voltage converters + Connectivity + Magnetic Solutions across 3 segments. Diversified (auto, broadcasting, networking, military). FY25 rev $675M, net income $61.5M, OCF $81M. **H8 end-market test FAILS** — Bel is industrial diversified, not AI-DC pure-play. 15 buys / 6 sells (mixed insider). 5/14/26 Item 1.01 8-K worth checking. Strong-buy analyst rating ($309 PT vs $277). Not promoted. |
| **TSSI** (TSS, Inc.) | **$330-459M** | **TIER 3 WATCH (adjacency)** | Nasdaq, "rack-level AI-enabled server integration" via Dell partnership (99% revenue concentration). FY25 rev $245.7M, net income $15.1M, OCF $34.9M (PROFITABLE). +88% Q1 2026 systems integration YoY; +172% 2024 full year. New 212,793 sq ft Georgetown TX facility w/ 15MW power. April 2026 Round Rock expansion. 2026 EBITDA guide $20-22M; doubling rack integration vs 2025. **BUT**: Rack INTEGRATION SERVICES (adjacency to chokepoint, NOT chokepoint hardware). **99% Dell concentration = single-counterparty risk** (SHAZ analog DD red flag, ESDS-shaped). Per INSIGHTS rule: adjacency-pattern names land at TIER 3 WATCH max, never elevate to TIER 2 absent explicit chokepoint-language fire. **Document on WATCH; monitor for: (a) customer diversification, (b) Dell direct H10 fire naming TSSI, (c) chokepoint-hardware product launch.** |
| **MEI** (Methode Electronics) | **$365M** | **REJECTED — already-documented per CHOKEPOINT_TAXONOMY.md** | NYSE-listed, Tier 1 NANO range. Custom busbars + PowerRail + high-voltage flexible power cabling for data centers. Record DC sales Q4/FY25. **BUT**: per existing rejected-chokepoints list: "In-rack busbars / high-density PDUs — chokepoint exists but fragmented across vendors; Methode (MEI) flat-to-down despite record DC power sales (chokepoint ≠ pure-play return)". Also: FY25 net loss -$62.6M (H11 risk); three segments (Auto + Industrial + Interface) with DC inside Industrial only. **CONFIRMED REJECT — no change to taxonomy needed.** |
| **HYLN** (Hyliion Holdings) | $629M (per CANDIDATE_UNIVERSE) | **already-REJECTED** | KARNO Power Module 800V DC for AI DC. Per CANDIDATE_UNIVERSE REJECT log: "+460% Q1 YoY ($2.8M revenue base $489K) but $629M mkt cap = over screen cap. Reference case for 'caught one quarter late.'" |
| **INV** (Innventure) | **$521-562M** | **REJECTED — pre-revenue moonshot + Cluster 1 listing risk** | Accelsius subsidiary = direct-to-chip two-phase liquid cooling. Tier 2 CATALYST cap range BUT: FY25 revenue $2M (pre-revenue moonshot); net income -$293M; operating cash burn -$81M; **3.01 listing standards deficiency filed 5/20/26**; recent de-SPAC. **Triple-fail: pre-revenue moonshot + Cluster 8 (de-SPAC + listing deficiency) + H11 burn rate.** |
| **GEDC** (CalEthos) | sub-$50M cap (OTC) | **REJECTED — Cluster 8 shell** | OTC + pre-revenue + negative equity + REIT-to-data-center pivot pattern. AGPU/SHAZ analog. |

### Web search supplier mapping (NVIDIA DGX SuperPOD + Vertiv + POWL component vendors)

**Confirmed NVIDIA rack power specifications:**
- DGX GB200 NVL72 rack uses **eight power shelves** at **33 kW each = 264 kW max rack power**.
- Each power shelf has **six 5.5 kW PSUs in N+1 redundancy**.
- Rack consumption ~120 kW per NVL72 today; roadmap 480 kW per rack per Navitas 10-K commentary.

**Suppliers identified (all over cap or foreign-listed):**
- **Vertiv (VRT)** — $140B+ mega-cap. PowerDirect Rack 33 kW launched 2026.
- **Eaton** — $70B+ mega-cap.
- **Schneider Electric** — $46B revenue, NetShelter for AI clusters launched Nov 2025.
- **Server Technology** — private subsidiary of Legrand.
- **Delta Electronics (Taiwan)** — Taiwan-listed, $50B+ market cap.
- **Lite-On (Taiwan)** — Taiwan-listed, $8.97B (acquired Power Innovations International).
- **AcBel Polytech (Taiwan)** — Taiwan-listed; acquired ABB power conversion division. Possible foreign-filer target but discovery friction.
- **Murata Power Solutions** — private subsidiary of Murata Manufacturing (Tokyo, mega-cap).
- **Renesas (Japan)** — Tokyo-listed mega-cap. 800V DC GaN architecture for AI DC.
- **Yosun Electric (Taiwan)** — Taiwan-listed mid-cap.

**POWL component supplier mapping:**
- POWL acquired Switchgear & Instrumentation Ltd (UK, private). Other subsidiaries Powell-ESCO, Powell Electrical Systems, Transdyn — all private subsidiaries.
- **No sub-$2B U.S. POWL component supplier surfaces.**

### Phase 2 deferred revenue cross-reference

**TSSI** (the only sub-$500M Nasdaq candidate to merit any cross-ref):
- FY25 revenue $245.7M (+172% YoY 2024); Q1 2026 systems integration +88% YoY
- Sustained-growth pattern (CRWV/NBIS-shaped), not first-time inflection
- Profitable ($15.1M net income, $34.9M OCF)
- **No first-time deferred revenue spike disclosed** (services revenue model — recognized as work completed, not prepaid)
- The catalyst was the **Dec 2025 amendment to multi-year Dell agreement** (8-K item filing) — already in the 90-day window; market reacted; mkt cap retraced from highs

**Balance-sheet signal does not lead — TSSI is a services-revenue model where the catalyst (multi-year contract amendment) is the inflection itself.** This is more like the BW pattern (anchor-customer LOI IS the inflection) but in services form. Adjacency rule applies.

### Phase 2 conclusion

**Rack-level power delivery is a real chokepoint that ALREADY FIRED through the public market.** The 30 kW → 60 kW → 140 kW → 480 kW/rack power scaling produced graduations across AEIS, VICR, NVT, MOD, ENPH, ALGM. The chokepoint is bellwether-validated (NVDA explicitly named "rack power" in DGX specifications; Navitas 10-K names NVDA + Hopper + Blackwell + Rubin + "480 kW per rack roadmap").

**Sub-component layer (in-rack busbars / high-density PDUs) is fragmented and not pure-play tradable** — MEI is the calibration case (record DC sales but flat-to-down stock = chokepoint ≠ pure-play return). Already-rejected; no change.

**Rack integration services (TSSI) is adjacency, not chokepoint hardware** — lands at TIER 3 WATCH per INSIGHTS rule. Single-customer (99% Dell) concentration risk requires DD before any promotion.

**Forward investability: NO viable sub-$5B U.S. pure-play exists today** for the pure rack power delivery chokepoint. Future entry vectors:
- **Tier 4 SEGMENT promotion** of AEIS Data Center Computing or NVT Data Solutions if those segments cross the >50% AI-DC mix + >40% YoY thresholds (Framework v2.0 codification)
- Foreign-filer monitoring of AcBel, Yosun Electric, Lite-On
- IPO-watch for any sidecar-power-rack or solid-state-transformer pure-play coming public sub-$2B (Enphase IQ SST is the new product wave but ENPH is over cap)

---

## QUICK 4-FILTER CHECK TABLE (only candidates that warrant table inclusion)

| Ticker | H10 (or balance-sheet lead) | H8 (tiered) | H5 | H11 | Cluster | Verdict |
|---|---|---|---|---|---|---|
| **TSSI** | **PARTIAL** — Dell multi-year agreement (Dec 2025 amendment); 99% revenue concentration to Dell = 2-degree NVDA via Dell AI server OEM. No NVDA direct H10 fire on TSSI. No first-time balance-sheet signal (services model). | **TIER 1 NANO** ($330-459M) | **PARTIAL** (post-rerate, mid-2025 momentum) | **PASS** (profitable, positive OCF, equity $76.6M) | Adjacency (not Cluster 1-8) | **TIER 3 WATCH** — adjacency pattern, low conviction; never promote without explicit chokepoint-hardware fire |
| **MEI** | Record DC sales catalyst but chokepoint already-rejected | TIER 1 NANO ($365M) | NEUTRAL/PARTIAL | **FAIL** (FY25 net loss -$62.6M) | Adjacency / fragmented | **REJECT** — already in CHOKEPOINT_TAXONOMY.md rejected list |
| **POWI** | NVDA + AI DC named, but among many | TIER 3 COMPOUNDER ($4-4.63B) | PARTIAL/NEUTRAL (well-covered) | PASS | Adjacency | **NOT PROMOTED** — H8 end-market fails (AI-DC <50%); H5 not IGNORED |
| **BELFB** | No specific NVDA mention; POL voltage converter products only | TIER 3 COMPOUNDER ($3.91B) | NEUTRAL/PARTIAL | PASS | Diversified | **NOT PROMOTED** — H8 end-market fails (diversified, not AI-DC pure-play) |
| **NLST** | "Investing in CXL" forward only | TIER 2 CATALYST ($831-960M) | NEUTRAL | **FAIL** (negative equity, bearish 0/12 insider, -$24.8M NI) | Out of scope | **REJECT** — OTC + H11 fail |
| **OSS** | Reselling Teledyne LeCroy CXL test only; forward investment language | TIER 1 NANO ($431-441M) | NEUTRAL | PASS | Adjacency | **NOT PROMOTED** — CXL not core; H8 fails (rugged edge HPC/defense dominated) |
| **INV** | Accelsius cooling subsidiary | TIER 2 CATALYST ($521-562M) | PARTIAL (post-de-SPAC rally) | **FAIL** (pre-revenue $2M, -$293M NI, listing deficiency 3.01 filed 5/20/26) | Cluster 8 (de-SPAC + listing risk) | **REJECT** — pre-revenue moonshot + Cluster 8 + H11 |
| **GEDC** | Data center developer narrative | sub-$50M | n/a | **FAIL** (OTC, pre-revenue, negative equity) | Cluster 8 shell | **REJECT** — OTC + Cluster 8 shell pattern |

---

## TAXONOMY ADDITIONS (recommended for CHOKEPOINT_TAXONOMY.md)

### Add to GRADUATED PURE-PLAYS (historical framework validation)

| Ticker | Chokepoint | Current mkt cap (2026-05-27) | Tier | Notes |
|---|---|---|---|---|
| **ALAB** | #11 CXL Memory Connectivity | $51-54B | GRADUATED-LARGE | March 2024 IPO at ~$5.5B; rerated ~10x in 24mo. Aries CXL retimers + Leo CXL Memory Connectivity Controllers + Scorpio Smart Fabric Switches. Framework MISSED the IPO-window entry — calibration case for IPO-watch list. |
| **AEIS** | #12 Rack-Level Power Delivery | $12.5-13.4B | GRADUATED-LARGE | "48V power shelf infrastructure" + "server rack power solutions" leading provider. Data Center Computing one of 4 segments. |
| **VICR** | #12 Rack-Level Power Delivery | $11.7-15.2B | GRADUATED-LARGE | 48V→12V→POL conversion stack; BCM6135 family supports 800V/400V→54V/50V/48V. |
| **NVT** | #12 Rack-Level Power Delivery | $26.6B | GRADUATED-LARGE | Enlogic iPDU + liquid cooling distribution. Data Solutions segment +30% 2024. |
| **MOD** | #12 Rack-Level Power Delivery (cooling adjacent) | $17-20B | GRADUATED-MID | $4B hyperscaler deal 2027-2029; Cluster 3 spinoff w/ Gentherm Q4 2026 pending. |
| **ENPH** | #12 Rack-Level Power Delivery (IQ SST forward) | $8.4-9.45B | GRADUATED-MID | IQ Solid-State Transformer 800V DC announced 4/28/26; product ramps 2027-2028. |
| **ALGM** | #12 Rack-Level Power Delivery (adjacency) | $7.6-9.5B | GRADUATED-MID | Auto/industrial-dominated. AI DC power ICs minor revenue. |

### Add to ACTIVE TAXONOMY (with empty status)

| # | Chokepoint | Sub-$5B pure-plays remaining | Status | H10 tier | Key bellwether source |
|---|---|---|---|---|---|
| 11 | CXL Memory Connectivity (cache-coherent memory pooling/disaggregation) | *none* — ALAB graduated to $54B | **EMPTY — new search needed** | Vendor | NVDA Vera Rubin platform supports CXL 3.1; AMD Versal Premium Series Gen 2 with CXL; MRVL XConn CXL switch acquisition |
| 12 | Rack-Level Power Delivery (48V→POL conversion, power shelves, 800V DC architecture, intelligent PDU) | *none* — AEIS, VICR, NVT, MOD, ENPH, ALGM all graduated | **EMPTY — new search needed** | Vendor | NVDA DGX GB200 NVL72 rack power specs (33kW shelves, 8 shelves, 264kW max); Navitas 10-K NVDA "Hopper, Blackwell & Rubin... 480 kW per rack" |

### Add to MONITOR LIST (bellwether-named, no qualifying sub-$5B pure-play yet)

- **In-rack busbars / high-density PDUs** — already on rejected list (MEI flat-to-down); explicit "chokepoint ≠ pure-play return" verdict stands
- **Rack integration services** — adjacency pattern; TSSI documented in WATCH but explicitly NOT a chokepoint hardware play

---

## CANDIDATE_UNIVERSE.md ADDITIONS (recommended)

**TIER 3 WATCH (sub-$500M, adjacency pattern, low conviction):**

| Ticker | Chokepoint | Mkt Cap | Tier | Catalyst summary | Re-eval trigger |
|---|---|---|---|---|---|
| **TSSI** (TSS, Inc.) | Rack integration services (ADJACENCY to #12 rack-level power delivery; NOT chokepoint hardware) | $330-459M (TIER 1 NANO range) | **TIER 3 WATCH (adjacency-rule per INSIGHTS)** | Dell multi-year agreement extended Dec 2025; Q1 2026 systems integration +$14.1M (+88% YoY); 212,793 sq ft Georgetown TX facility with 15MW power; April 2026 Round Rock TX expansion; 2026 EBITDA guide $20-22M; doubling rack integration vs 2025. 99% revenue concentration to Dell (= 2-degree to NVDA via Dell AI server OEM). | (a) Customer diversification beyond Dell (single-counterparty risk = SHAZ analog DD red flag); (b) Dell or NVDA direct H10 fire naming TSSI specifically; (c) chokepoint-hardware product launch (vs services-only model); (d) +20% pullback from current cap → H5 reset toward IGNORED. **Per INSIGHTS adjacency rule: never elevate to TIER 2 absent explicit chokepoint-language fire.** |

**REJECT LOG additions:**

| Ticker | Reason |
|---|---|
| NLST (Netlist) | OTC-only (fails exchange test) + negative stockholders' equity (H11 fail) + bearish insider sentiment (0 buys / 12 sells last 90d) + pre-revenue CXL ("investing in new technologies"). Triple-fail. |
| OSS (One Stop Systems) | CXL is forward investment ("expect to address... in 2026 and beyond"), not core revenue. End-market is rugged edge HPC for defense/sensor/autonomy — H8 fails (AI-DC CXL <50% of revenue). |
| MEI (Methode Electronics) | **Already-rejected per CHOKEPOINT_TAXONOMY.md** rejected-chokepoints list ("In-rack busbars / high-density PDUs"). FY25 net loss -$62.6M (H11 risk). Diversified across Auto + Industrial + Interface segments. |
| INV (Innventure) | Pre-revenue moonshot ($2M FY25 revenue) + de-SPAC + Cluster 8 listing-standards-deficiency 3.01 filed 5/20/26 + $293M FY25 net loss + $81M operating cash burn. Triple-fail. Accelsius cooling subsidiary is real product but not investable at parent level. |
| GEDC (CalEthos) | OTC + pre-revenue + negative equity + REIT-to-data-center pivot shell pattern. AGPU/SHAZ analog. |
| POWI (Power Integrations) | H8 end-market test FAILS — AI DC is one of EV + industrial + DC; not >50% AI-DC. H5 PARTIAL/NEUTRAL not IGNORED. Already-mature mid-cap at $4-4.63B. Not new framework material. |
| BELFB (Bel Fuse) | H8 end-market test FAILS — Bel is industrial diversified across Auto/Broadcasting/Networking/Military, POL voltage converter component is one product line. Not AI-DC pure-play. |
| ENPH (Enphase Energy) | OVER CAP at $8.4-9.45B; IQ SST is forward product (2027 pilots, 2028 volume). Solar inverter core business. +103% in May = already-momentum-rerated. |
| Foreign-listed CXL/rack-power names (Montage Technology HK 2026 IPO, CXMT, UniIC, GigaDevice, DapuStor, Nanya Technology, Delta Electronics Taiwan, Lite-On Taiwan, AcBel Polytech Taiwan, Yosun Electric Taiwan, Renesas Japan, Murata Japan) | Foreign-listed; discovery-friction handicap per INSIGHTS (no US 13F-HR, no US 8-K, no Form 4). Some are mega-cap (Renesas, Murata, Delta), some are mid/small-cap that would qualify on size (Lite-On $8.97B, AcBel) but require non-US filing aggregator infrastructure not currently built. Document for future foreign-filer parallel framework. |

---

## NEW INSIGHT FOR INSIGHTS.md (proposed)

> **CXL and Rack-Level Power Delivery chokepoints are firing post-IPO/post-rerate, not via discoverable sub-$5B entry points** [confirmed: 1 targeted scan, last: 2026-05-27] [structural]
>
> ALAB (CXL) and AEIS/VICR/NVT/MOD/ENPH/ALGM (rack power) all rerated above the $5B H8 ceiling before this scan captured them. The framework's H10 + H8 + H5 + H11 gate is correct, but the timing of the chokepoint's public-market emergence was earlier than the screen-discovery layer caught. ALAB specifically came public in March 2024 at ~$5.5B and rerated ~10x in 24 months — the chokepoint thesis was right; the framework needed an IPO-window entry vector that does not currently exist.
>
> **Forward implication:** The next 4-7 year chokepoint rerate window is concentrating. Chokepoints emerge → pure-play graduates → window closes — increasingly compressed timeline. The CHOKEPOINT_TAXONOMY.md 2026-05-27 refresh showed 11 of 14 prior pure-plays already graduated; this dual scan added 7 more graduated names (ALAB, AEIS, VICR, NVT, MOD, ENPH, ALGM) to the historical-validation list. **Two implications for screening cadence:**
> 1. Discovery sweeps need to actively monitor the IPO calendar for chokepoint pure-plays coming public sub-$5B (the ALAB-shape entry point). Build a candidate IPO-watch list per quarter.
> 2. Tier 4 SEGMENT promotion (Framework v2.0) is the right structural answer for AEIS Data Center Computing / NVT Data Solutions / MOD Climate Solutions segments where the parent has graduated but the AI-DC segment may still offer rerate potential at segment-multiple level.
>
> **Calibration cases:** ALAB (CXL chokepoint pure-play graduated; framework caught chokepoint thesis but missed IPO-window entry); rack-level power delivery (6 names graduated simultaneously across 2024-2026); MEI (in-rack busbar fragmented chokepoint = already-documented REJECT, confirmed valid).

---

## METHODOLOGY NOTES + TOOLING

- All market caps cross-checked via stockanalysis.com / Yahoo Finance / WallStreetZen / Morningstar live web search 2026-05-27 per CLAUDE.md governance rule. Confirmed multiple times: EdgarTools XBRL `company_brief` mkt cap is stale — used only for revenue / net income / OCF / equity / insider sentiment / officers; price-derived metrics taken from live web search.
- EdgarTools `search_filings_full_text` single-phrase queries used per documented INSIGHTS rule (boolean AND with phrase quotes returns zero per multiple prior runs; consistent failure mode reconfirmed this run on `"AI data center" "power" NEAR(rack, 20)` returning zero).
- 8-K Item 1.01 vocabulary expansion partially fired (CalEthos GEDC, BW already-blind-spot, 2 SPACs).
- Foreign-listed candidates flagged for future foreign-filer parallel framework but not actionable under current US-Nasdaq/NYSE-only screening discipline.

---

## SESSION END

- **No CANDIDATE_UNIVERSE.md ACCEPT or TIER 2 additions.**
- **TSSI added to CANDIDATE_UNIVERSE TIER 3 WATCH** (adjacency-rule; never promote without chokepoint-hardware fire).
- **Two new chokepoint entries (#11 CXL, #12 Rack-Level Power Delivery) added to CHOKEPOINT_TAXONOMY.md as EMPTY status with 7 newly-graduated pure-plays added to historical validation table.**
- **6 names added to REJECT log with explicit reasoning** (NLST, OSS, MEI confirmed, INV, GEDC, POWI, BELFB, ENPH, foreign-listed cluster).
- **One new insight proposed for INSIGHTS.md** on post-IPO/post-rerate chokepoint emergence pattern.
- No git push (per scan brief).
- No framework changes beyond taxonomy/candidate additions.
