## MANDATORY — READ BEFORE ANYTHING ELSE

Read these files IN FULL before doing anything:

1. /Users/michaelturner/Desktop/Claude Builds/_master_docs/WORKING_PHILOSOPHY.md
2. /Users/michaelturner/Desktop/Claude Builds/archos/CLAUDE.md
3. /Users/michaelturner/Desktop/Claude Builds/archos/CHOKEPOINT_TAXONOMY.md
4. /Users/michaelturner/Desktop/Claude Builds/archos/CANDIDATE_UNIVERSE.md
5. /Users/michaelturner/Desktop/Claude Builds/archos/INSIGHTS.md

Confirm by stating the LAST LINE of WORKING_PHILOSOPHY.md.
Do not run any commands or make any changes until confirmed read.

---

## SESSION TYPE

THIS IS A NEW SECTOR LENS DISCOVERY SCAN — Physical AI / Humanoid Robotics. Identifying the component-level chokepoints in the humanoid robotics buildout and finding sub-$5B pure-play suppliers before the market discovers them.

---

## CONTEXT

The humanoid robotics buildout is accelerating:
- Tesla Optimus: targeting mass production, factory deployment starting 2025-2026
- Figure: $2.6B+ valuation, partnered with BMW/OpenAI, Figure 02 in production
- Aptronic: NASA partnership, warehouse deployment
- 1X (NEO): backed by OpenAI, Samsung
- Boston Dynamics (Hyundai): Atlas electric humanoid
- NVIDIA Isaac robotics platform: the GPU ecosystem extending to embodied AI
- Chinese players: Unitree, Fourier, UBTECH (already public)

The thesis: just as the AI data center buildout created component chokepoints (GPUs → HBM → optical → power → cooling), the humanoid robotics buildout creates component chokepoints:
- Force/torque sensors (every joint needs force feedback)
- Precision actuators and servo motors (humanoid movement)
- Encoders and position sensors (joint angle measurement)
- Haptic feedback systems (hands/grippers)
- Specialized AI chips for real-time motor control
- Computer vision systems for navigation and manipulation
- Battery/power management for mobile platforms
- Harmonic drives / strain wave gearing (precision joint mechanisms)
- Custom cables / slip rings for articulated joints

VPG (Vishay Precision Group, $1.7B) already ran 5x on this thesis — CEO called 2026 "a pivotal year" for Physical AI, Q1 bookings +25.5%, book-to-bill 1.21x. VPG is the POWL of robotics — it validated the pattern. The question: who is the NEXT VPG? Who makes the components that every humanoid needs, at sub-$5B, before the market connects the dots?

---

## TASK: PHYSICAL AI / ROBOTICS CHOKEPOINT SCAN

### PHASE 1 — Map the Component Chokepoints (30 min)

Before searching for companies, map what components a humanoid robot NEEDS:

**Step 1: Reverse-engineer the humanoid BOM (Bill of Materials)**
Web search for:
- "humanoid robot components" OR "humanoid robot bill of materials"
- "Tesla Optimus teardown" OR "Optimus components suppliers"
- "Figure 02 components" OR "humanoid actuator supplier"
- "humanoid robot supply chain" 2026
- "robotics component market" report 2026
- NVIDIA Isaac platform: what hardware does it certify/integrate with?

Build a component map:
| Component Category | Function | Example Suppliers (any size) | Publicly Traded? |
|---|---|---|---|

**Step 2: Identify the concentration points**
Which components have only 2-3 suppliers globally? Those are the chokepoints. Specifically:
- Harmonic drives: Harmonic Drive Systems (Japan, 6324.T) dominates. Any US/European alternative?
- Force/torque sensors: ATI Industrial Automation (private, acquired by Novanta), VPG, who else?
- Precision actuators for humanoids: who makes the specific actuators Tesla/Figure use?
- Encoders: Renishaw (UK), Heidenhain (private Germany), who else?
- Specialized motor controllers: TI, Infineon (too large), who at sub-$5B?

### PHASE 2 — EdgarTools Filing Discovery (45 min)

**Step 1: 10-K full-text search for robotics language**
Run single-phrase queries against 10-K filings, sub-$5B market cap:
- "humanoid"
- "humanoid robot"
- "force sensor"
- "torque sensor"
- "actuator" AND robotic context
- "servo motor" AND robotic context
- "robotic joint"
- "haptic"
- "physical AI"
- "embodied AI"
- "harmonic drive"
- "strain wave"
- "collaborative robot" OR "cobot"
- "dexterous"
- "legged robot" OR "legged locomotion"
- "Tesla Optimus"
- "Figure" AND robot context

For each hit: verify market cap via web search. Filter to sub-$5B. Read snippet to determine if robotics is core product or just a mention.

**Step 2: 8-K search for robotics contract announcements**
Run against 8-K filings from last 90 days:
- "robotics" AND "agreement" OR "contract"
- "humanoid" AND "supply"
- "actuator" AND "production"
- "NVIDIA Isaac"
- "Tesla" AND "robotics" OR "Optimus"

**Step 3: Revenue inflection in robotics-adjacent companies**
Run against 10-Q filings from last 60 days:
- "robotics" AND "revenue increased" OR "record"
- "automation" AND "backlog" OR "orders increased"
- "physical AI"

### PHASE 3 — Web Search Discovery (30 min)

**Step 1: Robotics pure-play landscape**
- "robotics stock small cap 2026"
- "humanoid robot supplier publicly traded"
- "force torque sensor company stock"
- "actuator company publicly traded robotics"
- "harmonic drive alternative company stock"
- "robotics component manufacturer Nasdaq NYSE"
- "physical AI stock small cap"
- "Tesla Optimus supplier publicly traded"
- site:stockanalysis.com "robotics" OR "actuator" OR "sensor" market cap

**Step 2: VPG supply chain mapping**
VPG is the validated winner. Who are VPG's competitors at sub-$5B?
- "VPG competitors" force sensor precision measurement
- "force sensor manufacturer publicly traded" NOT VPG
- "precision measurement company stock small cap"
- Companies in VPG's 10-K named as competitors

**Step 3: Robotics ETF holdings**
- Pull holdings of ROBO (ROBO Global Robotics & AI ETF), BOTZ (Global X Robotics), IRBO (iShares Robotics)
- Filter for sub-$5B holdings
- Cross-reference against Archos universe

**Step 4: Japanese/European component companies with US listings**
Many robotics component leaders are Japanese or European. Check for:
- US ADR listings of key robotics component companies
- Any recently US-listed robotics hardware companies
- Harmonic Drive Systems ADR? Fanuc ADR? SMC Corp ADR?
- Any sub-$5B US-listed company competing with Japanese incumbents

### PHASE 4 — Candidate Evaluation (30 min)

For each sub-$5B company found, apply the framework:

| Check | Robotics-specific criteria |
|---|---|
| H10-R | Binding supply agreement with Tesla/Figure/Aptronic/Boston Dynamics/1X, OR NVIDIA Isaac certification, OR named supplier in a humanoid OEM's BOM/teardown |
| H8 | >50% revenue from robotics/automation end-market |
| H5 | IGNORED or NEUTRAL — the robotics component layer should be undiscovered (VPG was $25 before the rerate) |
| H11 | Standard balance sheet check |
| Revenue trend | Is robotics revenue inflecting? Bookings accelerating? Book-to-bill >1.0? |
| Concentration | How many competitors make this component? Fewer competitors = stronger chokepoint |
| TAM scaling | Does demand scale linearly with humanoid production? (Force sensors: yes, 40+ per humanoid. Custom chips: maybe not — could be one design for all units) |

**The VPG test:** Does this company show the same pattern VPG showed 12 months ago? Precision industrial company, boring sector, flat revenue for years, then robotics demand inflection drives bookings acceleration that the market hasn't priced?

### PHASE 5 — Cross-reference with Existing Archos Candidates (15 min)

Check if any existing CANDIDATE_UNIVERSE.md names have robotics exposure that wasn't previously tagged:
- Does any defense AI company (AISP, SPAI, CTM, FEIM) have robotics applications?
- Does any sensor/measurement company in the universe have humanoid exposure?
- Are any of the graduated chokepoint winners (POET, AEHR, etc.) pivoting to robotics applications?

### BONUS — Proposed Chokepoint Entries

If this scan identifies genuine chokepoints (concentrated supplier base for humanoid-critical components), propose new taxonomy entries:

Potential Chokepoint #13: Humanoid Force/Torque Sensing
Potential Chokepoint #14: Precision Actuators / Harmonic Drives
Potential Chokepoint #15: Robotic Motor Control Silicon

Each proposed chokepoint needs: supplier count, concentration ratio, demand scaling logic, and at least one sub-$5B pure-play candidate.

---

## OUTPUT

Write results to:
/Users/michaelturner/Desktop/Claude Builds/archos/weekly-scan/runs/2026-05-28-physical-ai-robotics-scan.md

Format:

# Physical AI / Robotics Chokepoint Scan — 2026-05-28

## Humanoid BOM Component Map
[Table of components, functions, supplier concentration]

## Sub-$5B Candidates Found
[Full table with framework quick-check]

## Proposed New Chokepoints
[Per-chokepoint: logic, supplier count, sub-$5B pure-play candidates]

## DD Queue Recommendations
[Priority ordered]

## The "Next VPG" Assessment
[Which candidate most closely matches VPG's pre-rerate profile?]

Update CANDIDATE_UNIVERSE.md with any new WATCH candidates.
Update CHOKEPOINT_TAXONOMY.md with any new proposed chokepoints (as PROPOSED status, pending Sounding Board confirmation).

---

## SESSION END

No git push. No framework changes beyond candidate/taxonomy additions.

Output summary to chat:
- How many robotics component companies found at sub-$5B
- Which components are genuine chokepoints (concentrated supply)
- Top 3 candidates with the "next VPG" profile
- Any existing Archos names with untagged robotics exposure
- Proposed taxonomy additions
- Is Physical AI investable today or still 6-12 months out?

STOP after summary.
