# SCORING_SYSTEM.md — Archos
# Framework version: v3.1 (created 2026-05-28 as v3.0; refined 2026-05-29 — v3.1: CAUTION split into paid-manufactured vs organic-overheated; inflection signal #4 gains a declining-slice −4 penalty rung + multi-segment chokepoint-identification hazard note — both from PENG-dd-2026-05-29 §7)
# Read this at session start. This file defines the scorecard the operator reads.

## What this file is

Archos's job is **detection + pattern-matching + ranking + trap-detection**. It
does NOT size positions, recommend entries/exits, or manage risk — the operator
(Michael) owns all of that. This file defines the output Archos produces for every
live candidate: a **scored, ranked dossier** that names a candidate's strengths,
weaknesses, and traps, and places it against the reverse-engineered signature of
prior parabolic winners.

Three things are produced per candidate, and they are **NEVER blended into one
number** (surface conflicts, don't average — a 90 Pattern Strength with a Kill is
a "90 with a kill-switch," not a 50):

1. **Pattern Strength (0-100)** — how closely the candidate matches the
   pre-breakout signature of prior winners. Hit-rate-weighted; every point traces
   to a measured signal from `research/pattern-discovery/PATTERN_MATRIX_UNIVERSAL.md`.
2. **Trap Risk (Clear / Caution / Kill)** — the two-pronged trap check. A separate
   flag, never folded into Pattern Strength. **Kill overrides everything.**
3. **Bet Shape (Bull / Base / Bear)** — the three-scenario return shape that
   conveys asymmetry. Plus **closest historical analog**, **Δ since last run**, and
   **rank vs the live watchlist**.

**No company has a perfect score pre-breakout.** The winners had clusters of
signals *with* weaknesses, not flawless scorecards. A sub-$500M clean-on-every-axis
company doesn't exist; if it did it wouldn't be sub-$500M and ignored. The flaws
ARE the entry point. A Pattern Strength of 100 is structurally unreachable in
practice (it requires IGNORED-extreme + sub-$100M + bellwether-fired +
fastest-growing-end-market-with-balance-sheet-confirm + customer-deposit +
revenue-inflection + triple-cluster, all at once — the perfect pre-breakout winner
that does not exist). Stop chasing a perfect score; **rank, don't binary-classify.**

---

## SCORE 1 — PATTERN STRENGTH (0-100)

### Design rule (reproducibility)

Every point traces to a signal with a **measured historical hit rate** from
PATTERN_MATRIX_UNIVERSAL §1 (universe N=61, 500%+ winners across all sectors). Max
points per signal are set in proportion to that hit rate, then grouped into
**Heavy / Medium / Bonus** bands. The three *graded* signals (sentiment, cap,
end-market inflection) use a **dose-response sub-scale** because PATTERN_MATRIX
documents dose-response for them explicitly. **A score you can't explain back to a
hit-rate is the system lying — tie every point to the data.**

The 100-point base sums only if *every* validated signal fires at full strength —
which essentially never happens. Real winners scored ~55-85 with named weaknesses.

### The weighting table

| # | Signal | PM hit rate | Band | Max pts |
|---|---|---|---|---|
| 1 | **Extended bellwether fire** (sector-conditional H10 family — see CLAUDE.md) | **90%** univ | HEAVY | **20** |
| 2 | **IGNORED / NEUTRAL sentiment** (H5, dose-response) | **87%** univ | HEAVY | **20** |
| 3 | **Sub-$2B cap geometry** (H8, dose-response; smaller = more) | **80%** univ | HEAVY | **16** |
| 4 | **Chokepoint end-market INFLECTION** (fastest-growing slice + balance-sheet confirm — the AXTI-vs-MIR discriminator) | composite (rev-inflection 67% + deposit 36/70%) | HEAVY | **16** (−4 floor) |
| 5 | **Customer-deposit / deferred-revenue spike** (sector-conditional) | **36%** univ / **70%** def-nuke | MEDIUM | **8** |
| 6 | **Revenue inflection >40% YoY first-time** (where eligible) | **67%** eligible | MEDIUM | **8** |
| 7 | **Signal-cluster match** (de-SPAC / squeeze / spinoff-REORG / gov-anchor; multi-cluster scores highest) | 30-36% each; triple-firers = top winners | BONUS | **12** |
| | **TOTAL** | | | **100** |

*Signal #4 can score a **−4 declining-slice penalty** (a multi-segment chokepoint whose anchor
end-market is SHRINKING YoY — PENG AI/HPC −42%); the −4 is a penalty FLOOR, not part of the
additive 100-point all-fire ceiling.*

**Overlays — NOT base points (they raise magnitude expectation, i.e. the Bull
case, not Pattern Strength):**
- **Short interest >15% rising** (PM 30%, AMPLIFIER) — converts a +200% setup into
  a +1000% setup via squeeze dynamics; documented in the Bull case, not scored.
- **Foreign filer (6-K/20-F), low US coverage** (PM 15%, AMPLIFIER) — discovery
  friction → bigger surprise on the catalyst; noted, not scored.

### Per-signal scoring rubric (how to assign partial credit)

**1. Extended bellwether fire — max 20.** Sector-conditional H10 family (CLAUDE.md
four-filter). `0` = no bellwether at all; `10` = category-level fire (bellwether
named the chokepoint *category*); `20` = vendor-level fire (bellwether named the
company or invested / a binding sector-anchor award: NVDA stake, DOE LPO, NRC
milestone, named-prime funded award, Big-Pharma binding partner). *Discovery note:
a name surfaces on a balance-sheet signal even with NO bellwether (CHANGE 4 — the
bellwether is the CONFIRMATION layer, not the gate); when the bellwether later
fires, this is the single biggest Δ-driver in the score.*

**2. IGNORED / NEUTRAL sentiment — max 20, dose-response (H5).** `LOVED` 0 (and see
Trap/▪ note: LOVED-EXTREME parabolic-retail is a Kill-adjacent magnitude veto, not
just 0) · `PARTIAL` 6 · `PARTIAL-RECOVERING` 8 (post-catalyst >25% retrace, thesis
intact) · `NEUTRAL` 12 · `IGNORED` 16 · `IGNORED-extreme` 20. Dose-response per
PATTERN_MATRIX (IGNORED-extreme winners 1,500-9,600%; PARTIAL 50-265%).

**3. Sub-$2B cap geometry — max 16, dose-response (H8).** `>$5B` 0 · `$2-5B` 6 ·
`$500M-2B` 10 · `sub-$500M` 14 · `sub-$100M` 16. Smaller float + smaller dollar
base = larger mechanical re-rate (Cluster 5 dollar-stock geometry). *This is a
MAGNITUDE descriptor, not a sizing instruction — the operator sizes.*

**4. Chokepoint end-market INFLECTION — max 16, −4 floor (the discriminator).** This is the
audit's #1 fix (CHANGE 3): score the *derivative*, not the *level*. `−4` (penalty) = the
chokepoint slice is **DECLINING YoY** (PENG AI/HPC −42%) — strictly worse than flat; this is an
active Bear-case driver, not a neutral zero. Floor the signal at −4 (do not let it drag the
whole score below what the other signals support — it is a penalty rung, not an unbounded
negative). · `0` = flat/incidental, NOT the fastest-growing slice (the WOLF / Anritsu / Sumitomo
/ MIR "diluted-and-flat" shape — hold) · `6` = chokepoint slice growing but not yet the
fastest-growing end-market · `10` = chokepoint end-market is the **fastest-growing** slice (even
if a minority of trailing total) · `16` = fastest-growing **AND** a first-time chokepoint
deferred-revenue / customer-deposit signal >$10M OR >X% of incremental/forward (next-2-quarter
or contracted) revenue. **This is what separated AXTI-at-low (diluted-but-inflecting → catch)
from MIR-today (diluted-and-flat → hold).** It need NOT be >50% of trailing total.

*HAZARD — fix the chokepoint segment BEFORE scoring #4.* In a multi-segment company, identify
which reported segment IS the chokepoint thesis and score #4 on THAT segment's trajectory — not
the fastest-growing segment by default. PENG is the calibration case: the chokepoint thesis is
the AI/HPC (Advanced Computing) segment (−42% YoY → −4), NOT the Integrated-Memory segment
(+63%, memory-cycle-driven, not the AI-cluster thesis). Scoring the wrong segment swings #4 by
14 points (−4 ↔ +10) and inverts the verdict. State explicitly in the dossier which segment was
scored and why.

**5. Customer-deposit / deferred-revenue spike — max 8, sector-conditional.** `0` =
none · `5` = present (AI-infra / general, PM 36%) · `8` = present in
defense/nuclear/space (PM 70% — gov-contract prepayments are the cleanest
balance-sheet tell). >50% QoQ increase OR first-time absolute >$10M. *May co-fire
with signal #4 (it is one of the tells that satisfies the heavy inflection read);
score both, but do not invent a third instance of the same fact.*

**6. Revenue inflection >40% YoY first-time — max 8.** `0` = no inflection or
sustained-growth (already >40% in prior year = CRWV/NBIS-shape, not first-time
APLD-shape) · `8` = first-time >40% YoY with <20% prior year. `N/A` for pre-revenue
/ clinical-stage (excluded from the achievable max for that candidate — see
normalization note).

**7. Signal-cluster match — max 12, BONUS.** Match against the named clusters in
`SIGNAL_CLUSTERS.md`: Cluster 1 (de-SPAC reanimation), 2 (squeeze-amplified), 3
(spinoff/REORG), 4 (gov-contract anchor), 5 (broken-IPO/post-failure pivot). `0` =
no cluster · `+4` = one cluster · `+8` = two clusters · `+12` = three+ clusters
(triple-firer). PATTERN_MATRIX/SIGNAL_CLUSTERS finding: **triple-firers (RKLB,
OKLO, QBTS, USAR) were the highest-conviction winners.** *Clusters 6 (commodity
beta — excluded), 7 (legacy-industrial pivot — accepted blind spot), and 8
(meme/squeeze) score ZERO here; Cluster 8 routes to Trap Risk = Kill.*

### Normalization for pre-revenue / clinical-stage candidates

When signal #6 (and sometimes #4's revenue tell) is structurally `N/A` (pre-revenue
moonshot, clinical-stage biotech), compute Pattern Strength as
`points_earned / max_achievable_for_this_candidate × 100`, where the denominator
excludes the N/A signals. State the exclusion in the dossier (e.g., "scored out of
84; rev-inflection N/A pre-revenue"). Do not silently penalize a pre-revenue name
for a test it cannot take — that was the old Moonshot-cap error.

### What Pattern Strength is NOT

- It is **not a buy signal, a probability, or a price target.** It is a similarity
  score to prior winners' pre-breakout shape.
- It is **not** the discovery gate. Discovery (what surfaces a name) is the
  balance-sheet-primary hierarchy in CLAUDE.md; Pattern Strength scores a name once
  surfaced. A name can surface (deferred-rev signal) and score low (no bellwether
  yet, NEUTRAL not IGNORED) — that's a real, useful state.
- It does **not** decide position size. The operator sizes off Bet Shape + Trap
  Risk + Pattern Strength together.

---

## SCORE 2 — TRAP RISK (Clear / Caution / Kill)

This is the **sole hard-reject layer** in v3.0 and the crown-jewel capability. In
the sub-$500M world the base rate of paid-promotion fluff is shockingly high;
telling a real company from a manufactured one is the single most valuable thing
Archos does. Run via the DD checklist + the mandatory `/last30days` social sweep
(DD §6). Two prongs — **the GAP between them is the signal.**

### Prong A — AUTHENTICITY (is the company real underneath?)

- Clean-enough balance sheet — survives without serial toxic raises; no
  death-spiral ELOC / variable-conversion notes. **H11 going-concern-to-zero is the
  kill line** (load-bearing, audit-confirmed; do NOT loosen).
- Real product with **named, verifiable, paying customers** (not LOI/MOU theater).
- Credible operator-founders — not narrative-hopping serial promoters. Run the DD
  §1.7 network-failure check (COMSovereign / Akoustis pattern).
- Genuine advisory board / executive pedigree — real domain authority (the
  USSOCOM / CBP / ex-Anduril-type cluster is REAL signal; verify it's not decorative).
- Auditor is not a PCAOB-deficient single-office shop (DD §1.8).

### Prong B — PROMOTION (is the bull case organic or manufactured?)

Run the `/last30days` sweep. Tells of a manufactured narrative:
- Syndication networks: IBN / InvestorBrandNetwork, DefenseWireNews,
  NetworkNewsWire, MissionIR, RedChip, PCG, MZ Group, Litchfield Hills.
- "May receive compensation for placement" disclosures; news-bot cashtag
  amplification; PR reposted as if it were analysis; announcements timed to
  lockups/raises.
- Question: is there **organic credible capital** independently making the case
  (named buy-side, substantive independent DD), or does the ENTIRE bull case trace
  back to paid infrastructure?

### The verdict logic (the gap is the signal)

- **KILL (hard reject):** manufactured promotion **AND** hollow substance (SPAI,
  PPSI, SHAZ class). Goes to the REJECT log with the evidence. Pattern Strength is
  irrelevant — **a Kill overrides any score** and removes the name from the ranked
  field.
- **CAUTION — PAID-MANUFACTURED:** paid/syndicated promotion infrastructure (IBN /
  RedChip / MZ Group / Litchfield Hills / "compensation for placement" / news-bot
  amplification) wrapped around real-but-thin substance (SPAI: real Army demo + $1M
  subcontract under the IBN froth). This is a PROMOTION-INTEGRITY flag — the closer the
  substance is to hollow, the closer it trends to Kill. Value only the verifiable
  substance; treat the paid narrative as adversarial noise; name the gap.
- **CAUTION — ORGANIC-OVERHEATED:** promotion is ORGANIC (no paid infrastructure — Prong B
  on the paid axis reads CLEAR), but the loud organic narrative's specific claims are
  contradicted by the filings and/or the entry is a chased sympathy/momentum spike at a
  rich price (PENG: organic FinTwit + "same AI clusters as Dell" while the AI segment is
  −42% + ~2x consensus PT on a Dell-sympathy pop). This is a VALUATION/TIMING flag, NOT a
  promotion-integrity flag — a real company that can become a GOOD entry on a pullback.
  Most of the warning should express through LOW Pattern Strength + an unfavorable Bet
  Shape, not through Trap Risk. Name the gap between the narrative and the filings.

  *Both are CAUTION (not Kill, not Clear) and both stay on the ranked field. The subtype tells
  the operator WHICH kind of caution: integrity (is the promotion bought?) vs valuation/timing
  (is a real company being chased too hard?). If a name is BOTH paid-manufactured AND hollow, it
  is a Kill, not a Caution.*
- **CLEAR:** real substance with organic-or-no promotion. This is a **POSITIVE
  signal** — "real AND ignored" is the core winner profile. A Clear on a
  high-Pattern-Strength name *strengthens* the bull case; trap-detection here
  CONFIRMS, it doesn't just veto.

### Other hard rejects that route to KILL (traps, not risk-sizing)

These are preserved from prior framework and are NOT graded weaknesses:
- **Counterparty insolvency / contract cancellation** (DD §2 RED) — SHAZ ESDS.
- **Fraud / self-dealing / restatement** (DD §1 RED) — SHAZ.
- **Meme/squeeze structural anomaly (SIGNAL_CLUSTERS Cluster 8):** float <20% +
  borrow >50% + zero bellwether + zero gov-contract + minimal revenue (RGC, SHAZ).
- **H11 going-concern-to-zero** (EOSE, WOLF-pre) — audit-confirmed correct
  strictness.
- **LOVED-EXTREME** — parabolic, retail-driven, at/above the cap fundamentals
  justify. This is a magnitude veto (the upside is gone), recorded as a Kill-adjacent
  call; it removes the name from the ACCEPT-track ranked field even though the
  company itself may be clean.

**Everything ELSE that used to hard-reject is now a graded weakness in Pattern
Strength, not a veto** (already-ran/near-high = H5 PARTIAL points; dilution absent
going-concern; thin coverage; one soft quarter; DD §5 valuation-RED — AEHR is the
calibration case). Net insider selling is **modal** (killed-H3) and is at most a
minor graded weakness, never a veto.

---

## BET SHAPE — Bull / Base / Bear

For each candidate, the three-scenario return shape. Two names can both score 80
Pattern Strength with totally different Bull/Bear spreads — and THAT asymmetry is
what the operator sizes on.

- **Bear:** what breaks the thesis, and the downside if it does (the trap that would
  fire, the H11 line, the end-market that stays flat).
- **Base:** the partial-recovery / consensus-target case (analyst PT, partial
  pattern completion).
- **Bull:** the full pattern-completion (10x-class) case — what it looks like if the
  candidate becomes the next AXTI/SNDK/POWL. Apply SI / foreign-filer amplifiers
  here.

---

## CLOSEST HISTORICAL ANALOG

Which prior winner(s) does this most resemble **pre-breakout**, and on which
signals. Draw from PATTERN_MATRIX_UNIVERSAL / graduated pure-plays. Example: "AEHR
pre-breakout — low-IV compounder, bellwether-adjacent, IGNORED, WLBI chokepoint."
The analog grounds the Bet Shape and tells the operator which historical tape to
study.

---

## Δ SINCE LAST RUN

Pattern Strength is **recomputed every rescan** because inputs are event-driven. The
delta is its own signal — surface it.

- NVDA names the company as a vendor → bellwether signal #1 flips category→vendor →
  **score jumps**.
- First deferred-revenue spike in a 10-Q → signals #4/#5 fire → **score jumps**.
- Sentiment moves IGNORED → PARTIAL → signal #2 drops → **score DROPS** (asymmetry
  eroding — a falling score is as useful as a rising one; the window is closing).
- Promotion pattern emerges in the `/last30days` sweep → Trap Risk can flip
  Clear → Caution → Kill.

Write one delta line per rescan: `Δ since last run: <what moved the score and why>`.

---

## RANKING (mandatory output)

Every dossier entry ends with its rank versus the rest of the live watchlist by
Pattern Strength. **Kills are excluded from the ranked field** and parked in the
REJECT log with their evidence. The whole watchlist sorts by Pattern Strength so the
operator sees, at a glance, what's best. "They can't all be maybes" — the ranking is
mandatory, not optional. Ties break by: (1) Bull/Bear asymmetry width, (2)
multi-cluster firing, (3) freshness of the bellwether fire.

---

## CANONICAL DOSSIER ENTRY FORMAT

Use this exact shape per candidate (in CANDIDATE_UNIVERSE.md and DD outputs):

> **TICKER** — Pattern Strength **NN** | Trap Risk: **Clear / Caution (paid-manufactured | organic-overheated) / Kill** | Rank: **k of N**
> Closest analog: <winner> pre-breakout (<why>)
> Bear: <thesis-break, downside>. Base: <partial/consensus>. Bull: <full completion>.
> Firing: <signals on, with hit-rate weights, e.g. "bellwether vendor-level +20, IGNORED +16, sub-$500M +14, end-market fastest-growing+deposit +16, gov-anchor cluster +4">.
> Missing/weak: <signals off or flagged, e.g. "no revenue-inflection yet (pre-rev, N/A); NEUTRAL not IGNORED">.
> Trap check: Authenticity <…> / Promotion <…> / Gap <…>.
> Δ since last run: <what moved the score>.

### Worked illustration (format only — not a live call)

> **EXMPL** — Pattern Strength **65** | Trap Risk: **Clear** | Rank: **2 of 9**
> Closest analog: AXTI pre-breakout (sub-cap substrate pure-play, AI-DC the
> fastest-growing minority slice, IGNORED).
> Bear: chokepoint end-market stays a flat minority and the deferred-rev tick was
> one-off → re-rates to nothing, ~-40% to cash floor (H11 clean, no zero risk).
> Base: catalyst converts to 2 quarters of >40% segment growth → consensus PT,
> ~2-3x. Bull: vendor-level bellwether fire + squeeze (SI 22% rising) → full
> AXTI-class completion, 10x+.
> Firing: IGNORED +16, sub-$500M +14, end-market fastest-growing + first-time
> deferred-rev >$10M +16, category bellwether +10, customer-deposit tell +5,
> broken-IPO cluster +4 (= 65); +SI-amplifier (Bull only, not scored).
> Missing/weak: no vendor-level bellwether yet (the key upgrade Δ to watch);
> revenue-inflection not yet first-time (+8 available); no second cluster.
> Trap check: Authenticity CLEAR (named paying customer, Big-4-adjacent auditor,
> clean balance sheet) / Promotion CLEAR (no IBN/RedChip footprint; two independent
> buy-side writeups) / Gap none — real and ignored.
> Δ since last run: +11 (first deferred-rev >$10M in the new 10-Q moved end-market
> inflection +10→+16 and fired the customer-deposit tell 0→+5).

---

## RE-SCORING ON RESCAN

See DUE_DILIGENCE_CHECKLIST.md §7 (WATCH Re-eval → Re-scoring protocol). On each
rescan: recompute Pattern Strength from current inputs, re-run the two-pronged Trap
check if any new filing/social signal warrants, update Bull/Base/Bear if a
catalyst/earnings/PT moved, refresh the ranking, write the Δ line.

---

*Created 2026-05-28. Implements the v3.0 detection-and-ranking refactor (Sounding
Board decision 2026-05-28), authorized by research/FRAMEWORK_OVERFIT_AUDIT.md. The
discovery engine (IGNORED + sub-cap + balance-sheet-primary + signal clusters) is
unchanged (~88% discovery sensitivity); v3.0 replaces the overfit ACCEPT/SIZING
gates with this graded scoring layer, restoring effective sensitivity to ~92% (audit
Reading C) without touching specificity (H11 / meme-squeeze / fraud / counterparty
traps still reject all 10 adversarial controls).*

*v3.1 (2026-05-29) — minor refinement from the first live v3.0 scorecard (PENG-dd-2026-05-29
§7): CAUTION split into PAID-MANUFACTURED (promotion-integrity) vs ORGANIC-OVERHEATED
(valuation/timing) subtypes; inflection signal #4 gains a −4 declining-slice penalty rung
(a shrinking chokepoint segment is worse than flat) + a multi-segment "fix the chokepoint
segment first" hazard note. Load-bearing walls untouched; specificity unchanged.*
