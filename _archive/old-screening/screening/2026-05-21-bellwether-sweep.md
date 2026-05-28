# Bellwether Relationship Sweep — 2026-05-21

## Sweep parameters

- **Search window:** last 30 days (focus on 2026-04-21 → 2026-05-21);
  several hits extend back to Feb-Mar 2026 because they are the
  load-bearing bellwether-relationship announcements not yet in 13Fs.
- **Market cap filter:** strict < $10B (live, web-verified — not XBRL)
- **Bellwethers:** NVDA, TSMC, AVGO, Microsoft, Meta, AMD
- **Exclusions applied:**
  - Confirmed winner universe (Phase 1+3): AXTI, SNDK, AEHR, NVTS, POWL,
    ONTO, APLD, POET, IREN, BE, NBIS, AAOI, CRDO
  - Borderline-large already in taxonomy: LITE
  - Phase 2 controls (10 names): AMAT, KLAC, MRVL, AMD, COHR, WOLF, ACLS,
    AMKR, ARM, CRUS
  - Prior CANDIDATE_UNIVERSE: SHAZ (DD REJECTED), SIVEF (WATCH)
  - Prior reject log: DUOT, EOSE, TE, HPS.A, LTRX, NNBR, DIOD, FPS, IESC,
    SPXC, CAMT, MOD, IPWR, HIVE, BITF, CLSK, RIOT, KEEL, EVTV, USAR,
    GLW, MU, HLIT, LPTH, AAON, PSIX
- **Total search queries executed:** 21 web + 1 EdgarTools 8-K full-text

---

## TIER 1 hits — equity investment or direct contract from bellwether

**NONE qualifying under $10B and not in exclusion list.**

The 2026 NVDA equity-investment cohort (COHR $2B in March, MRVL $2B
March 31, LITE $2B in March, IREN up-to-$2.1B, NBIS $2B March, CRWV
$2B January, GLW multi-year May 6) is high-signal but every name
is either (a) already a confirmed winner, (b) a Phase 2 control, or
(c) materially above $10B post-announcement.

Microsoft's compute-capacity neocloud deals (~$33B aggregate across
Nebius $19.4B, Nscale $14B, CoreWeave, Lambda) involve only
above-threshold or non-public counterparties.

| Candidate | Bellwether | Why excluded |
|---|---|---|
| COHR | NVDA $2B March 2026 multi-year optics partnership ([NVIDIA newsroom](https://nvidianews.nvidia.com/news/openai-and-nvidia-announce-strategic-partnership-to-deploy-10gw-of-nvidia-systems)) | Phase 2 control AND market cap now $57.65B (May 1, 2026) ([macrotrends](https://www.macrotrends.net/stocks/charts/COHR/coherent/market-cap)) |
| MRVL | NVDA $2B + NVLink Fusion March 31, 2026 ([NVDA 8-K filing](https://www.sec.gov/Archives/edgar/data/1835632/000119312526134462/d113606dex991.htm)) | Phase 2 control AND >$80B mega-cap |
| CRWV | NVDA $2B January 2026 | >$20B post-IPO |
| Nscale | $14B Microsoft Norway data-center deal | PRIVATE — not investable |
| Lambda | Microsoft compute deal | PRIVATE |

---

## TIER 2 hits — design win / certified supplier / cloud partner under $10B

| Company | Ticker | Mkt Cap | Bellwether | Relationship | Date | Source |
|---|---|---|---|---|---|---|
| SAKURA Internet | 3778.T (Tokyo) | **~$762M USD** (May 15, 2026) | **Microsoft** | Named as primary domestic GPU-compute partner in MSFT $10B Japan AI infrastructure investment 2026-2029. Sovereign-cloud architecture — Sakura supplies GPU compute consumed through Azure. | **2026-04-03** | [Microsoft Source Asia](https://news.microsoft.com/source/asia/2026/04/03/microsoft-deepens-its-commitment-to-japan-with-10-billion-investment-in-ai-infrastructure-cybersecurity-workforce/), [CNBC](https://www.cnbc.com/2026/04/03/sakura-internet-microsoft-ai-japan-softbank-investment.html) |
| Kulicke & Soffa | KLIC | **~$5.30B USD** (May 20, 2026) | **NVDA / TSMC** (category, via HBM packaging chain) | TCB (thermo-compression bonding) equipment supplier. ASMPT-Hanmi-K&S triumvirate for HBM4 die-stack bonding. Q1 FY26 revenue +27% YoY, TCB and memory the named growth drivers. | Q1 FY26 reported earlier 2026 | [stockanalysis KLIC](https://stockanalysis.com/stocks/klic/market-cap/), [Yahoo Finance article](https://finance.yahoo.com/news/amkor-technology-amkr-33-5-031459607.html) (context only) |

### Per-candidate quick H8/H10 check

**SAKURA Internet (3778.T) — chokepoint #7 AI hosting / GPU colos / neocloud**
- **H10 (bellwether mention):** **PASS — Vendor-level.** Microsoft Japan named Sakura as a primary collaborator alongside SoftBank and three system integrators (Fujitsu, Hitachi, NEC, NTT Data) in the April 3, 2026 sovereign-cloud announcement. This is the same shape of vendor-level H10 fire that triggered the NBIS PIPE ($700M Dec 2024) and APLD stake ($160M Sep 2024) signals — a named bellwether putting capital and direct commercial commitment into the named company.
- **H8 (sub-$5B + >50% AI-infra revenue):** **PASS on size ($762M USD); UNVERIFIED on revenue mix.** Sakura's legacy revenue is Japanese domestic hosting/colo and SaaS — the AI cloud carve-out is the recent vector. The framework's WOLF guardrail says product-line concentration ≠ end-market concentration. Risk profile mirrors SIVEF (mixed revenue base awaiting clean AI-DC carve-out).
- **H5 (sentiment):** **BORDERLINE PARTIAL.** Stock surged 20.27% on April 3 announcement. Year-to-date and trailing-month sentiment should be re-measured before classification — the April pop puts H5 dose-response in the PARTIAL-to-LOVED transition zone, not IGNORED.
- **H11 (balance sheet):** **UNVERIFIED.** Foreign-listed (TSE); need to pull most recent annual filing for net debt / FCF runway / auditor opinion.
- **Verdict:** **WATCH** — pending H8 revenue-mix decomposition and H11 balance-sheet verification. The H10 fire is unambiguous (vendor-level Microsoft, dated, sourced). The framework's two foreign-listed handicaps apply: (a) US 13F-HR universe will not show specialist mandates (H7 silent — accepted per Phase 3 downgrade), and (b) full-text 8-K search is unavailable; must rely on TSE filing translations.
- **Action:** Add to CANDIDATE_UNIVERSE.md as WATCH. Next-cycle full 6-check screening when (a) FY2025 / latest quarterly filing translation surfaces revenue mix, AND (b) sentiment re-measures post-April pop.

**Kulicke & Soffa (KLIC) — chokepoint #3-4 HBM stack inspection / wafer-level bonding adjacency**
- **H10:** Category-level only, via the HBM packaging supply chain. NVDA names HBM at every earnings cycle; HBM stacking requires TCB; KLIC is one of three TCB suppliers (with ASMPT and Hanmi). NOT a direct vendor-level bellwether mention.
- **H8:** **LIKELY FAIL.** TCB and Advanced Solutions are a growth segment but ball/wedge bonding for consumer/auto remains the revenue plurality. AI-infrastructure end-market is <50% as of latest reporting.
- **H5:** **LOVED — FAIL.** Stock up +210.95% trailing one year per stockanalysis.com. Mar 2026 mkt cap $3.65B → May 2026 $5.30B = +45% in two months. Post-rerate, not IGNORED.
- **H11:** Clean balance sheet (not a concern).
- **Verdict:** **REJECT on H5 LOVED + H8 end-market mix.** Note as a Tier 4 supply-chain inference for chokepoint #3-4 but the entry window is closed and the AI-infrastructure pure-play test fails. Consistent with framework correctly rejecting LOVED rerated names (HPS.A pattern). **Do not advance.**

---

## TIER 3 hits — MOU / non-binding / exploratory (re-check in 30 days)

| Company | Ticker | Mkt Cap | Bellwether (implied) | Relationship | Date | Source |
|---|---|---|---|---|---|---|
| Ceres Power | CWR.L | **~$1.65B USD** (~£1.24B post-rerate, May 2026) | Meta / Microsoft (category-level on SOFC chokepoint #9) | Delta Electronics + Centrica data-center SOFC partnership announced. Delta is the integration partner — not a bellwether — but the implied bellwether layer is the Meta/MSFT category-level mention of energy as a constraint. Ceres Endura 10.8kW SOFC platform launched April 18, 2026 specifically for data center off-grid power. | **2026-04-18** (Endura launch) | [Proactive Investors CWR.L](https://www.proactiveinvestors.com/companies/news/1091503/), [tipranks](https://www.tipranks.com/news/company-announcements/ceres-power-sees-partner-fuel-cell-deal-target-data-centres-and-heavy-industry) |

**Why Tier 3 not Tier 2:** the announced counterparty (Delta + Centrica)
is not a bellwether on the Archos list. The bellwether linkage is
inferred through the SOFC chokepoint #9 (Meta Q3 2024, Microsoft 2024
"paucity of energy" category-level mentions). Direct vendor-level
bellwether name-drop is absent.

**Quick filter check:**
- H10: Category-level only (chokepoint #9 has Meta+MSFT mentions)
- H8: Royalty-licensing revenue model; ~£45M contracted 2026 with
  growing data-center share. AI-DC end-market crossing 50% is plausible
  but not yet verified.
- H5: **LOVED — Stock has more than doubled in one month** to May 2026.
  Goldman upgraded to "buy" on data center fuel cell opportunity.
  Jefferies raised PT to £480. This is the textbook post-rerate /
  consensus-discovery setup — framework H5 filter says LOVED = reject.
- H11: Pre-profit but well-capitalized after multiple equity raises.

**Verdict:** **NOTE BUT DO NOT ADVANCE.** Even if H10/H8/H11 fire,
the H5 LOVED state at +100% in one month is the same shape as the
HPS.A May 2026 ATH rejection. Recall: framework correctly rejected
HPS.A as the cleanest chokepoint #6 candidate purely because the
entry window had closed. Same logic. Re-eval on a 30%+ drawdown.

---

## TIER 4 hits — supply chain inference (no direct bellwether name-drop)

Per chokepoint cross-reference:

### Chokepoint #1 — CPO / InP substrates / laser arrays
- **Sumitomo Electric** (5802.T) — InP substrate competitor to AXTI per
  TrendForce supply-chain mapping. Japanese conglomerate, $20B+ market
  cap — **EXCLUDE on size**.
- **JX Metals / JX Holdings** — InP substrate. Private subsidiary of
  JX Holdings (5020.T, ~$10B+). **EXCLUDE on parent size + investability**.
- No new sub-$5B InP / CPO pure-plays identified beyond AXTI, POET,
  SIVEF (already on WATCH).

### Chokepoint #3-4 — HBM equipment (besides ONTO, AEHR)
- **ASMPT (HKEX 0522)** — HK$72.53B = **~$9.3B USD** market cap.
  Borderline-large per Archos Tier 2 (IREN/CLSK class). World's
  leading TCB / hybrid bonding / fan-out equipment supplier. Q1 2026
  EPS +290% YoY, revenue +27%, driven by AI-led TCB orders. SK hynix
  HBM4 TC bonder order December 2025.
  - H10: Category-level via NVDA HBM commentary cascading to TCB chain
  - H8: PROBABLY FAILS — diversified backend equipment supplier, AI
    end-market growing but not >50% yet
  - **Verdict:** **Note for Sounding Board discussion as $5-10B Archos
    Tier 2 class.** Not an Archos Tier 1 ($<5B) candidate. Borderline
    on H10 (chokepoint chain inference, not direct bellwether mention).
  - Source: [companiesmarketcap ASMPT](https://companiesmarketcap.com/hkd/asm-pacific-technology/marketcap/)
- **Hanmi Semiconductor (042700.KS)** — KRW 27.32T = ~$20B USD.
  HBM 6-side inspection + Dual TC Bonder. **EXCLUDE on size** (~$20B,
  way above $10B threshold).
- **BESI (AMS:BESI)** — €21.5B = ~$23B USD. Hybrid bonding leader
  (only tool capable of sub-micron HBM4 stacking). **EXCLUDE on size**.

### Chokepoint #8 — 800G+ optics / EML lasers / AECs (besides AAOI, CRDO, LITE)
- No new sub-$5B AI-DC optics pure-play surfaced. Dominant EML / DFB
  supply (Lumentum, Coherent, Mitsubishi, Sumitomo, Broadcom) is fully
  cataloged in existing taxonomy. AEC market dominated by mega-caps
  (Molex, Amphenol, TE Connectivity).
- LWLG remains the pre-revenue-moonshot blind-spot anti-pattern —
  out of scope per framework.

### Chokepoint #9 — SOFC / on-site DC power (besides BE)
- **Ceres Power (CWR.L)** — covered in Tier 3 above. Implied bellwether
  via Meta/MSFT category-level on power. Direct partner is Delta
  Electronics + Centrica.

### Chokepoint #6 — Grid / HV switchgear (besides POWL, HPS.A)
- Web search surfaced no new sub-$10B pure-play. Market is dominated
  by mega-caps (Schneider, Vertiv, ABB, Eaton, Siemens Energy, Hitachi
  Energy, GE Vernova). The chokepoint is real and well-named by
  Microsoft capex-constraint disclosures, but the public-pure-play
  surface is exhausted at AAON (rejected), HPS.A (LOVED-rejected),
  POWL (winner).

### Chokepoint #7 — AI hosting / GPU colos / neocloud (besides APLD, IREN, NBIS)
- **Sakura Internet (3778.T)** — covered in Tier 2 above.
- Nscale and Lambda (Microsoft counterparties) are PRIVATE — not investable.

---

## New names flagged for full screening

| Ticker | Mkt Cap | Tier | Chokepoint | Next step |
|---|---|---|---|---|
| **3778.T (Sakura Internet)** | ~$762M USD | T2 | #7 AI cloud / GPU colo (sovereign Japan) | **Add to WATCH.** Full 6-check next screening cycle after H8 revenue-mix verification (next TSE filing) + H5 re-measurement. |
| ASMPT (0522.HK) | ~$9.3B USD | T2-borderline / T4 | #3-4 HBM packaging supply chain | **Sounding Board flag.** $5-10B Archos Tier 2 class candidate (IREN/CLSK-pattern, not Tier 1 sub-$5B). Not added to WATCH — note in INSIGHTS only. |

---

## Sector-pivot blind-spot rejections (working as intended)

Searches naturally surface sector-pivot names — these are the
HIVE/BITF/CLSK/RIOT/KEEL/EVTV analog pattern documented as a blind spot.
Framework correctly rejects ex ante:

| Ticker | Sector pivot pattern | NVDA/B300 announcement |
|---|---|---|
| AlphaTON Capital Corp | Compute-lease shell | Blackwell compute lease, $1.2M/mo from March 2026 |
| Bitzero Holdings | Bitcoin miner pivot (Norway) | 8x B300 servers / 64 GPUs Q1 2026 |
| Axe Compute Inc. | Compute-pivot shell | $260M 36-month 2,304x B300 cluster |
| Digi Power X Inc. | Former Digihost (bitcoin miner) | $19.6M 24-month Blackwell GPU rental w/ SubQ AI |
| Alpha Compute Corp | Compute-pivot shell | $32.2M B200 lease (AI research lab) |
| K Wave Media | Compute-pivot shell | Meta/AI infrastructure adjacency |

**Pattern note:** every one of these has the same structure — shell
or pre-existing-non-AI-business retroactively re-narrated as an AI
compute provider via a single multi-million-dollar GPU contract.
This is the CIFR / pre-pivot APLD / pre-pivot IREN pattern. The
framework documents these as out of scope for the four-filter
ex-ante screen. The fact that the framework rejected each
without burning a full 6-check evaluation is a working-as-intended
test of the sector-pivot guardrail.

---

## Discovery notes

### New bellwether vocabulary / chokepoint language spotted

1. **NVDA "Omniverse DSX"** = NVIDIA Data center Service Explorer. Used
   in IREN partnership announcement ("up to 5 GW of NVIDIA DSX-aligned
   AI infrastructure"). This is the AI-factory-as-a-product framing —
   may become a new chokepoint #11 over time as NVDA productizes the
   integrated DC stack. **Watch:** next NVDA earnings (Q1 FY27 late
   May / early June 2026) for further DSX vocabulary.
2. **NVDA "Vera Rubin"** = next-gen CPU after Grace. Meta named "Grace
   and future Vera CPUs" as committed deployment in their 2026 NVDA
   partnership extension. Microsoft's Nscale Norway deal includes
   "Vera Rubin chips" — meaning bellwether forward-disclosure has
   moved one generation ahead of Blackwell.
3. **AMD MI450 (rack-scale Helios)** + MI300/MI350 deployments at Meta:
   the AMD-Meta 6-GW agreement (February 24, 2026) with 160M-share
   warrant is the largest single AMD-customer commitment in disclosure.
   Suggests an AMD ecosystem layer parallel to NVDA's neocloud +
   optical layers — but at current scale it's a two-party (AMD-Meta)
   story without obvious sub-$5B pure-play exposure.
4. **Broadcom "Tomahawk 6 Davisson"** = 102.4-Tbps Ethernet switch
   with integrated CPO. NextHop and Micas Networks named as design
   partners — both private. Reaffirms chokepoint #1 (CPO) as
   NVDA-AND-AVGO-named, multi-vendor — strengthens H10 conviction
   for AXTI / POET / SIVEF chain. **Action:** confirm next CHOKEPOINT
   refresh that AVGO mentions are now load-bearing on CPO, not just
   networking.

### Re-announcement vs new content

- **Coherent (COHR)** NVDA $2B partnership: not new — announced March
  2026, re-amplified at OFC May 2026 and Q3 FY26 earnings. Stock
  rerated +14% on the May amplification (now $57.65B — out of scope).
- **AMKR** advanced packaging boom: not new — 2026 capex narrative is
  consistent through Q1. AMKR is a Phase 2 control regardless.
- **TSMC CoWoS expansion** May 14, 2026: incremental capacity
  doubling (75-80K → 120-130K wafers/month by year-end 2026). Confirms
  the NVDA-60%-CoWoS-allocation chokepoint #1-3 dynamic but no
  sub-$10B pure-play action.

### Bellwether silence (negative signal)

- **AMD** has not named a sub-$10B partner in any 2026 announcement.
  All large AMD partnerships (Meta 6-GW, Nutanix, OpenAI-adjacent)
  involve only mega-cap or private counterparties. The AMD ecosystem
  layer has not yet diffused to the small-cap surface that NVDA has
  reached via APLD/NBIS/IREN/SHAZ/Sakura.
- **TSMC** advanced packaging partner-name surface is exhausted at
  mega-cap OSATs (Amkor/ASE) — no new sub-$10B chokepoint-pure-play
  inference identified this sweep.

### Tool-stack issues

- **EdgarTools `search_filings_full_text`** with query
  `"NVIDIA" AND ("agreement" OR "partnership" OR "investment")`
  on 8-K forms 2026-04-21 → 2026-05-21 returned **0 results**.
  Suspicious — should have caught the May Coherent earnings 8-K
  exhibit references at minimum. Either (a) the query is interpreting
  the boolean syntax differently than expected, or (b) full-text
  indexing of "NVIDIA" as a content term in 8-K exhibit attachments
  is weak. **Action:** for next bellwether-sweep cycle, switch
  EdgarTools query to phrase-specific ("strategic partnership"
  NEAR(NVIDIA, 10)) or use the form-filtered 8-K Item 1.01
  (Material Definitive Agreement) feed instead of free-text.

- **Web search yielded best signal for partnership announcements**;
  EdgarTools yielded best signal for full-text chokepoint language
  in earlier first-screen run. Different tools for different
  query types. Keep both in the cadence.

- **Foreign listings** are a recurring blind spot for forward bellwether
  sweeps — Sakura Internet (TSE), ASMPT (HKEX), Ceres Power (LSE),
  Hanmi (KRX), BESI (AMS) all surfaced only via web search, not via
  US-SEC EdgarTools. Need a parallel non-US filing aggregator (TSE
  EDINET, HKEX HKEXnews, LSE RNS) for next-generation bellwether
  sweep tooling.
