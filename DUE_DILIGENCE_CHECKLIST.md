# DUE_DILIGENCE_CHECKLIST.md — Archos
# Version: 2.0 (major update — tiered H11, moonshot classification,
# network-failure-pattern check, forward P/S framing, going-concern
# tiering, WATCH re-eval integration)
#
# CHANGELOG v1.1 → v2.0:
# - Added Check 1.7: Network-failure-pattern (from ALMU DD lesson)
# - Added Check 1.8: Auditor quality (from CYCU/EXYN DD lessons)
# - Added Check 2.6: Contract type classification (from CTM DD lesson)
# - Added Check 3.5: Toxic financing detection (from CYCU DD lesson)
# - Tiered H11 going-concern into RED vs FLAG (from EXYN/GCTS lesson)
# - Added Check 5.4: Forward P/S framing (from IREN/neocloud lesson)
# - Added Check 5.5: Backlog quality decomposition (from CTM/CYCU lesson)
# - Added Moonshot Classification tier (from AIRJ/pre-revenue lesson)
# - Added Section 7: WATCH Re-eval Protocol
# - Updated SHAZ calibration case + added CYCU/ALMU calibration cases
#
# PURPOSE: Every ACCEPT candidate must pass this checklist BEFORE
# capital allocation. The four-filter framework (H10/H8/H5/H11)
# finds candidates. This checklist vets them. Both are required.
#
# TIME BUDGET: 60-90 minutes per candidate via Code session.
# A single RED does not auto-reject — but it MUST be documented
# and the risk explicitly accepted before proceeding.

## How to use

After a candidate surfaces from the weekly scan or other screening,
run this checklist via Code. Each section produces a score:

  CLEAR  — no issues found
  FLAG   — issue found, manageable with position sizing or monitoring
  RED    — material risk that likely disqualifies the candidate

Hard reject rules:
- Three or more RED scores = hard reject regardless of framework score
- Any single RED on Section 1 (Management) or Section 2 (Counterparty)
  = hard reject unless the human explicitly overrides with documented reasoning

## Position sizing tiers (determined by DD outcome):

| Tier | DD Profile | Sizing | Instrument | Horizon |
|---|---|---|---|---|
| Conviction | 0 RED, ≤2 FLAG, bellwether confirmed | $15-25K | LEAPS preferred | 12-18 months |
| Standard | 0 RED, 3-4 FLAG, solid fundamentals | $5-10K | LEAPS or equity | 12-18 months |
| Nano-cap | 0 RED, ≤4 FLAG, sub-$500M, real revenue | $3-5K | Equity only | 12-18 months |
| Moonshot | 0 RED, pre-revenue, bellwether relationship, can raise capital | $1-2K | Equity only | 18-month hard expiry |

---

## Section 1 — Management Integrity

| Check | How | Red flag |
|---|---|---|
| 1.1 CEO/CFO litigation history | Web search + EDGAR full-text on CEO/CFO names + "lawsuit" / "sued" / "fraud" / "SEC" / "self-dealing" | Prior fraud allegations, self-dealing suits, SEC enforcement actions |
| 1.2 Prior company track record | Web search CEO name + prior companies. Check if prior entities are bankrupt, delisted, or faced regulatory action | Pattern of failed/litigious entities (SHAZ: Mawson sued Manning for $11.5M) |
| 1.3 Related-party transactions | Read most recent 10-K "Related Party Transactions" section. Flag any vendor, customer, or financing source controlled by management or their affiliates | Insider-controlled vendors receiving company payments. CEO acquiring own prior company (CYCU: Kelly acquiring Halo Privacy) |
| 1.4 Supervoting / entrenchment | Check proxy for dual-class. Flag if CEO controls >50% votes on <10% economics | Entrenchment without economic alignment (SHAZ: 65%/1%; IREN: 43.6%/4.6%) |
| 1.5 Public statement retractions | Web search for restatements, corrections, amended filings | Material claims made then retracted (SHAZ: "NVIDIA shareholder" retracted) |
| 1.6 Paid investor awareness | Web search for IR campaigns, promotional infrastructure. Check SEC filings for marketing disclosures. Look for CorporateAds, RedChip, Litchfield Hills, or similar paid micro-cap promoters | Company paying promoters while claiming transformative contracts (SHAZ: RedChip; CYCU: CorporateAds + Litchfield Hills) |
| 1.7 Network-failure-pattern | For each board member, 10%+ holder, and founding investor, check involvement in other public companies. Search for shared connections to prior bankruptcies, delistings, or SEC enforcement | Multiple principals sharing connections to a prior failure (ALMU: DenBaars + Tompkins + Shealy all tied to Akoustis Chapter 11; SPAI: Erdberg → COMSovereign delisted) |
| 1.8 Auditor quality | Identify the audit firm. Check PCAOB inspection reports for deficiencies. Flag single-office practitioners, firms with recent PCAOB sanctions, or firms cited for failing to test the exact categories relevant to the company | PCAOB-deficient auditor on categories matching company risk (CYCU: WWC cited for revenue + digital assets + related-party — all three present at CYCU) |

**Score:** CLEAR / FLAG / RED

---

## Section 2 — Counterparty Quality

| Check | How | Red flag |
|---|---|---|
| 2.1 Counterparty revenue vs contract value | Find counterparty annual revenue. Compare to annual contract obligation | Contract annual payment > 2x counterparty annual revenue (SHAZ: ESDS 6.3x) |
| 2.2 Counterparty balance sheet vs security requirements | Find counterparty total assets. Compare to LC/guarantee requirements | Security > counterparty total assets |
| 2.3 Counterparty public acknowledgment | Search counterparty's own communications for mention of the contract | Counterparty silence on a transformative deal |
| 2.4 Counterparty strategic logic | Does the contract make sense for the counterparty's stated business? | Contract contradicts counterparty positioning |
| 2.5 Counterparty sanctions / regulatory risk | Check counterparty customer list for OFAC SDN, EU sanctions | Major counterparty customer is sanctioned |
| 2.6 Contract type classification | For government contracts: determine FFP, CPFF, IDIQ, T&M, OTA. For commercial: binding vs LOI vs MOU. Read the actual filing language | IDIQ ceiling reported as "backlog" without disclosing funded amount (CTM: 79% priced options, only 4.8% funded). LOI reported as "contract" (SHAZ pattern). Subcontract reported as "direct award" (SPAI: $1M subcontract marketed as Army direct) |

**Score:** CLEAR / FLAG / RED

---

## Section 3 — Funding Source Verification

| Check | How | Red flag |
|---|---|---|
| 3.1 Lender identity | Is the lender a regulated bank, registered fund, or known credit provider? | Unregulated or recently-formed lender (SHAZ: USD.AI DeFi protocol) |
| 3.2 Lender capacity vs facility size | Find lender AUM or lending capacity. Compare to facility size | Facility > 50% of lender total capacity |
| 3.3 Lender's other borrowers | Search for other companies using the same lender | Co-borrowers are unrelated micro-caps or shell companies |
| 3.4 Facility conditions | Read 8-K for conditions precedent, drawdown triggers, contingencies | "Subject to execution of definitive documentation" = not binding (IREN: $3.6B GPU facility commitment letter not signed) |
| 3.5 Toxic financing detection | Check for equity lines of credit with variable conversion prices, convertible notes with death-spiral mechanics (conversion at discount to VWAP), or serial S-1/S-3 shelf takedowns | ELOC at 90% of lowest VWAP = death spiral (CYCU: Yield Point $60M ELOC). Multiple S-1 raises in 12 months. Pipeline dilution > 100% of current outstanding |

**Score:** CLEAR / FLAG / RED

---

## Section 4 — Short Interest & Adversarial Research

| Check | How | Red flag |
|---|---|---|
| 4.1 Published short reports | Web search for activist short reports | Detailed short report with specific, verifiable claims |
| 4.2 Short report claim verification | For each material claim, verify independently from primary sources | Claims that verify against SEC filings, court records, counterparty financials |
| 4.3 Short interest level | Web search short interest percentage | >15% SI on sub-$5B = significant adversarial conviction. NOTE: high SI is NOT auto-reject — it's a squeeze amplifier if the fundamental thesis is intact (Cluster 2) |
| 4.4 Insider selling post-IPO | Check Form 4s and S-1/S-3 resale registrations | Large insider blocks registered for resale. Discretionary selling (non-10b5-1) at peaks. CEO selling > $1M while company is pre-revenue |

**Score:** CLEAR / FLAG / RED

---

## Section 5 — Revenue Reality Check

| Check | How | Red flag |
|---|---|---|
| 5.1 Current vs projected revenue | Compare TTM revenue to forward estimates. Flag if consensus requires >5x current within 12 months | Extreme ramp dependency without binding contracts to support it |
| 5.2 Revenue concentration | What % from single contract/customer? | >50% from one counterparty = single point of failure |
| 5.3 Sell-side coverage quality | Check for conflicts: did covering firm lead IPO, hold shares, or receive fees? | Covering analyst firm is also selling shareholder (SHAZ: Lucid Capital; GCTS: Zacks SCR sponsored) |
| 5.4 Forward P/S framing | For companies with binding contracted revenue (LOI doesn't count), compute P/S on forward contracted ARR, not just TTM. For pre-revenue with no contracts, use TTM only | TTM P/S alone can be misleading for early-stage companies with signed contracts. IREN at 37x TTM but 5x forward contracted = reasonable. GCTS at 37x TTM with no binding contracts = expensive. The distinction is whether contracts exist to underwrite the forward revenue |
| 5.5 Backlog quality decomposition | For any company reporting "backlog": decompose into funded, unfunded, priced options, and IDIQ ceiling. Compute funded-to-total ratio | Funded < 20% of headline backlog = misleading (CTM: 4.8% funded; CYCU: ~40% "locked in"). Backlog growing while revenue declining = paper not converting (CYCU: backlog 5x'd while revenue -15%) |

**Score:** CLEAR / FLAG / RED

---

## Section 6 — Social Signal Layer (/last30days)

**This section runs as a Code session using /last30days tool.**

Output goes to: archos/due-diligence/last30days/{TICKER}-last30days-{date}.md

| Check | What to look for | Red flag |
|---|---|---|
| 6.1 Organic bull case exists | Are credible, named buy-side PMs or independent researchers making a fundamental case? | No organic bull case. Narrative carried entirely by paid promotion + conflicted sell-side |
| 6.2 Reddit engagement volume | Check major investing subs | Zero engagement = nobody with real capital is interested (not auto-reject, but combined with 6.1 failing = warning) |
| 6.3 Independent verification of bear claims | Has anyone independently verified short-seller claims? | Independent verification strengthens bear case materially |
| 6.4 Management response quality | Has management issued point-by-point rebuttal or deflected? | Deflection or silence on verifiable claims = claims likely not defensible. Suing anonymous critics instead of rebutting = deflection (CYCU: sued Stocktwits user) |
| 6.5 Paid promotion patterns | Paid IR, comment-bait, coordinated pump patterns? | Paid IR + social pump + news-bot amplification = promotional infrastructure |
| 6.6 Suspicious timing | Do announcements cluster around lockup expiries or insider selling windows? | Announcement → lockup expiry within 10 days = narrative management for exit |

**Score:** CLEAR / FLAG / RED

---

## H11 Going-Concern Tiering (v2.0 — replaces binary treatment)

Going-concern language in filings is NOT an automatic RED. Tier it:

**RED (hard reject):**
- Going concern + declining revenue + no binding customer contracts +
  cash < 6 months + no demonstrated ability to raise capital
- Going concern + toxic financing (death spiral ELOC, variable
  conversion notes) actively diluting
- Going concern + promotional infrastructure (the company is
  pumping stock to fund operations via dilution)
- Examples: CYCU ($2M cash, revenue declining, death spiral ELOC,
  paid promotion); GCTS ($7.2M cash, $49M debt due 2026, 37x P/S)

**FLAG (proceed with caution, reduce position size):**
- Going concern + real customers with binding contracts + post-IPO
  or post-de-SPAC with demonstrated ability to raise equity at
  reasonable terms + revenue growing or stable
- Going concern + legitimate strategic investors (VC, defense
  fund, sovereign) who would likely participate in next raise
- Going concern is a CASH problem, not a BUSINESS problem — the
  company has product-market fit but needs one more capital raise
  to reach escape velocity
- Examples: EXYN ($7.2M cash, but SOCOM evaluation + Reliance
  $25M investor + post-IPO with fresh capital — H11 alone would
  be FLAG; Hesai NDAA cliff was the actual killer)

**Apply the tier based on the COMBINATION of going concern + other factors,
not going concern in isolation.**

---

## Moonshot Classification (v2.0 — new tier)

A candidate that passes H10 (bellwether relationship), H5 (IGNORED),
and H11-tiered (can survive 12+ months with a raise) but is
PRE-REVENUE gets classified as a Moonshot rather than auto-rejected.

**Moonshot criteria (ALL must be met):**
1. H10 passes at category level or higher (real bellwether relationship)
2. H5 is IGNORED or NEUTRAL (asymmetry exists)
3. H11 is FLAG-tier (not RED-tier) going concern
4. DD Sections 1-2 are CLEAR or FLAG (no RED on management or counterparty)
5. No promotional infrastructure (Section 1.6 / 6.5 must be CLEAR)
6. Insider behavior is BUYING or NEUTRAL (not net selling)
7. Technology has independent validation (peer review, government
   testing authority, Nobel-class scientific foundation, or equivalent)

**Moonshot position rules:**
- $1-2K equity only (no LEAPS — no options chain at this cap)
- 18-month hard thesis expiry date set at entry
- If the commercial catalyst hasn't fired by expiry, sell regardless
- No averaging down — if the thesis breaks, exit at any price
- Monthly re-eval during WATCH re-eval cycle

**Moonshot examples from DD history:**
- AIRJ: Would qualify (GE Vernova JV, insiders buying, Nobel
  chemistry, CLEAR management, pre-revenue, $299M cap). $1-2K
  equity with 18-month expiry on commercial launch.
- ALMU: Would NOT qualify (RED management — insider selling
  $27.5M, Akoustis network failure pattern)
- EXYN: Would NOT qualify (RED H11 — Hesai NDAA regulatory cliff
  makes the going concern structural, not just a cash problem)

---

## Section 7 — WATCH Re-eval Protocol (v2.0 — new section)

Every WATCH candidate gets a 5-point status check during the
weekly WATCH re-eval cycle (runs from WATCH_REEVAL_PROMPT.md):

| Check | What | Action |
|---|---|---|
| 7.1 Trigger status | Has the specific re-eval trigger documented in CANDIDATE_UNIVERSE.md fired? | FIRED → promote to DD queue. NOT FIRED → hold. |
| 7.2 New material filings | Any 8-K, 10-Q, 10-K, Form 4 filed in last 14 days? | Material positive → consider promoting. Material negative (going concern, restatement, insider dump) → consider demoting. |
| 7.3 Price action | Stock up or down >20% since added to WATCH? | Up >50% with no catalyst → asymmetric window may be closing. Down >30% → verify thesis intact or cut. |
| 7.4 Sentiment shift | Has sentiment moved from IGNORED toward LOVED? | Analyst upgrades, ETF inclusion, FinTwit discovery all erode H5 edge. |
| 7.5 Thesis integrity | Based on 7.1-7.4, is the original thesis intact? | INTACT → hold. DEGRADED → consider demotion. BROKEN → demote to REJECT. |

**WATCH re-eval verdicts:**
- PROMOTE → trigger fired, thesis intact, queue for DD or position decision
- HOLD → no change, continue monitoring
- DEMOTE → thesis broken or degraded beyond recovery, move to REJECT log
- THESIS EXPIRY → name has been on WATCH >6 months with no trigger → demote unless human explicitly overrides with updated reasoning

---

## Calibration Cases

### SHAZ (6/6 RED — the original calibration)

| Section | Score | Key finding |
|---|---|---|
| 1. Management | RED | $11.5M self-dealing suit; 65%/1% supervoting; NVIDIA retraction; RedChip $50K |
| 2. Counterparty | RED | ESDS: $40M rev vs $250M/yr obligation; Gazprombank customer |
| 3. Funding | RED | USD.AI DeFi protocol; $284M capacity vs $500M facility |
| 4. Short / Adversarial | RED | Bleecker Street verified; 1/3 float registered for resale |
| 5. Revenue | RED | Near-zero TTM; conflicted sell-side |
| 6. Social | RED | Zero organic bulls; paid promotion; deflection response |

### CYCU (5/5 RED — v2.0 calibration, nano-cap promotional trap)

| Section | Score | Key finding |
|---|---|---|
| 1. Management | RED | CEO acquiring own prior company; COMSovereign-pattern serial failure; PCAOB-deficient auditor; 1-for-30 reverse split |
| 2. Counterparty | RED | $112M "backlog" = 40% locked-in, 60% IDIQ ceiling; revenue DECLINING while backlog 5x'd; subcontractor model |
| 3. Funding | RED | $2M cash, going concern, $60M death spiral ELOC at 90% lowest VWAP; 300%+ pipeline dilution |
| 4. Short / Adversarial | RED | Suing anonymous critics; "unauthorized press release" episode; stock manipulation investigation |
| 5. Revenue | RED | Revenue declining 3 years ($19.4M → $15.1M); "no AI in production software" per own 10-K; paid Litchfield Hills + CorporateAds |

### ALMU (4 RED / 2 FLAG — v2.0 calibration, network-failure-pattern)

| Section | Score | Key finding |
|---|---|---|
| 1. Management | RED | $27.5M insider selling on $4.7M revenue; CEO 10b5-1 amendment; Akoustis bankruptcy network (DenBaars + Tompkins + Shealy) |
| 2. Counterparty | FLAG | NASA/DoD contracts real but all R&D grants, zero production; commercial revenue $41K/quarter |
| 3. Funding | FLAG | $38.6M cash (adequate); $50M ATM filed; 47% share-count growth |
| 4. Short / Adversarial | RED | 20.46% SI; Mispriced Assets published bear thesis with specific claims |
| 5. Revenue | RED | $4.7M TTM on $420M cap = 90x P/S; guidance NARROWED to $4.2-4.6M = declining; gross margin compressed 35pp |
