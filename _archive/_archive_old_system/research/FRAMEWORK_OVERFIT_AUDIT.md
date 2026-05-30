# FRAMEWORK_OVERFIT_AUDIT.md — Archos

**Audit #3 — "Would the current v2.1 framework have ACCEPTED its own historical winners?"**
**Date:** 2026-05-28
**Session type:** autoresearch / audit (research only — no framework or DD-checklist changes made this session; this is the EVIDENCE a future governance session would act on).
**Method:** 25 in-design-intent winners reconstructed at their pre-discovery lows (5 parallel sector subagents, ground-truth = `research/pattern-discovery/batch1-5_*.md` + targeted web search), scored COLD against the CURRENT v2.1 rules (CLAUDE.md four-filter + DUE_DILIGENCE_CHECKLIST.md), no hindsight, no grading on a curve.
**Data note:** pre-move caps/prices/end-market mixes are historical lows taken from the batch files (sourced from financial aggregators / SEC filings on the 2026-05-26 discovery run) plus per-name SEC/10-K verification by the subagents. No *current* cap is written here, so the real-time-cap-verification governance rule is not triggered; the audit is backward-looking by construction.

---

## 1. EXECUTIVE SUMMARY

**True sensitivity under the CURRENT v2.1 rules is far below the CLAUDE.md-claimed "12/12 = 100% within design intent."** Scored cold at each pre-discovery low: **strict ACCEPT-track sensitivity = 2/24 ≈ 8% (rules as literally written) and ≈ 5/24 ≈ 21% (rules read as intended, sector-relative + H10-extended co-primary). Lenient sensitivity (WATCH + Moonshot-caught count as catches) = ~30% literal / ~63% intended.** The single biggest overfit leak is **the strict H8 ">50% of revenue from a single AI-DC end-market" gate**: applied at the pre-discovery low it REJECTS at least seven flagship AI-infra winners — **AXTI (97x), SNDK (44x), POWL (38x), NVTS (16x), BE (16x), AEHR (12x), LITE (10x)** — because at the low the chokepoint end-market was the *fastest-growing minority*, not the trailing majority. The test measures the level (trailing mix) and ignores the derivative (inflection), so it systematically rejects the exact pre-discovery shape the framework exists to catch. The crucial, non-obvious finding: **the overfit lives in the ACCEPT/SIZING gates, not in the DISCOVERY engine** — IGNORED + sub-cap + balance-sheet signals would have *surfaced* almost every winner, but the strict end-market gate, the narrow-H10-first ordering, and the $1-2K Moonshot cap then refuse to *size* them. The live-session flags on MIR/Anritsu/Sumitomo/Wonik were applications of this same miscalibrated rule.

---

## 2. THE COHORT TABLE

Verdict columns: **Literal** = rules exactly as written (strict ">50% AI-DC end-market" as a hard PASS/FAIL gate; narrow NVDA-list H10 as the primary four-filter gate). **Intended** = the v2.0/v2.1 machinery read charitably (sector-relative end-market; H10-extended co-primary; discovery hierarchy; flag taxonomy). Classification is the worst-of / most-honest read.

| # | Ticker | Sector | ~Return | Pre-disc. low (date / cap) | AI-DC / chokepoint END-MARKET % at low | H8 cap | H8 end-mkt | H10 narrow @low | H10 ext @low | H5 | H11 | Literal verdict | Intended verdict | CLASS |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | **AXTI** | AI-infra/CPO | ~97x | Apr'25 / ~$50M | ~15-25% (telecom/consumer majority) | T1 PASS | **FAIL** | Y cat | N | IGN-ext | PASS | REJECT | REJECT | **OVERFIT-LEAK** |
| 2 | **AEHR** | AI-infra/WLBI | ~12x | Feb'25 / ~$280M | ~10-15% (SiC/EV majority) | T1 PASS | **FAIL** | **N @low** (HBM4E post-low) | N | IGN | PASS | REJECT | REJECT | **OVERFIT-LEAK** |
| 3 | **NVTS** | AI-infra/GaN | ~16x | Apr'25 / ~$200M | <15% (mobile/consumer) | T1 PASS | **FAIL** | **N @low** (NVDA = inflection) | N | IGN | FLAG | REJECT | REJECT | **OVERFIT-LEAK** |
| 4 | **POWL** | AI-infra/grid | ~38x | Jun'23 / ~$230M | ~15% (oil&gas ~52% / utility) | T1 PASS | **FAIL** | Y cat (weak) | N | IGN | PASS | REJECT | REJECT | **OVERFIT-LEAK** |
| 5 | **APLD** | AI-infra/hosting | ~14x | Apr'24 / ~$320M | <20% (BTC-mining majority) | T1 PASS | **FAIL** | **N @low** (NVDA Sep'24) | N | IGN | FLAG | REJECT | WATCH (pivot) | **OVERFIT-LEAK** (lit) / PARTIAL |
| 6 | **BE** | Power/SOFC | ~16x | mid'24 / ~$2-3B | ~30% (comm/industrial+Korea ~70%) | T3 PASS | **FAIL** | Y cat (Meta/MSFT) | N | IGN | PASS | REJECT | REJECT | **OVERFIT-LEAK** |
| 7 | **AAOI** | Optical/800G | ~15x | Aug'24 / ~$575M | ~sub-50% (CATV dilutes) | T2 PASS | **FAIL/UNK** | Y cat (AVGO) | N | IGN | PASS | REJECT | WATCH | **PARTIAL** |
| 8 | **CRDO** | Optical/AEC | ~24x | May'23 / ~$1.06B | ~88% (hyperscaler) | T2 PASS | **PASS** | Y cat | N | IGN | PASS | **ACCEPT** | **ACCEPT** | **CAUGHT** |
| 9 | **POET** | Optical/CPO | ~5-6x | / ~$300M | pre-revenue | T1 | N/A (pre-rev) | Y cat | N | IGN | FLAG | MOONSHOT | MOONSHOT | **CAUGHT-SMALL** |
| 10 | **LITE** | Optical/EML | ~10x | Aug'24 / ~$4.87B | <50% (telecom majority) | T3 PASS | **FAIL** | **N @low** (NVDA $2B Mar'26) | N | NEU/PART | PASS | REJECT | REJECT | **OVERFIT-LEAK** |
| 11 | **LASR** | Optical+DEF | ~7x | early'25 / ~$300M | ~AI-DC minority (~55% defense) | T1 PASS | **FAIL (AI-DC)** | N | **Y (H10-D)** | IGN | PASS | REJECT | ACCEPT/WATCH (DEF lens) | **PARTIAL** (lens-dependent) |
| 12 | **SNDK** | Memory/NAND | ~44x | Apr'25 / ~$4.1B | ~13% (mobile/client/consumer ~87%) | T3 PASS | **FAIL** | Y cat (NVDA HBM) | N | NEU | PASS | REJECT | REJECT | **OVERFIT-LEAK** |
| 13 | **NBIS** | AI-hosting | ~14x | Oct'24 / ~$3.3B | >50% (pure neocloud) | T3 PASS | **PASS** | N @low → Y on PIPE | N | IGN | PASS | **ACCEPT** | **ACCEPT** | **CAUGHT** |
| 14 | **IREN** | AI-hosting | ~7x | Jan'25 / ~$1.93B | ~2.3% (94.9% BTC-mining) | T2 PASS | **FAIL** | N @low (MSFT Sep'25) | N | PART | PASS | REJECT | WATCH | **PARTIAL** |
| 15 | **ABVX** | Biotech | ~22x | Aug'24 / ~$200-250M | pre-rev clinical | T1 | N/A | N | **N (no H10-P @low)** | IGN | PASS/FLAG | REJECT | REJECT | **OVERFIT-LEAK** (diff-pattern) |
| 16 | **CELC** | Biotech | ~12x | 2024 / ~$300M | pre-rev clinical | T1 | N/A | N | **Y (FDA BT Jul'22)** | NEU/PART | PASS | MOONSHOT | MOONSHOT | **CAUGHT-SMALL** |
| 17 | **RLMD** | Biotech | ~12x | Aug'25 / ~$40-60M | pre-rev clinical | T1 | N/A | N | **N (Type-B mtg, post-low)** | IGN-ext | **FLAG/RED** | REJECT | REJECT | leak (H10-P) + correct-strict (H11) |
| 18 | **OKLO** | Nuclear | ~7-9x | mid'24 / ~$1-1.5B | pre-revenue | T2 | N/A | N | weak/partial H10-N | IGN | FLAG | MOONSHOT | MOONSHOT | **CAUGHT-SMALL** |
| 19 | **NNE** | Nuclear | ~9-12x | mid'24 / ~$300M | pre-revenue | T1 | N/A | N | **N H10-N** (only H10-D SBIR) | IGN | FLAG | REJECT/MOON-borderline | MOON-borderline | **PARTIAL** |
| 20 | **SMR** | Nuclear | ~10-15x | mid'24 / ~$0.7-1B | pre-revenue | T2 | N/A | N | **Y vendor (NRC cert Feb'23)** | IGN-ext | FLAG | MOONSHOT | MOONSHOT | **CAUGHT-SMALL** |
| 21 | **LEU** | Nuclear | ~5x | mid'24 / ~$0.7-1B | ~0% AI-DC / ~100% nuclear-DOE | T2 PASS | **FAIL (lit)/PASS (sector)** | N | **Y vendor (DOE HALEU)** | IGN | PASS | REJECT | **ACCEPT** | **CAUGHT** (intended) / leak (literal) |
| 22 | **PL** | Defense/Space | ~13x | early'25 / ~$0.7-1B | ~0% AI-DC / >50% gov-defense | T2 PASS | **FAIL (lit)/PASS (sector)** | N | **Y (H10-D, NRO since'22)** | IGN-ext | FLAG/PASS | REJECT | **ACCEPT** | **CAUGHT** (intended) / leak (literal) |
| 23 | **RKLB** | Defense/Space | ~11x | Apr'24 $3.47 / ~$2.5B | ~0% AI-DC / gov-space majority | T3 PASS | **FAIL (lit)/PASS (sector)** | N | **Y (H10-D, SDA $515M Jan'24)** | IGN | FLAG/PASS | REJECT | **ACCEPT** | **CAUGHT** (intended) / leak (literal) |
| 24 | **MP** | Crit. minerals | ~5-6x | 2024 / ~$2-3B | ~0% (≈100% concentrate→China @low) | T3 PASS | **FAIL** (China-export, not US-strat) | N | **N @low** (DoD/Apple = Jul'25) | NEU | PASS | REJECT | REJECT (no anchor yet) | **CORRECT OUT-OF-SCOPE MISS** |
| 25 | **USAR** | Crit. minerals | ~6.5x | Mar'25 deSPAC / <$500M | pre-revenue | T1 | N/A | N | partial (H10-M DPA/LOIs) | NEU | FLAG | MOONSHOT/REJECT (narrow-first) | MOONSHOT | **CAUGHT-SMALL** |

**Tally (intended reading, denominator = 24, MP excluded as out-of-scope-at-low):**
- CAUGHT (ACCEPT-track): CRDO, NBIS, LEU, PL, RKLB = **5**
- CAUGHT-SMALL (Moonshot $1-2K): POET, CELC, OKLO, SMR, USAR = **5**
- PARTIAL (WATCH / lens-dependent / borderline): AAOI, APLD, LASR, IREN, NNE = **5**
- OVERFIT-LEAK (hard REJECT of an in-design winner by a rule): AXTI, AEHR, NVTS, POWL, BE, LITE, SNDK + ABVX, RLMD = **9**
- CORRECT OUT-OF-SCOPE MISS: MP = 1 (excluded from sensitivity denominator)

---

## 3. RANKED WINNER-KILLING RULES (frequency)

| Rank | Rule | Winners it rejects / downgrades at the low | Count |
|---|---|---|---|
| **1** | **H8(b) strict ">50% of revenue from the AI-DC end-market"** (hard PASS/FAIL gate, scored on trailing mix at the low) | AXTI, AEHR, NVTS, POWL, APLD, BE, LITE, SNDK, AAOI, LASR, IREN — plus LEU/PL/RKLB under the *literal-AI-DC* reading | **11 (intended) / 14 (literal)** |
| **2** | **Narrow-H10-first as the primary four-filter gate** (extended bellwether presented only as an addendum) | PL, RKLB, MP, USAR, LEU, NNE, SMR, OKLO, ABVX, CELC, RLMD — plus LITE/AEHR/NVTS/APLD where the NVDA fire post-dated the low | **~11-15** (overlaps #1) |
| **3** | **Moonshot $1-2K sizing cap** (pre-revenue → routed small even with a vendor-level bellwether) | POET, CELC, OKLO, SMR, USAR (+NNE) — caught but capped | **5-6** |
| **4** | **H10-P cannot fire before the binary readout** (biotech) | ABVX (unpartnered, designation only at readout), RLMD (Type-B meeting, post-low) | **2** |
| **5** | **Moonshot criterion #6 "insiders net selling = disqualify"** (latent; contradicts killed-H3) | would have rejected OKLO if its 10b5-1/post-rerate sells were not timed to the entry window | **1 (latent)** |
| — | **H11 going-concern (RED tier)** | RLMD (also EOSE/WOLF-pre historically) — load-bearing, NOT a leak | correct-strictness |

---

## 4. OVERFIT-LEAK vs CORRECT-STRICTNESS DIAGNOSIS

Cross-check against the 10 adversarial controls (AMAT, KLAC, MRVL, AMD, COHR, ACLS, AMKR, ARM, CRUS, WOLF-pre), all of which the framework correctly rejects (PATTERN_MATRIX §3). The test for an overfit leak: **does the rule independently catch any control that the other filters would miss, or does it ONLY catch winners?**

| Rule | Verdict | Reasoning + control cross-check |
|---|---|---|
| **H8(b) strict >50% AI-DC end-market** | **OVERFIT LEAK (miscalibrated threshold + snapshot)** | Rejects 11-14 winners. Cross-check: every control is *already* rejected by H8-CAP (AMAT/KLAC/MRVL/AMD/COHR/AMKR/ARM are mega-cap), H5-LOVED, or H11. The end-market test's only "unique" target is WOLF (>50% EV/auto) — but **WOLF-pre is also rejected by H11 going-concern**, so the end-market test catches *no control independently*. It catches winners only. The PRINCIPLE (don't buy a diluted parent where AI-DC is incidental — Anritsu/Sumitomo/Wonik) is correct; the DEFECT is (a) the >50%-of-**trailing-total** threshold and (b) the **snapshot at the low**, which together can't distinguish AXTI-inflecting from WOLF-incidental. |
| **H8(b) hard-coded to "AI-DC" (not sector-relative)** | **OVERFIT LEAK (un-generalized rule)** | H10 was given sector-conditional treatment in v2.0 (H10-D/N/M/P/G); H8(b)'s end-market string was NOT. LEU (0% AI-DC / ~100% nuclear), PL/RKLB (0% AI-DC / gov-majority) fail the literal reading. Specificity risk of generalizing to ">50% of the chokepoint SECTOR's anchor end-market": LOW — extended end-markets don't apply to the AI-infra mega-cap controls. |
| **Narrow-H10-first ordering** | **OVERFIT LEAK for extended lenses (presentation/ordering)** | Narrow fires 92% within AI-infra (fine) but 0-46% for defense/nuclear/minerals/biotech. A narrow-H10-first operator kills PL/RKLB/MP/USAR/LEU/NNE/SMR/biotech before reaching the extended lens. Latent, not active (the live MIR/SPAI sessions DID apply H10-N/H10-D) — but the rules-as-written would reject if followed literally. Promoting H10-extended to co-primary admits **no control** (extended bellwethers don't apply to AI-infra mega-caps). |
| **Moonshot $1-2K cap** | **MISCALIBRATED THRESHOLD** | Catches OKLO/SMR/USAR/CELC/POET but caps a 7-15x at $1-2K. SMR had a *vendor-level* NRC certification at the low; LEU-shape pre-revenue names had DOE backing — exactly the conviction signal that should UPGRADE size, yet the flat cap treats "pre-revenue" as a near-veto on sizing (the error the v2.1 Flag Taxonomy warns against: a magnitude-input misapplied as a veto). |
| **Moonshot criterion #6 (insider net-selling disqualifier)** | **INTERNAL CONTRADICTION (with killed-H3)** | H3 was KILLED because "insiders sell into rerates" is the MODAL behavior across the entire winner universe (38/39 in the live insider screen). Criterion #6 then uses net selling as a disqualifier. OKLO is the live trap: its "-$174.7M, 165 sells, 0 buys" was a 10b5-1 plan executed post-rerate near peak; at the actual mid-2024 low insiders were neutral. An analyst not timing the sells would wrongly reject OKLO. |
| **H11 going-concern (RED tier)** | **CORRECT STRICTNESS — do not touch** | Rejects RLMD (near-delisting/thin cash) and historically EOSE, WOLF-pre. This is the one filter that independently catches a control (WOLF-pre) and is load-bearing per PATTERN_MATRIX §3. Loosening it remains "the worst-EV decision in the framework." |
| **MP miss** | **CORRECT OUT-OF-SCOPE MISS — not a leak** | At the 2024 low MP sold ~100% concentrate to China with zero US-gov anchor; the DoD $400M preferred + Apple $500M (the H10-M/H10-G fires) post-dated the low by ~12 months. Documented as H13 geopolitical-different-pattern. Counterfactual: a MP-shaped name *with the anchor in place* WOULD now be caught via H10-M + H10-G — so the rule is forward-correct; it just couldn't catch this MP at this bottom. |
| **Biotech H10-P pre-readout gap** | **DIFFERENT-PATTERN class (accept the miss)** | ABVX (unpartnered Phase-3, designation/endpoint only AT the readout) and RLMD are structurally uncatchable by a leading-signal framework. Only pre-stamped-designation biotechs (CELC, FDA BT Jul'22) catch. Loosening H10-P to admit unpartnered names would admit noise (every clinical micro-cap). Recommend documenting biotech as out-of-scope binary-readout, not loosening the gate. |

---

## 5. THE THREE LIVE-SESSION TENSIONS RESOLVED

### Tension A — Strict H8 end-market vs AI-infra winners → **CONFIRMED OVERFIT LEAK.**
At their pre-discovery lows the AI-DC end-market was a MINORITY for essentially every AI-infra winner: **AXTI ~15-25% (telecom-dominated), AEHR ~10-15% (SiC/EV-dominated — the literal WOLF shape), NVTS <15% (mobile/consumer), POWL ~15% (oil&gas ~52%), BE ~30% (commercial/Korea ~70%), SNDK ~13% (NAND broad), LITE telecom-majority, AAOI CATV-diluted.** These are 10-97x winners. Only CRDO (~88% hyperscaler) and NBIS (pure neocloud) passed the >50% test at the low. **The test gates on the trailing level and ignores the inflection** — it cannot tell AXTI-at-low (AI-DC the fastest-growing slice, balance-sheet/bellwether pointing at it) from WOLF (AI-DC incidental, EV/auto structural and flat).

**Proposed reformulation (for governance to consider, not implemented):** replace the trailing ">50% of total revenue from the AI-DC end-market" with an **inflection-clause**:
> *"The chokepoint end-market must be the **fastest-growing** end-market AND satisfy ONE of: (i) >X% of **incremental/forward** (next-2-quarter or contracted) revenue, OR (ii) a **first-time chokepoint deferred-revenue / customer-deposit signal >$10M** (the v2.0 PRIMARY discovery layer). It need NOT be >50% of trailing total — but it MUST be inflecting toward dominance (this growth guardrail is what distinguishes AXTI-inflecting from WOLF-incidental)."*

This directly upgrades the live-session calls: it gives the operator a principled way to separate **MIR/Anritsu/Sumitomo "real product, diluted-and-flat end-market" (correctly held at WATCH)** from **AXTI-shape "diluted-but-inflecting end-market" (should ACCEPT)** — by testing whether the AI-DC slice is the fastest-growing with a balance-sheet signal, not whether it has already crossed 50% of trailing revenue.

### Tension B — Narrow-H10-first vs the extended bellwether → **PROMOTE H10-EXTENDED TO CO-PRIMARY.**
Narrow H10 fired for ~92% of the AI-infra cohort but **0% of the defense/nuclear/minerals/biotech cohort at their lows** (PL/RKLB/MP/USAR/LEU/NNE/SMR/ABVX/CELC/RLMD). PATTERN_MATRIX's 48%-vs-90% gap reproduces exactly. CLAUDE.md still presents the NVDA-narrow list as the primary four-filter gate with the Sector-Conditional Extension as a SEPARATE section below — so a literal narrow-first operator kills ~11 extended-lens winners before the extended lens is reached. The contradiction is between PATTERN_MATRIX (extended = primary, narrow = one anchor) and the four-filter section's ordering. **Recommendation:** rewrite the four-filter H10 definition so H10 IS the sector-conditional FAMILY from the top (narrow for the AI-infra lens; H10-D/N/M/P/G for the others), with the v2.0 discovery-hierarchy demotion (balance-sheet PRIMARY, H10 CONFIRMATION) stated inside the four-filter section rather than as an addendum. Specificity risk: NONE (the controls are AI-infra mega-caps unaffected by extended bellwethers).

### Tension C — Pre-revenue moonshot REJECT vs the nuclear/quantum cohort → **CAUGHT, but the $1-2K cap MATERIALLY UNDER-CAPTURES.**
Good news: OKLO, NNE, SMR, USAR, CELC, POET all route to MOONSHOT-caught (not REJECT) — the moonshot tier works as a catch mechanism. The problem is sizing. Nuclear-cohort opportunity cost, realized multiples × ($2K cap vs $5K Tier-1/2):
- OKLO ~7-9x: $2K→+$12-16K vs $5K→+$30-40K (**gap ~$18-24K**)
- NNE ~9-12x: $2K→+$16-22K vs $5K→+$40-55K (**gap ~$24-33K**)
- SMR ~10-15x: $2K→+$18-28K vs $5K→+$45-70K (**gap ~$27-42K**)
- **Aggregate nuclear opportunity cost ≈ $70-100K** on a ~$6K-vs-$15K capital base.

Answer to "is catching a 10x at $1-2K a WIN or a MISS?": **a partial win that forfeits the majority of the asymmetry.** SMR is the sharpest case — a **vendor-level** bellwether (NRC design certification, the explicit H10-N trigger) was live at the low, yet the flat cap sized it like a category-only moonshot. **Proposed reformulation:** add a **"Moonshot+" $3-5K tier** for pre-revenue names that clear ALL existing Moonshot gates AND have a **vendor-level / binding** bellwether (NRC milestone, DOE LPO, gov-equity H10-G, named-prime funded award, Big-Pharma binding partner) — keeping the 18-month hard expiry, the H11-FLAG gate, and no-averaging-down. Specificity risk: MODERATE (binary regulatory exposure) — mitigated by the vendor-level requirement + expiry. Also surfaced: (a) NNE exposes a **Moonshot H10 gap** — its only pre-low anointment was an H10-D defense SBIR, not the H10-N the Moonshot rule names, so cross-lens fires are undefined; (b) the **OKLO insider-selling trap** (Tension-C-adjacent) confirms Moonshot criterion #6 must be struck or restricted to "discretionary open-market selling AT the entry window."

---

## 6. TRUE SENSITIVITY RECOMPUTATION

CLAUDE.md claims **"12/12 sensitivity within design-intent universe (100%)"** — measured on the original 8-12 winners under the ORIGINAL rules. Recomputed across this 24-name in-design cohort under the CURRENT v2.1 rules:

| Reading | Strict (ACCEPT-track only) | Lenient (ACCEPT + WATCH + Moonshot-caught) |
|---|---|---|
| **A — rules as literally written** (>50% AI-DC end-market hard gate; narrow-H10 primary) | **2/24 ≈ 8%** (CRDO, NBIS) | **~8/24 ≈ 33%** (the 2 ACCEPT + Moonshots; H8-end-market fails get NO WATCH because the discovery hierarchy still "requires H8 to pass") |
| **B — rules as intended** (sector-relative end-market; H10-extended co-primary; discovery hierarchy; flag taxonomy) | **5/24 ≈ 21%** (CRDO, NBIS, LEU, PL, RKLB) | **15/24 ≈ 63%** |
| **C — with the §7 recommended H8 inflection-clause fix applied** | ~12-15/24 ≈ 50-62% | **~22/24 ≈ 92%** (only the 2 unpartnered-biotech binary-readouts remain hard misses) |

**Headline:** the claimed 100% does NOT hold under current v2.1 rules. Strict ACCEPT-track sensitivity is **8% literal / 21% intended** — an order of magnitude below the claim. The DISCOVERY engine is highly sensitive (IGNORED + sub-cap + balance-sheet signals would surface ~88% of the cohort); the **ACCEPT/SIZING gates are the overfit layer** — they find the winners and then decline to size them. Reading C shows the leak is *recoverable*: the single H8 inflection-clause fix restores lenient sensitivity to ~92% without touching specificity (H11/H8-cap/H5-LOVED still reject all 10 controls).

---

## 7. RECOMMENDED FRAMEWORK CHANGES (prioritized — DO NOT IMPLEMENT this session; for a governance session)

Each: current rule → evidence it's a leak → proposed reformulation → specificity risk (does it admit any of the 10 controls?).

1. **[HIGHEST] Reformulate H8(b) with an inflection clause.**
   - *Current:* ">50% of revenue must come from a single AI-infrastructure chokepoint end-market" (trailing, hard PASS/FAIL).
   - *Evidence:* rejects AXTI (97x), SNDK (44x), POWL (38x), NVTS (16x), BE (16x), AEHR (12x), LITE (10x) at their lows; all had AI-DC as the fastest-growing MINORITY.
   - *Proposed:* AI-DC/chokepoint-sector must be the **fastest-growing** end-market AND (>X% of incremental/forward revenue OR a first-time chokepoint deferred-rev/customer-deposit signal >$10M), even if <50% of trailing total; retain a "must be inflecting toward dominance" guardrail.
   - *Specificity risk:* LOW-MODERATE. The growth guardrail preserves the WOLF/Anritsu rejection; WOLF-pre is independently caught by H11 regardless. Must keep the guardrail or it admits diversified-incidental names.

2. **[HIGH] Generalize H8(b) end-market from "AI-DC" to the chokepoint SECTOR (pairs with #1).**
   - *Current:* hard-codes "AI-data-center end-market."
   - *Evidence:* LEU (0% AI-DC / ~100% nuclear-DOE), PL/RKLB (0% AI-DC / gov-majority) fail the literal reading though H10-extended already brought their sectors in-scope.
   - *Proposed:* ">50% (or inflecting majority per #1) of the **chokepoint sector's anchor end-market**" (nuclear/DOE, defense-gov, critical-minerals-strategic, etc.).
   - *Specificity risk:* LOW (extended end-markets don't apply to AI-infra mega-cap controls).

3. **[HIGH] Promote H10-extended to co-primary; fold the discovery-hierarchy demotion into the four-filter section.**
   - *Current:* narrow NVDA-list is the four-filter primary gate; Sector-Conditional Extension is a separate addendum below.
   - *Evidence:* narrow fires 0% of the defense/nuclear/minerals/biotech cohort at their lows; a narrow-first operator kills ~11 extended-lens winners. Contradicts PATTERN_MATRIX (extended 90% / narrow 48%).
   - *Proposed:* define H10 as the sector-conditional family from the top; state balance-sheet signal PRIMARY, H10 CONFIRMATION, inside the four-filter section.
   - *Specificity risk:* NONE.

4. **[MEDIUM] Add a "Moonshot+" $3-5K tier for pre-revenue + vendor-level/binding bellwether.**
   - *Current:* flat $1-2K for all pre-revenue Moonshots.
   - *Evidence:* SMR (vendor-level NRC cert at low), OKLO, USAR capped at $1-2K on 7-15x outcomes ≈ $70-100K aggregate forfeited.
   - *Proposed:* $1-2K for category-only pre-revenue; $3-5K when a vendor-level/binding bellwether (NRC milestone / DOE LPO / H10-G gov equity / named-prime funded award / Big-Pharma binding partner) is present at entry. Keep 18-mo expiry + H11-FLAG gate + no-averaging-down.
   - *Specificity risk:* MODERATE (binary regulatory risk) — mitigated by vendor-level requirement + expiry.

5. **[MEDIUM] Resolve the Moonshot criterion #6 / killed-H3 contradiction.**
   - *Current:* "insiders net selling = disqualify" Moonshot.
   - *Evidence:* contradicts the KILLED H3 ("insiders sell into rerates" is modal/meaningless); would have wrongly rejected OKLO (10b5-1/post-rerate sells).
   - *Proposed:* restrict #6 to "discretionary open-market insider selling AT the entry window (exclude 10b5-1 and post-rerate sales)," or strike it.
   - *Specificity risk:* LOW.

6. **[LOW] Document biotech as a different-pattern binary-readout class (or add a biotech-specific entry gate); accept the unpartnered-Phase-3 miss.**
   - *Evidence:* ABVX (22x) and RLMD uncatchable pre-readout because H10-P only fires for pre-stamped designations/partners (CELC). Loosening H10-P admits clinical-micro-cap noise.
   - *Proposed:* either accept the unpartnered-Phase-3 blind spot explicitly, or gate biotech on (specialist-fund 13F + FDA designation OR disciplined balance sheet + IGNORED). Do NOT loosen H10-P.
   - *Specificity risk:* HIGH if H10-P is loosened — recommend ACCEPT-the-miss / document.

7. **[LOW/HOUSEKEEPING] Correct the CLAUDE.md "100% sensitivity" claim.**
   - *Evidence:* this audit — strict ACCEPT-track sensitivity is 8-21%, not 100%.
   - *Proposed:* split the framework-performance line into DISCOVERY-sensitivity (~88%) vs ACCEPT-track-sensitivity (8-21% pre-fix; ~50-62% with the #1 fix), so the metric stops overstating the gating layer.

---

## APPENDIX — adversarial-discipline notes

- **No grading on a curve:** AXTI is reported as a flat REJECT under the current rules; not rationalized as operator override.
- **No hindsight:** every filter scored on pre-discovery-low information; where a bellwether/partner/contract post-dated the low (AEHR HBM4E, NVTS/LITE NVDA deals, MP DoD/Apple, RLMD Type-B, OKLO Meta) it was scored as NOT firing at the low.
- **Conflicts surfaced, not averaged:** the PATTERN_MATRIX 48%/90% H10 finding vs the CLAUDE.md narrow-first ordering (Tension B); the killed-H3 vs Moonshot-#6 insider rule; the literal-AI-DC vs sector-relative H8 readings — all named explicitly with both sides.
- **FAIL-LOUD UNKNOWNs:** AAOI's exact AI-DC % at the Aug-2024 low (the 59.5% DC figure is the Nov-2024 inflection, not the low) marked UNKNOWN → classified PARTIAL, not assumed pass. LITE's datacom-vs-telecom split within Cloud&Networking is directional. NNE's cross-lens H10 (does an H10-D SBIR satisfy a Moonshot built on H10-N?) flagged as a rule gap.
- **The most valuable outcome was the loud one:** the current rules would reject ≥7 of the framework's own flagship AI-infra winners at their pre-discovery lows. That is the finding this audit exists to surface.
