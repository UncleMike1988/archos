# LOTTO TICKET BOX — Micro-Cap Recovery Screen

**Screen run:** 2026-06-03 (prompt dated 2026-06-01)
**Price/cap data as-of:** 2026-06-02 (Massive snapshot); SEC financials per latest 10-K/10-Q on file
**Sizing rule (operator's, not a recommendation):** $1K max per position. Expect 80-90% zeros. Entertainment with an edge.
**Isolation:** This box is a SEPARATE category from the Archos Equities research universe. NOT added to WATCHLIST.md.

---

## BOTTOM LINE UP FRONT

The sub-$5M space behaved exactly as the thesis predicted: it is overwhelmingly death-spirals, going-dark shells, serial reverse-split diluters, and dev-stage names that never had a real business. Out of a **raw universe of ~210 names** pulled across five SEC-filing vectors, the funnel produced **3 names that strictly clear every gate** (sub-$5M cap + real ≥$10M revenue once + still filing on a US exchange + not hard-rejected + at least one moderate recovery signal), plus **2 high-quality businesses that sit just over the $5M cap line** and are surfaced as honorable mentions because they are the best *businesses* in the entire screen.

This is **below the 5-15 "success" range** the prompt targets. That is an honest finding, not a methodology failure: when you intersect (a) under $5M now, (b) real $10M+ revenue history, (c) still exchange-listed and current on filings, (d) no toxic convert / no serial reverse split / no fraud, and (e) a credible "someone is trying to fix it" signal, the set is genuinely tiny. Most names die on (d) — the financing structure is already eating the equity.

**The qualifying three (sub-$5M):**

| Rank | Ticker | Cap | Rating | One-line |
|------|--------|-----|--------|----------|
| 1 | **DRCT** | $2.17M | LONG SHOT | $35M-rev adtech (peak $157M); just recapitalized via $25M non-toxic preferred + regaining listing; credible founder-CEO |
| 2 | **GWAV** | $2.95M | HAIL MARY | Real $33M-rev scrap-metal recycler run by a real operator, but ~2-3mo cash runway and imminent delisting |
| 3 | **SNYR** | $3.99M | HAIL MARY | $30M-rev consumer-health brand (FOCUSfactor); CEO was a heavy buyer in 2025 but balance sheet now negative-equity with huge dilution pending |

**Just over the $5M cap (best businesses, technically out of spec on criterion b):**

| Ticker | Cap | Rating | One-line |
|--------|-----|--------|----------|
| **SCKT** | $7.42M | LONG SHOT* | 30-yr real hardware co, $15M rev, 50% GM; Chairman just put $400K of his own cash in at the current price via a CLEAN convert — the single best fix-it signal in the screen |
| **CENN** | $6.52M | HAIL MARY* | Real $18M-rev commercial-EV maker, but -$73M loss on $18M rev, 1-for-60 reverse split, China-heavy |

\*Would be in the qualifying list if not for the cap. SCKT ($7.4M) and CENN ($6.5M) both breach the hard "under $5M" gate (criterion b) — included as honorable mentions only.

---

## PHASE 1 — UNIVERSE BUILD

Five vectors, all run against SEC EDGAR via authenticated filing tools. Vector logic: companies that *were* exchange-listed (so once real/sizable) and are *now* in listing trouble or restructuring (so now tiny) cluster in specific 8-K item codes and filing phrases.

| Vector | Method | Raw hits |
|--------|--------|----------|
| Listing-deficiency notices | 8-K **Item 3.01** (Notice of Delisting / Failure to Satisfy Continued Listing Rule), corpus-wide, two 90-day windows (Dec 2025–Jun 2026) | ~150 |
| Bankruptcy / receivership | 8-K **Item 1.03**, corpus-wide, 9 months | 17 |
| Listing compliance REGAINED | Full-text `"regained compliance"`, 8-K, last 90d (recovery-signal seam) | 81 |
| Reverse stock splits | Full-text `"reverse stock split"`, 8-K, last 60d | 64 (1,019 total) |
| (Cross-referenced) collapse / new mgmt | Item 5.02 / 1.01 picked up per-name in Phase 3 | — |

**Raw universe after dedup: ~210 unique tickers.** Target was 50-200; comfortably exceeded.

### Phase 1 → operating-company shortlist
The prompt's Phase 2 explicitly excludes dev-stage names ("we want fallen angels, not failed startups"). This is the highest-leverage filter and was applied first:

- **Dropped en masse: clinical-stage biotech** (no product revenue, ever) — ~70 names: RNAZ, ENSC, GTBP, PTN, SKYE, RANI, TPST, KZR, TERN, RAPT, VTYX, HOWL, LYRA, ANEB, CERO, HURA, TNYA, CRIS, OTLK, IOBT, FBLG, JUNS, KTTA, PDSB, MREO, ATOS, APLT, RVPH, ELOX, QNCX, CUE, KALA, SCYX, PSTV, DCOY, INTS, IMUX, ABP, GBIO, HCWB, VTGN, etc. These are *failed-startup-shaped* (no $10M revenue), not fallen angels.
- **Dropped en masse: SPACs / blank-checks** (never operated) — COLA, XXI, ASPC, FSHP, SPKL, ALCY, FVN, CCCX, BAYA, OAKU, CRTAF, CBRRF, RAC, RENX, MWYN, AFJK, QETA, DAIC, APAD, etc.
- **Dropped: obvious large/mid-caps** with technical (non-bid-price) 3.01 notices — LC, THR, GENC, NVRI, FFIC, CVGW, AMWD, RICK, HUBG, SNCY, CSGS, CCL, CTRA, CMA, CIVI, MAPS, DAY, ZEUS, SNCR, BRCC, DVAX, HI, JAMF, PCH, etc.

That left **~57 real operating-company candidates** (had or have a product/service business) carried into market-cap gating + full Phase 2-3 DD, run as 5 parallel due-diligence sweeps.

---

## PHASE 2-4 — THE FUNNEL (57 → 3+2)

Each of the ~57 was gated on **current market cap** (Massive ticker-overview `market_cap`, = price × shares, authoritative) then run through the real-business test, kill-signal screen, and recovery-signal tagging.

**Gate attrition:**
- **Cap > $5M → out of spec** (still real businesses, just too big now): FTHM $17.7M, BLIN $14M, LEDS $16M, SMSI $21.5M, CETX $10.4M, LASE $92.7M, AREC $293M, NIXX $22M, INTZ $16.6M, REBN $14.5M, TOMZ $20.9M, NUTR $169M, ILLR $40M, HTCR $82.8M, CETY $9.3M, ATER $13M, ANY $16.6M, AIRE $13.7M, GROV $60M, PRTS $40M, KORE $91M, CCEL $36M, CCLD $105M, GIFT $28.3M, DFNS $20.1M, CSAI $10.7M, DVLT $434M, SRXH $48M, USBC $133M, POLA $7.6M, OLB $6.7M, MGRX $6.6M, INHD $5.7M, NCPL $7.1M, HWH $7.7M. (SCKT $7.4M and CENN $6.5M held back as honorable mentions.)
- **Never had $10M revenue → fails Phase-2 criterion 1**: SINT (max $2.9M), SGLY (max $1.8M recent), ASNS ($3.7M), MGRX ($456K), INHD ($4.5M), NCPL ($8.5M), HWH ($867K), ATPC ($3.4M), OLB ($8.7M), MYSZ ($9.4M — just misses).
- **HARD REJECT — kill signal** (the heart of the screen): see catalog below.

### KILL-SIGNAL CATALOG (the instructive drops)
These are real, sub-ish-cap companies that an undisciplined screen would surface — and each is a trap:

| Ticker | Cap | Kill signal (HARD REJECT) |
|--------|-----|---------------------------|
| **ONFO** | $4.3M | **Toxic/variable convertible** — Nov-2025 SPA: up to $300M facility, conversion price *adjustable* with a $0.22 floor on a $0.64 stock; 424B3 resale active. Textbook CYCU/death-spiral structure. |
| **EDBL** | $2.1M | **Death spiral** — 8 separate "unregistered equity sales" (8-K 3.02) in 90 days (rolling at-market issuance) + delisting notice + going concern. |
| **CTNT** | $4.9M | **Death spiral** — 1-for-16 (Oct-24) + 1-for-200 (Apr-26) reverse splits, auditor change Jan-26, ATM dilution, China-trade-dependent rev collapsed 97% ($55M→$1.3M). |
| **EZRA** | $2.2M | **Chronic diluter** — 3 reverse splits in <4yr (1:15, 1:17, 1:40); active dilution shelf. |
| **KUST** | $1.5M | **Chronic diluter** — 3+ reverse splits in <1yr (ex-Digital Ally meme name). |
| **SDOT** | $2.7M | **Chronic diluter + insolvent** — 2 reverse splits in <12mo (1:10 Sep-25, 1:20 May-26), equity -$57M, $2.9M total assets, active delisting. |
| **SGLY** | $2.9M | China-based logistics; never $10M recent rev; unresolved securities class action re: CEO background. |
| **SOPA** | $0.17M | **Chapter 11** (8-K Item 1.03, May-2026). |
| **SSKN** | $0.6M | **Going dark** — filed Form 15 to terminate SEC reporting (~Mar-2026). Was a real $30M-rev derm-device co — now uninvestable. |
| **EVTV** | $6.1M | **Reverse-merger shell swap** — merging into "Azio AI"; existing holders diluted to 11%; no real revenue history. |
| **BKYI** | OTC | **Delinquent filer** — off Nasdaq to OTC Link; NT 10-K filed, no FY2025 10-K on file. Fails "no delinquent filer status." Real IAM product with a Q1 inflection, but no audited numbers to verify and no exchange listing. |
| **GWAV** (see below) | $2.95M | Borderline — survives into the list as a HAIL MARY but carries IBN paid-IR + late filings as yellow flags. |

The recurring lesson, matching `PATTERNS_AND_TRAPS.md`: **the financing structure is the tell.** Variable-rate/adjustable converts and serial reverse splits are the mechanism by which a "cheap" $30M-revenue company at a $2M cap grinds to zero regardless of the operating business. That kills most of the sub-$5M field before fundamentals matter.

---

## PHASE 4 — FINAL PROFILES (sorted REAL SHOT → LONG SHOT → HAIL MARY)

> No name in this screen reached **REAL SHOT** on a strict reading. The cleanest setup (SCKT) is over the cap; the best sub-$5M name (DRCT) carries a heavy dilution overhang. Ratings below reflect that honestly.

---

### 1. DRCT — Direct Digital Holdings, Inc.  ·  LONG SHOT
**Current price: $3.10 | Market cap: $2,172,353 | Nasdaq | 701,243 Class-A shares | 73 employees | listed Feb 2022**
Peak market cap (last 7y): ~$150-300M (2022-2023, revenue-surge era)

- **What it was/is:** End-to-end programmatic advertising platform. Two segments — **Colossus SSP** (sell-side; specializes in multicultural / underserved publishers) and **Orange 142 + Huddled Masses** (buy-side media buying; OTT/CTV, display, video, audio). All revenue US-attributed.
- **What happened:** Revenue went **$157M (FY2023) → ~$62M (FY2024) → $34.7M (FY2025)** — an ~78% top-line collapse in two years after a supplier dispute and a credit-facility squeeze hammered the SSP business; balance sheet went negative and Nasdaq sent a 3.01 deficiency notice (8-K 2026-04-07 and 2026-04-28).
- **Revenue history:** $157M → $62M → $34.7M. **$10M-once: PASS (overwhelmingly).**
- **Cash / runway:** OCF ~-$8.9M/yr (FY2025); equity turned marginally positive (~$0.4M) post-restructuring. Going concern flagged in the Q1-2026 10-Q.
- **Recovery signal:** **H (new financing, non-toxic)** + **F (working to regain compliance).** April-2026 8-K (items 1.01 new agreement / 1.02 termination / 3.03 / 5.03 charter amendment) is the **$25M Series A Preferred** recapitalization at a **fixed $2.50 conversion** (NOT a variable-rate death-spiral), which repaired the balance sheet and reset the listing path; a 2026-05-21 8-K (item 1.01) added a **Roth ~$50M equity facility** (S-1 registering ~20M shares for resale). *(SEC event data 13 days stale as of pull — confirm the compliance cure closed.)*
- **CEO background:** **Mark Walker** — co-founder, Chairman & CEO. Real operator pedigree (corporate dev / Deloitte background); built the company from zero to $157M revenue. Not a penny-stock promoter. No open-market insider buying in last 120d.
- **Bull case (1 sentence):** A genuinely real adtech business that did $157M revenue, now at a $2.2M cap with a non-toxic $25M recapitalization just completed — if revenue stabilizes around $35M and the equity facility is drawn sparingly, the tiny float re-rates violently.
- **Kill risk (1 sentence):** The Roth equity facility registers ~20M shares against 701K current — if drawn aggressively into a still-shrinking business, existing equity is diluted toward zero before the turnaround proves out.
- **Lottery ticket rating: LONG SHOT** (best sub-$5M name; real business + real, clean-ish recapitalization, offset by a brutal dilution overhang and an 78% revenue decline that hasn't visibly bottomed).

---

### 2. GWAV — Greenwave Technology Solutions, Inc.  ·  HAIL MARY
**Current price: $3.55 | Market cap: $2,945,190 | Nasdaq | 829,631 shares | 192 employees | listed 2015**
Peak market cap (last 7y): $200M+ (2021-2022; traded >$100/share pre-split)

- **What it was/is:** Operator of **13 scrap-metal recycling facilities** across VA, NC, OH — collects, classifies, shreds/shears/separates ferrous & nonferrous scrap (end-of-life vehicles, appliances, construction/industrial material) for resale. A genuine, physical, 192-employee operating business.
- **What happened:** Years of heavy losses and serial dilution/reverse-splits cut the share count to 830K; revenue is real but the operation is structurally cash-negative. Multiple Nasdaq 3.01 notices (Nov-2025, Apr-2026, May-2026); NT 10-K (Mar-2026) and NT 10-Q (May-2026) — **can't file on time.**
- **Revenue history:** ~$35.7M (FY2023) → $33.3M (FY2024). **$10M-once: PASS.** Trades at ~0.09x revenue.
- **Cash / runway:** ~$2.6M cash vs **-$17.3M operating cash flow** on $33M revenue (burning ~52% of revenue in cash) and $15.8M debt → **~2-3 months runway** absent emergency financing. Going concern: effectively yes.
- **Recovery signal:** Weak/stale — **G (restructuring):** CEO converted ~$17M of his own notes to equity to clear the convertible stack (May-2024, but >12mo old and itself dilutive); CFO change Feb-2026 (Isaac Dietrich). **Yellow flag:** paid IR via IBN (InvestorBrandNetwork).
- **CEO background:** **Danny Meeks** — founder of Empire Services, a *real* metal-recycling operator (not a serial promoter). The industry credibility is genuine; the financial execution has been catastrophic.
- **Bull case (1 sentence):** A real $33M-revenue recycler at 0.09x sales — if Meeks can drag operating cash flow toward breakeven, the equity is wildly mispriced.
- **Kill risk (1 sentence):** ~2-3 months of cash against a business that is cash-negative at the *operating* line and a delisting that looks imminent — without a dilutive rescue it reaches zero.
- **Lottery ticket rating: HAIL MARY** (real business + real operator, but the runway and delisting clock are the most acute in the qualifying set).

---

### 3. SNYR — Synergy CHC Corp.  ·  HAIL MARY
**Current price: $0.265 | Market cap: $3,993,169 | Nasdaq | 15,079,956 shares | 28 employees | listed 2013**
Peak market cap (last 7y): uncertain; plausibly $50M+ in prior years given $30M revenue

- **What it was/is:** Consumer-health / CPG brand house — **FOCUSfactor** (brain-health supplement with real shelf space in major US retailers) plus Flat Tummy, Hand MD, Neuragen. A real branded-products business with retailer distribution.
- **What happened:** Swung from **+$2.1M net income (FY2024) to -$12.3M loss (FY2025)** — a ~$14M deterioration — and stockholders' equity went to **-$23.1M (technically insolvent).** Nasdaq 3.01 deficiency 2026-05-18.
- **Revenue history:** ~$30.4M (FY2025). **$10M-once: PASS.** Trades at ~0.13x revenue.
- **Cash / runway:** OCF ~-$2.6M (FY2025, ~$650K/q); negative equity means it operates on borrowed money. Going concern: implied.
- **Recovery signal:** Marginal — **insider buying (signal C, but STALE):** CEO/Chairman **Jack Ross bought 35 times** through mid-2025 (net +1.85M shares, 6 insiders), strong conviction — **BUT** at $2.20-3.90 vs $0.27 now (he is ~88% underwater) and **the most recent buy was 2025-07-30, outside the 90-day window** → signal C does not strictly qualify. May-2026 8-K (item 1.01) = a new agreement (nature unconfirmed).
- **Kill signal watch:** Hudson Global ELOC registering **~101.7M shares vs 14.8M outstanding (~6.8x dilution)** and a proxy seeking **reverse-split authority up to 1-for-200** — heavy dilution machinery in place (ELOC, not a death-spiral convert, so not an auto-reject, but close).
- **CEO background:** **Jack Ross** — longstanding, real CPG operator; not a promoter. His 2025 buying shows belief; the post-buy collapse shows the thesis has gone against him.
- **Bull case (1 sentence):** FOCUSfactor is a genuine retail brand; at 0.13x revenue, if debt is renegotiated and losses stabilize, there's a real company under the wreckage.
- **Kill risk (1 sentence):** Negative -$23M equity plus a ~6.8x-dilution ELOC and a possible 1:200 reverse split means the balance sheet can't absorb another bad year and existing holders get crushed.
- **Lottery ticket rating: HAIL MARY** (real $30M brand, but the dilution structure is one notch from a hard reject and the insider signal is stale).

---

## HONORABLE MENTIONS — best businesses, JUST OVER the $5M cap

These two breach the hard "under $5M" gate (criterion b) and so are **not** in the qualifying list. They are surfaced because, on business quality and recovery signal, they are the strongest names the screen produced — operator's call on whether the $1.5-2.4M cap overage matters for a lottery basket.

### SCKT — Socket Mobile, Inc.  ·  (would be LONG SHOT) — cap $7.42M
**Price $0.90 | 8,240,958 shares | Nasdaq | 53 employees | listed 1995**
Peak cap: ~$82M (mid-2021 at ~$9.96/share)

- **Business:** Bluetooth/NFC barcode **data-capture hardware** for mobile POS, asset tracking, ticketing, healthcare, logistics (CaptureSDK developer ecosystem). A 30-year real business with real manufacturing/distribution in Fremont CA and ~50%+ gross margins.
- **Revenue:** ~$18.8M (FY2024) → ~$15.1M (FY2025), -20%; Q1-2026 ~$3.7M (-7%). **$10M-once: PASS.** Trades below one quarter's revenue.
- **Recovery signal — the best in the screen:** **C (verified) + H (clean financing).** Chairman / 10%-owner **Charlie Bass purchased a $400,000 convertible note at a FIXED $0.90/share** on **2026-03-27** (no reset, no floor, no variable rate; special-committee approved). That is a credible insider putting fresh capital in *at the current price* via a non-dilutive-style instrument — the textbook "someone credible is rebuilding at the bottom" tell.
- **Kill risk:** Revenue is in a real ~20%/yr decline (channel shrinkage — is it structural?); sub-$1 bid triggered a 2026-05-20 Nasdaq delisting notice; thin cash. 
- **Why it's only an honorable mention:** $7.42M cap exceeds the $5M rule. On every other axis it is the cleanest fallen-angel in the screen. If the operator is willing to flex the cap ceiling for a lottery basket, this is arguably the single best ticket here.

### CENN — Cenntro Inc.  ·  (HAIL MARY) — cap $6.52M
**Price $4.45 | 1,465,452 shares | Nasdaq | 155 employees | listed Jan 2022**
Peak cap: ~$500M+ (SPAC-listing era 2022)

- **Business:** Commercial **EV manufacturer** (Metro, Logistar, iChassis programmable platform) — real revenue across Europe/Americas/Asia, 155 employees.
- **Revenue:** ~$31.3M (FY2024) → ~$18.1M (FY2025), -42%. **$10M-once: PASS.**
- **Kill risk:** -$73M net loss on $18M revenue (losses ~4x revenue); **1-for-60 reverse split (Apr-2026)** signals severe prior share destruction; ongoing unregistered equity sales; China-heavy asset base (transparency/repatriation risk); leadership opacity in filings.
- **Recovery signal:** None strong (filings are administrative). Surfaced because it is a real $18M-revenue manufacturer at a $6.5M cap — but the loss profile and reverse-split history make it a HAIL MARY even before the cap overage.

## BORDERLINE / JUST-MISSES (documented, not in the list)
- **MYSZ — My Size ($2.65M):** Naiz Fit AI-sizing SaaS (real, growing ~131% CAGR since 2020) + Orgad e-commerce. **Fails Phase-2 criterion 1** — revenue peaked at **$9.4M (FY2025), never crossed $10M.** Also <1 quarter of cash ($0.9M vs ~$1.3M/q burn), going concern, Mar-2026 deficiency notice. A genuine micro-SaaS turnaround story but it does not clear the "$10M revenue once" bar, so it is out by the rules.
- **POLA — Polar Power ($7.6M):** Real DC-generator maker (peak rev ~$25M), but revenue -55% in one year to $6.3M, equity ~$144K, CEO departed, deficiency notice — active collapse, and over cap.

---

## WHY SO FEW PASSED (honest assessment)

The prompt asked for honesty if the count came in low. It did. Three reasons:

1. **The financing structures kill almost everything first.** The dominant population in the sub-$5M, still-filing, once-real cohort is companies kept alive by toxic variable-rate converts (ONFO), rolling at-market dilution (EDBL), or serial reverse splits (EZRA, KUST, SDOT, CTNT). These are *engineered* to transfer value from common holders to financiers — they are not recovery setups, they are slow-motion zeros. They correctly hard-reject, and they are most of the field.
2. **"Real $10M+ revenue once" is a strong filter.** It removes the entire clinical-biotech and SPAC population (which is the *majority* of sub-$5M Nasdaq names), leaving only companies that genuinely operated. Most of *those* that fell to sub-$5M did so because the business itself broke, not because the market overreacted.
3. **"Someone credible is trying to fix it" is rare and usually undercut.** A genuine, verifiable fix-it signal (insider buying their own stock with cash, a non-toxic recap, a credible new operator) is uncommon in this tier, and where it exists it is usually paired with a near-term runway or dilution cliff (DRCT's ELOC, GWAV's 2-month cash, SNYR's negative equity). SCKT is the one place the fix-it signal is clean — and it's $2.4M over the cap.

This is the box working as intended: it found the handful of real fallen operating companies in the rubble and rejected the manufactured ones. The expected outcome of the basket is still mostly zeros; the thesis is that one DRCT-shaped or SCKT-shaped name rebounds 100-500x and pays for the rest.

## METHODOLOGY LIMITATIONS (for the next run)
- **OTC Pink Current names under-covered.** The vectors keyed on SEC 8-K item codes (3.01/1.03) and listing-event phrases, which skew toward exchange-listed (Nasdaq/NYSE) names getting deficiency notices. A company already trading OTC that still files 10-Ks but doesn't file a *recent* listing-deficiency 8-K would be missed. A dedicated OTC Markets "Pink Current + once-$50M" screen is a separate pass worth running.
- **Chapter 11 *emergences* under-covered.** The 1.03 pull caught bankruptcy *filings*, not plan-effective *emergences with new equity* (which file as plan-confirmation 8-Ks / fresh-start 10-Ks). Most 1.03 hits were large-caps or shells; the post-emergence "clean balance sheet + new team" vector (signal D) deserves its own targeted search.
- **Data freshness.** Caps are a 2026-06-02 snapshot; some SEC event feeds ran ~13 days stale (flagged per name). Re-confirm DRCT's compliance cure and GWAV's late filings before any entry.

---

## DATA SOURCES
- SEC filing events / financials / insiders: authenticated EDGAR tool surface (`material_events` corpus-wide by 8-K item; `company_brief`, `financial_trends`, `insider_activity` per name).
- Market cap / shares / employees / list date: Massive `GET /v3/reference/tickers/{ticker}` (market_cap field = authoritative price × shares).
- Price history / peak detection: llmquant `equity_historical_prices` (adjusted for splits).
- Screen executed as 5 parallel DD sweeps over ~57 operating-company candidates; survivors re-verified individually against primary SEC filings.
