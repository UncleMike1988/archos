# ARCHOS WATCH RE-EVAL PROMPT
# Run after the weekly scan completes, or midweek when a trigger event fires.
# Output: archos/weekly-scan/runs/{date}-reeval.md

## MANDATORY READS
1. _master_docs/WORKING_PHILOSOPHY.md
2. archos/CLAUDE.md
3. archos/CANDIDATE_UNIVERSE.md
4. archos/DUE_DILIGENCE_CHECKLIST.md
5. archos/INSIGHTS.md

Confirm LAST LINE of WORKING_PHILOSOPHY.md before proceeding.

## CRITICAL EXECUTION RULE
# This is NOT a screening session. Do NOT search for new candidates.
# This session re-evaluates EVERY name currently on WATCH in
# CANDIDATE_UNIVERSE.md. The goal is to determine which names
# should be PROMOTED (trigger fired → queue for DD or position),
# DEMOTED (thesis broken → move to REJECT), or HELD (no change).

## TASK

Read CANDIDATE_UNIVERSE.md in full. Extract every ticker that
appears in any WATCH section (including WATCH, MASTER-SCREEN WATCH,
WEEKLY-SCAN WATCH, TIER 2 DD COMPLETED, and BTC-PIVOT WATCH).

For EACH ticker on the list, run this 5-point check:

### CHECK 1 — Trigger status
Each WATCH entry has a specific re-eval trigger documented in
CANDIDATE_UNIVERSE.md. Check whether that trigger has fired:
- For filing-based triggers (8-K, 10-Q, annual report): search
  EdgarTools for new filings since the last scan date.
- For price-based triggers (pullback to $X): check current price
  via web search.
- For event-based triggers (IPO, listing change, contract
  announcement): web search for news.

Status: FIRED / NOT FIRED / PARTIALLY FIRED

### CHECK 2 — New material filings (last 14 days)
Search EdgarTools for any 8-K, 10-Q, 10-K, 6-K, or Form 4
filed in the last 14 days for this ticker. Read the filing
snippet. Flag anything material:
- New contracts or material agreements (Item 1.01)
- Earnings releases (Item 2.02)
- Leadership changes (Item 5.02)
- Going concern or restatement (Item 4.02)
- Insider buying or selling (Form 4)

### CHECK 3 — Price action (last 14 days)
Web search for current stock price. Compare to the price at
the time the name was added to WATCH (documented in
CANDIDATE_UNIVERSE.md or the scan run that surfaced it).
Flag if:
- Up >20% since added (thesis may be playing out — is the
  asymmetric window closing?)
- Down >20% since added (thesis may be breaking — or creating
  a better entry)
- Hit a new 52-week high or low

### CHECK 4 — Sentiment shift
Quick web search: "[ticker] analyst upgrade" OR "[ticker]
analyst downgrade" OR "[ticker] ETF inclusion" in last 14 days.
Has sentiment shifted from IGNORED toward LOVED? If the stock
is getting picked up by FinTwit, analysts, or ETFs, the H5
IGNORED edge is eroding.

### CHECK 5 — Thesis integrity
Based on checks 1-4, is the original thesis for watching this
name still intact?
- If trigger fired + thesis intact → PROMOTE to DD queue
- If trigger fired + thesis broken → DEMOTE to REJECT
- If no trigger + thesis intact → HOLD on WATCH
- If no trigger + thesis degraded (bad filing, going concern,
  insider dumping, competitive loss) → DEMOTE to REJECT
- If price ran >50% since added with no trigger event →
  reassess whether the asymmetric window has closed

## OUTPUT

Write to: archos/weekly-scan/runs/{date}-reeval.md

Format:

# ARCHOS WATCH RE-EVAL — {date}

## Summary
- Total WATCH names evaluated: N
- PROMOTE to DD queue: N (list tickers)
- DEMOTE to REJECT: N (list tickers)
- HOLD unchanged: N
- ACTIONABLE (DD completed, position decision pending): N

## Per-name status

### {TICKER} — {PROMOTE / DEMOTE / HOLD / ACTIONABLE}
| Check | Status |
|---|---|
| 1. Trigger | FIRED / NOT FIRED / PARTIALLY |
| 2. New filings | [summary] |
| 3. Price action | [current vs added, % change] |
| 4. Sentiment shift | [IGNORED / NEUTRAL / PARTIAL / LOVED] |
| 5. Thesis integrity | [INTACT / DEGRADED / BROKEN] |

**Recommendation:** [one sentence]

[Repeat for every WATCH name]

## Actions required
- Names to promote: [list with next step — DD prompt or position decision]
- Names to demote: [list with reason — move to REJECT log]
- Names approaching thesis expiry: [list with deadline — if no trigger by X date, demote]
- DD-completed names awaiting position decision: [list — human decision needed]

---

Update CANDIDATE_UNIVERSE.md:
- Move any DEMOTED names to REJECT log with reason and date
- Update trigger status for any PARTIALLY FIRED names
- Add "last re-eval: {date}" note to each WATCH entry

Update state.md:
- Add timeline entry for re-eval run

## EXECUTION GUIDANCE

Time budget: 60-90 minutes total. Spend 3-5 minutes per WATCH
name on average. For names where all 5 checks come back clean
with no change, a 1-minute "HOLD — no change" entry is sufficient.
Spend more time on names where a trigger partially fired or where
price action is significant.

Use EdgarTools for filing checks. Use web search for price and
sentiment. Do NOT deep-dive into any single name — this is a
status check, not a DD session. If a name needs deeper investigation,
flag it for a separate DD session.

For names where DD has already been completed (IREN, CLSK, AMPG,
AISP, WYFI, CTM, etc.), the re-eval focuses on whether anything
has changed since the DD was written — not re-running the DD.

---

## SESSION END

No git push.

Files written:
- archos/weekly-scan/runs/{date}-reeval.md

Files updated:
- archos/CANDIDATE_UNIVERSE.md (demotions, trigger updates, re-eval dates)
- archos/state.md (timeline entry)

Output summary to chat:
- Total evaluated / promoted / demoted / held
- Any names where the trigger fired (these need immediate attention)
- Any names where the thesis is degrading
- DD-completed names still awaiting position decisions
- Confirmation all files updated

STOP after summary.
