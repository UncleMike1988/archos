# SPAI — /last30days Social Signal Sweep (DD Section 6)
# Safe Pro Group Inc. (NASDAQ: SPAI) — Defense AI / Drone Threat Detection
# Date: 2026-05-29 (data window 2026-04-28 → 2026-05-28)
# Session type: AUTORESEARCH / DD — research only, no code changes
# Framework: Archos Equities v2.1 | Bucket 3 (nanocap AI-adjacent) | Lens: Defense AI (H10-D)

## DECISIVE QUESTION

> Is SPAI's retail/investor interest ORGANIC or MANUFACTURED?

**ANSWER: MANUFACTURED.** The visible SPAI signal is a paid-syndication + cashtag-bot
construct wrapped around real-but-tiny underlying events. There is **no credible
independent bull case** — no named buy-side PM, no substantive independent DD, no
organic Reddit discussion on the major US investing subs, zero independent YouTube
analysis, no Substack. The signal that exists is (a) IBN / InvestorBrandNetwork paid
defense-news syndication and (b) automated cashtag/PR-amplifier X accounts reposting
the company's own press releases.

This is the SHAZ failure-mode *axis* (paid promotion + no organic bull case) — but at
**lower intensity** and **without SHAZ's fabricated claims / fake counterparty / DeFi
lender / self-dealing**. See the calibration note at the end ("syndicated paid-IR vs
direct paid-promotion").

---

## METHOD

Run via the `/last30days` engine (Reddit public JSON + ScrapeCreators backup, X via
browser-cookie auth, YouTube via yt-dlp, TikTok/Instagram via ScrapeCreators, HN,
Polymarket, GitHub) + targeted WebSearch supplements. Plan: 3 sub-queries
(primary SPAI; paid-promotion infrastructure; defense-drone narrative). Engine wall
clock 134s. Raw artifact: `~/Documents/Last30Days/safe-pro-group-spai-stock-paid-promotion-organic-raw-v3.md`.

Coverage caveat (FAIL-LOUD): r/pennystocks, r/wallstreetbets, r/stocks, r/Defense_tech,
r/drones returned HTTP 403 on the public-JSON path (Reddit rate-limiting), so the
engine's "Reddit results" fell through to false-match subs (r/IndianStockMarket,
r/JobPH, r/CasualRO — none about SPAI). Manual WebSearch cross-check for organic
Reddit DD on SPAI returned **nothing** on the major US investing subs. The absence is
the signal: a defense-AI name being syndicated this hard has produced **zero** organic
retail DD threads.

---

## 1. PAID PROMOTION INFRASTRUCTURE — CONFIRMED (IBN / InvestorBrandNetwork family)

The decisive §6.5 finding. SPAI is being pushed through the **InvestorBrandNetwork
(IBN) "Dynamic Brand Portfolio" (75+ brands)** — the same paid-IR ecosystem class the
DD checklist flags (§1.6 / §6.5). IBN brands observed pushing SPAI:

| Brand | Type | Evidence |
|---|---|---|
| **DefenseWireNews** | IBN brand (defense-news-styled) | "Featured in DefenseWireNews Editorial on AI-Enabled Edge…"; syndicated to Globe and Mail / Barchart. Carries: *"We have not reviewed, approved, or endorsed the content, and may receive compensation for placement."* |
| **DefenseNewsBreaks** | IBN brand | "Safe Pro Group… Positioned Amid Growing Pentagon Focus on Domestic Drone and AI Defense Technologies" — byline *Investor Brand Network*, syndicated to StreetInsider + Globe and Mail |
| **NetworkNewsWire (NNW)** | IBN brand | "Appoints COO, Is Also Awarded Government Support Order…" (networknewswire) |
| **MissionIR** | IBN-affiliated | "Experiences Rapid, High Margin Revenue Increase and Launches a New Growth Team" |

Pattern: the **same positioning piece** ("SPAI positioned amid Pentagon drone push")
is re-syndicated across Globe and Mail / Barchart / StreetInsider / MarketScreener
under different IBN brand mastheads — i.e., coordinated paid placement engineered to
look like independent editorial coverage. This is exactly the prompt's hypothesis (Q2).

**Note (balance):** SPAI's **official IR of record is Solebury Strategic
Communications** (Ankit Hira) — a *mainstream* IR firm (named on the Q1 2026 earnings
release), NOT a RedChip-style pump promoter. So SPAI runs BOTH a mainstream IR channel
AND a paid retail-awareness syndication campaign (IBN family). No RedChip / PCG
Advisory / MZ Group / Irth / Litchfield Hills relationship was found.

---

## 2. X / FINTWIT — bot-dominated, ~zero organic credible DD

14 X posts in window, 517 aggregate likes. The cashtag space is dominated by
**automated PR-amplifier / cashtag-aggregator accounts**, not independent analysts:

- **@NewsRamp_Alerts** — news-bot, multiple SPAI posts ("demonstrate AI threat
  detection on Black Widow drones for U.S. Army"; "Safe Pro + Lantronix complete AI
  threat detection integration") — 1-likes-class engagement.
- **@StocksDaily** — cashtag aggregator: "$SPAI received an additional U.S. Government
  subcontract modification… follow-on to the $1M award."
- **@listingtrack** — "Daily Gainers & Losers" bot: "SPAI rose 14.01% to $4.72 after
  announcing…" (3 likes).
- **@marketwirenews** — explicit PR syndication ("News & Disclaimer" + t.co link).
- **@scbower / @Stockspy1** — boilerplate: @Stockspy1's "speculative long $SPAI -
  Drone related" post (5 likes) is a verbatim copy of the company's product
  description, not analysis.

The only genuinely *human retail* voice with substance: **@lithologuy** (5/28, 1 like)
— "I've held Safe Pro Group for a while now. Luckily they are in a partnership with
UMAC, so benefiting from today's crazy upswing!" — confirms (a) a small organic holder
base exists and (b) the 5/28 move was **sympathy off Unusual Machines (UMAC)**, not
SPAI-specific news. **No named buy-side PM, no track-record analyst, no disclosed-
position substantive thread.** §6.1 organic bull case = effectively ABSENT.

---

## 3. REDDIT / YOUTUBE / TIKTOK / SUBSTACK / HN — organic discovery essentially nil

- **Reddit:** Zero genuine SPAI DD on r/pennystocks, r/wallstreetbets, r/stocks,
  r/Defense_tech, r/drones (403s + WebSearch cross-check both empty). For a defense-AI
  nano up triple-digits over the year, the absence of any organic Reddit DD is itself
  diagnostic of a promotion-driven (not community-driven) signal. §6.2 = zero.
- **YouTube:** 0 videos. No independent analyst/breakdown content.
- **Substack:** none found.
- **Hacker News:** 0.
- **TikTok:** 4 low-signal videos (~131K combined views, creators kaebae56 /
  stockaustinhilton / nicoleisbannedagain) — generic penny-stock/cashtag content, not
  substantive DD; treat as noise.
- **Instagram:** 0 reels.
- **Polymarket / GitHub:** false matches (Counter-Strike esports markets; openai/codex)
  — irrelevant, discarded.

---

## 4. INSIDER ACTIVITY (cross-checked vs Form 4s — FAIL-LOUD correction)

The aggregate "0 buys / 3 sells / net -76,184 sh" headline (company_brief)
**overstates bearishness.** Form 4 detail (180-day) shows the "sells" are **NOT
discretionary**:
- **Code F (tax withholding on RSU/RSA vesting):** Erdberg 47,942 (3/6) + 120,000 +
  120,000 (12/11); Carlise 19,242 (3/6).
- **Code G (gifts, to Erdberg Foundation):** Erdberg 9,000 (3/6) + 24,000 (12/23).
- **Code A (grant):** Erdberg **1,000,000-share** award (12/11/25).

→ **ZERO discretionary open-market sales AND zero open-market buys = NEUTRAL insider
posture.** Not a bearish dump (per the INSIGHTS at-vesting-withholding ≠ sell rule),
but also no conviction buy. The 1M-share CEO grant + heavy FY25 stock-based comp
(~$6.9M, 47% of opex) is a **dilution/enrichment flag**, not a fraud flag.

---

## 5. THE +20% MOVE ON 2026-05-28 — SYMPATHY, NOT SPAI NEWS

Confirmed: a sector-wide drone/defense rally on the Trump-admin/Pentagon drone-funding
report. Same-day moves: **UMAC +25%, RCAT +13%, AeroVironment +10%, Kratos +10%,
Ondas +9%, AIRO +7%.** The report named **Unusual Machines, Performance Drone Works,
Neros Technologies** as participants in Pentagon/OSC funding discussions — **NOT Safe
Pro.** SPAI rode the wave because Ondas + Unusual Machines are its strategic investors
+ collaboration partners, and the move was amplified by IBN's "SPAI Positioned Amid
Growing Pentagon Focus" syndication. This is the canonical "PR positioning around
others' news" pattern.

---

## 6. AISP (Airship AI) COMPARISON — the higher-quality analog

| Axis | **SPAI** (this name) | **AISP** (Airship AI, the analog) |
|---|---|---|
| Cap (TIER 1 NANO) | ~$112M (post 5/28 pop; ~$91M pre) | ~$79-86M |
| Gov contracts | ONE $1M **subcontract** to an **unnamed prime**, marketed around Army exercises | **Direct, NAMED-agency (DHS), FUNDED, firm-fixed-price**, recurring ($2.1M + $1.9M + $2.1M FFP awards) |
| Insider posture | NEUTRAL (no discretionary buy/sell) | **Buying** |
| Social/promotion | IBN paid syndication + cashtag bots; **zero organic DD** | Passed DD with FLAGS; cleaner contract base |
| Pipeline anchor | Sympathy positioning around UMAC/Ondas Pentagon narrative | OB3 / DHS procurement, direct |

**Conclusion:** AISP is materially higher quality on the axes that decide a defense-AI
nano — **contract directness (named DHS FFP vs unnamed-prime subcontract), recurrence,
and insider conviction (buying vs neutral).** SPAI is the *weaker* analog: it is roughly
what AISP would look like if AISP's contract base were a single subcontract, its
insiders weren't buying, and it were paying for defense-news syndication.

---

## §6 SCORE: RED (paid promotion + no organic bull case)

- 6.1 Organic bull case: **ABSENT** (no named buy-side / independent analyst).
- 6.2 Reddit engagement: **ZERO** genuine on major subs.
- 6.3 Independent verification of bear claims: n/a (no published short report exists).
- 6.4 Management response quality: n/a (no short report to rebut).
- 6.5 Paid promotion: **PRESENT** — IBN family (DefenseWireNews / DefenseNewsBreaks /
  NetworkNewsWire / MissionIR) + cashtag/PR bots. **RED.**
- 6.6 Suspicious timing: PR cadence clusters around the Pentagon-drone narrative +
  sympathy moves; serial S-3/424B3 shelf takedowns through late 2025 = capital-raise
  context for retail-awareness spend. Flag, not dispositive.

**§6 = RED**, but explicitly the **"syndicated paid-IR around a real (non-fraudulent)
company"** variant — NOT a SHAZ 6/6 fabricated-claims construct.

---

## CALIBRATION: "syndicated paid-IR" vs "direct paid-promotion" (NEW)

SHAZ (the calibration baseline) = **direct paid-promotion (RedChip) + FABRICATED
claims (retracted "NVIDIA shareholder") + FAKE/insolvent counterparty (ESDS) + DeFi
lender (USD.AI) + management self-dealing** → 6/6 RED, hard delete.

SPAI = **syndicated paid-IR (IBN defense-news-styled brands, "may receive
compensation") + cashtag-bot amplification, wrapping REAL-but-tiny events** ($1M
subcontract actually delivered/paid; real Army demos; real strategic investors Ondas +
Unusual Machines), on a **clean balance sheet** (H11 strong, $14.8M cash), with **no
fabricated claims, no fake/insolvent counterparty, no DeFi lender, no self-dealing,
mainstream IR (Solebury) also present, NEUTRAL insiders.**

**Discriminator:** Are the PROMOTED CLAIMS fabricated / the counterparty fake-or-
insolvent (→ SHAZ hard-delete), or REAL-but-inflated-in-framing around a non-fraudulent
company (→ §6-RED that drives a REJECT-for-ACCEPT-track, not a fraud delete)? SPAI is
the latter. Paid syndication is a promotional-infrastructure RED that disqualifies the
ACCEPT-track / Moonshot status (DD Moonshot criterion #5 requires CLEAN promotion) —
but it is NOT, by itself, the SHAZ fraud pattern.

---

## STATS

- X: 14 posts │ 517 likes │ 46 rt │ 32 re — voices @listingtrack, @NewsRamp_Alerts (bots)
- Reddit: 0 genuine SPAI threads on target subs (403 + WebSearch cross-check empty)
- YouTube: 0 │ TikTok: 4 (~131K views, low-signal) │ Instagram: 0 │ HN: 0 │ Substack: 0
- Web/PR: dominated by IBN-family syndication (DefenseWireNews / DefenseNewsBreaks /
  NetworkNewsWire / MissionIR) re-published on Globe and Mail / Barchart / StreetInsider /
  MarketScreener
- Insider (Form 4, 180d): 0 discretionary buys, 0 discretionary sells, 1M-share CEO grant
- 5/28 +20%: sympathy on UMAC +25% / RCAT +13% / Pentagon-drone report (named others, not SPAI)
