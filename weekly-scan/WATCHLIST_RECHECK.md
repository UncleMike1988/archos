# WEEKLY WATCHLIST RECHECK — status check, not a new hunt

Paste into a fresh Code session. Output: weekly-scan/runs/{date}-recheck.md

## STARTUP — read in full, follow exactly
1. /Users/michaelturner/Desktop/Claude Builds/_master_docs/WORKING_PHILOSOPHY.md (confirm last line)
2. /Users/michaelturner/Desktop/Claude Builds/archos/CLAUDE.md
3. /Users/michaelturner/Desktop/Claude Builds/archos/WATCHLIST.md (the list to recheck)
Also available if needed: current DDs at the TOP LEVEL of due-diligence/ ONLY (ignore the
due-diligence/due-diligence-old/ subfolder — those are archived old-system DDs, not current).
Do NOT read any _archive file. Do NOT search for new candidates — this is a STATUS check, not a hunt.

## THE TASK
For EVERY name in WATCHLIST.md, check what changed in the last week and decide: did the trigger fire,
did the thesis strengthen, weaken, or break, or no change. Keep each name tight (a few minutes); spend
more only where something real moved.

For each name check:
- Trigger status: has the documented "trigger to act" fired / partially fired / not fired? (verify via
  fresh filings + news + price).
- Material news/filings in the last ~7-14 days (contracts, earnings, leadership, dilution, going-concern, insider trades).
- Price action since added (and since last recheck): up a lot = thesis confirming but check if the window/
  valuation is getting rich; down a lot = thesis breaking OR a better entry — which?
- Sentiment drift: is it going from ignored toward crowded/LOVED (asymmetry eroding)?
- Thesis integrity: still intact / strengthened / degraded / broken.

Decision per name: ACT-NOW (trigger fired + thesis intact → flag for a position decision or full DD) /
HOLD (no change) / DROP (thesis broken or facts changed — note why) / WINDOW-CLOSING (ran far enough that
asymmetry is fading).

## OUTPUT
Write weekly-scan/runs/{date}-recheck.md: a one-line summary (how many act-now / hold / drop), then a tight
per-name status (trigger, what moved, decision, one-line reason). Then UPDATE WATCHLIST.md: refresh each
"Last note," move DROPPED names to the "Recently retired" section with the reason, and surface ACT-NOW names
at the top of the chat summary so the operator sees them first. This is the time-series engine — the value
is the DELTA week over week. Decisions are the operator's; flag, don't act.

## SESSION END
git add -A; git commit -m "Weekly watchlist recheck {date}"; git push origin main; verify clean + synced.
