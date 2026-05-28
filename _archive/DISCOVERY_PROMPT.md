# DISCOVERY_PROMPT.md — Archos
# Version: 1.0 (derived from 3-phase research, 32-stock validation)
# Framework: H10 + H8 (refined) + H5 + H11 with H1' / H7 as supplementary

## Usage

This file is the reusable evaluation prompt for screening a candidate against the four-filter framework plus two supplementary signals. When running a screening session in Code, copy the "6-check evaluation prompt" section verbatim into the Code TASK section, replace `{CANDIDATE}` with the ticker, and execute. For batch screening across many candidates, use the wrapper at the bottom of this file and write results to `archos/screening/{YYYY-MM-DD}-screen.md`.

Every PASS verdict requires citations: source URLs, filing accession numbers, transcript dates. Do not produce "PASS" without evidence.

---

## The 6-check evaluation prompt

> For candidate {CANDIDATE}, evaluate the six checks below and produce a structured verdict using the rubric at the bottom. Cite source URLs, filing accessions, or transcript dates for every claim. Use BACKWARD-LOOKING analysis only — do not predict prices or recommend trades.

### Check 1 — Chokepoint mapping (H10)

**Question:** Does {CANDIDATE} have pure-play exposure to a chokepoint listed in `CHOKEPOINT_TAXONOMY.md`?

**Procedure:**
1. Open `CHOKEPOINT_TAXONOMY.md`. Identify which chokepoint row the candidate maps to. If no row matches, the candidate FAILS H10 — either the chokepoint belongs to the Monitor list (no qualifying pure-play in our universe yet) or the taxonomy is stale.
2. If a row matches, verify the bellwether mention is still current (within the last 18 months). Use web search to confirm the most recent quarter that NVDA / TSMC / AVGO / Microsoft / Meta / AMD discussed the chokepoint.
3. Determine the H10 tier:
   - **Vendor-level PASS:** Bellwether named {CANDIDATE} specifically, OR made a direct equity investment, OR announced a strategic partnership. Cite the date, source, and verbatim quote.
   - **Category-level PASS:** Bellwether named the chokepoint category but did not single out {CANDIDATE}. Cite the date, source, and verbatim quote.
   - **FAIL:** Neither vendor nor category mention found in the last 18 months.

**Tools:** `CHOKEPOINT_TAXONOMY.md` (this repo), web search for bellwether transcripts (Motley Fool / SemiAnalysis / Benzinga / company IR), EdgarTools `company_filings` for 8-K equity-investment disclosures.

**Output:**
- Status: VENDOR-LEVEL PASS / CATEGORY-LEVEL PASS / FAIL
- Mapped chokepoint: (from taxonomy)
- Bellwether: (which one)
- Mention date: YYYY-MM-DD
- Verbatim quote: "…"
- Source URL: …

### Check 2 — Structural filter (H8 refined)

**Question:** Is {CANDIDATE}'s market cap below $5B AND is more than 50% of its revenue tied to a single AI-infrastructure chokepoint end-market?

**Procedure:**
1. Pull live market cap via Alpha Vantage. **Do NOT use EdgarTools XBRL market cap** — it is stale and has produced material errors in prior research (e.g., showed AXTI $273M when real was $4.5B).
2. Pull most recent 10-K or 10-Q segment disclosure. Calculate the percentage of revenue from the chokepoint end-market. Note: end-market not product-line. WOLF passed product-line concentration on SiC but failed end-market because >50% revenue was EV/automotive, not AI infrastructure.
3. If pre-revenue (LWLG pattern), score H8 as FAIL on literal test and flag the candidate as "pre-revenue moonshot — out of design intent for this framework."

**Tools:** Alpha Vantage MCP for live market cap; EdgarTools `company_filings` for 10-K / 10-Q segment data; web search for company segment-revenue disclosures if filings are unclear.

**Output:**
- Status: PASS / BORDERLINE / FAIL
- Live market cap: $X (date, source)
- Revenue concentration: X% from the chokepoint end-market (cite filing)
- Notes: diversification details, if any; flag if pre-revenue

### Check 3 — Sentiment state (H5)

**Question:** What is {CANDIDATE}'s pre-screen sentiment classification?

**Procedure:**
1. Count sell-side analysts covering with current PT. Use Zacks / Finviz / consensus aggregators.
2. Check AI-thematic ETF inclusion: AIQ, BOTZ, ROBO, SOXX, SMH, WCLD. Use stockanalysis.com ETF holdings pages.
3. Estimate FinTwit / Reddit / Stocktwits mention volume using LunarCrush if available; manual web search as fallback.
4. Identify the dominant pre-screen narrative ("legacy industrial," "broken IPO," "regulatory duress," "consensus AI play," etc.).
5. Classify on the rubric:
   - **IGNORED-extreme:** regulatory duress, delisting threat, broken-IPO narrative, going-concern. Highest expected dose-response in design-intent winners (AXTI, NVTS, POWL, CRDO). **BUT:** structural-distress IGNORED-extreme can be wrong-tailed (WOLF wiped). Pair with H11 check before treating as upgrade.
   - **IGNORED:** low FinTwit volume, no AI-ETF inclusion, multi-year flat range, narrative confused
   - **NEUTRAL:** visible but not consensus AI play
   - **PARTIAL:** on some AI watchlists, lower expected magnitude
   - **LOVED:** consensus AI play → REJECT

**Tools:** Web search (analyst PTs, ETF holdings, narrative); LunarCrush MCP (social sentiment, micro-cap coverage thin); stockanalysis.com ETF holdings.

**Output:**
- Status: IGNORED-extreme / IGNORED / NEUTRAL / PARTIAL / LOVED
- Analyst count: N (cite source)
- AI-ETF inclusion: yes/no (cite source)
- FinTwit/Reddit volume estimate: low/medium/high (cite evidence)
- Dominant narrative: "…"

### Check 4 — Balance-sheet survival (H11)

**Question:** Can {CANDIDATE} survive long enough to capture the chokepoint rerate?

**Procedure:**
1. Pull most recent 10-Q or 10-K balance sheet via EdgarTools `company_filings`.
2. Calculate Net debt / EBITDA TTM. If under 5x → PASS.
3. If above 5x, calculate FCF runway: (cash + short-term investments) / TTM operating cash burn. If runway > 18 months → PASS.
4. Check 10-K for going-concern qualification language ("substantial doubt about ability to continue as a going concern"). If present → FAIL or BORDERLINE depending on whether asset-sale / refi roadmap is visible.
5. If sponsor-dependent (PSIX/Weichai pattern), flag separately — sponsor reliability is a hidden risk factor.

**Tools:** EdgarTools `company_filings` for 10-K / 10-Q balance sheet and going-concern language; web search for refinancing announcements.

**Output:**
- Status: PASS / BORDERLINE / FAIL
- Net debt: $X
- EBITDA TTM: $X
- Net debt / EBITDA: X.X x
- FCF runway: N months
- Going-concern in latest 10-K: yes/no
- Notes: sponsor dependency, refi roadmap, recent asset sales

### Check 5 — 8-K / 6-K confirmation trigger (H1', supplementary)

**Question:** Has {CANDIDATE} filed an 8-K or 6-K in the last 16 weeks containing chokepoint-confirmation language?

**Procedure:**
1. Run EdgarTools `search_filings_full_text` with form filter set to 8-K (US issuers) and 6-K (foreign private issuers — POET, IREN class names). Query terms:
   - "capacity expansion"
   - "record backlog"
   - "supply constrained"
   - "design win"
   - "long-term agreement"
   - "qualified supplier"
   - "production ramp"
   - "strategic partnership"
2. For each hit in the last 16 weeks, note accession number, filing date, and the lead time relative to today.
3. Score:
   - **PRESENT (with lead time):** at least one hit in the last 16 weeks; cite accession and date.
   - **ABSENT:** no hits matching the language set in 16 weeks.

**Tools:** EdgarTools `search_filings_full_text` (8-K + 6-K).

**Output:**
- Status: PRESENT / ABSENT
- Accession(s): …
- Filing date(s): YYYY-MM-DD
- Language matched: "…"
- Lead time vs today: -N days/weeks

### Check 6 — Specialist 13F upgrade (H7, supplementary)

**Question:** Has any specialist mandate fund opened a NEW position in {CANDIDATE} in the most recent quarterly 13F window?

**Procedure:**
1. Pull the most recent two quarterly 13F filings (45-day lag means Q1 filings appear by 5/15, Q2 by 8/15, etc.) for the specialist watchlist:
   - Hood River
   - William Blair
   - Baillie Gifford
   - Sculptor
   - Slate Path
   - Caption
   - Bridgeway
   - Kennedy
   - Acadian
   - Alyeska
   - Point72
   - Also: Aschenbrenner's Situational Awareness LP
2. For each fund, check whether {CANDIDATE} is a NEW position (not held in the prior quarter).
3. Score:
   - **PRESENT:** at least one specialist NEW position; cite fund + quarter + size + % of book.
   - **ABSENT:** no specialist NEW positions.

**Note:** H7 weakened materially in Phase 3 — 0/4 design-intent winners surfaced specialist 13F entries with meaningful lead time. Treat as opportunistic upgrade signal when present, NOT as a required filter. Absence does not preclude a candidate.

**Tools:** EdgarTools `search_filings_full_text` over 13F-HR forms with manager CIK list; LLMQuant `sec_13f_list_ticker_holders` as faster secondary when API up; whalewisdom.com as web fallback.

**Output:**
- Status: PRESENT / ABSENT
- Funds with new positions: (list with $ size + % of book + quarter)

---

## Verdict rubric

| Core filters passed (H10 + H8 + H5 + H11) | Verdict | Action |
|---|---|---|
| **All 4** | **ACCEPT** | Add to `CANDIDATE_UNIVERSE.md` as ACCEPT. Begin paper-track. |
| **3 of 4, with BORDERLINE on the miss** | **WATCH** | Add to `CANDIDATE_UNIVERSE.md` as WATCH with the borderline filter and reason annotated. Revisit when conditions update. |
| **2 or fewer core filters, OR any clean FAIL** | **REJECT** | Log in screening file with reason. Do not add to universe. If the candidate fits one of the documented different-pattern variants (sector pivot, M&A pivot, pre-revenue moonshot, geopolitical materials, AI services), note that classification. |

Supplementary checks (H1' filing trigger, H7 specialist 13F) upgrade conviction on ACCEPT candidates but do not change the verdict. A WATCH candidate with active H1' is a higher-priority watch than one without.

### Sentiment-magnitude dose-response (used to rank ACCEPT candidates)

When multiple candidates score ACCEPT, rank by H5 sentiment extremity:
1. IGNORED-extreme with H11 PASS → highest expected magnitude
2. IGNORED with H11 PASS → second
3. NEUTRAL with H11 PASS → third
4. PARTIAL with H11 PASS → lower-magnitude, include with caveat

**Critical caveat:** IGNORED-extreme with H11 FAIL is the WOLF anti-pattern — appears asymmetric, returns -98%. The H11 PASS is the dose-response disambiguator.

---

## Batch screening wrapper

For multi-candidate screening, paste the following as the Code TASK and supply the candidate list:

> Apply the 6-check evaluation prompt above to each candidate in the list below. For each candidate, run all 6 checks and produce the verdict using the rubric. Aggregate results into a single screening output file at `archos/screening/{YYYY-MM-DD}-screen.md` with the format:
>
> ```markdown
> # Screening run — {YYYY-MM-DD}
> 
> ## Summary
> - Candidates screened: N
> - ACCEPT: M (list)
> - WATCH: P (list)
> - REJECT: Q (list)
> 
> ## Per-candidate scorecards
> 
> ### {TICKER 1}
> [full 6-check output]
> 
> ### {TICKER 2}
> [full 6-check output]
> 
> ...
> ```
>
> When the batch exceeds 15 candidates, spawn parallel general-purpose subagents (one per 5 candidates) and synthesize their outputs into the single screening file. This is the operational pattern used in Phase 3 — sequential 6-check screening of 20+ candidates exceeds context budget.
>
> Candidates to screen:
> {paste comma-separated ticker list}

---

## Phase-3 refinements baked into this prompt

1. **H8 wording is the refined version** — "sub-$5B + >50% revenue from a single AI-infrastructure chokepoint END-MARKET" (not just product line). Product-line concentration is insufficient if revenue is anchored to a non-AI end-market (the WOLF / EV-automotive pattern).
2. **H10 is two-tiered** — vendor-level and category-level. Category-level still permits ACCEPT but requires H8 + H5 + H11 to do more discrimination work.
3. **H11 is a CORE filter, not supplementary** — Phase 2 added H11 after WOLF (going-concern IGNORED-extreme returned -98%). Phase 3 confirmed H11's value via correct rejection of BW (going-concern qualified Dec 2024 10-K, returned 30-49x — admitting BW would explode false-positive risk from any going-concern legacy industrial with vague chokepoint exposure).
4. **H7 has been downgraded** — 0/4 Phase 3 design-intent winners surfaced specialist mandate 13F entries with meaningful lead time. Combined hit rate 3/12 = 25%. Treat as opportunistic upgrade only.
5. **H5 sub-classifier** — IGNORED-extreme must be paired with H11 to distinguish narrative-neglect IGNORED (right-tailed, e.g., AXTI / CRDO / BE) from structural-distress IGNORED (can be wrong-tailed, e.g., WOLF, or unpredictably right-tailed, e.g., BW).

## Source files

Full draft prompt origin: `_master_docs/bottleneck-asymmetry-research/DISCOVERY_ENGINE_SPEC_v2.md`
Phase 3 refinements: `_master_docs/bottleneck-asymmetry-research/HYPOTHESIS_EVOLUTION.md` §"Phase 3"
Chokepoint mapping: `CHOKEPOINT_TAXONOMY.md` (this repo)
