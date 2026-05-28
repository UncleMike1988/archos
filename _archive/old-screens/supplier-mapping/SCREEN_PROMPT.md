# SCREEN_PROMPT.md — Supplier Mapping Screen (v2)

## Version history

- **v1 (2026-05-21)** — one-degree only. Searched sub-$5B 10-Ks for
  bellwether name-drops. Surfaced FN (NVDA 27.6%) and OKLO (Meta
  prepayment) but **FAILED the AXTI retroactive test** because AXTI
  sells to Lumentum/Coherent/EMCORE (one degree from us = optics
  vendors; two degrees from us = NVIDIA). The highest-alpha names
  are TWO degrees from the bellwether — v1 missed all of them.
- **v2 (2026-05-24)** — adds two-degree chain hop. Searches mid-chain
  companies' 10-Ks for THEIR suppliers, then reverse-searches sub-$5B
  10-Ks for mid-chain customer mentions. AXTI retroactive test is
  mandatory exit criterion.

## OBJECTIVE

Find sub-$5B companies that supply components to AI infrastructure
bellwethers (NVDA / AVGO / TSMC / MSFT / META / AMD) — either **one
degree** (direct supplier, names bellwether in 10-K) or **two degrees**
(supplies a mid-chain company that supplies a bellwether).

The two-degree case is the higher-alpha discovery vector. The pattern:

```
NVIDIA (bellwether)
    ↑
    │  buys 800G transceivers from
    │
Lumentum / Coherent / Fabrinet  (mid-chain, $5-30B mkt cap, already rerated)
    ↑
    │  buys InP substrates from
    │
AXTI / [hidden sub-$5B suppliers]  (two-degree, $200M-$5B, pre-rerate)
```

The bellwether sweep finds the announcement. The v1 screen found the
mid-chain. **v2 finds the hidden two-degree layer behind the mid-chain.**

## METHOD

### Step 1 — Direct (one-degree) search (unchanged from v1)

Use `search_filings_full_text` to scan 10-K filings from the last 12
months for sub-$5B companies that name a bellwether as a customer:

```
form_type: 10-K
date_range: last 365 days

queries (run separately, dedup later):
  "NVIDIA" AND ("customer" OR "revenue" OR "sales")
  "Broadcom" AND ("customer" OR "revenue" OR "sales")
  "TSMC" OR "Taiwan Semiconductor" AND ("customer" OR "revenue" OR "sales")
  "Microsoft" AND ("customer" OR "revenue" OR "sales")
  "Meta Platforms" AND ("customer" OR "revenue" OR "sales")
  ("AMD" OR "Advanced Micro Devices") AND ("customer" OR "revenue" OR "sales")
```

Note: boolean AND with phrase quotes is broken in EdgarTools (see
INSIGHTS.md). Use single-phrase queries and triage manually.

### Step 2 — Two-degree search (NEW)

**Mid-chain companies (priority order — run the top 5 first):**

| # | Ticker | Company | Chokepoint | Why this mid-chain? |
|---|---|---|---|---|
| 1 | **COHR** | Coherent | CPO / photonics | Same chokepoint as AXTI; should name InP substrate supplier in 10-K |
| 2 | **LITE** | Lumentum | Photonics / lasers | NVDA $2B investment Mar 2026; should name laser/substrate suppliers |
| 3 | **FN** | Fabrinet | Optical packaging | NVDA 27.6%, CSCO 18.2% (FY2025); contract manufacturer with deep supplier list |
| 4 | **AAOI** | Applied Optoelectronics | 800G transceivers | Phase 3 winner; names MSFT + META as customers; should name component suppliers |
| 5 | **AMKR** | Amkor | Advanced packaging | OSAT for everyone; should name substrate/leadframe/wire-bond suppliers |

**Extended mid-chain (if time allows):**

| # | Ticker | Company | Chokepoint |
|---|---|---|---|
| 6 | **CRDO** | Credo | AECs, SerDes |
| 7 | **MU** | Micron | Memory / HBM |
| 8 | **AMAT** | Applied Materials | Fab equipment |
| 9 | **ONTO** | Onto Innovation | Fab inspection |
| 10 | **BE** | Bloom Energy | On-site DC power |
| 11 | **POWL** | Powell Industries | Switchgear |
| 12 | **SK Hynix** | (foreign filer; press releases) | HBM |
| 13 | **Samsung** | (foreign filer; press releases) | HBM |
| 14 | ASE Group | (foreign filer 20-F) | Advanced packaging |
| 15 | II-VI (now COHR) | (merged with Coherent) | Compound semis |

**For EACH mid-chain company, run two passes:**

#### Pass A — Forward (read mid-chain's 10-K)

Search the mid-chain company's most recent 10-K for supplier/vendor
language naming specific companies:

- `business_overview` section: "we source", "our suppliers include",
  "we purchase from", "we rely on"
- `risk_factors` section: "single-source supplier", "concentration of
  supply", "qualified vendor"
- `mdna` section: cost-of-goods discussion may name specific input
  suppliers
- XBRL notes: `note:ConcentrationRiskDisclosureTextBlock` may list
  supplier concentration if disclosed

Capture any sub-$5B US-listed supplier the mid-chain names.

#### Pass B — Reverse (search sub-$5B 10-Ks for mid-chain customer name)

Run `search_filings_full_text` on:

```
form_type: 10-K
date_range: last 365 days

per mid-chain (in priority order):
  "Coherent" AND ("customer" OR "revenue" OR "% of")
  "Lumentum" AND ("customer" OR "revenue" OR "% of")
  "Fabrinet" AND ("customer" OR "revenue" OR "% of")
  "Applied Optoelectronics" AND ("customer" OR "revenue" OR "% of")
  "Amkor" AND ("customer" OR "revenue" OR "% of")
```

This catches the AXTI pattern: a sub-$5B 10-K naming a mid-chain
company as a >10% customer. Document the chain explicitly:

> NVIDIA → Coherent (direct customer, FN/COHR 10-K confirms) → [ticker]
> (supplies Coherent, disclosed in [ticker]'s 10-K)

### Step 3 — Verify market cap (live)

For each hit (one-degree or two-degree), verify market cap < $5B using
live data (Massive Market Data MCP or web search). EdgarTools XBRL
market cap is stale — AXTI calibration ($273M shown when real was
$4.5B; see INSIGHTS.md).

### Step 4 — Read the filing context (mandatory disambiguation)

For each filing hit, read the actual passage that contains the
mid-chain or bellwether name. Classify same as v1:

| Classification | Pattern | Keep? |
|---|---|---|
| **Direct customer (named)** | "Coherent represented X% of revenue" | YES |
| **Direct customer (anonymized)** | "one large customer" + context | MAYBE |
| **Material customer (named)** | "Coherent is a material customer" | YES |
| **Partnership / agreement** | "we have a multi-year agreement with Coherent" | YES |
| **Reference / industry context** | "we compete with companies that supply Coherent" | NO |
| **Historical (lost the customer)** | "we previously supplied Coherent" | NO |

### Step 5 — Quantify the chain

For each KEEP candidate, capture:

- **Direct customer**: which mid-chain company buys from them
- **Direct customer % of revenue** (if disclosed)
- **What they supply** (component / material / service)
- **Mid-chain → bellwether linkage** (which bellwether ultimately
  pulls through demand)
- **Documented chain in standard format**:
  > Bellwether → Mid-chain (% of mid-chain revenue or "direct customer
  > status verified") → Sub-$5B supplier (% of sub-$5B revenue)

### Step 6 — Map to chokepoint

Map what-they-supply to a chokepoint in `CHOKEPOINT_TAXONOMY.md`. The
two-degree hits often map to the SAME chokepoint as the mid-chain
(AXTI / Lumentum / Coherent all on #1 CPO / #8 optical interconnect).

If chokepoint match: flag for full 6-check.
If no map but technology is AI-infra-relevant: note for taxonomy
refresh discussion.
If no AI-infra connection: pass.

### Step 7 — Exclude (mandatory rejections)

Filter out:
- **Already-known names** — anything in CANDIDATE_UNIVERSE.md or
  Phase 1/2/3 winner universe or Phase 2 control universe
- **Sector-pivot blind-spot names** — bitcoin-miner-pivot or shells
  (HIVE, BITF, CLSK, RIOT, KEEL, EVTV, AlphaTON, Bitzero, Axe Compute,
  Digi Power X, Alpha Compute Corp, K Wave Media)
- **Incidental mentions** — "we compete with vendors that also serve
  Coherent" / "companies like Lumentum dominate"
- **Reseller / distributor** — Arrow, Avnet, etc.

## EXECUTION NOTES

### Why 10-K not 10-Q

Same logic as v1 — 10-Ks contain the Item 1 Business narrative and
the Item 7 MD&A customer-concentration disclosures. 10-Qs reference
the 10-K rather than re-stating.

### Why the mid-chain priority order

COHR, LITE, FN, AAOI, AMKR are the **photonics + packaging spine** of
the NVDA AI rack. AXTI sits two degrees behind them. The same logic
applies to AMKR (advanced packaging) — substrate vendors like Kulicke
& Soffa, Tongfu Microelectronics, JCET (foreign), or compound-semi
specialty firms sit two degrees behind. Memory + power + equipment are
lower priority because the existing one-degree disclosures (MU/AMAT/BE)
are large companies whose suppliers are already mega-cap.

### Foreign filers (extended)

20-F filers (Hua Hong, Lattice's Asian peers, JCET, ASE, Sakura
Internet) are NOT caught by 10-K queries. v2 adds an optional 20-F
pass for the top 3 mid-chain companies if their named suppliers are
foreign-listed.

## OUTPUT

Write the run report to:
`/Users/michaelturner/Desktop/Claude Builds/archos/screens/supplier-mapping/runs/{YYYY-MM-DD}-v2-run.md`

### Format

```markdown
# Supplier Mapping Screen v2 — {YYYY-MM-DD}

## Run parameters
- 10-K date range: {YYYY-MM-DD} to {YYYY-MM-DD}
- Bellwethers queried (degree 1): NVDA, AVGO, TSMC, MSFT, META, AMD
- Mid-chain queried (degree 2): {list}
- One-degree filings returned: {N}
- Two-degree filings returned: {N}
- After market-cap filter: {N}
- After context-disambiguation read: {N}
- After exclusion list: {N}
- Time spent: {N} minutes

## Results

| Ticker | Company | Mkt Cap | Chain | What They Supply | Chokepoint? | Flag for DD? |
|--------|---------|---------|-------|------------------|-------------|--------------|
| ... | ... | ... | NVDA → COHR → [ticker] | ... | ... | ... |

## Top names (narrative)

### 1. {TICKER} — {one-line supply-chain inference}
Chain: {full bellwether → mid-chain → sub-$5B path with verbatim quotes}
Filing passage (verbatim from sub-$5B 10-K): "..."
Filing passage (verbatim from mid-chain 10-K, if forward-pass hit): "..."
What they supply: ...
% of revenue (sub-$5B to mid-chain): ...
% of revenue (mid-chain to bellwether): ...
Chokepoint mapping: ...
Recommendation: full 6-check / WATCH / pass

### 2. ...

### 3. ...

## AXTI retroactive validation (MANDATORY)

**Test 1: Does AXTI's recent 10-K name COHR / LITE / EMCORE / IQE
as a customer?**

Result: {PASS / FAIL}

**Test 2: Does COHR's recent 10-K name AXTI as a substrate supplier?**

Result: {PASS / FAIL}

**Test 3: Does LITE's recent 10-K name AXTI as a substrate supplier?**

Result: {PASS / FAIL}

If AXTI appears via the chain: v2 screen works as designed. Document
the exact chain.

If AXTI still doesn't appear: diagnose. Either (a) the supplier
disclosure is anonymized at both layers (likely), (b) AXTI is a 3-degree
supplier (substrate → wafer-shop → laser-vendor → bellwether), or
(c) AXTI is named in a 20-F or non-US disclosure. Document for v3.

## Refinement notes

- Query effectiveness per mid-chain
- Disambiguation cost (% of raw hits that were references vs. real customers)
- Forward-pass vs reverse-pass: which yielded more candidates?
- Foreign-filer blind spot (if any 20-F follow-up was run)
- Tooling friction
```

## TEST CASES (for retroactive validation)

Same as v1 but extended:

- **AXTI** — Should surface via Coherent/Lumentum chain (test of v2 design)
- **CRDO** — SerDes IP / AECs; named in AVGO ecosystem
- **AAOI** — Optical transceivers; named in MSFT/META supply chain (one-degree)
- **NVTS** — GaN; named directly by NVDA May 2025 (one-degree)
- **POWL** — Switchgear; data center customers but bellwether name?

If v2 catches AXTI via the two-degree chain, the upgrade is validated.

## NEXT RUN

Quarterly cadence: mid-March (calendar-year 10-Ks) and mid-June
(fiscal-year-ending-March 10-Ks). For mid-chain companies with
fiscal-year-ending June 30 (e.g., Coherent), additional run mid-September.
