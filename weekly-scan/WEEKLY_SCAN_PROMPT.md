# ARCHOS WEEKLY MASTER SCAN
# Paste this prompt into Claude Code every Sunday.
# Output: archos/weekly-scan/runs/{date}-run.md

## CRITICAL EXECUTION RULE
# This is the FULL comprehensive sweep — NOT a light weekly check.
# Run ALL screens at their FULL lookback windows every single week:
# - 8-K screens: 7 days (Screens 1, 4)
# - 10-Q screens: 60 days (Screens 2, 3)
# - Keyword emergence: 90 days (Screen 7)
# - De-SPAC timing: full 24-36 month window (Screen 5)
# - Spinoff/REORG: full 6-18 month window (Screen 6)
# - Short interest overlay: current snapshot (Screen 8)
# Do NOT narrow, truncate, or optimize any screen for speed.
# Breadth across all 8 screens is more important than speed.
# There is no separate monthly run — this weekly run IS the
# comprehensive scan covering the entire market surface.

## MANDATORY READS
1. _master_docs/WORKING_PHILOSOPHY.md
2. archos/CLAUDE.md
3. archos/CHOKEPOINT_TAXONOMY.md
4. archos/CANDIDATE_UNIVERSE.md
5. archos/INSIGHTS.md

Confirm LAST LINE of WORKING_PHILOSOPHY.md before proceeding.

## PARAMETERS
- Date: {today's date}
- Market cap tiers:
  * Tier 1 moonshots: sub-$500M
  * Tier 2 catalyst plays: $500M-$5B
  * Tier 3 compounders: $5B-$25B
- Lookback: 7 days for 8-K/material agreements, 60 days for 10-Q
- Exclusion: all tickers in CANDIDATE_UNIVERSE.md (WATCH + REJECT + DD REJECT + Tier 2 DD Completed) plus all confirmed winners and Phase 2 controls from research/
- Sector lenses: AI Infrastructure, Defense/Space, Nuclear, Critical Minerals, GLP-1/Pharma, Physical AI/Robotics, Telecom/Broadband, Uncategorized

## THE EIGHT SCREENS — RUN IN PARALLEL

### Screen 3 — Customer Deposit / Deferred Revenue Scanner (PRIMARY DISCOVERY SCREEN — elevated 2026-05-27 Framework v2.0)
**Screen 3 is the primary discovery screen per the 2026-05-27 framework evolution. Balance-sheet signals lead bellwether mentions by 1-3 quarters (SNDK, LEU, POWL, AEHR calibration cases). Run this screen FIRST in execution order; use results to prioritize which candidates get deeper screening on subsequent screens.**

Search EdgarTools for 10-Q filings from the last 60 days.
Queries: "customer deposits increased", "deferred revenue increased", "contract liabilities increased", "advance payments", "customer prepayments"
For each hit: verify market cap < $25B. Compute QoQ change in customer deposits or deferred revenue. Flag if increase > 50% QoQ OR absolute new deferred rev > $10M (v2.0 absolute threshold). Cross-reference with any bellwether or government customer relationship. This is a demand signal hiding on the balance sheet before it becomes revenue.
**Per v2.0 discovery hierarchy:** a first-time deferred revenue buildup >$10M from a chokepoint-adjacent end-market qualifies for TIER 2 WATCH even without H10 fire (provided H8/H5/H11 pass). H10 fire upgrades to TIER 1 / ACCEPT-track.

### Screen 1 — Material Agreement Scanner (H10 confirmation layer)
Search EdgarTools for 8-K filings from the last 7 days.
Query set A — mega-cap counterparties (one query each, single-phrase, post-filter for "agreement" or "contract"):
NVIDIA, Microsoft, Meta Platforms, Amazon, Alphabet, Apple, Broadcom, Tesla, Novo Nordisk, Eli Lilly
Query set B — defense/gov counterparties:
Lockheed, Northrop, Raytheon, SpaceX, Anduril, Palantir, Department of Defense, Department of Energy, NASA, DARPA, NRC, Space Force
Query set C — corpus-wide Item 1.01 feed (last 7 days)
For each hit: verify market cap < $25B using web search (NOT XBRL). Read the filing snippet. Is this binding or LOI? Dollar value? Which sector lens? **Cross-check against Screen 3 results — bellwether mention on a candidate already showing balance-sheet signals = ACCEPT-track promotion (per v2.0 discovery hierarchy: balance sheet leads, H10 confirms).**

### Screen 2 — Revenue Inflection Scanner
Search EdgarTools for 10-Q filings from the last 60 days.
Queries: "record quarterly revenue", "revenue increased", "highest quarterly revenue", "revenue growth exceeded"
Also web search: "fastest growing small cap stocks {current quarter} {current year}", "micro cap revenue growth leaders {current year}"
For each hit: verify market cap < $25B. Pull actual revenue from 10-Q. Compute YoY growth. Was prior year growth < 20%? (first-time inflection filter). What is driving the growth?

### Screen 4 — Government Contract Awards Scanner
Search EdgarTools for 8-K filings from the last 7 days.
Queries: "contract award", "U.S. Navy", "U.S. Army", "U.S. Air Force", "Space Force", "DARPA", "NASA award", "Department of Energy grant", "DPA Title III", "CHIPS Act", "NRC license", "Other Transaction Authority"
Also web search: "contract award" site:defense.gov {current year} last 7 days, "DOE loan program" OR "DOE grant" {current year}
For each hit: is contractor publicly listed? Market cap < $25B? Contract value as % of TTM revenue (> 20% = material). Duration and type (IDIQ ceiling vs firm-fixed-price vs CPFF — contract TYPE determines revenue reliability).

### Screen 5 — De-SPAC Reanimation Scanner (NEW — from pattern discovery)
Web search: list of all US-listed de-SPACs that completed mergers between November 2023 and May 2024 (24-36 months ago). Cross-reference with EdgarTools for any that filed 8-K material agreements or reported revenue inflection in the last 90 days.
Filter: market cap < $5B, government contract or bellwether customer relationship, IGNORED sentiment.
This catches the "abandoned survivors" at the 24-36 month window where PIPE warrants have washed out and the first real catalyst triggers a rerate from a bottomed base. 60% hit rate in defense/space/nuclear/quantum per SIGNAL_CLUSTERS.md.

### Screen 6 — Spinoff / REORG Catalyst Scanner (NEW — from pattern discovery)
Web search: "spinoff 2025 2026", "chapter 11 emergence 2025 2026", "divestiture 2025 2026 completed", "Nasdaq relisting 2025 2026"
Filter for: companies that completed a corporate restructuring event 6-18 months ago AND are sub-$10B AND have not yet been re-rated (stock still near post-event lows).
Check: did a new CEO or CFO come in with the restructuring? (20% hit rate on winners, high quality when present per PATTERN_MATRIX_UNIVERSAL.md)

### Screen 7 — Keyword Emergence Scanner
Search EdgarTools for 10-Q filings from the last 90 days.
AI cluster: "artificial intelligence" AND "new customer", "data center" AND "first time", "GPU" AND "deployment"
Defense cluster: "hypersonic", "directed energy", "autonomous systems", "counter-UAS"
Nuclear cluster: "small modular reactor", "SMR", "HALEU", "nuclear fuel", "nuclear instrumentation", "reactor coolant", "nuclear construction", "NRC license", "DOE Loan Programs Office", "fuel fabrication", "nuclear safety", "reactor components", "balance of plant" AND nuclear context, "spent fuel", "uranium enrichment"
Pharma cluster: "semaglutide", "GLP-1", "peptide synthesis", "fill-finish"
Physical AI/Robotics cluster: "humanoid", "humanoid robot", "force sensor", "torque sensor", "actuator", "servo motor", "robotic joint", "haptic", "physical AI", "dexterous manipulation", "legged locomotion", "Tesla Optimus", "Figure", "embodied AI"
For each hit: verify market cap < $25B. Was this keyword present in the prior 4 filings? If yes, not emergence — skip. If no, this is a demand signal before revenue.

### Screen 9 — Senior Defense/IC Board Appointment Scanner (NEW — 2026-05-28)
Search EdgarTools for 8-K filings from the last 90 days.
Query set A — Item 5.02 director/officer appointments at sub-$1B companies:
"appointed to the board", "joined the board", "advisory board", "board of directors"
For each hit at a sub-$1B defense/space/intelligence-adjacent company: read the 8-K to identify the appointee. Web search the appointee's name + "general" OR "admiral" OR "director" OR "deputy director" to verify whether they held flag rank (1-4 star general/admiral) or agency leadership (Director/Deputy Director level) at any of: DoD, Joint Chiefs, CIA, FBI, NSA, DIA, NRO, NGA, DHS, CBP, ICE, Secret Service, Space Force, CYBERCOM, SOCOM, CENTCOM, INDOPACOM, EUCOM, DARPA, MDA, SDA, AFRL, NAVAIR, or equivalent.
Query set B — compensation verification:
For each confirmed senior appointee, check the 8-K and/or most recent DEF 14A proxy for compensation disclosure. Flag if the appointee received stock grants, options, RSUs, or other equity compensation. Cash-only advisory = weaker signal. Equity compensation = conviction signal (reputational skin in the game).
Query set C — web search supplement:
"former general joins board" OR "retired admiral advisory board" + "defense" + sub-$1B company context, last 90 days
"former CIA director board" OR "former FBI director advisory" + publicly traded company, last 90 days
This screen catches the AISP pattern (former CBP Acting Commissioner Aguilar joining advisory board with equity comp). Senior defense/IC leaders don't join sub-$1B companies for consulting fees — they join because they've seen the product, know which budgets are funded, and are betting their reputation on the company's growth. Their appointment IS a forward signal 12-18 months ahead of the contract awards their rolodex will generate.
Conviction boost: if a Screen 9 hit ALSO fires on Screen 4 (government contract) or Screen 3 (deferred revenue), auto-promote to TIER 1 URGENT.

### Screen 8 — Short Interest Amplifier Overlay
Web search: "highest short interest stocks May 2026", "most shorted stocks small cap"
Also search Finviz if reachable: short interest > 15% filter
Cross-reference EVERY short-interest hit against results from Screens 1-7. A candidate that already passed a screen AND has >15% short interest gets an automatic conviction upgrade. The short interest doesn't find winners — it AMPLIFIES the move when a catalyst hits.
Do NOT surface short-interest-only candidates (no fundamental catalyst = meme/squeeze REJECT pattern per Cluster 8 in SIGNAL_CLUSTERS.md).

### Screen 10 — Government Equity / Strategic Investment Scanner (NEW — 2026-05-28)
The Trump administration has taken direct equity stakes in strategic companies since 2025. Every single position has massively outperformed: Intel ($20→$125, +510%), MP Materials (Pentagon = 15% largest shareholder), quantum companies (+14-30% day-one on $2B announcement). The government-as-bellwether signal is STRONGER than any corporate bellwether because it removes bankruptcy risk, signals classified procurement pipeline knowledge, and creates a self-fulfilling prophecy as other investors pile in.

**Query set A — SEC filings for government equity events:**
Search EdgarTools for 8-K filings from the last 30 days:
"government equity", "equity stake", "preferred stock" AND "Department" context, "warrant" AND "Department of Defense" OR "Department of Commerce" OR "Department of Energy" context, "CHIPS Act" AND "equity", "golden share", "government investment"

**Query set B — grant-to-equity conversions and direct investment:**
Search EdgarTools for 8-K filings from the last 30 days:
"Department of Commerce" AND "investment", "Department of Defense" AND "investment", "Department of Energy" AND "loan", "DPA Title III", "Investment Accelerator", "Pax Silica"

**Query set C — web search for upcoming government investment targets:**
"Trump administration equity stake" 2026
"Commerce Department investment" company 2026
"Pentagon equity stake" OR "DoD investment" company 2026
"DOE Loan Programs Office" commitment 2026
"CHIPS Act" equity OR stake 2026
"government strategic investment" publicly traded 2026
"executive order" AND sector-specific terms (quantum, semiconductors, critical minerals, nuclear, defense, AI)
site:whitehouse.gov investment OR funding OR equity 2026
site:commerce.gov investment OR equity 2026

**Query set D — speech and executive order name-drops:**
Search for companies named by Trump, Lutnick, or senior officials in speeches, Truth Social posts, or executive orders in the last 30 days. When the President personally name-drops a company (Micron hit $1T the day after Trump discussed it), the stock reprices immediately.
"Trump" AND company name AND "investment" OR "great company" OR "billions"

**Signal hierarchy:**
- Government takes EQUITY STAKE (common stock, preferred, warrants) → TIER 1 URGENT regardless of market cap. This is the Intel pattern — removes downside, signals insider knowledge of procurement pipeline.
- Government announces direct FUNDING with equity component (grant-to-equity conversion, loan + warrant) → TIER 1 URGENT. USA Rare Earth / Vulcan pattern.
- Government announces GRANTS/LOANS without equity → TIER 2 STRONG. Still significant government validation.
- Government NAMES company in speech/EO without funding → TIER 3 WATCH. Micron pattern — attention catalyst, not structural backstop.
- Company is in a SECTOR the administration has identified as strategic priority (quantum, critical minerals, nuclear, defense AI, semiconductors) but has not yet received direct investment → MONITOR for future rounds.

For each hit: verify market cap, check if already in CANDIDATE_UNIVERSE.md, assess whether the government investment creates a structural floor (equity stake) or is just a funding event (grant). Cross-reference with Screens 3-4 — a company receiving government equity AND showing deferred revenue growth AND winning contracts = maximum conviction.

## FILTERING — APPLY TO ALL RAW HITS

For every candidate surfaced by any screen:

Step 1 — Market cap verification (LIVE data, web search):
- Sub-$500M: tag Tier 1
- $500M-$5B: tag Tier 2
- $5B-$25B: tag Tier 3
- Over $25B: REJECT

Step 2 — Extended bellwether check:
Does this company have a relationship with a mega-cap, government entity, or sector-specific bellwether (Big Pharma for biotech, major MNOs for telecom)? If no bellwether relationship of any kind, REJECT unless the revenue inflection or customer deposit signal is exceptionally strong.

Step 3 — Sentiment quick-check:
Web search "[ticker] analyst coverage", "[ticker] ETF inclusion". Classify as IGNORED / NEUTRAL / PARTIAL / LOVED. LOVED = deprioritize (asymmetry reduced). IGNORED = prioritize (asymmetry maximized).

Step 4 — Balance sheet quick-check:
Going concern? Debt/equity > 5x? Cash runway < 12 months? If any flag, mark H11 risk but do NOT auto-reject — note it for DD.

Step 5 — LEAPS check:
Does a LEAPS chain exist (expiry > 12 months out)? If yes, note the furthest expiry and approximate ATM premium as % of stock price. If IV is >80%, note "high IV — premium expensive." If no LEAPS chain, note "equity only." This information is for position-sizing, not for filtering.

## SECTOR TAGGING

Tag every surviving candidate with one or more sector lenses:
- AI Infrastructure: maps to CHOKEPOINT_TAXONOMY.md or bellwether is NVDA/TSMC/AVGO/MSFT/META/AMD
- Defense/Space: bellwether is DoD/NASA/DARPA/SpaceX/Lockheed/Northrop/RTX/Anduril/Palantir/L3Harris/Space Force
- Nuclear: bellwether is DOE/NRC or product is reactor/fuel/coolant/instrumentation
- Critical Minerals: bellwether is DoD DPA/DOE LPO or product is rare earth/lithium/cobalt/gallium processing
- GLP-1/Pharma: bellwether is Novo Nordisk/Eli Lilly/Amgen or product is API/peptide/fill-finish/delivery device
- Physical AI/Robotics: bellwether is Tesla (Optimus)/Figure/Aptronic/Boston Dynamics/NVIDIA (Isaac platform) or product is force/torque sensors, actuators, servo motors, precision encoders, robotic joints, haptic feedback, or embodied AI software for humanoid/industrial robotics. H10-R = binding supply agreement with a humanoid OEM or NVIDIA Isaac robotics platform certification.
- Telecom/Broadband: bellwether is major MNO/MSO or product is network infrastructure with >50% market share
- Uncategorized: interesting catalyst but no lens match. Note for Sounding Board.

## CONVICTION RANKING

Rank all surviving candidates by conviction level:

TIER 1 URGENT (fast-track to DD immediately):
- Triple-cluster fire (matches 3+ named clusters from SIGNAL_CLUSTERS.md)
- Material agreement with named mega-cap, binding, dollar value disclosed, sub-$2B
- Government contract > 50% of TTM revenue at sub-$2B company
- Cross-screen hit (surfaced by 2+ screens independently)

TIER 2 STRONG (queue for DD this week):
- Double-cluster fire
- Material agreement with government counterparty, binding
- Revenue inflection + customer deposit spike on same name
- Any sub-$500M candidate passing all 4 universal filters

TIER 3 WATCH (add to CANDIDATE_UNIVERSE.md, re-evaluate next scan):
- Single screen hit with clear sector lens match
- LOI/MOU (not binding) with quality counterparty
- $5B-$25B compounder with strong fundamentals and clean LEAPS chain
- Revenue inflection without clear catalyst explanation

REJECT:
- Over $25B market cap
- No bellwether relationship and no exceptional fundamental signal
- Float < 20% + borrow > 50% + no fundamental catalyst (Cluster 8 meme/squeeze)
- LOVED sentiment with no new catalyst (asymmetry gone)

## OUTPUT

Write to: archos/weekly-scan/runs/{date}-run.md

Format:

# ARCHOS WEEKLY SCAN — {date}

## Parameters
[Market cap tiers, lookback windows, exclusion count]

## Screen results (one section per screen with tables)

## Cross-screen hits
[Candidates surfaced by 2+ screens — highest conviction]

## Sector lens summary
| Sector | Hits | Top candidate |

## Conviction ranking
### TIER 1 URGENT
[Full details — ticker, market cap, sector, screens fired, one-line thesis, LEAPS available?]

### TIER 2 STRONG
[Same format]

### TIER 3 WATCH
[Same format]

### REJECT log
[One line per reject with reason]

## New vocabulary / taxonomy updates
[Any new bellwether language, chokepoint terminology, or sector signals spotted]

## Screen effectiveness notes
[Which screens produced, which didn't, tool issues, refinements for next week]

---

Update CANDIDATE_UNIVERSE.md:
- Add TIER 1 and TIER 2 candidates to appropriate sections
- Add TIER 3 to WATCH with screen attribution and re-eval trigger

Update state.md:
- Add timeline entry for this week's scan

Append to INSIGHTS.md (only if a genuinely new lesson was learned — do NOT append routine scan notes):
- New screening lessons that change how future scans should run
