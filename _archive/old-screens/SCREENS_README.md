# SCREENS_README.md — Archos

## What lives here

The `screens/` directory holds **discovery screens** — reusable Code
prompts that surface sub-$5B candidates the existing weekly bellwether
sweep, monthly sentiment refresh, and Aschenbrenner 13F pull would miss.

Each screen targets a **different information gap** in the four-filter
framework (H10 / H8 / H5 / H11). They are complements, not substitutes.
A candidate that surfaces on a screen is **not** a thesis — it is a
ticket into the existing 6-check evaluation pipeline.

> Flow: screen output → quick H8/H10 sanity check → CANDIDATE_UNIVERSE.md
> WATCH entry → full 6-check (DISCOVERY_PROMPT.md) → if ACCEPT → full
> DD checklist (DUE_DILIGENCE_CHECKLIST.md). **Nothing here bypasses
> the two-stage SCREEN + VET process.**

## The six screens

| # | Screen | Information gap it closes | Status |
|---|---|---|---|
| 1 | **revenue-inflection** | Catches first-time YoY revenue >40% growth — the inflection point where something fundamental changed. The bellwether sweep finds *partnerships*; this finds *the financial confirmation* a partnership already exists. | **ACTIVE** |
| 2 | **supplier-mapping** | Reads sub-$5B 10-Ks for direct mentions of NVDA / AVGO / TSMC / MSFT / META / AMD as customers. Catches the hidden supply chain that bellwethers haven't publicly named. The AXTI test case. | **ACTIVE** |
| 3 | **insider-buying-weakness** | Detects Form 4 open-market BUYS during -20%+ drawdowns. Killed as an entry signal in Phase 1 (H3), but resurrected here as a **contrarian add-on filter** — insiders buying *on weakness* (not into rallies) is a different signal than the H3 "insiders buy ahead of inflection" hypothesis that failed. | **ACTIVE** (v1 live 2026-05-24; EdgarTools `insider_activity` per-name pulls as primary path — OpenInsider unreachable from environment) |
| 4 | **master-screen** | Universal multi-lens sweep — runs 5 parallel sub-screens (material-agreement, revenue-inflection, insider-buying, gov-contracts, keyword-emergence) across the ALL-sector sub-$500M universe + 5 sector lenses (AI Infra, Defense/Space, Nuclear, Critical Minerals, GLP-1/Pharma). Closes the gap between AI-infra-only screens and the parallel-lens opportunity surface that bellwethers and Aschenbrenner 13F do not cover. | **ACTIVE** (v1 live 2026-05-24; produced 1 TIER 1 [CTM], 4 TIER 2, 8 TIER 3, ~25 REJECT additions in first run) |
| 5 | **patent-cluster** | USPTO patent assignee + class concentration. Sub-$5B companies suddenly filing in NVDA-adjacent CPC classes (G06N, H01L, H04B/H04L) signal capability without a press release. Catches IP-stage chokepoint pure-plays before commercialization. | **PLANNED** (needs USPTO API integration or scraping; Phase 2 build) |
| 6 | **conference-presenter** | Presenter lists at OCP Global Summit, OFC, SC, GTC, Hot Chips, ISSCC, ECOC. Sub-$5B companies on the speaking docket at chokepoint-relevant conferences = qualified by the conference committee that they have substantive technology. | **PLANNED** (needs conference website scraping; cadence-dependent on conference calendar) |

## How they complement each other

Each screen attacks a different stage of the **information surfacing
chain** for a chokepoint pure-play:

| Stage | What the company has done | Best screen | Lead time vs. inflection |
|---|---|---|---|
| Capability | Filed patents in a chokepoint area | **patent-cluster** | -18 to -36 months |
| Visibility | Presented at a chokepoint conference | **conference-presenter** | -12 to -18 months |
| Relationship | Named a bellwether customer in 10-K | **supplier-mapping** | -6 to -12 months |
| Confirmation | First-time YoY revenue inflection | **revenue-inflection** | -0 to -6 months |
| Insider conviction | Insiders buying on temporary weakness | **insider-buying-weakness** | -0 to -3 months (confirmation, not lead) |
| Bellwether announcement | Direct NVDA/AVGO partnership 8-K | *bellwether sweep (existing)* | -0 to -1 month (often IS the inflection) |
| Specialist 13F | Aschenbrenner-class fund initiates | *13F pull (existing)* | -3 to -5 months (when present, ~25%) |

The bellwether sweep is the **right-most** signal: cleanest, latest,
most actionable. These five screens push the surfacing window earlier
and catch names the bellwether sweep would never name.

## Candidate flow (mandatory)

```
SCREEN HIT
    ↓
Quick H8/H10 sanity check (5 min)
  - market cap < $5B? (live data, not XBRL)
  - chokepoint maps to CHOKEPOINT_TAXONOMY.md?
  - already in CANDIDATE_UNIVERSE.md or any rejected log?
    ↓
If yes: add to CANDIDATE_UNIVERSE.md as WATCH with
        note "surfaced via [screen name], pending full 6-check"
    ↓
Schedule full 6-check (DISCOVERY_PROMPT.md) on next cadence
    ↓
If ACCEPT from 6-check → DUE_DILIGENCE_CHECKLIST.md (mandatory)
    ↓
Section 6 of DD = /last30days social signal sweep
    ↓
If DD CLEAR → paper-track candidate
```

**Nothing skips a stage.** SHAZ is the calibration case: it passed all
four filters at Stage 1 and was 6/6 RED at Stage 2. The screens here
shorten the candidate-discovery tail; they do not shorten the vetting.

## Recommended cadence

| Screen | Cadence | Trigger / timing |
|---|---|---|
| **revenue-inflection** | **Monthly** | Run on the 15th of each month — 10-Q filing deadline is typically the 5th-10th business day after quarter-end (~45 days post-quarter for accelerated filers, ~45 days for non-accelerated). Monthly run catches the trailing quarter's filings. Sooner if a sub-$5B name with a known chokepoint association is expected to file. |
| **supplier-mapping** | **Quarterly** | Run mid-March (after calendar-year 10-Ks file) and mid-June (after fiscal-year-ending-March 10-Ks file). 10-Ks are once-per-year per filer, so quarterly cadence cycles through different fiscal-year-end cohorts. |
| **insider-buying-weakness** | **Monthly** | Run on the 1st of each month — Form 4 must file within 2 business days of transaction, so a monthly sweep catches the prior month's window cleanly. |
| **master-screen** | **Monthly** | Run on the 24th of each month — captures the trailing 30 days of 8-K filings + trailing 60 days of 10-Q filings + trailing 90 days of insider activity. Sub-screens execute as parallel subagents (~28 min wall-clock each, ~30 min total). |
| **patent-cluster** | **Quarterly** | USPTO publication lag is 18 months for non-provisional applications; weekly run adds no signal over quarterly. |
| **conference-presenter** | **Quarterly** | Anchor to major chokepoint conference calendar (OCP late Sept-Oct, OFC March, SC mid-November, GTC March, Hot Chips August, ISSCC February, ECOC September). Run 30 days before each conference (presenter list public ~60 days out) and 30 days after (review the announcements / demos shown). |

## Status legend

- **ACTIVE** — SCREEN_PROMPT.md is written and ready to run. Tooling
  available in current MCP stack.
- **PLANNED** — Concept defined, directory exists, SCREEN_PROMPT.md
  not yet written because additional tooling (USPTO API, conference
  scraping pipeline, deeper Form 4 filtering) is required first.

## Output convention

Every screen run writes to its own `runs/{YYYY-MM-DD}-run.md` file.
Format is consistent across screens:

1. **Header**: screen name, run date, query parameters, time spent
2. **Methodology note**: which option (A/B/C) was used and why
3. **Results table**: standardized columns per screen
4. **Top 3-5 narrative**: most interesting names with thesis fragments
5. **Refinement notes**: what to change in the next run

## Cross-references

- **CANDIDATE_UNIVERSE.md** — WATCH entries from screens land here
- **CHOKEPOINT_TAXONOMY.md** — every screen hit must map to a chokepoint
- **DISCOVERY_PROMPT.md** — the 6-check evaluation that screens feed into
- **DUE_DILIGENCE_CHECKLIST.md** — the post-ACCEPT vetting (SHAZ calibration)
- **INSIGHTS.md** — append lessons from each screen run (signal/noise,
  query effectiveness, blind spots discovered)
- **state.md** — append each run as a timeline entry

## Adding a new screen

To add a sixth screen later:

1. Create `screens/{screen-name}/` and `screens/{screen-name}/runs/`
2. Write `SCREEN_PROMPT.md` with: OBJECTIVE, METHOD (numbered steps),
   OUTPUT (table format), and any TEST CASES (like AXTI for supplier-mapping)
3. Add the screen to the table at the top of this README
4. Specify the cadence and the trigger
5. Document what information gap it closes

The bar for a new screen: **it must close an information gap not
covered by the existing screens or the bellwether sweep.** Adding
more screens that find the same names is anti-productive.
