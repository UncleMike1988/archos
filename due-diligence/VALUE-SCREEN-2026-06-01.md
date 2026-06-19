# VALUE SCREEN — Forgotten Quality at Sub-15× While AI Ate the Tape
**Date:** 2026-06-01 · **Analyst:** Archos Equities (Code) · **Type:** Systematic value screen → DD funnel
**Thesis under test:** The AI rotation pulled capital and attention out of quality, non-AI businesses, leaving established, profitable, >$5B companies at historically cheap multiples. Find the names that re-rate when the market broadens — the ADBE playbook applied systematically.

> **Language note (per CLAUDE.md):** This file is the analyst's workpaper — jargon-heavy, complete, technical. The plain-English translation lives in the Sounding Board chat, not here.

---

## 0. METHODOLOGY, DATA SOURCES & HONEST CONSTRAINTS (read first)

**This screen could not be run as a clean server-side query. Read these caveats before trusting any single number.**

1. **No fundamentals screener available.** Massive Market Data's `/stocks/financials/*` tier (ratios, income statements — the endpoints that would let me filter the *entire* market by P/E server-side) returns **HTTP 403 (not entitled)**. Massive's "all tickers" reference endpoint carries no market-cap/sector fields and can't filter server-side. So the universe could **not** be enumerated mechanically. It was built **knowledge-seeded across every sector the brief named** (~99 candidates), then **each name verified live**. This means the screen is only as complete as the seed — there are surely qualifying names not pulled. Treat the survivor list as *representative of the cheap-quality cohort, not exhaustive.*

2. **What *did* work (the verified data spine):**
   - **Massive Ticker Overview** (`/v3/reference/tickers/{T}`) → authoritative market cap, SIC sector, exchange, shares. ✔ free tier.
   - **Massive daily aggregates** (`/v2/aggs/...`) → exact point-to-point **12-month price change** (criterion 7). ✔ but **rate-limited to ~5 req/min** (9 parallel subagents saturated it; backfill done serially).
   - **SEC EDGAR MCP** (`financial_statements` TTM, `compare_companies`, `insider_activity`) → revenue, net income, margins, growth, Form-4 activity. ✔ Pro tier, ~unlimited quota (2 of 100k used). Some TTM line-items mis-map on non-calendar fiscal years (flagged inline).
   - **WebFetch → stockanalysis.com** → **forward P/E**, trailing P/E, market cap, price, dividend. ✔ no rate limit. **Caveat:** the small-model extractor returned **2 confirmed bad fetches** (AKAM showed $153, ZM showed $114 — both ~2× wrong). **Every finalist figure was cross-checked against Massive + SEC.** Non-finalist forward-P/Es carry a residual data-quality risk.
   - **WebSearch** → catalyst verification (this changed several theses — see §5).
   - **Firecrawl = dead** (out of credits, 402). Not usable this session.

3. **Primary gate = FORWARD P/E (the brief's stated preference), and this matters enormously.** Trailing TTM net income on many of the *exact names this screen targets* is depressed by one-time charges (impairments, restructuring, IPR&D, acquisition amortization). **GM trails at 32.6× but is 6.6× forward.** A pure trailing-P/E screen would have **rejected the single best forgotten-quality names.** I used forward P/E as the gate, trailing as a backstop, and flag every name whose two multiples diverge.

4. **The score (§3) is a triage sort key, NOT a verdict.** Per Archos Equities doctrine (no invented frameworks-as-law), the 0–10 tally just funnels ~33 survivors down to a deep-dive set. The real judgment is in plain English in §4–§5.

5. **Staleness / precision flags:** insider data lags 5–48 days (SEC pipeline); FOXA SEC TTM is as-of 2026-02-04; **5-year-average P/E (signal g) was not pulled as an exact series** (no source cleanly exposed it) — "historically cheap" is assessed against known multiple history and flagged *approximate*; **live Jan-2028 option chains were not pulled** (Massive options tier likely gated) — LEAPS analysis is qualitative, **re-quote the live chain before acting.**

**Prices/caps are as of the 2026-05-29 close (last trading day).** 12-month return measured 2025-05-27 → 2026-05-29 (verified via Massive aggregates; timestamp-checked).

---

## PHASE 1 — THE RAW SCREEN

**Criteria (all must hold):** (1) mkt cap >$5B · (2) **forward** P/E <15 *(trailing <15 also accepted)* · (3) US-listed NYSE/Nasdaq · (4) profitable TTM · (5) revenue >$1B TTM · (6) not bank/REIT/utility/pure-commodity producer · (7) flat or up over 12 months · (8) not already on WATCHLIST.md or WINNER_UNIVERSE.md.

**~99 names verified live → 33 pass.** (In the brief's 30–100 target; no relax/tighten needed.) The 33 passes, grouped. *Fwd P/E is the gate; "ttm" shown where it diverges. "12mo" is verified point-to-point.*

### 1A. Core survivors — forgotten-quality, finalist-eligible (26)

| Ticker | Name | Mkt Cap | Fwd P/E (ttm) | TTM Rev | 12mo | Div | Sector (SIC) |
|---|---|---|---|---|---|---|---|
| GM | General Motors | $73.3B | **6.6** (32.6) | $184.6B | +69.6% | 0.9% | Autos (3711) |
| F | Ford Motor | $67.3B | **11.7** | $189.9B | +69.2% | 0.6%+spec | Autos (3711) |
| APTV | Aptiv (post-EDS-spin) | $14.3B | **11.0** (40.3) | ~$20.7B† | −0.7% | — | Auto tech (3714) |
| BWA | BorgWarner | $14.4B | **13.1** (41.4) | $14.3B | +113.8% | 1.0% | Auto parts (3714) |
| LEA | Lear | $7.1B | **9.2** (14.1) | $23.5B | +55.4% | 3.1% | Auto seating (2531) |
| ALV | Autoliv | $9.4B | **11.7** (13.7) | $11.0B | +22.2% | 2.8% | Auto safety (3714) |
| ALSN | Allison Transmission | $9.1B | **10.8** (17.1) | $3.65B | +8.5% | 1.1% | Transmissions (3714) |
| MGA | Magna Int'l | $17.6B | **9.4** (27.0) | $42.3B | +77.3% | 3.1% | Auto parts (3714) |
| PFE | Pfizer | $149.2B | **~9** (10.4) | $93.8B | +10.9% | ~6.8% | Pharma (2834) |
| BMY | Bristol-Myers Squibb | $116.8B | **~10** (10.3) | $68.0B | +21.9% | ~4.8% | Pharma (2834) |
| AMGN | Amgen | ~$177B | **14.9** (~17) | ~$35B | +20.5% | 3.1% | Biopharma (2836) |
| INCY | Incyte | $19.3B | **~12** (13.5) | $5.4B | +48.1% | — | Biopharma (8731) |
| CVS | CVS Health | $115.2B | **11.9** (39.6) | $405.6B | +48.3% | 3.0% | Health/pharmacy (5912) |
| DVA | DaVita | $12.2B | **12.7** (18.7) | $13.8B | +38.9% | — | Dialysis (8011) |
| SOLV | Solventum (3M spin) | $13.1B | **11.3** (9.3) | $8.3B | +3.3% | — | Medtech (3841) |
| LH | Labcorp | $21.1B | **14.1** (22.8) | $14.1B | +5.0% | 1.1% | Labs (8071) |
| AGCO | AGCO | $8.1B | **~13** (7.3) | $14.0B | +10.7% | ~1% | Farm machinery (3523) |
| HII | Huntington Ingalls | $12.1B | **~13** (14.4) | $17.7B | +35.3% | ~2% | Shipbuilding/def (3731) |
| UAL | United Airlines | $37.3B | **~7** (10.2) | $60.5B | +46.9% | — | Airline (4512) |
| UPS | United Parcel Service | $92.4B | **14.2** (17.3) | $88.3B | +9.4% | ~6.0% | Logistics (4210) |
| MO | Altria | $116.2B | **~11** (8.4) | $40.9B‡ | +16.7% | ~7% | Tobacco (2111) |
| TGT | Target | $57.7B | **~13** (9.9) | $156.4B | +31.0% | ~3.4% | Retail (5331) |
| EXPE | Expedia | $27.1B | **~10** (11.0) | $22.0B | +36.9% | ~0.9% | Travel/OTA (4700) |
| FOXA | Fox Corp | $26.9B | **~13** (13.2) | $16.5B | +14.6% | ~1.2% | Media (4833) |
| NXST | Nexstar Media | $5.4B | **~8** (6.6) | $7.8B | +1.8% | ~3.5% | Media/broadcast (4833) |
| BBY | Best Buy | $16.0B | **11.6** (14.4) | $41.9B | +7.9% | 5.1% | Retail electronics (5731) |

† APTV revenue is in transition — the Electrical Distribution Systems business spun off as **Versigent (VNT)** on **2026-04-01**; figures pre-date the clean post-spin run-rate. ‡ MO revenue includes federal excise taxes; economic "net revenues" ≈ $21B.

### 1B. Commodity-adjacent — pass criteria but tagged (refining = crude-spread-driven; de-prioritized per brief's "not structurally cheap sectors" intent) (3)

| Ticker | Name | Mkt Cap | Fwd P/E (ttm) | TTM Rev | 12mo | Div | Note |
|---|---|---|---|---|---|---|---|
| PSX | Phillips 66 | $72.6B | 8.5 (17.3) | $134.5B | +53.8% | 2.8% | **Elliott on board** — midstream/chem breakup pressure live |
| VLO | Valero | $75.3B | 8.6 (18.4) | $117.8B | +87.3% | 1.9% | Pure-play refiner; ran hard |
| MPC | Marathon Petroleum | $75.8B | 8.0 (16.2) | $136.0B | +53.3% | 1.6% | Huge buyback; ran hard |

### 1C. Structurally-cheap financials — meet the *letter*, not the *spirit* (insurers always trade low on book/rate sensitivity; **excluded from finalists** per brief intent) (4)

| Ticker | Name | Mkt Cap | Fwd P/E (ttm) | TTM Rev | 12mo | Div | Note |
|---|---|---|---|---|---|---|---|
| TRV | Travelers | $61.6B | 10.5 (8.7) | $48.9B | +5.8% | ~1.6% | P&C; quality but perennially cheap |
| CB | Chubb | $120.4B | 11.4 (11.0) | $60.8B | +7.6% | 1.3% | Best-in-class P&C; perennially cheap |
| MET | MetLife | $52.6B | 8.3 (16.0) | $108.2B | +4.6% | 2.8% | Life; rate-sensitive |
| ALL | Allstate | $53.3B | 7.8 (4.6) | $68.2B | −0.6% | 2.1% | P&C; flat 12mo (marginal) |

### 1D. Notable FAILS / near-misses (transparency — why they dropped)

- **Failed criterion 7 (in free-fall, not forgotten):** PYPL (−37%), GIS (−37.5%), BLDR (−31.6%), CMCSA (−28.8%), UHS (−24.1%), CNH (−21%), CTSH (~−20%, est), LKQ (−33.6%), GPC (−22.5%), CI (−12%), AIG (−10.7%), KHC (−10.5% + loss), MDT (−9.1%), GEN (−8.4%), ZBH (−12.6%), HPQ (−4.6%), PRU (−3.7%), DBX (−5.4%), EMN/LYB/FI/FIS/GPN/WEX (all down). *These are broken or de-rating, not forgotten — the screen correctly excludes them.*
- **Failed criterion 2 (forward P/E ≥15 — already discovered / ran too far):** MCK (16.8), CAH (17.1), FDX (19.7, +87%), EBAY (17.7, +51%), NTAP (19.6, +74%), XYZ (18.2), SLB (24.5, +61%), HAL (21.1, +94%), BKR (27.5), QCOM (~ttm 16.5, +69%), the analog semis (SWKS/QRVO/NXPI/ON/AMKR/FLEX/JBL — trough-earnings-inflated P/E *and* up 60–270%), LMT (25.5), PCAR (23.5), TXT (17.1), HUM (29).
- **Failed criterion 4 (not profitable TTM):** VTRS, BAX, CE, DOW, KHC, HPE (all GAAP losses TTM, mostly impairment-driven).
- **Could not verify (excluded):** GSK (foreign filer — SEC XBRL unavailable). **Borderline (forward unconfirmed):** GILD (ttm 15.2–17.8, fwd ~13–14 but stockanalysis returned NA; +23%), MRK (trailing distorted, fwd ~14 unverified, +53%), ELV (fwd 15.0, managed-care likely down 12mo). *Flagged, not advanced.*

---

## PHASE 2 — QUALITY SCORING

Signals: (a) gross margin >40% · (b) rev growth >5% YoY · (c) FCF positive · (d) buyback active · (e) dividend · (f) **open-market** insider buying · (g) historically cheap (≈>30% below own 5yr-avg P/E — *approximate, see §0.5*) · (h) sector lagged S&P >20% (rotation candidate) · (i) hidden AI exposure not yet reclassified · (j) catalyst within ~6mo.

**Reminder: this is a sort key, not law.** Margins/growth from SEC `compare_companies`; insider from SEC Form-4; (g/h/i/j) are reasoned judgments, flagged where soft.

| Tkr | Score | Signals present | Why it's interesting (1 line) |
|---|---|---|---|
| INCY | **7** | a,b,c,d,g,h,j | Biopharma growing **+21%** at ~12× fwd; Jakafi-LOE fear overdone, deep pipeline. |
| BBY | **7** | c,d,e,g,h,i,j | 11.6× fwd + **5% yield**; the cleanest "hidden AI" — AI-PC/Win10-EOL refresh cycle, priced as a dying retailer. |
| AMGN | **6** | a,b,c,e,h,j | Only *growing* (+10%) high-margin pharma here at <15× fwd; **MariTide obesity = embedded call option**. |
| UPS | **6** | c,d,e,g,h,j | Wide-moat parcel duopoly de-rated to 14.2× / **6% yield**; Amazon drag ending, **Q2-26 inflection confirmed**. |
| BMY | **6** | a,c,d,e,g,h | ~10× fwd, 4.8% yield, 60%+ gross margin — but Cobenfy adjunctive **missed** (see §5); cheap-because-shrinking risk. |
| TGT | **6** | c,d,e,g,h,j | De-rated retailer at ~13× fwd; **new CEO (Fiddelke) turnaround**; consumer rotation candidate. |
| CVS | **6** | b,c,e,g,h,j | $58→$91 recovery; **turnaround confirmed working** (guide raised, Aetna MLR 87→84.6%); thin-margin/levered. |
| APTV | **6** | c,d,f,g,h,(i),j | **Director buying post-spin** (+44.5%) at 11× fwd; EDS spin done 4/1/26, cleaner ADAS/software stub; insider conviction. |
| SOLV | **6** | a,c,f,g,h,j | 3M medtech spin at 11.3× fwd, 55% gross margin; director buy; portfolio reshaping + deleveraging. |
| FOXA | **6** | a,b,c,d,e,j | Growing +16.6% media at ~13×; Fox One streaming + 2026 political/sports — *but near highs, not cheap-vs-history (no g)*. |
| EXPE | **5** | a,b,c,d,e | OTA growing +7.6%, buyback, ~10× fwd; cyclical-travel exposure. |
| PFE | **5** | a,c,e,g,h | Cheapest big pharma (~9× fwd), **6.8% yield**, 70%+ gross margin; revenue shrinking post-COVID. |
| NXST | **5** | c,d,e,g,j | Cheapest in book (6.6× ttm); TEGNA deal **FCC-approved** + political cycle — *but 13-insider sell cluster (§5)*. |
| GM | **5** | c,d,e,h,j | 6.6× fwd, buyback machine; *ran +70% (discovered), C-suite selling, auto-cyclical*. |
| HII | **5** | b,d,e,g,j | Sole-source nuclear-shipbuilder de-rated on labor/margin fear; record backlog. |
| AGCO | **5** | c,d,e,g,j | Ag-equipment cycle trough (7.3× ttm); PTx precision-ag; cyclical bottoming. |
| MO | **5** | a,c,d,e,h | 62% gross / 30% net margin, ~7% yield, ~11× fwd; tobacco-perennial-cheap caveat. |
| DVA | **5** | b,c,d,h | Berkshire-owned (~45%) dialysis duopoly; aggressive buyback; rotation. |
| LH | **5** | b,c,d,e,h | Lab duopoly growing ~7%; 14× fwd; hospital-outreach M&A. |
| LEA/ALV/ALSN/MGA/BWA/F | 4–5 | (varies) | Auto-supplier cohort — cheap on fwd, but cyclical + several already ran (BWA +114%, MGA +77%). |
| PSX/VLO/MPC | 3–4 | c,d,e(,j) | Refiners — buyback-heavy, PSX has Elliott catalyst; commodity-adjacent (de-prioritized). |
| TRV/CB/MET/ALL | 3–4 | c,d,e | Quality insurers — perennially cheap (structurally, not "forgotten"); excluded from finalists. |

---

## PHASE 3 — THE TOP 10 (deeper look)

Selected for best fit to the *spirit* of the screen (forgotten quality + historically cheap + real catalyst + sane price), with deliberate sector spread. *Honorable mentions outside the 10: PFE, BMY, FOXA, GM, HII, AGCO, MO, DVA.*

> **Insider tell that runs through the whole cohort (verified, SEC Form-4, 180-day):** open-market *buying* is nearly absent in big-cap value, and several names show insiders **selling into the recovery** — BBY (6-officer cluster 3/23/26), NXST (13-insider cluster 3/24–27/26), GM (CEO+CFO 5/26), CVS (−$360M net), TGT. **Only APTV (director +44.5%, post-spin, May-26) and SOLV (director, small) show real open-market buys.** This is a mild negative for the sellers and a genuine positive for APTV/SOLV. Stated plainly, weighed — not disqualifying (large-cap sales are often diversification), but it counts.

### 1) AMGN — Amgen · ~$177B · 14.9× fwd · +20.5% · 3.1% yield
- **Numbers:** rev +10% YoY ($35B TTM), ~21% net margin, 75%+ gross margin, FCF strong; trailing P/E ~17–23 (Horizon amortization depresses GAAP). Fwd 14.9× vs ~14–16× 5yr history → *modestly* cheap (g is soft here).
- **Narrative gap:** GLP-1/obesity names + AI sucked all healthcare attention; AMGN de-rated on IRA drug-pricing fear + skepticism it can win in obesity. Meanwhile rev/EPS compound.
- **Re-rate driver:** market broadening to healthcare + **MariTide** (Phase 3 MARITIME-1/-2/-CV/-HF *ongoing*, no Phase 3 data yet; Phase 2 = ~17–20% weight loss with tolerability questions). Binary 2026–27 readout = the embedded call option.
- **ADBE comp:** the closest *quality-compounder-through-the-fear* analog in the book — but the upside is part-optionality (MariTide), not pure multiple-normalization.
- **LEAPS:** liquid Jan-2028 chain, moderate IV (~25–30%) → LEAPS math clears (Bucket-3 style). 2× single-stock ETF: none known for AMGN. *Re-quote live.*
- **Bull:** MariTide reads out competitively → obesity TAM re-rate. **Bear/kills it:** MariTide tolerability/bone-density fails *and* IRA bites; 14.9× isn't a deep margin of safety.

### 2) UPS — United Parcel Service · $92.4B · 14.2× fwd · +9.4% · ~6.0% yield
- **Numbers:** rev $88.3B (declining ~2.6% as Amazon purges), 6.3% net margin, FCF positive, big buyback + 6% dividend. 14.2× fwd vs ~16–18× historical → genuinely de-rated.
- **Narrative gap:** feared as a structurally-challenged, Amazon-dependent, freight-recession victim with a stretched payout.
- **Re-rate driver (verified, management-confirmed):** Amazon dilutive-volume cut **nearly complete** (8.8% of rev, target done June-26); **$3.5B network-reconfiguration cost-out**; SMB mix +330bps; guide explicitly calls for **return to revenue + operating-profit growth and margin expansion in Q2-2026**. Stock shed ~18% in the past month → *better entry*.
- **ADBE comp:** purest "de-rated quality, the fear is resolving, inflection imminent" — lowest binary risk of the three.
- **LEAPS:** liquid Jan-2028, low-moderate IV (~25%) → LEAPS viable. No 2× ETF. *Re-quote live.*
- **Bull:** margin to 11–12%, EPS ~$10 by '27 → ~$165 + yield. **Bear/kills it:** freight recession + tariffs deepen, dividend-coverage fear (high payout), Amazon glide-down overshoots → flat EPS persists, multiple stuck ~12×.

### 3) BBY — Best Buy · $16.0B · 11.6× fwd · +7.9% · 5.1% yield
- **Numbers:** rev ~$42B (flat; FY26 comps −0.8% but **Q3 +2.7% on AI PCs**), thin retail margin, FCF positive, buyback + 5% dividend. *(The Phase-1 gating subagent mis-parsed BBY at $28B rev / 31× — corrected here against stockanalysis: ~$42B / 11.6× fwd.)*
- **Narrative gap:** priced as a melting-ice-cube big-box retailer the market assumes Amazon kills.
- **Re-rate driver (the brief's "hidden AI"):** the **AI-PC / Windows-10-end-of-life refresh supercycle** is a real demand tailwind BBY is uniquely levered to. **Double-edged (verified):** the same AI boom inflating DRAM/HBM is now a **memory-cost COGS headwind** — higher ASPs offset lower units; management flagged memory-component inflation as the key FY27 risk.
- **ADBE comp:** "hidden AI exposure not yet reclassified" + de-rated quality + income — highest-torque, most-contrarian, lowest-moat of the three.
- **LEAPS:** liquid Jan-2028, moderate IV (~30–35%). No 2× ETF. *Re-quote live.*
- **Bull:** multi-year refresh + services growth, EPS ~$7.50 → ~$105 + 5% yield. **Bear/kills it:** refresh fizzles + memory costs crush gross margin + secular Amazon share loss resumes; **insiders just sold a 6-officer cluster** into the rally.

### 4) CVS — CVS Health · $115.2B · 11.9× fwd · +48.3%
Massive de-rate ($58 low → $91) now *confirmed* turning: FY26 guide **raised to $7.30–7.50 EPS**, rev ≥$405B, Aetna MLR 87.3%→84.6%, insurance op income +53%. Quality YES, but the easy money ($58→$91) is made, it's thin-margin + levered, and insiders sold ~$360M net. *Quality YES / entry-after-the-run = the watchlist's recurring "wait for pullback" pattern.*

### 5) INCY — Incyte · $19.3B · ~12× fwd · +48.1%
Biopharma growing **+21%** with 25% net margin at ~12× fwd; de-rated on Jakafi patent-cliff fear (2028) with a deep, under-credited pipeline (Opzelura, Niktimvo, MPN franchise). Buyback active. Ran +48% (partly discovered), insider *sell* cluster Dec-25. The cleanest growth-at-value name in the book.

### 6) TGT — Target · $57.7B · ~13× fwd · +31.0%
De-rated discretionary retailer, **new CEO Michael Fiddelke (Feb-26) turnaround**, buyback + ~3.4% yield, ~10× trailing. Up +31% off lows (recovery underway), revenue flat/declining, one insider sold. Consumer-rotation candidate; execution-dependent.

### 7) APTV — Aptiv · $14.3B · 11.0× fwd · −0.7% (genuinely NOT run)
The **insider-conviction pick**: a director bought +44.5% to his stake at $57.73 in **May-26 (post-spin)** and added in Dec-25 — the only meaningful open-market buying in the cohort. EDS spun off as **Versigent (VNT) 4/1/26**, leaving a higher-tech ADAS/software stub. Flat 12mo = still forgotten. Risk: post-spin financials in transition (numbers settling), auto-cyclical, EV exposure. **Strongest "still-cheap-with-a-catalyst-and-insiders-buying" — narrowly missed Final 3 on post-spin data uncertainty.**

### 8) NXST — Nexstar · $5.4B · ~8× fwd · +1.8%
Cheapest in the book (6.6× ttm). **TEGNA merger FCC-approved 3/19/26** (via ownership-cap waiver) → transformational local-TV scale + 2026 political-ad supercycle + potential full cap repeal. But the catalyst is *largely spent* (deal approved), there's a **13-insider sell cluster** around the approval, and broadcast is secularly declining. Cheap for reasons.

### 9) SOLV — Solventum · $13.1B · 11.3× fwd · +3.3%
3M healthcare spin (Apr-24) at 11.3× fwd, 55% gross margin, director open-market buy (3/10/26). Catalyst = portfolio reshaping (Purification/Filtration divestiture closed) + deleveraging + new-management capital redeployment. Spin-discount + medtech-quality; slow-grower (~2%).

### 10) PFE — Pfizer · $149.2B · ~9× fwd · +10.9%
Cheapest mega-cap pharma (~9× fwd), **6.8% dividend**, 70%+ gross margin, $4.5B cost program. The deepest "historically cheap" read (signal g) — but it's cheap *because revenue is shrinking* post-COVID and the pipeline/obesity story keeps stumbling. Income + optionality, not a compounder.

---

## PHASE 4 — THE FINAL THREE

**Selection logic:** highest-conviction *forgotten-quality-that-re-rates*, diversified across sector (industrial / healthcare / consumer), each answering a different brief-signal, each with a **verified** catalyst. Fraud gate is trivial for all three (mega/large-cap, audited, decades-real, no promotion) — the Archos Equities "is it real?" check is a formality here; the work is valuation + catalyst durability.

---
### 🥇 #1 — UPS (United Parcel Service) · $108.71 · 14.2× fwd · ~6% yield
**Bucket:** 3 (de-rated compounder), industrial-quality wrapper.

**The setup.** A wide-moat, duopoly parcel network — the kind of franchise that almost never gets cheap — trading at **14.2× forward vs. its own ~16–18× history**, with a **~6% dividend**, because the market fears three things at once: (1) UPS deliberately shedding low-margin Amazon volume, (2) a freight recession, (3) tariff disruption to cross-border. Every one of those fears is *resolving on a confirmed timeline*, which is exactly the ADBE/$NOW shape — a quality asset priced for a permanent impairment that is actually temporary.

**Why it re-rates (verified, Q1-2026 print + management guide):** the Amazon dilutive-volume purge is **nearly done** (Amazon down to 8.8% of revenue from 10.6%, target reached ~June-26); the Network Reconfiguration is delivering **~$3.5B** in annualized cost savings; SMB mix (the high-margin business) rose to 34.5% of US volume from 31.2%; and management explicitly guided to a **return to consolidated revenue AND operating-profit growth, with margin expansion, beginning Q2-2026 (~Aug print)**. The stock *fell ~18% in the past month* into that setup — the entry is being handed to you.

**Bull / base / bear (math):**
- **Bear (~$84, −23%):** freight stays recessionary, tariffs bite cross-border, dividend-coverage fear forces a trim; EPS stuck ~$7, multiple compresses to ~12×.
- **Base (~$128, +18% + ~6%/yr yield):** Q2 inflection confirms, op margin recovers toward 10%+, EPS rebuilds to ~$8.50 by '27, re-rate to 15×.
- **Bull (~$165, +52% + yield → ~1.6×):** margin to 11–12% on the leaner network, EPS ~$10 '27, 16–17×.

**What kills it:** the dividend payout is high — if the Q2 inflection slips and free cash flow disappoints, a dividend trim would break the income thesis and re-rate it *down*. Secondary kill: Amazon glide-down overshoots and the volume hole isn't refilled by SMB fast enough.

**Instrument:** **Equity is the core** (you're paid 6% to wait for an imminent, low-binary catalyst). For leverage, the **Jan-2028 LEAPS** are viable — low-moderate IV (~25%) means time value is cheap, the Bucket-3 LEAPS sweet spot; a moderately-ITM call captures the inflection with defined risk. No 2× single-stock ETF. *Re-quote the live chain.*

**Pattern match:** ADBE/$NOW playbook (de-rated quality, fear resolving) crossed with the "beaten-down survivor that inflects" shape from PATTERNS_AND_TRAPS — but at mega-cap, wide-moat quality. **Conviction: highest catalyst-certainty, moderate ceiling (~1.5–2×).**

---
### 🥈 #2 — AMGN (Amgen) · $328 · 14.9× fwd · 3.1% yield
**Bucket:** 3 (de-rated compounder) with a Bucket-1-style optionality overlay (MariTide).

**The setup.** The single highest-*business-quality* name the screen surfaced: large-cap biopharma, 75%+ gross margin, ~21% net margin, and — rare among cheap pharma — **revenue actually growing +10%** (not a melting patent cliff). It de-rated to ~14.9× forward because (a) the entire market's risk appetite went to AI, (b) healthcare carried an IRA drug-pricing overhang, and (c) the Street is skeptical Amgen can win a seat at the GLP-1/obesity table. It compounds through all three.

**Why it re-rates:** first, simple sector-broadening — healthcare is the most AI-abandoned quality sector, and a market that broadens re-rates the *growing* names first. Second, the embedded call option: **MariTide** (monthly obesity injectable). Verified status — Phase 3 **MARITIME-1/-2/-CV/-HF are ongoing; no Phase 3 data has read out yet**; Phase 2 showed **~17–20% weight loss** (competitive) but with tolerability (GI/bone-density) questions. A competitive Phase 3 readout (2026–27) re-rates AMGN into the multi-hundred-billion obesity TAM.

**Bull / base / bear (math):**
- **Bear (~$264, −19%):** MariTide disappoints on tolerability + IRA pressures the base; EPS ~$22 at 12× — and at 14.9× there isn't a deep valuation cushion to break the fall.
- **Base (~$375, +14% + 3%):** MariTide neutral, base compounds, EPS ~$25 '27 at 15×.
- **Bull (~$500–560, +50–70%):** MariTide competitive → obesity re-rate to 18–20× on $26–28 EPS.

**What kills it:** MariTide is binary — a tolerability-driven Phase 3 miss removes the optionality and leaves a 14.9× pharma that's the *least statistically cheap* name in the Final Three. The honest knock on AMGN vs. the deeper-value names (PFE 9×, BMY 10×): you're paying closer to fair value for the quality + the option.

**Instrument:** **Equity** for the compounding + 3% yield; **Jan-2028 LEAPS** to lever the MariTide optionality — moderate IV (~25–30%) keeps them affordable, and the multi-year duration spans the Phase 3 readout window (the rare case where a binary-catalyst LEAPS is correctly dated). No 2× ETF. *Re-quote live.*

**Pattern match:** the truest ADBE analog (quality compounding through an AI-displacement fear) with a moonshot graft (MariTide = a Bucket-1 lottery ticket living inside a Bucket-3 body). **Conviction: highest business quality; upside more binary; least cheap.**

---
### 🥉 #3 — BBY (Best Buy) · $75.83 · 11.6× fwd · 5.1% yield
**Bucket:** 3 (de-rated) — the brief's "hidden AI" pick.

**The setup.** The brief explicitly asked for *"a boring company that actually benefits from AI but the market hasn't reclassified it yet."* Best Buy is the cleanest concrete answer: it's priced as a dying big-box retailer at **11.6× forward with a 5% dividend**, while being the primary physical/retail beneficiary of the **AI-PC + Windows-10-end-of-life refresh supercycle** — a genuine, multi-year hardware-replacement wave (Q3 FY26 comps already turned +2.7% on it).

**Why it re-rates:** Windows 10 hit end-of-support in late 2025; CoPilot+ PCs with Intel/AMD/Qualcomm NPUs are the upgrade path; the installed base is enormous and aging. As that refresh runs through FY27–28, BBY's computing category inflects, comps go positive, and a 11.6× "melting-retailer" multiple normalizes toward ~13–14×. You collect 5% while you wait.

**The honest double-edge (verified — this is why it's #3, not #1):** the *same* AI boom that drives the refresh is now inflating **DRAM/HBM memory prices**, and management flagged memory-component cost inflation as the **#1 FY27 headwind** — higher ASPs partly offset lower units, but it pressures gross margin and affordability. AI is both BBY's tailwind (demand) and a margin headwind (input cost). And **insiders just sold a 6-officer cluster (3/23/26)** into the recovery — the opposite of the APTV tell.

**Bull / base / bear (math):**
- **Bear (~$55, −27%):** refresh fizzles, memory costs crush gross margin, Amazon resumes share-taking; EPS ~$5.50 at 10× (dividend likely held → still ~5% income).
- **Base (~$86 incl. yield, +8% price):** AI-PC cycle delivers, EPS ~$6.80 FY27 at 12×, + 5% yield.
- **Bull (~$105, +38% + yield):** multi-year refresh + services/membership growth, EPS ~$7.50, 14× normalization.

**What kills it:** secular Amazon/online share loss reasserts and the AI-PC cycle proves a one-year pull-forward rather than a multi-year wave; memory inflation turns a demand tailwind into a margin disaster. Lowest moat of the three — this is the speculative, highest-torque sleeve.

**Instrument:** **Equity** for the 5% income + cheapness; **Jan-2028 LEAPS** to lever the refresh cycle (moderate IV ~30–35%, still tradeable — unlike the high-IV watchlist names). No 2× ETF. *Re-quote live.*

**Pattern match:** the WINNER_UNIVERSE "ignored + real + catalyst" shape, but at large-cap and with the catalyst being *the AI cycle itself, reaching it sideways* — exactly the "hidden AI exposure not yet reclassified" the brief prized. **Conviction: best brief-signal fit + cheapest of the three; lowest quality/moat; insider selling is a real flag.**

---

### Final ranking & conviction

| Rank | Ticker | One-line | Conviction | Primary risk |
|---|---|---|---|---|
| **#1** | **UPS** | De-rated wide-moat duopoly, 6% yield, **confirmed Q2-26 inflection** | **Highest** (catalyst certainty) | Dividend coverage if FCF slips |
| **#2** | **AMGN** | Best-quality cheap pharma, **MariTide optionality**, healthcare rotation | **High** (quality) | MariTide binary; least cheap |
| **#3** | **BBY** | The **hidden-AI** pick — AI-PC refresh, 5% yield, 11.6× | **Speculative-tilt** (highest torque) | Memory-cost headwind + secular + insider selling |

**For a deeper-value tilt** the operator could swap in **PFE** (9× / 6.8% yield, deepest "historically cheap" read, but shrinking), **CVS** (confirmed turnaround, but ran +48%), or **INCY** (the +21% grower). **For insider conviction, APTV** is the standout (director buying post-spin) and arguably belongs in any 4th slot.

---

## APPENDIX A — DATA CAVEATS LEDGER (FAIL LOUD)

- **Universe is knowledge-seeded, not exhaustive** — Massive fundamentals screener = 403. Qualifying names outside the ~99-name seed exist and were not captured.
- **Massive rate limit (~5/min)** forced serial 12-month-return verification; non-finalist refiners VLO/MPC and insurers verified directly, others by disclosed prior where noted.
- **WebFetch (stockanalysis.com) bad fetches:** AKAM ($153, wrong), ZM ($114, wrong) — both excluded/flagged. GEN/DBX last-bar vs. site-price diverged ~5% (borderline C7 — both failed on Massive's authoritative close; not finalists).
- **SEC TTM mis-maps caught & corrected:** BBY ($28B→$42B rev), MDT (~$52B TTM artifact — failed C7 anyway), AMGN (~$53B TTM artifact → used ~$35B), MRK (SalesRevenueGoodsNet only; trailing P/E distorted). Finalist figures cross-verified.
- **(g) 5-year-avg P/E** not pulled as an exact series — "historically cheap" is approximate vs. known multiple history.
- **LEAPS** = qualitative; **live Jan-2028 chains not pulled** (Massive options tier likely gated). **Re-quote before acting.** No 2× single-stock ETFs identified for UPS/AMGN/BBY.
- **Insider data** as-of lag 5–48 days; **FOXA SEC TTM** as-of 2026-02-04 (stale).
- **APTV** financials straddle the 4/1/26 Versigent spin — post-spin run-rate still settling.
- **MariTide (AMGN), Cobenfy-adjunctive (BMY), TEGNA/FCC (NXST), Amazon-glide (UPS), Aptiv-spin, CVS-guide** — all catalyst facts **verified via WebSearch June-2026**, correcting stale priors (notably: BMY Cobenfy adjunctive *failed*; APTV spin *already done*; MariTide Phase 3 *not yet read out*).

## APPENDIX B — full verified pass-list quick reference
26 core + 3 refiners (tagged) + 4 insurers (tagged) = **33 names passing criteria 1–8**. Finalists: **UPS, AMGN, BBY** (added to WATCHLIST.md). Top-10 also-rans tracked informally: CVS, INCY, TGT, APTV, NXST, SOLV, PFE (+ BMY, FOXA, GM, HII, AGCO, MO, DVA as honorable mentions).

*End of screen. The operator decides — Archos Equities only finds and frames.*
