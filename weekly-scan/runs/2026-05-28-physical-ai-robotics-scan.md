# Physical AI / Robotics Chokepoint Scan — 2026-05-28

**Scan prompt:** `research/prompts/SCAN_PHYSICAL_AI_ROBOTICS.md` (new sector lens discovery)
**Framework:** Archos v2.0 (sector-conditional H10-extended; tiered H8; PARTIAL-RECOVERING H5; balance-sheet primary discovery layer)
**Lens-conditional bellwether class:** **H10-R "Physical AI / Humanoid Robotics"** — proposed (parallels H10-D/H10-N/H10-M/H10-P/H10-G).
**Trigger:** binding supply agreement with Tesla / Figure / Apptronik / Boston Dynamics / 1X / Unitree / Fourier / UBTECH, OR NVIDIA Isaac certification, OR named supplier in a humanoid OEM's BOM/teardown, OR multi-customer aggregation across ≥3 named humanoid developers (MIR-template multi-customer chokepoint validation).
**Calibration case:** VPG (Vishay Precision Group) — already ran 5x on this thesis; +$1.0M Q1 2026 humanoid bookings, 4th developer in engineering discussions; CEO calls 2026 "pivotal year" for Physical AI.

All market caps verified via Yahoo Finance / stockanalysis.com / Robinhood / Macrotrends in real time 2026-05-27 (per CLAUDE.md mandatory real-time price verification rule).

---

## 1. Humanoid BOM Component Map

Mapped against Tesla Optimus, Figure 02, 1X NEO, Apptronik Apollo, Boston Dynamics Atlas Electric. Goldman Sachs / Morgan Stanley "Humanoid 100" BOM cost framework: actuators ~35%, reducers ~15%, screws ~18%, motors ~12%, sensors ~20%, perception ~5%, batteries/electronics ~5%.

| # | Component category | Function | Qty / humanoid | Top global suppliers | Concentration | Sub-$5B U.S.-listed pure-play? |
|---|---|---|---|---|---|---|
| 1 | **Frameless torque motors / BLDC** | Joint actuation | 14-28 | Kollmorgen (RBC parent), Maxon (private CH), Faulhaber (private DE), Estun/Inovance (CN), Allient (US) | Fragmented; CN entrants growing | **ALNT** (Nasdaq, $1.08B) — partial; servo motors are part of broader motion-control portfolio |
| 2 | **Harmonic / strain-wave reducers** | Joint reduction, zero backlash | 14 (Optimus rotary) | Harmonic Drive Systems (6324.TYO ~50-70% global share), Leader Harmonious (688017.SHA), Green Harmonic (CN), Nabtesco (6268.TYO) | **~80-85% Top-4 concentration** | **NONE** — chokepoint without a U.S. vehicle |
| 3 | **Cycloidal / planetary reducers** | Heavy-load joints, hip/shoulder | 6-12 | Nabtesco (6268.TYO ~70% global share), Spinea (private SK), Nidec (6594.TYO), Schaeffler (SHA0.ETR) | Nabtesco dominant | **NONE** |
| 4 | **Planetary roller screws** | Linear joint actuation | 14 (Optimus linear) | Rollvis/GSA (Swiss, private), Hangzhou Xinjian (CN), Schaeffler segment | Duopoly | **NONE** |
| 5 | **Force / torque sensors (strain-gauge)** | 6-axis & 1-axis joint load sensing, fingertip tactile | 6-20+ | ATI Industrial (Novanta-acquired 2024), HBM (Spectris UK), Kistler (private CH), FUTEK (private US), **VPG Micro-Measurements (NYSE)** | Fragmented but VPG only U.S. pure-play | **VPG** (NYSE, $1.72B) — ✅ canonical |
| 6 | **Encoders (magnetic/inductive/optical)** | Joint position feedback | 25-50 | Renishaw (RSW.L UK), Heidenhain (private DE), AMS-Osram (AMS.SW), Celera Motion / Novanta (NOVT) | Mid-concentrated | **NOVT borderline-graduated ($5.82B)** — TIER 4 SEGMENT candidate |
| 7 | **Motor controller / servo-drive ICs** | 3-phase BLDC drive, GaN, sensor fusion | 14-28 channels | TI, Infineon (IFX), STMicro (STMPA), ON Semi, Allegro (ALGM $7.08B), Melexis (MELE.BR) | Mega-cap dominant | **None pure-play** — ALGM/SYNA/AMBA/INDI/CEVA partial coverage |
| 8 | **IMU / 9-DOF MEMS** | Stability, orientation | 1-3 | Bosch Sensortec (private), TDK Invensense, STMicro, ADI, Honeywell, VectorNav (private) | Mega-cap dominant | None pure-play |
| 9 | **Computer vision (depth / RGB / LiDAR)** | Perception | 4-6 cams + opt LiDAR | Sony IMX, OmniVision, Mobileye, **Ouster (OUST)**, Hesai (HSAI), Aeva (AEVA), Innoviz, Luminar, MicroVision | Fragmented post-Velodyne | **OUST $2.83B, AEVA $0.84-1.70B, MVIS $217M, LIDR $77-115M** |
| 10 | **Tactile skin / fingertip pressure** | Manipulation feedback | 10-30 per hand | XELA (private JP), Tekscan (private), Pressure Profile (private), Hanwei (CN) | Privately held | **None U.S.-listed** — white-space chokepoint |
| 11 | **Battery cells / packs** | Mobile energy (2-5 kWh) | 1-2 packs | CATL (300750.SZ), LG ES, Samsung SDI, Panasonic, **Amprius (AMPX)** | Mega-cap dominant | **AMPX** (NYSE, $2.17-2.27B) — silicon-anode partial-fit |
| 12 | **BMS / DC-DC / 48V power electronics** | Bus regulation | 1-3 | Vicor (VICR), POWI, MPWR, Infineon | Mid-concentrated | None pure-play robotics-first |
| 13 | **Real-time motor MCU / edge AI compute** | Joint control + edge inference | 1 SoC + 14-28 MCUs | NVIDIA Jetson, Qualcomm, Renesas, TI Sitara, **Ambarella (AMBA)**, **Synaptics (SYNA)** | Mega-cap dominant | **AMBA $3.85-4.10B, INDI $1.00B, CEVA $1.09B** |
| 14 | **Haptic feedback ICs / actuators** | Hands/grippers tactile | 5-20+ | **Immersion (IMMR)**, **Interlink (LINK)**, TI, Bosch | Fragmented small-cap | **IMMR ($216M), LINK ($74M)** |
| 15 | **Precision bearings, rod-ends, sphericals** | Joint mechanical structure | 100+ | Schaeffler, SKF, NSK, THK, Hiwin (2049.TW), RBC ($11B above cap) | Mid-concentrated | **None pure-play sub-$5B** |
| 16 | **Rare-earth permanent magnets (NdFeB)** | Motor torque | 14-28 motors × ~150g | MP Materials, USA Rare Earth, Hitachi Metals, JL Mag (300748.SZ) | Geopolitically concentrated | **MP ~$11B, USAR ~$5.5-6.1B — both graduated** (parallel "geopolitical materials" lens, not core H10-R) |
| 17 | **Voice / mic array** | HMI | 4-8 | Knowles (KN), Goertek, AAC, Cirrus Logic | Mid-concentrated | None pure-play |
| 18 | **Wire harness / slip rings / connectors** | Articulated routing | extensive | Molex (private), TE Connectivity, Amphenol, Harting (private), MOOG | Mega-cap dominant | None pure-play |

**Structural finding:** The most-concentrated chokepoints (#2 harmonic reducers, #3 cycloidal reducers, #4 planetary roller screws) are **structurally non-U.S.-investable** at the sub-$5B level. Japanese leaders (Harmonic Drive 6324.TYO, Nabtesco 6268.TYO, Yaskawa 6506.TYO, SMC 6273.TYO, Fanuc 6954.TYO) trade as **OTC-only sponsored ADRs** (YASKY, SMCAY, HSYDF) — auto-REJECT per Archos NLST precedent. The chokepoint **logic** is real; the chokepoint **ownership** is locked to Tokyo/Taipei/Shanghai. **The U.S. sub-$5B robotics surface skews toward the sensing / perception / haptics sub-chokepoint, not the actuator sub-chokepoint.**

---

## 2. Sub-$5B Candidates Found — Framework Quick-Check

Full universe of sub-$5B U.S.-listed (Nasdaq / NYSE / NYSE American — no OTC) candidates surfaced by Phases 1-3. Market caps verified live 2026-05-27.

| Ticker | Exch | Mkt Cap (verified) | Tier | H10-R | H8 (>50% robotics/automation end-market) | H5 sentiment | H11 (balance-sheet) | Provisional disposition |
|---|---|---|---|---|---|---|---|---|
| **VPG** | NYSE | **$1.72B** | TIER 2 CATALYST | **PASS** — $1.0M Q1'26 humanoid bookings + 4th humanoid developer in engineering discussions (multi-customer aggregation, MIR-template) | **FAIL** — diversified industrial precision; humanoid ~5-8% of revenue Q1'26 inflecting | **PARTIAL-RECOVERING** — already +5x; $128.97 vs ATH; humanoid catalyst is fresh; CEO "pivotal year" framing | **PASS** | **WATCH (calibration case, post-rerate)** — Stage-2 DD already implicit; reference-class winner. Document re-entry decision via PARTIAL-RECOVERING entry geometry. |
| **ALNT** | Nasdaq | **$1.08B** | TIER 2 CATALYST | **FLAG** — Apr 23, 2026 humanoid motor whitepaper + May 19, 2026 "thermally-optimized humanoid joints" webinar + Robotics Summit 2026 demo. NO BINDING OEM CUSTOMER NAMED YET. | **FAIL** — Allient is broad precision motion (industrial + medical + aerospace + vehicle); robotics is one segment | **NEUTRAL/IGNORED** — boring industrial supplier; $61.80, +1Y modest; coverage thin | **PASS** — profitable, $44.28 P/E | **TIER 2 WATCH** — strongest "next VPG" candidate by pattern fit. Re-eval trigger: named humanoid OEM customer 8-K (Tesla/Figure/Apptronik). |
| **CEVA** | Nasdaq | **$1.09B** | TIER 2 CATALYST | **FLAG** — Self-described "leader in silicon and software IP enabling Physical AI"; 14 IP licensing deals Q1'26; AI >20% of licensing. No named humanoid OEM. | **FAIL** — IP licensing spans mobile, IoT, auto, robotics; robotics is forward-mix | **NEUTRAL** — recovered from 2024 lows | **PASS** | **TIER 2 WATCH** — IP-licensing chokepoint angle (different from VPG's hardware angle). Re-eval trigger: AI/Physical-AI licensing >40% of total. |
| **OUST** | Nasdaq | **$2.83B** | TIER 3 COMPOUNDER | **PASS** — Self-described "leader in sensing and perception for Physical AI"; NVIDIA DRIVE Hyperion qualified; Stereolabs acquisition; explicit humanoid mention in 10-K | **PARTIAL** — auto + smart infra + industrial + robotics; "Physical AI platform" repositioning suggests >40% mix but verify | **PARTIAL** — 52w $10.36 → $44.46 (+4.3x); rerate underway but not LOVED-extreme | **PARTIAL** — narrowing losses, post-Velodyne consolidation cash | **TIER 3 WATCH** — needs robotics revenue-mix verification before promotion. Re-eval trigger: 10-Q segment disclosure of Physical AI / robotics share. |
| **AMBA** | Nasdaq | **$3.85-4.10B** | TIER 3 COMPOUNDER | **FLAG** — Vision SoC referenced as Tesla Optimus vision and in 10-K humanoid context; multiple ETF inclusion (ROBO + THNQ) | **PARTIAL** — auto / IoT camera / robotics mix; not pure-play | **PARTIAL** — recovered substantially from 2024 lows | **PASS** | **TIER 3 WATCH** — already partially-discovered (in earlier Archos scans + ETF holdings); document robotics exposure formally. |
| **AEVA** | Nasdaq | **$0.84-1.70B** (volatile) | TIER 1-2 (range) | **PASS** — Q1'26 named three Physical AI commercial deployments (Forterra defense, Aeva CityOS ITS, **Nikon factory automation**); LG Innotek + NVIDIA partnerships | **PARTIAL** — auto primary but factory automation expansion confirmed | **PARTIAL-RECOVERING** — Q1 rev +90% YoY ($6.3M); stock +253% post-LiDAR contract intra-Q1 | **PARTIAL** — cash-burn but raised; verify runway | **TIER 2 WATCH** — FMCW differentiation + multi-vertical Physical AI commercialization. Re-eval trigger: factory-automation revenue mix; cash runway. |
| **AMPX** | NYSE | **$2.17-2.27B** | TIER 3 COMPOUNDER | **FLAG** — Robotics named as target end-market in 10-K; primary today is defense aviation/UAV. Forward-looking. | **PARTIAL** — silicon-anode batteries broad EM; robotics is forward expansion | **PARTIAL** — down -29% from recent highs | **PASS** — Q1'26 record revenue + raised guidance | **TIER 3 WATCH** — silicon-anode play on humanoid energy-density binding constraint. Re-eval trigger: named humanoid OEM design-in. |
| **INDI** | Nasdaq | **$1.00B** | TIER 2 CATALYST | **FLAG** — May 2026 8-K acquired ams OSRAM CMOS image sensor line "to support expansion into Physical AI… humanoid robots, cobots, AMRs" | **FAIL** — primarily automotive ADAS / EV semis; Physical AI is forward expansion | **PARTIAL** — recovered from $1.50s in 2024; now ~$5 | **PARTIAL** — narrowing losses; verify cash runway | **TIER 2 MONITOR** — Physical AI is one of several pivots. Document but do not promote until end-market test passes. |
| **IMMR** | Nasdaq | **$216M** | TIER 1 NANO | **FLAG** — 10-K names robotics adjacency in haptic IP licensing | **FAIL** — primarily consumer/gaming/auto haptic IP; robotics is small | **IGNORED** — $6.47, sub-$300M, low coverage | **PASS** — IP-licensing model, profitable | **TIER 1 NANO MONITOR** — haptics chokepoint angle but consumer/gaming dominates. Re-eval trigger: named humanoid OEM IP license. |
| **LINK** | Nasdaq | **$74M** | TIER 1 NANO | **FLAG** — 10-K names Force-Sensing-Resistor + haptic actuator IP; "operate in reverse as actuators for haptic feedback" | **PARTIAL** — sensors + printed electronics for HMI/IoT; verify robotics mix | **IGNORED-EXTREME** — $4.70, $74M cap, 1 analyst | **PARTIAL** — 2026 guidance: return to profitability; double-digit organic growth | **TIER 1 NANO WATCH** — highest-asymmetry-tier candidate; FSR + haptic-actuator pure-play. Re-eval trigger: humanoid OEM contract disclosure. |
| **MVIS** | Nasdaq | **$217M** | TIER 1 NANO | **FLAG** — lidar Physical AI positioning; industrial/defense primary; humanoid context referenced | **FAIL** — industrial/defense primary | **IGNORED-EXTREME** — $0.66 sub-$1 | **RISK** — repeatedly broken-IPO; cash burn; H11 risk | **TIER 1 NANO MONITOR** — H11 fragility ahead of broken-IPO H5 setup. Re-eval trigger: cash runway extension + Physical AI customer. |
| **LIDR** | Nasdaq | **$77-115M** | TIER 1 NANO | **FLAG** — 10-K names "physical AI sensing solutions built on high-performance, active lidar" | **PARTIAL** — but Q1 rev only $101K | **IGNORED-EXTREME** — pre-revenue scale | **RISK** — burn rate vs cash | **TIER 1 NANO MONITOR** — pre-revenue moonshot risk; document but not promote. |
| **VTIX** | Nasdaq | **$105M** | TIER 1 NANO | **FLAG** — Omni One treadmill for humanoid teleoperation training; UCF + U.S. Army interest; NX1 partnership with 1HMX | **FAIL** — VR gaming/fitness primary; humanoid-training adjacency | **IGNORED** — $3.30, recent SPAC | **PARTIAL** — verify runway | **MONITOR** — adjacency to humanoid training data pipeline, not chokepoint hardware. |
| **NOVT** | Nasdaq | **$5.45-5.82B** (just over cap) | **TIER 4 SEGMENT candidate** | **PASS at segment level** — ATI Industrial Automation segment world leader in force/torque sensors + robot tooling; >10 humanoid OEM engagements; NVIDIA Halos Lab integration; expects robotics/automation to double 2026, double again 2027 | **PASS at segment level** — Automation Enabling Tech segment $131M Q1'26 rev, bookings +37%, B/B 1.10; need to verify AI-DC/robotics >50% segment | **NEUTRAL** | **PASS** — profitable, raised 2026 guidance | **TIER 4 SEGMENT WATCH** — Framework v2.0 Tier 4 candidate; verify segment AI-DC/robotics revenue mix exceeds 50% and >40% YoY growth (per CLAUDE.md). |
| **SYNA** | Nasdaq | **$5.55-5.71B** (just over cap) | **TIER 4 SEGMENT candidate** | **FLAG** — Q1'26 8-K explicitly cites "multiple additional design wins in Physical AI and robotics"; Coralboard Edge AI w/ Google Research at I/O 2026 | **PARTIAL** — consumer/PC/IoT/auto/mobile mix; Physical AI is forward | **PARTIAL** — 52w $57.54 → $148.10 (+2.5x) | **PASS** | **TIER 4 SEGMENT MONITOR** — verify Physical AI/robotics segment economics. |
| **ALGM** | Nasdaq | **$7.08B** (graduated above $5B) | GRADUATED-ADJACENT | **FLAG** — Allegro Humanoids application page; 2026 robotics sales doubling YoY | **FAIL** — auto-dominated | **PARTIAL** | **PASS** | **DOCUMENT-ONLY** — graduated above cap; reference for taxonomy validation. |

**Candidates examined and REJECTED (with documented reasons):**

| Ticker | Reason |
|---|---|
| **PDYN** (Palladyne AI) | $333M; **already in Archos REJECT** per CANDIDATE_UNIVERSE.md (M&A pivot blind spot; ex-Sarcos reverse-merger). Pure-play embodied-AI software pattern superficially attractive but blind spot holds — no override. |
| **RR** (Richtech Robotics) | $630-733M; service-robot OEM with Nov 2024 humanoid pivot announcement = sector-pivot blind-spot pattern (FABC/VWAV/VDTA analog). H5 LOVED + promotional sentiment. |
| **SERV** (Serve Robotics) | $687-702M; sidewalk delivery robots, not chokepoint hardware. H5 LOVED — sales +578% per Motley Fool; integrator not component pure-play. |
| **KSCP** (Knightscope) | $45-49M; autonomous security robots; chronic dilution, integrator. |
| **CYN** (Cyngn) | $21M; industrial autonomy SaaS for AGVs; H11 risk via persistent dilution. |
| **PRCT, ARAY, MBOT** | Surgical / medical robotics pure-plays — RIGHT STRUCTURE, WRONG END-MARKET. WOLF-anti-pattern: Physical AI thesis is industrial / humanoid / labor-substitution, not surgical. |
| **HSAI** (Hesai Group) | $3.24B Nasdaq main-board ADR but **Chinese ADR geopolitical / PCAOB risk**; treat as parallel framework. |
| **INVZ** (Innoviz) | Sub-$100M; March 2026 Nasdaq sub-$1 non-compliance notice = H11 RED FAIL. |
| **FFAI** (Faraday Future) | First-time "Robotics" segment in 10-Q matches balance-sheet signal pattern, BUT issuer is high-controversy EV reverse-merger; SHAZ-shape. REJECT per calibration. |
| **BBAI, INOD** | Software/data labeling; not chokepoint hardware. INOD already documented as AI services not AI infra (REJECT per CANDIDATE_UNIVERSE.md). |
| **GPUS, GGRP, NXNT, KITT, LCCC, LQMT** | Nano-cap pivot / de-SPAC shells with humanoid in PR-only branding. Cluster 8 risk. |
| **OTC ADRs** (YASKY, NCTKY, SMCAY, HSYDF, HSYDY) | Yaskawa, Nidec, SMC, Harmonic Drive Systems — all OTC-only sponsored ADRs. **Auto-REJECT per Archos NLST precedent.** Document as foreign-listed structural gap. |
| **MEGA-CAPS / GRADUATED** | CGNX $11B, SYM $30B, MTD $30B, AVAV $9B, MBLY $8.48B, ABB, RBC $11B, NVDA, TSLA, ISRG, Keyence — all over cap. |

**Total surfaced sub-$5B U.S.-listed candidates: 13 (TIER 1 NANO: 5 — LINK, IMMR, MVIS, VTIX, LIDR; TIER 2 CATALYST: 5 — VPG, ALNT, CEVA, INDI, AEVA; TIER 3 COMPOUNDER: 3 — OUST, AMBA, AMPX). Plus 2 TIER 4 SEGMENT candidates (NOVT, SYNA) just above $5B parent cap.**

---

## 3. Proposed New Chokepoints

**Chokepoint #13 — Humanoid Force / Torque Sensing**

**Logic:** Every humanoid actuator and gripper needs closed-loop torque/force feedback. Goldman/MS BOM estimate: sensors collectively ~20% of total cost. Per humanoid: 6-axis force/torque sensors at wrists (2), ankles (2), shoulders (2 × multi-axis), plus single-axis strain gauges at every joint torque-sensor location (12-20+). Component is non-substitutable in current architectures.

**Supplier concentration:** Fragmented globally but dominated by ATI Industrial Automation (Novanta-acquired 2024 — now in NOVT Automation Enabling Tech segment), HBM (Spectris UK), Kistler (private CH), FUTEK (private US), VPG (NYSE). Five-supplier oligopoly with no Chinese second-source at high-performance specification.

**Demand scaling:** Linear with humanoid unit production (each unit consumes ~20 strain-gauge channels + 4-6 multi-axis assemblies). Per-humanoid dollar content: $500-1,500.

**Sub-$5B pure-play candidates:**
- **VPG (NYSE, $1.72B)** — TIER 2 CATALYST — ACTIVE — H10-R PASS (multi-customer aggregation: 4 humanoid OEMs in commercial discussions per Q1'26 8-K). $1.0M Q1'26 orders booked; $600K shipped Q1; >2x guided for Q2; $4M 2025 → $5M+ 2026 baseline with 50% CAGR modeled.

**Status:** ACTIVE — proposed for taxonomy admission pending Sounding Board confirmation.

---

**Chokepoint #14 — Precision Actuator Components (Harmonic + Cycloidal Reducers + Planetary Roller Screws)**

**Logic:** Humanoid actuator stack = motor + reducer + position/torque sensors + drive electronics. Reducers are the **single most-concentrated chokepoint in the humanoid BOM**. 14 harmonic-drive rotary actuators per Optimus + 6-12 cycloidal + 14 planetary-roller-screw linear actuators. Combined BOM contribution: ~35-40% of unit cost.

**Supplier concentration:**
- **Harmonic reducers:** Harmonic Drive Systems (6324.TYO ~50-70% global share), Leader Harmonious (688017.SHA), Green Harmonic (CN), Sun Drive (CN) — Top-4 ~80-85%.
- **Cycloidal reducers:** Nabtesco (6268.TYO ~70% global share), Sumitomo Heavy, Nidec Drive Tech (post-Kollmorgen acquisition), Spinea (SK private).
- **Planetary roller screws:** Rollvis / GSA (Swiss private) + Hangzhou Xinjian (CN) duopoly.

**Demand scaling:** Linear with humanoid unit production. Per-humanoid dollar content: $5,000-12,000.

**Sub-$5B U.S.-listed pure-play candidates: NONE.**

**Status:** **EMPTY — DOCUMENTED CHOKEPOINT WITHOUT A U.S. VEHICLE.** Parallel to taxonomy entries #2 HBM/HBF (post-SNDK), #3 HBM inspection (post-ONTO), #5 GaN/SiC (post-NVTS), #8 Optical (structurally consolidated). All major suppliers Japanese (6324, 6268, 6594), Chinese (688017, 300748), or Swiss/private. **Adjacent candidate ALNT ($1.08B) supplies frameless motors / encoders for humanoid actuator stacks but does NOT manufacture reducers.** Discovery vectors for future quarterly refresh: (a) IPO pipeline for U.S./European reducer startups; (b) Schaeffler (SHA0.ETR) planetary-gear-actuator-for-humanoids CES 2026 announcement — verify if U.S.-tradable below $5B; (c) Nidec Drive Technology spin candidates.

---

**Chokepoint #15 — Humanoid Motor-Control & Sensor-Fusion Silicon**

**Logic:** Real-time joint control (sub-millisecond latency for 14-28 BLDC drive channels) + sensor fusion for vision/IMU/tactile + edge AI inference for closed-loop control. Three sub-categories: (a) motor driver ICs (Gallium-Nitride or Silicon, per-channel), (b) sensor SoCs (vision + tactile + IMU + audio fusion), (c) edge AI accelerator (real-time inference for VLA models like Figure Helix).

**Supplier concentration:** Mega-cap dominant — TI, Infineon, STMicro, Allegro (ALGM, just graduated $7.08B). Sub-$5B IP-licensing layer has CEVA. Sub-$5B sensor-SoC layer has INDI, AMBA, SYNA (graduated borderline).

**Demand scaling:** Bounded per-unit (1 main SoC + 14-28 MCUs + N driver ICs); per-humanoid dollar content $200-800 — meaningfully lower than #13 sensors or #14 reducers but per-unit-revenue concentrates with fewer suppliers.

**Sub-$5B U.S.-listed pure-play candidates:**
- **CEVA (Nasdaq, $1.09B)** — TIER 2 CATALYST — IP-licensing pure-play across edge AI / sensor fusion / "Physical AI" — H10-R FLAG (self-described leader, no named humanoid OEM)
- **INDI (Nasdaq, $1.00B)** — TIER 2 CATALYST — sensor-fusion silicon expanding into Physical AI via ams OSRAM CMOS line acquisition — H10-R FLAG
- **AMBA (Nasdaq, $3.85-4.10B)** — TIER 3 COMPOUNDER — vision SoC; Tesla Optimus vision reference + multiple ETF inclusion — H10-R FLAG
- **SYNA (Nasdaq, $5.55-5.71B)** — TIER 4 SEGMENT — Physical AI design wins disclosure Q1'26

**Status:** ACTIVE — proposed for taxonomy admission pending Sounding Board confirmation. Multiple sub-$5B candidates but no single chokepoint pure-play; this is a "fragmented chokepoint" with NOT one but several U.S. vehicles.

---

**Chokepoint #16 — Humanoid Perception (LiDAR + Active Depth + Vision)**

**Logic:** Humanoid mobility outside structured factory floors requires solid-state LiDAR + depth cameras for navigation, collision avoidance, dynamic-obstacle tracking. Post-Velodyne the LiDAR market has consolidated into 4-5 Tier 1 suppliers competing on auto + industrial + robotics.

**Supplier concentration:** Fragmented post-consolidation. OUST + AEVA + HSAI + INVZ + MVIS + LIDR + LAZR. Sony / OmniVision dominate RGB cameras (mega-cap).

**Demand scaling:** Per-humanoid: 0-1 LiDAR + 4-6 depth/RGB cameras. Per-humanoid dollar content: $500-2,000.

**Sub-$5B U.S.-listed pure-play candidates:**
- **OUST (Nasdaq, $2.83B)** — TIER 3 COMPOUNDER — H10-R PASS (NVIDIA DRIVE Hyperion qualified; humanoid named in 10-K; Stereolabs acquisition)
- **AEVA (Nasdaq, $0.84-1.70B)** — TIER 1-2 — H10-R PASS (Forterra + Aeva CityOS + Nikon factory automation in single Q1'26 quarter)
- **MVIS (Nasdaq, $217M)** — TIER 1 NANO — H10-R FLAG; H11 fragility caveat
- **LIDR / AEye (Nasdaq, $77-115M)** — TIER 1 NANO — H10-R FLAG; pre-revenue moonshot caveat

**Status:** ACTIVE — proposed for taxonomy admission pending Sounding Board confirmation.

---

**Chokepoint #17 — Humanoid Tactile Skin + Haptic Feedback**

**Logic:** Dexterous manipulation requires distributed pressure / shear / temperature sensors across fingertips, palm, sometimes torso (collision/safety). Plus haptic feedback actuators for teleoperation training. Both layers are emerging.

**Supplier concentration:** Tactile-skin layer is dominated by private (XELA JP, Tekscan US, PPS US, Hanwei CN). **No U.S.-listed pure-play exists for tactile skin** — genuine white space. Haptic feedback layer has Immersion (NASDAQ:IMMR, $216M) + Interlink (NASDAQ:LINK, $74M).

**Demand scaling:** Tactile skin per-humanoid: 10-30 sensors per hand × 2 hands + body coverage = 20-100 sensor channels. Haptic actuator demand is driven by humanoid TRAINING / teleoperation, not deployment — so demand is more tied to humanoid R&D headcount than unit production.

**Sub-$5B U.S.-listed pure-play candidates:**
- **IMMR (Nasdaq, $216M)** — TIER 1 NANO — H10-R FLAG (consumer-gaming-heavy mix; haptics-IP pure-play)
- **LINK (Nasdaq, $74M)** — TIER 1 NANO — H10-R FLAG (force-sensing-resistor + haptic actuator IP)

**Status:** PROPOSED — white-space-flagged. Tactile-skin sub-component has zero U.S. pure-play; haptic-feedback has two TIER 1 NANO candidates.

---

## 4. DD Queue Recommendations (priority-ordered)

| Priority | Ticker | Reason | DD trigger / re-eval condition |
|---|---|---|---|
| 1 | **VPG ($1.72B)** | Already running; reference-class winner; H10-R PASS via multi-customer aggregation; balance-sheet signal LIVE | **DD already implicit by post-rerate status.** Decision frame: enter via PARTIAL-RECOVERING geometry at 50% tier-standard position; OR document as "winner-already-running, no new initiation." Re-eval if 20-30% drawdown brings sentiment back toward NEUTRAL. |
| 2 | **ALNT ($1.08B)** | Strongest "next VPG" pattern fit: boring industrial motion supplier, NEUTRAL/IGNORED, sub-$2B, **supplier self-positioning into humanoid chokepoint** via Apr 23 / May 19 / May 26 2026 publications and demos. H8 end-market test fails today but inflection vector is identical to VPG's 2024-2025 trajectory. | **Full DUE_DILIGENCE_CHECKLIST.md within 14 days.** Section-2 priority: ALNT 10-K segment data for robotics/automation revenue share; named humanoid OEM 8-K (any of Tesla / Figure / Apptronik / Boston Dynamics / 1X). Re-eval trigger: binding humanoid OEM customer announcement = H10-R PASS upgrade. |
| 3 | **LINK ($74M)** | TIER 1 NANO highest-asymmetry candidate. FSR + haptic actuator pure-play. IGNORED-EXTREME sentiment. 2026 guidance: return to profitability + double-digit organic growth. | **Full DUE_DILIGENCE_CHECKLIST.md within 30 days.** Section-2 priority: humanoid OEM disclosure or VLM-training-tool design-in; cash runway; insider activity. Tier-1 NANO position size $3-5K. |
| 4 | **NOVT ($5.45-5.82B)** | TIER 4 SEGMENT candidate (Framework v2.0). ATI Industrial Automation segment is the world-leader force/torque-sensor + robot-tooling franchise, with >10 humanoid OEM engagements + NVIDIA Halos Lab integration. Parent just above cap. | **Verify TIER 4 qualification:** (a) Automation Enabling Tech segment >50% AI-DC/robotics end-market AND (b) segment growing >40% YoY (Q1'26 bookings +37% is borderline). If qualifies, treat segment as synthetic standalone. |
| 5 | **OUST ($2.83B)** | TIER 3 COMPOUNDER; H10-R PASS via NVIDIA DRIVE Hyperion qualification; "leader in sensing and perception for Physical AI" self-claim; Stereolabs acquisition completes vision-stack consolidation. | **DD within 30 days IF H8 verifies.** Section-2 priority: 10-Q segment disclosure of robotics/Physical-AI revenue share — needs to verify >50%. H5 caveat: already +4.3x off 52-week low — verify PARTIAL not LOVED. |
| 6 | **CEVA ($1.09B)** | IP-licensing chokepoint angle. 14 IP deals Q1'26; AI >20% of licensing. Self-described "Physical AI leader." Different chokepoint position from VPG (software-IP layer vs hardware-sensor layer). | **DD within 30 days.** Section-2 priority: verify Physical AI / robotics licensing mix >40% of total; named humanoid OEM IP licensee. |
| 7 | **AMBA ($3.85-4.10B)** | Already partially-discovered; vision SoC referenced in Tesla Optimus context + multiple ETF inclusion. Formal robotics-lens classification. | **Document robotics exposure** in existing AMBA entry. Lower urgency — already part-discovered, less asymmetry remaining. |
| 8 | **AEVA ($0.84-1.70B)** | H10-R PASS via 3-vertical Physical AI commercial deployment in single Q1'26 quarter (defense + ITS + factory automation). FMCW differentiation. | **DD with cash-runway focus.** Volatile price — verify H5 PARTIAL-RECOVERING via 25% pullback from Q1 high. H11 risk requires close attention. |
| 9 | **AMPX ($2.17-2.27B)** | Silicon-anode battery play on humanoid energy-density binding constraint. Robotics is forward end-market today. | **MONITOR.** Re-eval trigger: named humanoid OEM silicon-anode design-in (Figure, Optimus, Apptronik). |
| 10 | **IMMR ($216M)** | TIER 1 NANO haptics IP. Robotics is small share of mix today. | **MONITOR.** Re-eval trigger: named humanoid OEM haptic IP license. |

**Stage 2 DD reminder:** Each ACCEPT-track candidate (priorities 1-6 above) requires DUE_DILIGENCE_CHECKLIST.md Section 1-5 + mandatory Section 6 /last30days social signal sweep. SHAZ calibration case applies; never skip the social sweep.

---

## 5. The "Next VPG" Assessment

**Definition:** A "next VPG" candidate is a sub-$5B U.S.-listed precision industrial / sensing component supplier that (a) shows the same boring-sector + IGNORED/NEUTRAL + first-time humanoid order pattern VPG showed in 2024-2025, (b) is positioned at a verified chokepoint in the humanoid BOM, (c) has either the balance-sheet signal (first-time customer deposits / deferred revenue from a chokepoint-adjacent end-market) per Framework v2.0 discovery hierarchy OR explicit supplier-side self-positioning into the humanoid market.

**Ranked candidates:**

**#1 — ALNT (Allient, $1.08B)** — **strongest pattern fit.** Boring industrial motion-control supplier with motors + encoders + drives stack covering humanoid actuator electromechanical layer. Sub-$2B Tier 2 cap. NEUTRAL/IGNORED sentiment (only 1 analyst coverage). **Three pieces of supplier self-positioning in 33 days (April 23, May 19, May 26 2026)**: humanoid motor selection whitepaper, "thermally-optimized humanoid joints" webinar, Robotics Summit 2026 advanced motion solutions demo. This is the **identical pattern VPG showed before its humanoid revenue ramp** — supplier publishes technical material for humanoid OEM engineers, builds relationships, then customer wins materialize 2-4 quarters later. Critical gap vs VPG: no named binding humanoid OEM customer yet — H10-R FLAG (supplier self-marketing) not PASS (binding agreement). **DD priority 2 in queue above.**

**#2 — LINK (Interlink Electronics, $74M)** — **TIER 1 NANO highest-asymmetry pattern fit.** Force-sensing-resistor + haptic actuator IP pure-play. IGNORED-EXTREME sentiment at $4.70 / $74M cap. 10-K names FSR as "operate in reverse as actuators for haptic feedback" — direct humanoid hand / gripper applicability. 2026 guidance: return to profitability + double-digit organic growth (H11 inflection). Dose-response math: if LINK retraces VPG's 5x rerate from $74M base, that's $370M; if a humanoid OEM customer disclosure triggers a chokepoint-validation rerate to AEHR-tier $1-3B, that's a 16-40x outcome. Critical gap: no named humanoid OEM customer; revenue mix is HMI / IoT / printed-electronics across multiple end-markets.

**#3 — IMMR (Immersion Corporation, $216M)** — TIER 1 NANO haptics-IP licensing pure-play. Lower-conviction "next VPG" candidate because (a) consumer/gaming/auto dominates the existing IP licensing mix and (b) haptic IP for humanoid teleoperation training is forward-looking demand, not immediate humanoid-deployment demand.

**Honorable mention — NOVT (Novanta) TIER 4 SEGMENT:** ATI Industrial Automation segment is structurally the VPG analog at higher caliber (world-leader force/torque-sensor + robot-tooling franchise with >10 humanoid OEM engagements). Parent at $5.45-5.82B is just above the H8 cap. Under Framework v2.0 Tier 4 SEGMENT logic, if Automation Enabling Tech segment passes >50% AI-DC/robotics end-market AND >40% YoY (Q1'26 bookings +37% is borderline), the segment can be treated as synthetic standalone. **The framework's Tier 4 SEGMENT designation was DESIGNED for exactly this case** — NOVT is the canonical Tier 4 candidate of the humanoid lens.

**Verdict:** **ALNT is the cleanest "next VPG" pattern fit.** LINK offers higher TIER 1 NANO asymmetry but with more execution risk. NOVT is the TIER 4 SEGMENT structural analog. No candidate has the **binding multi-OEM customer aggregation** that VPG already has — meaning the next 1-3 quarters are an entry-window opportunity for whoever fires first.

---

## Existing Archos Universe Cross-Reference

Reviewed CANDIDATE_UNIVERSE.md entries (defense AI cluster + nano-cap AI cluster + chokepoint pure-plays + government-equity cluster + nuclear cluster + critical-minerals cluster) and CHOKEPOINT_TAXONOMY.md graduated pure-plays for untagged robotics exposure:

| Name | Existing classification | Robotics exposure? | Action |
|---|---|---|---|
| **AMBA** | (no formal entry; referenced in Phase 4 universal study at nano-cap AI tier) | **YES** — vision SoC for Tesla Optimus; multiple humanoid ETF inclusion (ROBO, THNQ); 10-K humanoid context | **Add formal TIER 3 WATCH entry for AMBA under proposed chokepoint #15 (Humanoid Motor-Control & Sensor-Fusion Silicon)** |
| **AISP** (Airship AI) | TIER 2 STRONG, fast-track DD per CANDIDATE_UNIVERSE.md | No humanoid exposure; defense ML video surveillance | None — defense AI lens only |
| **SPAI** (Safe Pro Group) | TIER 1 NANO, fast-track DD per Screen 9 quad-confluence | No humanoid exposure; counter-UAS imagery AI | None — defense AI lens only |
| **CTM** (Castellum) | TIER 1, counter-UAS defense | No humanoid exposure | None |
| **FEIM** (Frequency Electronics) | TIER 1 NANO / TIER 2 CATALYST defense PNT | No humanoid exposure; satellite timing pure-play | None |
| **POET** | ACTIVE chokepoint #1 CPO | No direct humanoid exposure | None |
| **AEHR** | ACTIVE chokepoint #4 HBM burn-in (borderline-graduated $3.46B) | No humanoid exposure | None |
| **HPS.A** | ACTIVE chokepoint #6 Grid | No humanoid exposure | None |
| **PSIX** | ACTIVE chokepoint #10 Gensets | No humanoid exposure | None |
| **WYFI** | ACTIVE chokepoint #7 Neocloud | No humanoid exposure | None |
| **DUOT, MOVE** | TIER 1 NANO Neocloud sub-WATCH | No humanoid exposure | None |
| **LSCC** (Lattice Semi) | Phase 1 near-miss control; over cap | Edge-inference adjacency includes robotics applications, but already graduated | None (out of cap) |
| **PDYN** | REJECTED per M&A pivot blind spot | YES, pure-play embodied AI software — but blind spot holds | **Maintain REJECT** — M&A pivot blind spot is structural; PDYN's humanoid relevance does not override it |
| **MIR, LEU, NNE, ASPI, NUCL** | Nuclear cluster (proposed chokepoint #11) | No humanoid exposure | None |
| **CRML, UAMY, NB, IDR, METC, UURAF, ALM, TMC** | Critical minerals + gov equity | Rare-earth magnets for humanoid actuators is a forward demand sink; tracked separately under H10-M / H10-G lens, not core H10-R | None for core robotics lens |

**Conclusion:** **Only AMBA shows material untagged robotics exposure** within the existing Archos universe. The defense-AI cluster (AISP, SPAI, CTM, FEIM) is structurally adjacent (autonomy + sensor fusion + AI) but has not transitioned to humanoid-OEM customer disclosure. Defense-robotics adjacency (counter-UAS, ground robots, exoskeletons) is real but is governed by H10-D, not H10-R.

---

## Summary

**Sub-$5B U.S.-listed robotics candidates surfaced:** 13 + 2 TIER 4 SEGMENT candidates (NOVT, SYNA) + 1 graduated-adjacent (ALGM).

**Genuine chokepoints (concentrated supplier base) for humanoid-critical components:**
- **#13 Humanoid Force/Torque Sensing** — VPG is the sole U.S. sub-$5B pure-play; 5-supplier global oligopoly
- **#14 Precision Actuators / Reducers / Roller Screws** — **NO U.S. SUB-$5B VEHICLE EXISTS** — most-concentrated chokepoint globally (Tokyo/Shanghai/Swiss-private locked); EMPTY status
- **#15 Humanoid Motor-Control & Sensor-Fusion Silicon** — fragmented chokepoint with multiple U.S. candidates (CEVA, INDI, AMBA, SYNA, ALGM)
- **#16 Humanoid Perception (LiDAR + Vision)** — fragmented post-Velodyne; OUST/AEVA/MVIS/LIDR all U.S. sub-$5B
- **#17 Tactile Skin + Haptic Feedback** — tactile-skin is white-space; haptic-feedback has IMMR + LINK at TIER 1 NANO

**Top 3 "next VPG" candidates:**
1. **ALNT ($1.08B)** — strongest pattern fit; motor / encoder / drive supplier publishing humanoid technical material into the chokepoint; lacks binding customer
2. **LINK ($74M)** — highest TIER 1 NANO asymmetry; FSR + haptic actuator pure-play; 2026 inflection guidance
3. **NOVT ($5.45-5.82B, TIER 4 SEGMENT)** — structural Tier 4 candidate; ATI Industrial Automation segment is the segment-level VPG analog

**Existing Archos universe with untagged robotics exposure:** **AMBA** only. (PDYN has humanoid software exposure but stays REJECTED per M&A pivot blind spot.)

**Proposed taxonomy additions (PROPOSED status, pending Sounding Board confirmation):**
- **#13 Humanoid Force/Torque Sensing** — ACTIVE, VPG sole U.S. pure-play
- **#14 Precision Actuators / Reducers / Roller Screws** — EMPTY, chokepoint without a vehicle
- **#15 Humanoid Motor-Control & Sensor-Fusion Silicon** — ACTIVE, fragmented (CEVA, INDI, AMBA, SYNA)
- **#16 Humanoid Perception (LiDAR + Vision)** — ACTIVE, fragmented (OUST, AEVA, MVIS, LIDR)
- **#17 Tactile Skin + Haptic Feedback** — PROPOSED, white-space on skin layer; haptic-feedback IMMR + LINK at TIER 1 NANO

**Is Physical AI investable today or still 6-12 months out?**

**Investable today, but with bifurcated structure:**

The thesis is investable today through **VPG (already running)**, **ALNT (next-VPG fast-track)**, **OUST (NVIDIA-qualified perception)**, **CEVA (IP-licensing chokepoint)**, **NOVT TIER 4 SEGMENT**, and **LINK / IMMR (TIER 1 NANO asymmetry tier)**. The H10-R bellwether-fire pattern is firing across multiple sub-chokepoints in real time — VPG Q1'26 8-K is the highest-conviction single signal in the lens, and ALNT's Apr-May 2026 supplier-self-positioning cluster is the second-highest.

**However, the most-concentrated chokepoint surface (reducers / roller screws / harmonic drives) is STRUCTURALLY NON-U.S.-INVESTABLE at the sub-$5B level.** The Tokyo / Shanghai / Swiss-private supplier base means U.S. small-cap investors cannot access the most-concentrated 35-40% of the humanoid BOM. This is the equivalent of the framework's chokepoint #2 HBM/HBF (SNDK graduated) or #14 Reducers situation — chokepoint exists, vehicle is foreign-only or already-graduated.

**The cleanest entry today is the SENSING and PERCEPTION sub-chokepoint stack, not the actuator stack.** This biases the Archos robotics lens toward the same sub-chokepoint position that VPG already validated — meaning the lens is essentially "VPG + close VPG-shaped peers" rather than a broad humanoid play. That's a feature, not a bug; the framework selects for what's investable, and what's investable in U.S. small-cap is sensing/perception/haptics, not actuation/reduction.

**Forward catalyst calendar (next 90 days):**
- **June 2026:** Tesla Optimus production milestone updates (10-Q); Figure 02 commercialization updates
- **July-August 2026:** Q2 earnings for VPG (5/2026 base shipped Q1 → 2x Q2 guide); ALNT Q2 segment data; OUST Q2 robotics mix disclosure; CEVA Physical AI licensing mix
- **Aug-Sep 2026:** Roze (SoftBank robotics) U.S. IPO — will be over $5B at print but S-1 mining surfaces named U.S. suppliers
- **Continuous:** any sub-$5B U.S.-listed 8-K Item 1.01 naming Tesla / Figure / Apptronik / Boston Dynamics / 1X / Unitree / Fourier / UBTECH as binding customer = H10-R PASS fire

---

## Sources

**Phase 1 — BOM mapping:**
- [Tesla Optimus Hardware: Actuators, Hands & Sensors (2026)](https://optimusk.blog/blog/tesla-optimus-hardware-specs/)
- [Tesla Optimus Supply Chain](https://optimusk.blog/blog/tesla-optimus-suppliers/)
- [Morgan Stanley: Humanoid Robot Market $5T by 2050](https://www.morganstanley.com/insights/articles/humanoid-robot-market-5-trillion-by-2050)
- [Goldman Sachs: Global market for humanoid robots](https://www.goldmansachs.com/insights/articles/the-global-market-for-robots-could-reach-38-billion-by-2035)
- [Mapping the Humanoid Robot Value Chain — MS Humanoid 100](https://advisor.morganstanley.com/john.howard/documents/field/j/jo/john-howard/The_Humanoid_100_-_Mapping_the_Humanoid_Robot_Value_Chain.pdf)
- [Harmonic Reducer for Humanoid Robot Market](https://www.congruencemarketinsights.com/report/harmonic-reducer-for-humanoid-robot-market)

**Phase 2 — EdgarTools filings:**
- [VPG 10-K FY2025 (filed 2026)](https://www.sec.gov/Archives/edgar/data/0001487952/000143774926005982/vpg20251231_10k.htm)
- [VPG Q1 2026 earnings 8-K](https://www.sec.gov/Archives/edgar/data/1487952/000143774926016226/ex_924354.htm)
- [VPG Q1 2026 transcript with humanoid commentary](https://www.fool.com/earnings/call-transcripts/2026/05/12/vpg-q1-2026-earnings-call-transcript/)
- [VPG Q1 2026 — Stock Titan (humanoid bookings + 4th developer)](https://www.stocktitan.net/news/VPG/vpg-reports-fiscal-2026-first-quarter-results-orders-exceed-100-nmtnfxrtgq4t.html)
- [CEVA 10-K (Physical AI leader claim)](https://www.sec.gov/Archives/edgar/data/1173489/000143774926006091/ceva20251231_10k.htm)
- [OUST 10-K (Physical AI leader claim + humanoid)](https://www.sec.gov/Archives/edgar/data/1816581/000162828026013313/oust-20251231.htm)
- [PDYN 10-K (embodied AI)](https://www.sec.gov/Archives/edgar/data/1826681/000119312526092443/pdyn-20251231.htm)
- [IMMR 10-K (haptic robotics IP)](https://www.sec.gov/Archives/edgar/data/1058811/000119312526102681/immr-20250430.htm)
- [LINK 10-K (FSR + haptic actuator)](https://www.sec.gov/Archives/edgar/data/828146/000110465926035244/link-20251231x10k.htm)
- [AEye 10-K (Physical AI lidar)](https://www.sec.gov/Archives/edgar/data/1818644/000143774926008858/lidr20251231_10k.htm)
- [INDI 8-K (Physical AI expansion via ams OSRAM acquisition)](https://www.sec.gov/Archives/edgar/data/1841925/000119312526216934/indi-ex99_1.htm)
- [T-Mobile 8-K (Figure AI F03 + 5G)](https://www.sec.gov/Archives/edgar/data/1283699/000128369926000062/tmus03312026ex991.htm)
- [FFAI 10-Q (first-time Robotics segment)](https://www.sec.gov/Archives/edgar/data/1805521/000162828026035138/ffie-20260331.htm)

**Phase 3 — Web sweep:**
- [Allient ALNT humanoid robotics motor whitepaper (April 23 2026)](https://www.roboticstomorrow.com/news/2026/04/23/allient-inc-publishes-new-whitepaper-on-motor-selection-for-humanoid-robotics-systems/26473)
- [Allient thermally-optimized humanoid joints webinar (May 19 2026)](https://www.roboticstomorrow.com/news/2026/05/19/allient-inc-to-present-at-upcoming-webinar-on-engineering-thermally-optimized-joints-for-humanoids/26590/)
- [Allient Robotics Summit 2026 advanced motion solutions](https://www.roboticstomorrow.com/news/2026/05/26/allient-inc-to-demonstrate-advanced-motion-solutions-at-robotics-summit-expo-2026/26616/)
- [VPG Q1 2026 humanoid commentary - AOL](https://www.aol.com/articles/vpg-q1-2026-earnings-call-141755000.html)
- [AEVA Q1 2026 commercial Physical AI deployments](https://www.businesswire.com/news/home/20260506436947/en/Aeva-Reports-First-Quarter-2026-Results)
- [OUST Q1 2026 Physical AI platform](https://pitchbook.com/profiles/company/170435-53)
- [Ouster Rev8 Native Color LiDAR - TechCrunch](https://techcrunch.com/2026/05/04/ousters-new-color-lidar-is-coming-to-replace-cameras/)
- [Novanta NOVT robotics + AI 2026 guidance raised](https://briefglance.com/articles/novanta-surges-on-strong-bookings-eyes-growth-in-ai-and-robotics)
- [SoftBank Roze IPO May 2026](https://money.usnews.com/investing/news/articles/2026-05-26/softbank-hires-banks-for-us-ipos-of-sb-energy-and-ai-robotics-spinoff-roze-sources-say)
- [Unitree 2026 STAR Market IPO (KraneShares)](https://kraneshares.com/a-complete-guide-to-unitree-robotics-2026-ipo-why-it-matters-for-star-market-etf-kstr-humanoid-robotics-etf-koid/)

**Phase 3 — ETF holdings:**
- [ROBO ETF holdings](https://www.stockanalysis.com/etf/robo/holdings/)
- [BOTZ ETF holdings](https://www.stockanalysis.com/etf/botz/holdings/)
- [THNQ ETF holdings](https://www.stockanalysis.com/etf/thnq/holdings/)
- [ROBT ETF holdings](https://www.stockanalysis.com/etf/robt/holdings/)
- [ARKQ ETF holdings](https://www.stockanalysis.com/etf/arkq/holdings/)
- [KOID humanoid robotics ETF](https://kraneshares.com/koid/)

**Real-time price verification (2026-05-27):**
- [VPG $1.72B - stockanalysis](https://stockanalysis.com/stocks/vpg/)
- [ALNT $1.08B - marketbeat](https://www.marketbeat.com/stocks/NASDAQ/ALNT/)
- [OUST $2.83B - stockanalysis](https://stockanalysis.com/stocks/oust/)
- [AEVA $0.84-1.70B range - macrotrends](https://www.macrotrends.net/stocks/charts/AEVA/aeva-technologies/market-cap)
- [IMMR $216M - WallStreetZen](https://www.wallstreetzen.com/stocks/us/nasdaq/immr)
- [NOVT $5.45-5.82B - stockanalysis](https://stockanalysis.com/stocks/novt/)
- [AMBA $3.85-4.10B - macrotrends](https://www.macrotrends.net/stocks/charts/AMBA/ambarella/market-cap)
- [CEVA $1.09B - stockanalysis](https://stockanalysis.com/stocks/ceva/market-cap/)
- [INDI $1.00B - public.com](https://public.com/stocks/indi/market-cap)
- [AMPX $2.17-2.27B - stockanalysis](https://stockanalysis.com/stocks/ampx/)
- [LINK $74M - WallStreetZen](https://www.wallstreetzen.com/stocks/us/nasdaq/link)
- [SYNA $5.55-5.71B - stockanalysis](https://stockanalysis.com/stocks/syna/)
- [VTIX $105M - financecharts](https://www.financecharts.com/stocks/VTIX/summary/market-cap)
- [MVIS $217M - companiesmarketcap](https://companiesmarketcap.com/microvision/marketcap/)
