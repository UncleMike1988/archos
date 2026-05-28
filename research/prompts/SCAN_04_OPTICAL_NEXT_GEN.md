## MANDATORY — READ BEFORE ANYTHING ELSE

Read these files IN FULL before doing anything:

1. /Users/michaelturner/Desktop/Claude Builds/_master_docs/WORKING_PHILOSOPHY.md
2. /Users/michaelturner/Desktop/Claude Builds/archos/CLAUDE.md
3. /Users/michaelturner/Desktop/Claude Builds/archos/CHOKEPOINT_TAXONOMY.md
4. /Users/michaelturner/Desktop/Claude Builds/archos/CANDIDATE_UNIVERSE.md
5. /Users/michaelturner/Desktop/Claude Builds/archos/INSIGHTS.md
6. /Users/michaelturner/Desktop/Claude Builds/archos/research/pattern-discovery/SIGNAL_CLUSTERS.md

Confirm by stating the LAST LINE of WORKING_PHILOSOPHY.md.
Do not run any commands or make any changes until confirmed read.

---

## SESSION TYPE

THIS IS A TARGETED DISCOVERY SCAN — identifying next-generation optical interconnect companies positioned for the 1.6T transceiver and co-packaged optics (CPO) cycle deploying in 2027-2028.

---

## CONTEXT

The optical interconnect layer is chokepoint #1 (CPO) and #8 (800G+ transceivers / AECs / SerDes) in the Archos taxonomy. The first wave of winners — AAOI, CRDO, LITE, AXTI, POET — caught the 800G cycle. Most have likely graduated well above $5B by now.

The NEXT cycle is 1.6T (1.6 terabit) transceivers and co-packaged optics for NVIDIA's Vera Rubin and successor platforms. Each NVL72+ rack needs more optical bandwidth than the prior generation. The 1.6T qualification cycle is happening NOW (2026) for 2027-2028 volume deployment.

The opportunity: companies that are in 1.6T qualification or early production TODAY but haven't been bid up because the market is still focused on the 800G winners. This is the same pattern as AAOI being ignored while everyone watched LITE — the next-gen cycle creates new winners.

Key technical areas:
- 1.6T pluggable transceivers (200G-per-lane, LPO vs DSP)
- Co-packaged optics modules (light source + modulator integrated on-package)
- Silicon photonics engines (the optical chiplets that go into CPO)
- EML and VCSEL laser arrays for next-gen data rates
- Optical test and measurement for 1.6T qualification
- Active Electrical Cables (AECs) competing with optics at short reach

---

## TASK: NEXT-GEN OPTICAL INTERCONNECT SCAN

### PHASE 1 — EdgarTools Filing Discovery (45 min)

**Step 1: 10-K full-text search for 1.6T / next-gen optical language**
Run these single-phrase queries against 10-K filings:
- "1.6 terabit"
- "1.6T transceiver"
- "200G per lane"
- "co-packaged optics"
- "silicon photonics"
- "optical engine"
- "CPO module"
- "EML laser"
- "VCSEL" AND "data center" (run "VCSEL" alone, filter snippets)
- "linear pluggable optics" OR "LPO"
- "optical interconnect"
- "active electrical cable"

For each hit: real-time market cap verification. Filter to sub-$5B. Read snippet to determine if this is a MANUFACTURER of optical components or just a USER/integrator.

**Step 2: 8-K search for qualification and design win announcements**
- "design win" AND "optical" (run "design win" alone, filter)
- "qualified supplier" AND "transceiver" OR "optical"
- "800G" (catch companies just now entering 800G production — they're one cycle behind the leaders but may leapfrog to 1.6T)
- "Broadcom" AND "optical" (AVGO is the networking ASIC that pairs with transceivers)
- "Spectrum-X" OR "NVLink" (NVIDIA networking platforms that drive optical demand)

**Step 3: Supplier mapping from NVIDIA/Broadcom optical specs**
- Who supplies the optical modules for NVIDIA NVL72 racks?
- Who are Broadcom's Tomahawk 6 optical ecosystem partners?
- Any sub-$5B companies named in OFC 2026 (Optical Fiber Communication Conference) presentations or press releases?
- Search: "OFC 2026" + company name for sub-$5B optical companies

### PHASE 2 — Web Search Discovery (30 min)

**Step 1: 1.6T / CPO company landscape**
- "1.6T transceiver company stock 2026"
- "co-packaged optics company publicly traded"
- "silicon photonics company small cap"
- "optical interconnect IPO 2025 2026"
- "next generation transceiver manufacturer Nasdaq NYSE"
- "CPO supplier NVIDIA"
- site:stockanalysis.com "optical" OR "photonics" market cap

**Step 2: Industry reports and analyst coverage**
- "optical transceiver market share 2026" (who are the emerging players?)
- "1.6T transceiver qualification" (which companies are in qual today?)
- "co-packaged optics timeline deployment" (when does volume ship?)
- LightCounting or Cignal AI reports on optical transceiver market (analyst firms that track this space)

**Step 3: Check graduated winners for supply chain leads**
AAOI, CRDO, LITE, AXTI, POET all filed 10-Ks naming their suppliers. Run supplier-mapping:
- Who supplies InP substrates to the 1.6T transceiver makers? (AXTI analog)
- Who makes the test equipment for 1.6T qualification? (AEHR analog for optical)
- Who makes the packaging substrates for CPO modules? (Advanced packaging analog)
- Any sub-$5B company in the 1.6T supply chain that the 800G cycle didn't surface?

### PHASE 3 — Taxonomy Verification (15 min)

Pull current market caps for ALL optical names currently in the taxonomy:
- Chokepoint #1 (CPO): AXTI, POET — current market cap?
- Chokepoint #8 (800G+ transceivers): AAOI, CRDO, LITE — current market cap?

For any that have graduated above $5B:
- Document the graduation
- Identify whether a sub-$5B replacement exists on the SAME chokepoint
- If no replacement exists, the chokepoint has an EMPTY active candidate slot — highest priority for this scan to fill

### PHASE 4 — Cross-reference with Balance Sheet Signals (15 min)

For any new optical company found:
- Pull most recent 10-Q
- Check deferred revenue / customer deposits — any first-time appearance?
- Check revenue trajectory — any first-time >40% YoY inflection?
- Check backlog or design-win pipeline disclosures
- Apply the discovery hierarchy: balance-sheet lead qualifies for TIER 2 WATCH even without H10 bellwether fire

---

## CANDIDATE EVALUATION

For each candidate, apply the framework check with optical-specific criteria:

| Check | Optical-specific criteria |
|---|---|
| H10 | NVDA/AVGO named the optical chokepoint (category-level). Design win with a hyperscaler or NVIDIA = vendor-level. Qualification announcement = early-stage vendor-level |
| H8 (tiered) | Sub-$500M = Tier 1 Nano (highest asymmetry — the AXTI pattern). $500M-$2B = Tier 2. $2-5B = Tier 3 |
| H5 | The 800G winners are LOVED. The 1.6T next-gen companies should be IGNORED or NEUTRAL if they haven't shipped volume yet |
| H11 | Optical companies often carry debt from fab buildout. Check: is capex funded by customer prepayments (good) or dilutive equity (risky)? |
| Technology position | Is this company in 1.6T qualification NOW, or still shipping 400G/800G? Qualification timing matters — too early (R&D only) or too late (800G commoditizing) are both wrong |
| Customer concentration | Optical companies often have 1-2 customers >50% of revenue. This is H8 end-market risk — verify the end-market is AI-DC, not telecom or enterprise |

Do NOT run full DD in this session. Flag candidates for DD queue only.

---

## OUTPUT

Write results to:
/Users/michaelturner/Desktop/Claude Builds/archos/weekly-scan/runs/2026-05-27-optical-next-gen-scan.md

Update CANDIDATE_UNIVERSE.md with any new WATCH candidates.
Update CHOKEPOINT_TAXONOMY.md: graduate any >$5B names, add any new sub-$5B names, update Monitor list if 1.6T chokepoint is confirmed but no pure-play exists yet.

---

## SESSION END

No git push. No framework changes beyond candidate/taxonomy additions.

Output summary to chat:
- Current market cap of all existing optical taxonomy names (AXTI, POET, AAOI, CRDO, LITE) — how many graduated?
- Any chokepoint slots now EMPTY of sub-$5B candidates?
- New 1.6T / CPO companies found (public vs private)
- Any in qualification NOW for 2027-2028 deployment?
- Any with balance-sheet leading signals (deferred revenue, design-win backlog)?
- DD queue recommendations
- Is 1.6T investable today or still 6-12 months from having identifiable public pure-plays?
- Taxonomy update recommendations

STOP after summary.
