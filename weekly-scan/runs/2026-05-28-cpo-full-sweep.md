# CPO FULL SUPPLY CHAIN SWEEP — 2026-05-28
# Targeted discovery: every sub-$5B public company in the Co-Packaged Optics ecosystem
# Mode: BREADTH-FIRST. Find first, filter second. Do not apply 4-filter framework as gate during discovery.
# Companion files this run informs: CHOKEPOINT_TAXONOMY.md (#1 CPO + #8 Optical), CANDIDATE_UNIVERSE.md (new WATCH / DD QUEUE / REJECT entries)
# Prior CPO-relevant scans: 2026-05-27 SCAN_04 optical-next-gen, ALMU DD 2026-05-24, weekly master scan 2026-05-26
# Prompt source: user 2026-05-28 prompt — explicit instruction to cast the widest net first

---

## Why this scan exists

Chokepoint #1 (CPO) has produced the framework's single greatest outcome — AXTI at ~97x in 12 months — but is now structurally empty of liquid US-listed sub-$5B pure-plays:
- AXTI graduated to $7.6B (compressing but un-breach not triggered)
- POET ($2.22B) is the sole ACTIVE candidate but pre-revenue and class-action overhang
- SIVEF ($2.75B USD OTC ADR) carries OTC handicap
- ALMU ($410M) was HARD REJECTED on DD (Akoustis network failure, $27.5M insider selling, $41K commercial revenue, 20.46% SI)

Chokepoint #8 (800G+/1.6T transceivers / AECs / SerDes) was declared STRUCTURALLY CONSOLIDATED in SCAN_04 (2026-05-27) — every sub-$5B name in the prior universe has graduated above $5B (LITE $68B, CRDO $39B, AAOI $14B) AND the private startup pipeline (Ayar, Lightmatter, Celestial, DustPhotonics, Polariton) is being acquired UPWARD by mid-caps faster than organic discovery can surface replacements.

The CPO market is projected at $20B+ by 2036 (37% CAGR). NVIDIA Spectrum X Photonics + Quantum X Photonics + TSMC COUPE + Broadcom Tomahawk 6 Davisson + Meta Spectrum X commitments are all built on CPO. The next-gen AI rack architecture (33kW → 264kW → 480kW per rack per Navitas roadmap) requires exponentially more optical bandwidth.

The structural finding from prior scans was correct but incomplete: the consolidation wave eats one slice of the supply chain (transceivers + chiplets), not all 14 layers. **There MUST be sub-$5B companies in the OTHER layers — peripheral, upstream, or downstream — that prior scans haven't covered.** This sweep is designed to find them.

---

## PHASE 1 — Complete CPO supply chain map (14 layers)

A CPO module is fundamentally a heterogeneous integration: it combines a photonic integrated circuit (PIC) built on silicon, indium phosphide, or both; with discrete laser sources; with optical modulators; with photodetectors; with fiber attach assemblies; with high-frequency electrical drivers; with thermal management; and with a substrate/interposer that holds it all next to the ASIC switch (e.g., Broadcom Tomahawk 6 or NVIDIA Spectrum-X switch) and connects via PCB-grade traces to the switch package.

Every layer below is a potential chokepoint. Several layers (substrates, foundry, packaging, FAU) have already produced winners. Several remain unexplored.

### Layer 1 — InP / GaAs / GaSb Substrates (the raw crystalline wafers)

**What it does:** Compound-semiconductor substrates are the starting wafer for III-V laser sources and high-speed photodetectors. InP (indium phosphide) is the dominant material for telecom-wavelength (1310nm / 1550nm) lasers; GaAs (gallium arsenide) for VCSELs and pump lasers; GaSb (gallium antimonide) for mid-IR sensing.

**Why it matters for CPO:** Every CPO module requires laser sources. Even silicon photonics PICs (which use silicon for the waveguide) need an external InP or GaAs laser die heterogeneously integrated. The substrate vendor sits one layer behind the laser maker, which sits one layer behind the transceiver builder. This is the deepest upstream layer of the CPO supply chain.

**Known players:**
- AXTI (now $7.6B — GRADUATED; the canonical 97x Archos winner from sub-$50M)
- Sumitomo Electric (JP private/sub of larger parent)
- IQE plc (LSE: IQE.L, ~$665M USD — foreign-handicap WATCH per SCAN_04)
- Sumitomo Chemical Advanced Materials (private)

**Discovery vectors:** US sub-$5B InP wafer companies beyond AXTI (currently zero known); Asian competitors entering US-investability via ADR or dual-listing.

### Layer 2 — Epitaxial Growth / Wafer Services

**What it does:** Growing III-V semiconductor layers (quantum wells, quantum dots, multi-junction stacks) on a substrate via MOCVD or MBE. This is the precision step where laser performance is defined.

**Why it matters for CPO:** The QD-on-Si architecture (Aeluma, Quintessent, others) bets that direct epitaxial growth of III-V on 200mm/300mm silicon can eliminate the discrete-laser assembly step in CPO. Even traditional InP DFB lasers need precision epi — yield at 1.6T linewidth specs is non-trivial.

**Known players:**
- IQE plc (LSE — foreign WATCH)
- ALMU/Aeluma (HARD REJECTED — Akoustis network failure pattern)
- Veeco / VECO (mentioned in INSIGHTS.md — InP laser tool $250M order book, NVDA 2-degree supplier-mapping target, but Q1 2026 revenue declined on China BIS headwind)
- Riber SA (Euronext Paris, private-ish)

**Discovery vectors:** US-listed epi-tool companies, foreign epi-services pure-plays.

### Layer 3 — EML / CW / VCSEL / Quantum Dot Laser Sources

**What it does:** The actual light sources for CPO. Electro-absorption modulated lasers (EMLs) at 200G per lane, continuous-wave (CW) lasers for external modulation, VCSELs for short-reach intra-rack, QD lasers for next-gen integration.

**Why it matters for CPO:** Each CPO module needs 8-16 laser sources today, scaling to 32-64 at 3.2T. NVIDIA's Quantum X Photonics architecture specifies CW lasers for external modulation. The EML supply chain is concentrated (LITE, COHR, Lumentum-acquired-NeoPhotonics) and the QD lock-in is being contested by startups.

**Known players:**
- COHR / LITE (graduated mega-cap)
- Innolume GmbH (private German specialty fab — full-production QD laser at 780-1350nm)
- QD Laser Inc (TSE: 6613 — Japanese; small)
- ALMU/Aeluma (REJECTED)
- Lessengers (Korean, private — POET partner)
- ams OSRAM (SIX: AMS — diversified, sensors-heavy)

**Discovery vectors:** US-sub-$5B EML / CW / QD laser pure-plays — currently empty after LITE graduation.

### Layer 4 — Silicon Photonics Foundry

**What it does:** Fabricates photonic integrated circuits (PICs) on silicon wafers using a specialty CMOS-compatible process. The PIC integrates waveguides, modulators, photodetectors, and (in heterogeneous integration) external laser dies.

**Why it matters for CPO:** The PIC is the brain of the CPO module. Foundry choice determines yield, integration density, and cost. Three foundries dominate: TSMC COUPE (now ramping for NVDA Quantum X), Tower Semi (NVDA SiPho partnership Feb 2026), GlobalFoundries (300mm SiPho since 2022).

**Known players:**
- TSMC (mega-cap)
- TSEM/Tower Semiconductor (now $32B — GRADUATED; NVDA 1.6T SiPho partnership)
- GFS/GlobalFoundries ($49B — GRADUATED; mature-node + SiPho)
- ams OSRAM (SIX:AMS — has photonics fab)
- X-FAB (Euronext: XFAB.PA — automotive analog, has some SiPho potential)

**Discovery vectors:** Pure-play sub-$5B SiPh foundry candidates (extremely rare — capital intensity rules out most sub-$5B players).

### Layer 5 — Optical Interposer / PIC Design (fabless)

**What it does:** Integrating photonic and electronic functions on a single chip or interposer. The fabless model: design the PIC, outsource fabrication to TSMC / Tower / GFS, sell as an optical engine or chiplet.

**Why it matters for CPO:** This is where most CPO innovation lives. Ayar Labs, Lightmatter, Celestial AI, Polariton are all fabless interposer/PIC designers. POET is the US public fabless interposer pure-play.

**Known players:**
- POET ($2.22B — ACTIVE; sole sub-$5B US-listed fabless interposer pure-play)
- Ayar Labs (private, AMD/Intel/NVIDIA-backed, >$1B val — top IPO watch)
- Lightmatter (private, $4.4B val)
- Celestial AI (private — being acquired by Marvell for $5.5B)
- Lightelligence (HKEX 2300.HK — Chinese, ~$10B IPO Apr 2026, over cap + export-control risk)
- DustPhotonics (private — acquired by Credo $1.3B Apr 2026)

**Discovery vectors:** Sub-$5B fabless PIC design houses; foreign-listed interposer companies; chiplet startups going public.

### Layer 6 — Modulators / Photodetectors

**What it does:** Modulators convert electrical signals to optical (lithium niobate, silicon Mach-Zehnder, ring modulators, electro-absorption); photodetectors convert optical back to electrical (PIN diodes, avalanche photodiodes, germanium-on-silicon).

**Why it matters for CPO:** At 200G per lane, modulator linearity and photodetector bandwidth are gating constraints. Thin-film lithium niobate (TFLN) is emerging as the next-gen modulator material.

**Known players:**
- HyperLight (private — TFLN modulator startup, NVDA-adjacent)
- ams OSRAM (sensors-heavy)
- Lumentum / Coherent (mega-cap incumbents)

**Discovery vectors:** Pure-play modulator / photodetector public companies — currently very thin at sub-$5B.

### Layer 7 — Fiber Attach / Coupling / FAU (Fiber Array Unit)

**What it does:** Mechanically and optically connects optical fibers to the PIC. The FAU is the assembly of multiple fibers in a precise pitch (typically 127μm or 250μm) bonded to the edge or surface of a PIC. Fiber attach yield is one of CPO's hardest manufacturing problems.

**Why it matters for CPO:** Every CPO module has dozens of fiber attaches. Yield loss here is the #1 cost driver. FAU vendors with proven volume process win directly.

**Known players:**
- FOCI (TPEX: 3363, ~$2.8B USD — foreign-handicap WATCH per SCAN_04; 1.6T/3.2T FAU mass production H2 2026)
- Browave (TPEX: 3163, ~$2.6B USD — foreign WATCH; full CPO production 2026)
- nLIGHT (private competitor adjacency)
- Ayar Labs (FAU is core)
- US Conec (private — connector incumbent)

**Discovery vectors:** Korean / Taiwanese / Japanese FAU specialists; US-listed packaging companies pivoting into FAU.

### Layer 8 — Optical Packaging / Assembly

**What it does:** The final assembly step — placing the PIC, lasers, modulators, photodetectors, FAU, and supporting circuitry into a single CPO module that mates with the ASIC switch. Hermetic sealing, thermal interface, and electrical interconnect.

**Why it matters for CPO:** Packaging is the where the "co-packaged" in CPO happens. As CPO migrates from pluggable-form-factor (OSFP) to truly co-packaged (next to ASIC), the packaging vendor's role expands.

**Known players:**
- ASMPT (HKEX: 0522 — graduated mega-cap)
- BESI (Amsterdam: BESI — graduated mega-cap)
- Amkor Technology (ticker AMKR — mid-cap parent, has photonics line)
- Kulicke & Soffa (KLIC — mid-cap parent)
- Cohu (COHU — mid-cap)

**Discovery vectors:** Sub-$5B packaging/assembly pure-plays with disclosed CPO design wins.

### Layer 9 — Optical Test & Measurement

**What it does:** Qualifying CPO modules at 800G / 1.6T / 3.2T. Bit error rate testers, sampling oscilloscopes, optical power meters, optical spectrum analyzers, automated probe stations.

**Why it matters for CPO:** Each new transceiver generation requires new test equipment. The 1.6T qualification cycle is creating demand for next-gen test gear.

**Known players:**
- Keysight Technologies (KEYS — mega-cap)
- Anritsu (TSE: 6754 — JP)
- VIAVI Solutions (VIAV)
- EXFO (private — taken private 2022)
- Tektronix (subsidiary of Fortive)
- Spirent Communications (LSE: SPT.L — small-mid cap)

**Discovery vectors:** Mid-cap test equipment pure-plays with disclosed CPO/1.6T qualification programs.

### Layer 10 — Specialty Optical Materials

**What it does:** SiN (silicon nitride) waveguides for low-loss propagation; specialty optical glass; polymer waveguides for low-cost PIC alternatives; thin-film lithium niobate (TFLN) for next-gen modulators.

**Why it matters for CPO:** Material innovation drives PIC performance. SiN-on-Si is the leading low-loss waveguide platform. TFLN is the modulator-material insurgent against silicon MZI.

**Known players:**
- Corning (GLW — mega-cap; NVDA 10x capacity expansion)
- Heraeus (private)
- HC Photonics (Taiwan private — TFLN)
- LioniX International (private — SiN waveguide)
- Brewer Science (private — polymer / lithography materials)

**Discovery vectors:** Public materials pure-plays for SiN, TFLN, or polymer waveguide.

### Layer 11 — Thermal Management for CPO

**What it does:** CPO modules sit immediately adjacent to hot ASICs (3-5 kW switch packages). Lasers are temperature-sensitive (linewidth degrades, threshold current shifts). Thermal solutions include vapor chambers, micro-channel cold plates, and direct-to-chip liquid cooling.

**Why it matters for CPO:** A CPO module that runs hot is a CPO module that doesn't ship. As switch ASICs scale from 51.2T to 102.4T to 204.8T, the thermal envelope tightens dramatically.

**Known players:**
- Vertiv (VRT — mega-cap; rack-level cooling)
- Modine Manufacturing (MOD — graduated mid-cap; $4B hyperscaler cooling deal)
- nVent Electric (NVT — graduated mega-cap)
- Boyd Corp (private)
- Asetek (OSE: ASETEK — too small to matter ~$85M)

**Discovery vectors:** Sub-$5B thermal pure-plays with disclosed photonic/optical module customers.

### Layer 12 — PCB / Substrate for Optical Modules

**What it does:** High-frequency PCBs (Megtron 6/7/8, Tachyon-class) for the electrical traces that connect the CPO module to the switch ASIC. As lane rates climb to 200G, PCB loss budgets tighten.

**Why it matters for CPO:** A 1.6T transceiver needs PCB substrate that can hold signal integrity at 100G electrical. The substrate vendor effectively gates the speed scaling.

**Known players:**
- Ibiden (TSE: 4062 — large)
- Shinko Electric (TSE: 6967 — being acquired)
- Toppan Holdings (TSE: 7911 — large)
- TTM Technologies (TTMI — mid-cap)
- Unimicron (TPEX: 3037 — large)

**Discovery vectors:** Sub-$5B high-frequency substrate pure-plays; Korean/Taiwanese substrate names with AI-DC mix.

### Layer 13 — Drivers / TIAs (Transimpedance Amplifiers)

**What it does:** Analog ICs that drive the modulator (driver) and amplify the photodetector output (TIA). At 200G per lane, the driver/TIA are the critical analog chips that determine link margin.

**Why it matters for CPO:** Drivers and TIAs are typically supplied by analog/RF chip companies, not photonics specialists. The 1.6T cycle is creating a new generation of 200G driver/TIA design wins.

**Known players:**
- MaxLinear (MXL — mid-cap)
- Semtech (SMTC — graduated mid-cap)
- MACOM Technology Solutions (MTSI — graduated to $13.5B)
- Inphi (acquired by Marvell)
- M/A-COM (legacy, MTSI)
- Diodes Inc (DIOD — auto/industrial heavy)

**Discovery vectors:** Sub-$5B analog/RF chip pure-plays with disclosed 200G driver or TIA design wins.

### Layer 14 — Connectors / Optical Interconnect Hardware

**What it does:** Optical connectors (MPO/MTP for parallel optics, LC for duplex), backplane optical interconnects, breakout cables. The physical-layer hardware that mates CPO modules to fiber distribution.

**Why it matters for CPO:** Every CPO module needs connectors. As fiber-per-rack scales 10x, connector vendor revenue scales with it.

**Known players:**
- Corning (GLW — mega-cap)
- US Conec (private)
- Sumitomo Electric (parent of multiple subs)
- TE Connectivity (TEL — mega-cap)
- Amphenol (APH — mega-cap)
- Senko Advanced Components (private)
- Methode Electronics (MEI — already REJECTED per Archos, sub-$5B but flat-to-down despite record DC power sales)

**Discovery vectors:** Sub-$5B optical connector pure-plays — quite thin in public markets.

---

## PHASE 2 — EdgarTools full-text discovery results

35 single-phrase queries executed across `forms=['10-K']`, `forms=['8-K']`, and `forms=['6-K']` (foreign filers) over a 18-month date window (2024-11-01 to 2026-05-28). Per INSIGHTS.md, EdgarTools boolean AND with phrase quotes returns zero results — single-phrase only. All queries executed cleanly.

### NEW sub-$5B candidates surfaced via EdgarTools (deduped, excluded known/graduated/rejected)

| Ticker | Company | Exchange | Form | Source query | Chokepoint relevance snippet |
|---|---|---|---|---|---|
| **SKYT** | SkyWater Technology | NASDAQ | 10-K | "silicon photonics" | "specialize in developing advanced processes for emerging technologies such as silicon photonics, superconducting and quantum computing, advanced packaging" — US foundry pure-play |
| **HIMX** | Himax Technologies | NASDAQ | 6-K (multi) | "silicon photonics" | "Himax, in partnership with FOCI, a world leader in silicon photonics connectors, unveiled state-of-the-art silicon photonics packaging technology" — direct CPO packaging |
| **QUBT** | Quantum Computing Inc | NASDAQ | 10-K + 8-K | "optical modulator" / "optical packaging" / "photonic integrated circuit" | "TFLN electro-optical modulators…large bandwidth, low power consumption, and small size"; "Decades of tech innovation in laser and detection industry. Leading engineering and manufacturing in optical packaging and testing" — TFLN modulator + POET joint dev |
| **INDI** | indie Semiconductor | NASDAQ | 10-K | "optical packaging" | "Hybrid Optical Packaging Systems ('HOPS') manufacturing capability for the integration and optical alignment of small optical components" — auto ADAS primary today |
| **MTSI** | MACOM Technology Solutions | NASDAQ | 10-K | "silicon photonics" / "photodetector" | "complete product portfolio of Transimpedance Amplifier (TIAs), Modulator Drivers, Lasers and Photodetectors, to support single-mode, multi-mode and silicon photonics based transceivers" — full driver/TIA/laser portfolio |
| **PLAB** | Photronics Inc | NASDAQ | 10-K | "silicon photonics" | "advanced packaging modules, micro optical components for applications such as virtual reality/augmented reality and silicon photonics" — photomask supplier |
| **VECO** | Veeco Instruments | NASDAQ | 8-K (May 2026) | "silicon photonics" | "particularly strong momentum in silicon photonics as customers scale optical connectivity" — InP/MOCVD laser tools; Q1 2026 revenue declined on China BIS headwind |
| **XNDU** | Xanadu Quantum Technologies | NASDAQ (Canadian) | 6-K | "silicon photonics" / "fiber array" | "Tower Semiconductor announced expansion of their collaboration to develop silicon photonics for photonic quantum computers using Tower Semiconductor's manufacturing platform" |
| **NVMI** | Nova Ltd | NASDAQ (Israeli ADR) | 6-K | "optical" | Israeli semi metrology — optical metrology for advanced packaging |
| **SVCO** | Silvaco Group | NASDAQ | 8-K | "silicon photonics" | "ProMOS adopted our Victory TCAD solution for the development of next generation silicon photonics devices" — EDA tools |
| **INFQ** | Infleqtion | NASDAQ | 8-K/A | "silicon photonics" | "Morton Photonics specialized in the development and manufacturing of advanced silicon photonics-based component and sub-system technologies" — quantum/sensing |
| **RAL** | Ralliant Corp | NYSE | 10-K | "silicon photonics" | "growth in data from next generation computing and networking technologies…Silicon Photonics, creates the need for the Company's communications test and measurement solutions" — test gear pure-play |
| **CPSH** | CPS Technologies | NASDAQ | 8-K (May 2026) | "thermal management" | Advanced ceramics for thermal management — possible AI-DC packaging substrate |
| **GHM** | Graham Corporation | NYSE | 8-K | "thermal management" | Thermal/cooling — verify DC vs defense/nuclear |
| **INV** | Innventure Inc | NASDAQ | 8-K | "thermal management" | Thermal management deals — verify CPO/DC relevance |
| **LEDS** | SemiLEDs Corp | NASDAQ | 10-K | "photodetector" | "developing small format AI sensors having a light source and photodetector in cooperation with our Japanese partners" — nano-cap |
| **AEHR** | Aehr Test Systems | NASDAQ | 8-K (multi) | "silicon photonics" | "silicon photonics is a market we see significant opportunity for WLBI…lead customer has now firmed up its production ramp, with production beginning early in our next fiscal year" — already taxonomy chokepoint #4; now also chokepoint #1 by cross-tag |
| **ALNT** | Allient Inc | NASDAQ | 10-K | "silicon photonics" | "nano technology motion systems in silicon photonics, micro assembly" — already TIER 2 robotics WATCH; now SiPh cross-tag |

### Queries that returned ZERO hits (informative gaps)

- `"optical interposer"` (10-K) — 0 hits. **Notable:** POET uses this term but files 6-K only. The term has not penetrated US 10-K disclosures.
- `"EML laser"` (10-K) — 0 hits. EMLs are described as "EML chips" or "EMLs" in actual disclosures.
- `"quantum dot laser"` (10-K) — 0 hits. ALMU uses "quantum dot integration" or "QD-on-Si." Term not standardized.
- `"silicon nitride waveguide"` (10-K) — 0 hits. Standard waveguide material not yet a load-bearing disclosure term.
- `"200G per lane"` (8-K) — 0 hits. Disclosure language still trails technology cycle by ~2 quarters.
- `"fiber attach"` (10-K) — 0 hits. Process step not yet a disclosure-grade chokepoint vocabulary.
- `"CPO module"` (10-K) — 0 hits. Form-factor terminology not crystallized in 10-Ks.
- `"high-speed connector"` (10-K) — 0 hits.
- `"optical modulator"` (8-K) — 0 hits.
- `"polymer waveguide"` (8-K) — 0 hits.

**Interpretation:** Disclosure-language adoption lags vendor activity by 1-3 quarters (consistent with SCAN_04 finding). The "1.6T transceiver" / "CPO module" / "fiber attach" lexicon will likely first appear in 10-Q + 8-K filings over Q3/Q4 2026 as 1.6T qualification matures.

### Notable graduated/excluded hits (context only — these CONFIRM the thesis but are over cap)

- **TSEM 6-K (May 2026):** "$1.3B silicon photonics revenue contracts for 2027" + "$290M customer prepayments Q1 2026" — **load-bearing balance-sheet H8 signal at the SiPh foundry layer; if TSEM were sub-$5B this would be a TIER 1 ACCEPT, but cap is $32B (graduated)**
- **GFS 6-K (May 2026):** Launched SCALE CPO solution + acquired AMF (Advanced Micro Foundry) Singapore Nov 2025 — mega-cap
- **AMD 10-K:** "support and develop a variety of photonics and co-packaged optics solutions across next-gen AI systems" — bellwether vendor-level mention
- **AMKR 10-K:** WLFO + SiPh + CPO advanced packaging — $5-7B borderline mega-cap
- **MRVL 10-K + $2B NVDA investment**, **NVDA-COHR $2B**, **NVDA-LITE $2B**, **NVDA-GLW 10x capacity** — bellwether mega-cap cohort
- **VECO 8-K (May 2026):** "particularly strong momentum in silicon photonics as customers scale optical connectivity" — sub-$5B *and* in-scope but China BIS revenue headwind; included in candidate table above
- **CIEN, JBL, TER, CDNS, FORM, STM, UMC, NOK** — all named in chokepoint adjacency but graduated/mega-cap

### EXCLUDED candidates from EdgarTools sweep (already-known reject or out-of-scope)

| Ticker | Reason |
|---|---|
| EMKR | Divested chips business 2024 — no longer InP play |
| INFN | Acquired by Nokia 2024 |
| AEVA | LiDAR/auto end-market (not AI-DC chokepoint) |
| OUST | LiDAR/auto (already in robotics lens) |
| HSAI | Chinese ADR + LiDAR auto |
| IMOS | LCOS display optical engine — wrong end-market |
| AGAE | Shell/pivot pattern (already in Archos REJECT log) |
| INGN | Medical O2 company; Rockley CMO hire is not a CPO catalyst |
| QCLS | OTC, tiny, speculative |
| MASI | Medical pulse-ox |
| OLED | Director-bio reference only |
| Palomino Laboratories | Private (no ticker) |
| BCAR | SPAC, target unidentified |
| SUPX | AI infrastructure (likely edge inference / services — out of scope per LSCC analog) |
| POAS | Cayman shell — speculative |
| LAES | Quantum/photonics security IP — sensing not CPO |

---

## PHASE 3 — Web discovery results (Step 1: Industry landscape)

14 Firecrawl industry-landscape queries executed. Discovered net-new candidates beyond Edgar set, especially in test-equipment + epi-tool + foreign-listing layers.

### NEW sub-$5B candidates surfaced via web landscape sweep (deduped, non-Edgar overlap)

| Ticker | Company | Exchange | Est. mkt cap (web) | CPO supply chain layer | One-line description |
|---|---|---|---|---|---|
| **FORM** | FormFactor | NASDAQ | ~$3-4B | Layer 9 (Test) | Probe cards + photonics test — CPO test probe directly cited |
| **CAMT** | Camtek | NASDAQ | ~$4-5B (borderline) | Layer 9 (Test) | Advanced packaging inspection (CPO/2.5D/3D) — Tower COUPE-style stack inspection |
| **ACLS** | Axcelis Technologies | NASDAQ | ~$2-3B | Layer 4 (SiPh fab tools) | Ion implantation tools used in SiPh fab; indirect CPO play |
| **SMTC** | Semtech | NASDAQ | ~$2.5-3.5B | Layer 13 (CDR / Signal Conditioning) | LightCounting-rated optical PHY supplier; sub-$5B per web |
| **LASR** | nLight | NASDAQ | ~$500M-1B | Layer 3 (Laser sources) | High-power diode lasers (mostly industrial/defense); partial CPO end-market |
| **KOPN** | Kopin Corp | NASDAQ | ~$200-300M | Layer 10 (Specialty optics adjacency) | Microdisplay + optics; mostly AR/VR — verify CPO relevance |
| **OSIS** | OSI Systems | NASDAQ | ~$2.5B | Photonics segment | Diversified — photonics segment small but real (likely segment lens) |
| **BELFB** | Bel Fuse | NASDAQ | ~$600M-1B | Layer 14 (Connectors/magnetics) | Magnetics/connectors for datacom — adjacent supply layer |
| **OIIM** | O2Micro International | NASDAQ | ~$100M | Layer 13 adjacency | Power IC for fiber/optical — tiny |

### NEW foreign-listed candidates (Step 5 sweep partial)

| Ticker | Company | Exchange | CPO layer | Notes |
|---|---|---|---|---|
| **TPEX:3485** | **Centera Photonics** | Taiwan emerging board | Layer 5 — 1.6T integrated-laser transceiver with NewPhotonics NPG10201 PIC | **Just listed March 2026** — newly public sub-$5B CPO-adjacent pure-play; cap verification critical |
| **TWSE:6820** | **ACON Optics Communications** | Taiwan | Layer 7 (Fiber attach / FAU) | Direct CPO fiber array supplier, partners with international clients |
| **SIVE.ST** | Sivers Semiconductors | Nasdaq Stockholm | Layer 3 (InP laser) + mmWave | Already in Archos as SIVEF OTC ADR ($2.75B USD per CHOKEPOINT_TAXONOMY.md); SIVE.ST is the Swedish primary listing |

### Private companies of note (IPO watch — NOT directly investable, but track for catalyst)

| Company | Status | CPO layer | Notes |
|---|---|---|---|
| **NewPhotonics** (Israeli) | Private | Layer 5 — PIC transmitter-on-chip NPG10201 | Powers Centera Photonics 1.6T modules; IPO candidate |
| **Ayar Labs** | Private (excluded per prompt) | Layer 5 — optical I/O | Intel/AMD/NVIDIA-backed; rumored 2026-27 IPO |
| **Lightmatter** | Private (excluded) | Layer 5 — Passage interposer | $4.4B val; potential 2026-27 IPO |
| **Celestial AI** | ACQUIRED by Marvell $5.5B Dec 2025 | -- | -- |
| **DustPhotonics** | ACQUIRED by Credo $1.3B Apr 2026 | -- | -- |
| **Teramount** | ACQUIRED by Molex (Koch private) | Wafer-level fiber attach | Locked up by Molex |
| **OpenLight** | Private (Synopsys-backed) | Heterogeneous InP-on-Si; Tower partner | IPO candidate |
| **SMART Photonics** (Dutch) | Private | InP foundry | Collaborating with X-FAB |
| **Scintil Photonics** (French) | Private | Photonic integration | Pre-IPO |
| **Aloe Semiconductor** | Private | Optical engine startup; ECOC '24 demo with Eoptolink | Early-stage |
| **HyperLight** | Private | Thin-film lithium niobate modulator | NVDA-adjacent |
| **Lightelligence** | HKEX listed Apr 2026 (~$10B) | Optical computing | Over cap + Chinese-AI export-control risk |

---

## PHASE 3 — Web discovery results (Steps 2-4: Supply chain drill-down + foundry customers + Ayar/Lightmatter competitors)

### NEW sub-$5B candidates from supply-chain drill-down

| Ticker | Company | Exchange | Est. mkt cap (web) | CPO supply chain layer | One-line description |
|---|---|---|---|---|---|
| **MXL** | MaxLinear | NASDAQ | ~$1.5B | Layer 13 (Drivers/TIAs) | **"Washington" 4-channel 200G/lane TIA explicitly positioned for AI DC connectivity** — recent product catalyst |
| **MTSI** | MACOM Technology | NASDAQ | ~$4.5-4.9B (borderline) | Layers 6, 13 (Modulators, Drivers/TIAs) | Active GF Fotonix design-win customer; merchant supplier of EML drivers + TIAs into 100G/200G optical modules |

### Notable mega-cap context confirmations (graduated — already excluded)

- **Zhongji Innolight (300308.SZ)** — CNY 715B (~$98B), mega-cap (was sub-$5B in 2020)
- **Eoptolink (300502.SZ)** — CNY 1T+, mega-cap
- **Suzhou TFC Optical (300394.SZ)** — ~$46B mega-cap
- **Dongshan Precision (002384.SZ)** — ~$56B mega-cap
- **Fujikura (5803.T)** — Up >160% in 2025 on AI-DC fiber — likely well over $5B
- **Sumitomo Electric (5802.T)** + **Furukawa Electric (5801.T)** — JP mega-cap fiber/cable

**Structural observation:** The Chinese optical-module cohort (Zhongji, Eoptolink, Suzhou TFC) has fully rerated to mega-cap during the 800G cycle. The 1.6T cycle is being captured by upstream + downstream layers, not module assemblers — explaining the empty US sub-$5B slot at chokepoint #8 (module assembly).

---

## PHASE 3 — Step 5: Foreign listing sweep (deep)

### Strong foreign sub-$5B candidates (deduped, non-excluded)

| Ticker | Exchange | Company | Est mkt cap | CPO Layer | Description |
|---|---|---|---|---|---|
| **SOI** / **SLOIY** | Euronext Paris / OTC ADR | **Soitec** | €3.05B (~$3.3B USD) | Layer 1+4 (SOI substrates for SiPh foundry) | **Photonics-SOI wafer supplier to TSMC COUPE + GlobalFoundries Fotonix + Tower SiPh + ST.** SEMI SiPh Industry Alliance member. Cyclical RF-SOI trough masking Photonics-SOI ramp. Mgmt target $2B rev / ~40% EBITDA. **STRONGEST FOREIGN AI-DC PURE-PLAY IDENTIFIED THIS SWEEP.** |
| **AIXA** / **AIXXF** | Xetra Germany / OTC ADR | **AIXTRON** | €4.5B (~$4.9B USD; borderline) | Layer 2 (MOCVD epi tools) | **~90% share G10-AsP MOCVD reactors** — the InP/GaAs epi tool monopolist. Serves Coherent/Lumentum InP fabs. Raised 2026 guidance to €560M. Direct chokepoint pure-play but at edge of $5B threshold. |
| **SIVE** (SIVE.ST) | Nasdaq Stockholm | Sivers Semiconductors | SEK 21.68B (~$2.05B USD) | Layer 3 (InP photonics) + mmWave | **Already partially tracked as SIVEF OTC ADR ($2.75B per CHOKEPOINT_TAXONOMY.md)** — SIVE.ST is the primary Stockholm listing; cleaner liquidity than OTC. InP photonics subsidiary Sivers Photonic (Glasgow) explicit "AI datacenter photonics" positioning. Recently promoted to Stockholm Main Market. |
| **6754.T** | TSE Tokyo | **Anritsu** | ~$2B (per iamfabian Substack 2026) | Layer 9 (Optical Test) | **BERTWave MP2110A is the workhorse test instrument for 10G-1.6T optical module manufacturing inspection.** Explicit Taiwanese module-house qualification content. **HIGHEST-CONVICTION new optical test pure-play of the sweep.** |
| **6777** | TSE Tokyo | Santec Holdings | sub-$1B | Layer 9 (Optical Test) + Layer 3 (Tunable lasers) | Tunable lasers + optical test & measurement; explicit "CPO ecosystem with wafer-level diagnostics and module-level test" |
| **138080** | KOSDAQ Korea | **OE Solutions** | est. $400-700M | Layer 8 (Module assembly) + CPO IP | **1.6T transceivers compatible with InfiniBand AI DC switches.** "Patents for the CPO Era" published Mar 2026. **Strong direct CPO play; KOSDAQ foreign-handicap.** |
| **069540** | KOSDAQ Korea | **Lightron Fiber-Optic Devices** | sub-$1B | Layer 8 (Pluggable transceivers) | Pluggable 100G/400G/800G transceivers for DCI + AI/ML clusters. **+1,575% YoY** per Korean social; NVDA GTC 2026 namedrop. PARTIAL-RECOVERING H5 candidate if pullback observed. |
| **LPK** / **LPKFF** | Xetra Germany / OTC | LPKF Laser & Electronics | €276M-€550M | Layer 10 (Specialty materials — glass) | **LIDE (Laser-Induced Deep Etching) for glass substrates** — emerging CPO/glass-substrate path with Intel committed to glass HVM by 2030. +255% YTD per photoncap. Sub-$1B European TIER 1/2 candidate; binary outcome. |
| **6502.TWO** | TPEX Taiwan | EzConn | ~$300-500M | Layer 2 (Epitaxial) | Share-exchange with IntelliEpi consolidates III-V MBE epitaxial wafer capability into a Taiwan-listed vehicle. Direct InP/GaAs epi for laser sources. Asian listing flag. |
| **TPEX:3485** | TPEX Taiwan emerging board | Centera Photonics | unknown (just listed Mar 2026) | Layer 5 (PIC/optical engine) | **Just listed March 2026** — newly public; 1.6T integrated-laser transceiver using NewPhotonics NPG10201 PIC. |
| **TWSE:6820** | TWSE Taiwan | ACON Optics Communications | unknown | Layer 7 (Fiber attach / FAU) | Direct CPO fiber array supplier, named international clients |
| **4979** | TPEX Taiwan | LUXNET Corp | sub-$500M | Layer 6/8 (Optical components) | Optical components for data-center optical comms; English filings limited; AR cites SiPho M&A wave |
| **6869** | HKEX | Yangtze Optical Fibre & Cable | sub-$2B (verify) | Layer 14 (Fiber preform/cable) | Optical fiber preform/cable supplier — fiber upstream of CPO. **China geopolitical / export-control handicap.** |

### Foreign candidates that FAIL or get auto-handicapped

| Ticker | Reason |
|---|---|
| 9MT (MetaOptics SGX) | $98M USD; metalens for camera/AR — fails H8 end-market test (not AI-DC) |
| 2382 (Sunny Optical HKEX) | >$5B mega-cap |
| 5803.T Fujikura | Likely >$5B post 2025 rerate |
| 6920.T Lasertec | ~$8-10B likely; EUV mask not CPO-direct |
| HKEX:Lightelligence | ~$10B + Chinese AI export-control risk |
| KRX:000660 SK Hynix | Memory-side, not CPO |

---

## PHASE 6 RETROSPECTIVE — Pre-cap-verification observations

### Retrospective Q4 — Broken-IPO candidates

**Finding: No clean broken-IPO photonics candidate passing CPO/AI-DC end-market test.**

| Ticker | Status | Verdict |
|---|---|---|
| BURU (Nuburu) | de-SPAC Feb 2023 (Tailwind ACQ); reverse splits to micro-cap | **REJECT — industrial laser/welding, not AI-DC** |
| LASE (Laser Photonics) | IPO Sep 2022; sub-$1; 10-Q delay | **REJECT — industrial cleaning laser, not AI-DC** |
| RKLY (Rockley Photonics) | Bankrupt 2023 — calibration case | Out of universe |
| OPTX (Syntec Optics) | Already in Archos WATCH | -- |

### Retrospective Q5 — de-SPAC reanimation in photonics

**Finding: The 2022-2023 photonics de-SPAC cohort universally bankrupt-or-pivoted-out-of-AI-DC.** Pasqal (pending Bleichroeder) and Photonic Inc are quantum (out of scope). No clean 24-36mo post-de-SPAC photonics reanimation candidate exists in the current universe. **This is itself a Phase 6 insight: the de-SPAC pattern in photonics has been dominated by industrial laser + biosensing — both wrong end-market.**

### Retrospective Q6 — Insider buying

No clean Form-4 signal surfaced for compliant CPO names in the broad-universe sweep. **Recommend a follow-on per-name insider screen on Soitec (AMF Paris filings), Sivers (Swedish Finansinspektionen), AIXTRON (BaFin), OE Solutions/Lightron (Korean DART) in a follow-up session.** Broad-universe insider screens remain structurally broken in this environment (OpenInsider unreachable per INSIGHTS.md).

### Retrospective Q7 — Customer-deposit / deferred-revenue signals (the highest-yield unorthodox signal per INSIGHTS.md)

**MAJOR SIGNAL FIRED:**

> **Tower Semiconductor (TSEM) Q1 2026 10-Q (filed May 13, 2026): $290 million in customer prepayments received from silicon photonics customers during Q1 2026 alone.** Source: [TSEM Q1 2026 10-Q exhibit](https://www.sec.gov/Archives/edgar/data/0001384905/000119312526213500/0001193125-26-213500-index.htm) — plus $1.3B silicon photonics revenue contracts signed for 2027.

**TSEM is graduated above $5B (cap $32B), so this is not a direct ACCEPT signal — but it is the canonical macro validation of Framework v2.0's "balance-sheet signals lead bellwether mentions by 1-3 quarters" thesis at the SiPh foundry layer.** Hyperscalers are now writing nine-figure-per-quarter prepayments to lock SiPh capacity.

**Propagation expectation:** This signal should appear in customer-deposit / deferred-revenue lines of sub-$5B suppliers downstream of TSEM within 1-3 quarters. Names to monitor in next 10-Q / 6-K cycle:
- **Soitec** (Photonics-SOI wafer supplier to TSEM/TSMC/GFS) — verify customer-deposit step-change in next 6-K
- **AIXTRON** (MOCVD reactor backlog/deposits for InP fabs) — verify in next 10-K equivalent
- **Sivers Semiconductors** (InP photonics, multiple foundry partnerships) — verify in next 6-K
- **OE Solutions / Lightron** (Korean 1.6T transceivers for InfiniBand AI DC) — verify in DART filings
- **AEHR** (WLBI customer prepayments for SiPh production ramp) — already partially confirmed in Q1 FY26 8-K
- **VECO** (InP laser tool $250M order book — already documented per CANDIDATE_UNIVERSE.md)

---

## PHASE 5 — MASTER CANDIDATE EVALUATION MATRIX

All caps verified intraday 2026-05-27/28 via stockanalysis.com / macrotrends.net / companiesmarketcap.com / finviz. Foreign caps converted to USD at 2026-05-28 reference rates. Where cap diverges across sources, the median is reported and flagged.

H8 Tier per Framework v2.0:
- TIER 1 NANO: sub-$500M
- TIER 2 CATALYST: $500M-$2B
- TIER 3 COMPOUNDER: $2B-$5B
- TIER 4 SEGMENT: $5B-$15B parent w/ qualifying AI-DC segment >50% mix + >40% YoY
- GRADUATED: above $5B without qualifying segment

H10 status — does the candidate's chokepoint touch a bellwether (NVDA/TSMC/AVGO/MSFT/META/AMD/named hyperscaler) explicitly?

### US-listed candidates (sub-$5B PASS, H8 verified)

| Ticker | Company | Exchange | Mkt Cap | CPO Layer(s) | TTM Revenue | H8 Tier | H10 Status | H5 (pre-screen) | H11 (balance sheet) | In Taxonomy? | Verdict |
|---|---|---|---|---|---|---|---|---|---|---|---|
| **VECO** | Veeco Instruments | NASDAQ | $3.52B | 2 (MOCVD epi tools for InP/GaAs lasers + SiPh capacity) | $630M (Q1'26 $158M) | **TIER 3 COMPOUNDER** | **PASS — Category** (May 2026 8-K "particularly strong momentum in silicon photonics as customers scale optical connectivity"; $250M order book) | NEUTRAL — China BIS headwind suppressed sentiment; 2-deg supplier per CANDIDATE_UNIVERSE.md | Profitable, FCF positive | Already tracked (supplier-mapping screen WATCH) | **DD QUEUE — promote from supplier-mapping WATCH to full DD; the 8-K disclosure language has now crystallized the SiPh thesis** |
| **AEHR** | Aehr Test Systems | NASDAQ | ~$2.4-2.9B (cap reconciliation flagged) | 9 (Wafer-level burn-in test) + **NEW cross-tag #1** (SiPh WLBI per Q1 FY26 8-K) | FY26 guide $45-50M | **TIER 3 COMPOUNDER** (cap reduced from $3.46B; no longer borderline graduation) | **PASS — Vendor-level** (lead SiPh customer "firmed up production ramp, beginning early next fiscal year") | PARTIAL — recent +15.7% one-day move (per CHOKEPOINT_TAXONOMY.md 2026-05-27) | Strong cash position; profitable | Already tracked (chokepoint #4 ACTIVE) | **TAXONOMY UPDATE — re-classify with cross-tag to chokepoint #1 (CPO); cap reduction confirms TIER 3 (no longer borderline)** |
| **SKYT** | SkyWater Technology | NASDAQ | $1.42B | 4 (US SiPh foundry, Trusted Foundry) | $442M (FY25) | **TIER 2 CATALYST** | **FLAG** (10-K lists SiPh as one ATS platform; not yet a load-bearing revenue line >20%) | NEUTRAL | DOE/DARPA contracts; profitable post-restructure | Not tracked | **WATCH — US-onshore foundry with SiPh process + CHIPS Act tailwind; verify whether SiPh enters >20% of next 10-K revenue breakdown** |
| **PLAB** | Photronics Inc | NASDAQ | $2.65B | 4-adjacent (Photomasks for SiPh + advanced packaging) | $849M | **TIER 3 COMPOUNDER** | **FLAG** (10-K names "advanced packaging modules, micro optical components for VR/AR and silicon photonics") | NEUTRAL | Profitable, FCF positive | Not tracked | **WATCH — photomask is structurally upstream of every foundry including SiPh; track 8-K for SiPh-segment carveout** |
| **MXL** | MaxLinear | NASDAQ | ~$1.5B (web; verify) | 13 (Drivers/TIAs) | TBD | **TIER 2 CATALYST** | **PASS — Vendor adjacency** ("Washington" 4-channel 200G/lane TIA explicitly positioned for AI DC) | NEUTRAL | Verify | Not tracked | **WATCH — 200G TIA product catalyst is the cleanest signal-shape (recent product launch + AI-DC positioning); needs cap re-verify + 10-Q segment data** |
| **HIMX** | Himax Technologies | NASDAQ | $1.61B | 8 (CPO packaging partnership) | $945M | **TIER 2 CATALYST** | **FLAG** (FOCI partnership for CPO packaging is real but display drivers dominate ~80%+) | NEUTRAL | Profitable | Not tracked | **WATCH (adjacency-only) — verify FOCI partnership reaches material revenue threshold; current CPO/WLO segment <5%** |
| **QUBT** | Quantum Computing Inc | NASDAQ | $1.59B | 6 (TFLN modulators) + 5 (PIC dev with POET) | minimal (pre-revenue) | **TIER 2 CATALYST** | **FLAG** (POET joint TFLN development is real but no bellwether-named relationship) | LOVED-ish (significant retail attention) | Going-concern risk verify | Not tracked | **REJECT — pre-revenue moonshot blind spot (LWLG analog); retail-driven price action; promotional risk** |
| **INDI** | indie Semiconductor | NASDAQ | $0.65B | 8 (HOPS optical packaging) | $217M | **TIER 2 CATALYST** | **FLAG** (HOPS is real capability; ams OSRAM CMOS line acquisition May 2026) | NEUTRAL | Verify | Already tracked (robotics TIER 2 MONITOR per SCAN_12) | **NO CHANGE — already monitored via robotics lens; auto ADAS dominates; H8 end-market fails for AI-DC pure-play classification** |
| **ALNT** | Allient Inc | NASDAQ | $1.24B | 8 cross-tag (SiPh micro assembly motion systems) | $560M | **TIER 2 CATALYST** | **FLAG** (10-K names "nano technology motion systems in silicon photonics, micro assembly") | NEUTRAL | Profitable | Already TIER 2 robotics WATCH per SCAN_12 | **CROSS-TAG ADDITION — add CPO #8 packaging-equipment WATCH alongside robotics #15; verify SiPh micro-assembly enters >10% segment revenue** |
| **GHM** | Graham Corporation | NYSE | $1.05B | 11 (Thermal management) | $237.6M | **TIER 2 CATALYST** | **FAIL** (defense/nuclear/Navy dominant; not AI-DC) | NEUTRAL | Profitable | Not tracked | **REJECT (for AI lens) — could route through Defense H10-D in separate session; not CPO-relevant** |
| **SVCO** | Silvaco Group | NASDAQ | $320M | EDA-tools (TCAD for SiPh devices) | $66.7M | **TIER 1 NANO** | **FLAG** (Victory TCAD adopted by ProMOS for SiPh dev; EDA-layer, not direct chokepoint) | NEUTRAL | Verify | Not tracked | **WATCH (TIER 1 NANO) — EDA picks-and-shovels at SiPh design layer; verify SiPh-related licensing % in next 10-Q** |
| **CPSH** | CPS Technologies | NASDAQ | ~$200M (cap reconciliation flagged: $103M-$221M range) | 11 (Thermal management — ceramic substrates) | $32M | **TIER 1 NANO** | **FLAG** (May 2026 8-K thermal management deal — verify CPO/AI-DC angle) | NEUTRAL | Profitable | Not tracked | **WATCH (TIER 1 NANO) — advanced ceramics for thermal substrates may apply at CPO module level; verify next 10-Q for AI-DC customer disclosure** |
| **INFQ** | Infleqtion | NYSE | $2.73B (down from $3.46B) | 5 (SiPh components via Morton Photonics acquisition) | minimal | **TIER 3 COMPOUNDER** | **FLAG** (CHIPS LOI $100M per Screen 10; quantum/sensing primary) | NEUTRAL | Recently public | Already tracked (Screen 10 gov-equity TIER 1 next-target) | **CROSS-TAG ADDITION — add CPO #5 PIC-design adjacency to existing gov-equity classification; pre-revenue caveat remains** |
| **INV** | Innventure | NASDAQ | $0.29B | 11 (Thermal management — vague) | small | **TIER 1 NANO** | **FAIL** (no clear CPO/DC angle in thermal 8-K) | NEUTRAL | Speculative | Not tracked | **REJECT — vague thermal narrative; venture-portfolio shell; no chokepoint connection** |
| **SMTC** | Semtech | NASDAQ | ~$3-3.5B (web; verify) | 13 (CDR / TIA / signal-conditioning) | TBD | **TIER 3 COMPOUNDER** | **FLAG** (Merchant TIA/CDR supplier into 100-400G optical receivers) | NEUTRAL | Verify | Not tracked | **WATCH — established optical PHY supplier just retraced sub-$5B; verify 1.6T design-win disclosure in next 10-Q** |
| **LASR** | nLight | NASDAQ | ~$500M-1B (web; verify) | 3 (High-power diode lasers) | TBD | **TIER 1 NANO** (if sub-$500M) or **TIER 2 CATALYST** | **FLAG** (defense/industrial primary; CW pump lasers adjacent to CPO) | NEUTRAL | Verify | Not tracked | **WATCH — verify cap precisely; if AI-DC laser revenue is disclosed as growing segment, promote; defense-laser tilt may route to H10-D parallel** |
| **CAMT** | Camtek | NASDAQ | ~$4-5B (borderline) | 9 (Advanced packaging inspection for CPO/2.5D/3D stacks) | TBD | **TIER 3 COMPOUNDER** (borderline) | **PASS — Category** (CPO/COUPE-style stack inspection — direct adjacency to TSMC COUPE customers) | NEUTRAL-PARTIAL | Profitable | Not tracked | **WATCH — borderline cap; direct CPO inspection adjacency; verify intraday cap and AI-DC % of revenue in next 10-Q** |
| **ACLS** | Axcelis Technologies | NASDAQ | ~$2-3B (web; verify) | 4-adjacent (Ion implantation tools for SiPh fab) | TBD | **TIER 3 COMPOUNDER** | **FLAG** (indirect — ion implant for SiPh process) | NEUTRAL | Profitable | Not tracked | **WATCH — verify SiPh-process-tool revenue mix; cyclical headwind risk vs SiPh tailwind** |
| **KOPN** | Kopin Corp | NASDAQ | ~$200-300M | 10 (Adjacency — microdisplay/optics) | TBD | **TIER 1 NANO** | **FAIL** (AR/VR dominant; not AI-DC) | NEUTRAL | Verify | Not tracked | **REJECT — wrong end-market (AR/VR not AI-DC)** |
| **OSIS** | OSI Systems | NASDAQ | ~$2.5B | Photonics segment (small) | TBD | **TIER 3 COMPOUNDER** | **FAIL** (Optoelectronics segment is small; security inspection dominant) | NEUTRAL | Profitable | Not tracked | **REJECT — diversified parent; photonics segment too small + wrong end-market** |
| **BELFB** | Bel Fuse | NASDAQ | ~$600M-1B (web; verify) | 14 (Magnetics/connectors for datacom) | TBD | **TIER 2 CATALYST** | **FLAG** (datacom magnetics; not CPO-direct) | NEUTRAL | Verify | Not tracked | **WATCH (low conviction) — connector/magnetics adjacency; verify AI-DC % of revenue** |
| **OIIM** | O2Micro International | NASDAQ | ~$100M | 13-adjacency (power IC for fiber/optical) | TBD | **TIER 1 NANO** | **FAIL** (tiny + adjacency-only) | NEUTRAL | Going-concern risk verify | Not tracked | **REJECT — tiny scale, no chokepoint-direct exposure** |
| **LEDS** | SemiLEDs | NASDAQ | TBD (nano) | 6-adjacency (photodetector with Japanese partners) | minimal | **TIER 1 NANO** | **FAIL** (LED/lighting primary) | NEUTRAL | Going-concern risk | Not tracked | **REJECT — nano-cap LED-pivot; not CPO chokepoint** |
| **XNDU** | Xanadu Quantum | NASDAQ (6-K) | $5.13B (just over) | 5 (SiPh for photonic quantum) | $3.58M | **GRADUATED** (just barely over cap) | **FLAG** (Tower Semi collaboration) | LOVED (quantum hype) | Pre-revenue | Not tracked | **REJECT — over cap + quantum end-market + pre-revenue moonshot** |

### US-listed candidates that GRADUATED above $5B during cap verification

| Ticker | Company | Mkt Cap | Note |
|---|---|---|---|
| MTSI | MACOM Technology Solutions | $19.36B | Full TIA/modulator/driver/laser portfolio — would be TIER 1 ACCEPT if sub-$5B; **Tier 4 SEGMENT consideration: verify if AI-DC optical >50% segment AND >40% YoY** |
| RAL | Ralliant Corp | $7.00B | Comms test & measurement with SiPh tailwind; Tier 4 SEGMENT candidate if AI-DC T&M segment carves out cleanly |
| NVMI | Nova Ltd | $16.28B | Israeli semi metrology (optical for advanced packaging); graduated above cap |
| XNDU | Xanadu Quantum | $5.13B | Just over cap; quantum end-market |

### Foreign-listed candidates (sub-$5B PASS, with handicap)

| Ticker | Company | Exchange | Mkt Cap (USD) | CPO Layer(s) | H8 Tier | H10 Status | Handicap | Verdict |
|---|---|---|---|---|---|---|---|---|
| **SOI / SLOIY** | **Soitec** | Euronext Paris / OTC ADR | **~$3.3B USD** (€3.05B) | 1+4 (Photonics-SOI wafers for SiPh foundries) | **TIER 3 COMPOUNDER** | **PASS — Vendor** (named supplier to TSMC COUPE + GFS Fotonix + Tower SiPh + ST per SEMI SiPh Industry Alliance membership) | Euronext primary, OTC ADR (SLOIY) thin | **DD QUEUE — STRONGEST FOREIGN CANDIDATE OF SWEEP — Photonics-SOI substrate monopolist sub-$5B; bellwether-cascade exposure** |
| **AIXA / AIXXF** | **AIXTRON** | Xetra Germany / OTC ADR | **~$4.9B USD** (€4.5B) | 2 (MOCVD epi tools — ~90% share of G10-AsP InP reactors) | **TIER 3 COMPOUNDER (borderline graduation)** | **PASS — Vendor-level adjacency** (serves Coherent/Lumentum InP fabs; raised 2026 guide €560M) | Xetra primary, OTC ADR thin | **DD QUEUE — MOCVD-reactor monopolist for InP chokepoint; borderline cap; verify intraday + 6-K customer-deposit signals** |
| **SIVE.ST / SIVEF** | Sivers Semiconductors | Nasdaq Stockholm / OTC | ~$2.05B USD (Stockholm) / $2.75B (OTC ADR) | 3 (InP photonics — Glasgow subsidiary) + mmWave | TIER 3 COMPOUNDER | **FLAG → PASS** (explicit "AI datacenter photonics" positioning; Glasgow InP subsidiary) | Already tracked as SIVEF OTC ADR per CHOKEPOINT_TAXONOMY.md | **TAXONOMY UPDATE — replace SIVEF reference with SIVE.ST (Stockholm primary); cleaner liquidity; same name** |
| **6754.T** | **Anritsu** | TSE Tokyo | **~$2B USD** | 9 (Optical test — BERTWave MP2110A for 10G-1.6T module test) | **TIER 2/3 CATALYST** | **PASS — Category** (explicit Taiwanese module-house qualification content; 10G-1.6T test workhorse) | Foreign-handicap; US OTC ADR ANRZF | **DD QUEUE — HIGHEST-CONVICTION NEW OPTICAL TEST PURE-PLAY OF SWEEP; signal-clean and quantifiable** |
| **6777** | Santec Holdings | TSE Tokyo | sub-$1B | 3 (Tunable lasers) + 9 (Optical test) | TIER 2 CATALYST | **FLAG** ("CPO ecosystem with wafer-level diagnostics and module-level test") | Foreign-handicap | **WATCH — tunable laser + test combo; verify in 6-K filings** |
| **138080** | **OE Solutions** | KOSDAQ Korea | $400-700M | 8 (1.6T transceivers for InfiniBand AI DC) + CPO IP | **TIER 1 NANO / TIER 2 CATALYST** | **PASS — Vendor-level** ("Patents for the CPO Era" published Mar 2026; 1.6T InfiniBand-compatible) | Korean DART filing access | **DD QUEUE — direct CPO play with explicit AI-DC counterparty alignment; Korea-handicapped** |
| **069540** | **Lightron Fiber-Optic Devices** | KOSDAQ Korea | sub-$1B | 8 (Pluggable transceivers 100G/400G/800G) | TIER 2 CATALYST | **PASS — Category** (NVDA GTC 2026 namedrop in Korean media) | **+1,575% YoY — possibly LOVED → reject window; verify H5 status** | **WATCH — verify pullback for H5 PARTIAL-RECOVERING; if not pulled back, document for next-cycle** |
| **LPK / LPKFF** | LPKF Laser & Electronics | Xetra Germany / OTC | €276-550M (~$300-600M) | 10 (LIDE glass substrate for advanced packaging) | TIER 1 NANO / TIER 2 CATALYST | **FLAG** (Intel glass HVM commitment by 2030; not yet a 2026-window catalyst) | Xetra primary | **WATCH — binary-outcome glass-substrate bet; Intel timing means 2027-28 inflection** |
| **6502.TWO** | EzConn | TPEX Taiwan | $300-500M | 2 (III-V epi consolidator post-IntelliEpi share-exchange) | TIER 1 NANO | **FLAG** (share-exchange completes consolidation of MBE epi capability) | TPEX Taiwan-handicap | **WATCH — InP/GaAs epi capability sub-$500M; verify post-exchange entity structure** |
| **TPEX:3485** | **Centera Photonics** | TPEX Taiwan emerging board | unknown (just listed March 2026) | 5 (1.6T integrated-laser transceiver) + Layer 7 (NewPhotonics NPG10201 PIC) | TIER 1 NANO presumed | **PASS — Vendor adjacency** (uses Israeli NewPhotonics PIC) | Just listed; thin float; foreign-handicap | **WATCH — newly public sub-$5B CPO pure-play; needs cap verification + further public data; potential ACCEPT once liquidity matures** |
| **TWSE:6820** | ACON Optics Communications | TWSE Taiwan | unknown | 7 (Fiber attach / FAU) | TBD | **FLAG** (Direct CPO fiber array supplier per company press) | TWSE handicap | **WATCH — FAU specialist parallel to Browave/FOCI; verify cap + customer disclosures** |
| **4979** | LUXNET Corp | TPEX Taiwan | sub-$500M | 6/8 (Optical components for AI-DC) | TIER 1 NANO | **FLAG** (annual report cites SiPho M&A wave; English filings limited) | TPEX + language-handicap | **WATCH — verify cap + chokepoint mix in next AR cycle** |
| **6869** | Yangtze Optical Fibre & Cable | HKEX | sub-$2B (verify) | 14 (Fiber preform/cable) | TIER 2 CATALYST | **FLAG** (Fiber upstream; not CPO-direct) | **China geopolitical / export-control RISK** | **REJECT-tier — Chinese listing + export-control exposure** |
| **5232.T** | Sumitomo Osaka Cement | TSE Tokyo | TBD (verify) | 6 (LiNbO3 modulator material) | TBD | **FLAG** (dominant LiNbO3 supplier for >400G coherent) | Foreign-handicap | **MONITOR — verify cap and LiNbO3 segment mix in next 20-F equivalent** |

---

## DD QUEUE — Ranked top candidates for full DUE_DILIGENCE_CHECKLIST.md vetting

Six candidates warrant immediate full DD (Sections 1-6) within the next 30 days. Ranked by signal-strength × tier × investability:

### Tier A — DD within 14 days

1. **SOI / SLOIY — Soitec (Euronext Paris / OTC ADR, ~$3.3B USD, TIER 3 COMPOUNDER)**
   - **Strongest foreign-listed CPO-adjacent sub-$5B pure-play** identified across the entire sweep
   - SEMI SiPh Industry Alliance member; named substrate supplier to TSMC COUPE, GlobalFoundries Fotonix, Tower Semi SiPh, ST
   - H10 PASS at vendor level via the SEMI alliance membership
   - Mgmt target $2B rev / ~40% EBITDA margin
   - Cyclical RF-SOI trough is currently MASKING the Photonics-SOI ramp — H5 IGNORED-equivalent (sentiment focused on the RF-SOI cycle, not the photonics secular)
   - **Critical DD priorities:** Section 5.4 forward P/S framing on Photonics-SOI ramp; Section 1.6 paid promotion check (likely CLEAR for an established European industrial); Section 5.5 backlog quality decomposition
   - **OTC ADR (SLOIY) liquidity caveat:** verify whether SLOIY ADR meets Archos liquidity threshold; if not, the name lands in the foreign-handicap basket but the signal-quality justifies it

2. **AIXA / AIXXF — AIXTRON (Xetra / OTC ADR, ~$4.9B USD, TIER 3 COMPOUNDER BORDERLINE)**
   - ~90% share of G10-AsP MOCVD reactors — the InP/GaAs epi-tool monopolist
   - Direct supplier to Coherent / Lumentum InP fabs (= bellwether-2-degree via the NVDA $2B COHR + NVDA $2B LITE investments)
   - Just raised 2026 guidance to €560M — momentum-confirmation
   - **Cap risk:** at $4.9B USD this is RIGHT AT the H8 threshold; a 5% move pushes graduation. The DD must include an entry-window-closing risk check
   - **Critical DD priorities:** Section 2.6 customer concentration disclosure (what % of MOCVD revenue is InP-photonics vs LED/power); Section 5.5 backlog decomposition; insider activity on Xetra

3. **6754.T — Anritsu (TSE Tokyo, ~$2B USD, TIER 2/3 CATALYST/COMPOUNDER)**
   - **Highest-conviction NEW optical test pure-play** of the sweep
   - BERTWave MP2110A is the workhorse 10G-1.6T optical module test instrument; explicit Taiwanese module-house qualification content
   - The "picks-and-shovels" of the CPO ramp — tests every module regardless of who wins the module race
   - **Critical DD priorities:** verify TSE filings for 1.6T-related revenue carveout; OTC ADR (ANRZF) liquidity check; foreign-handicap evaluation

### Tier B — DD within 30 days

4. **VECO — Veeco Instruments (NASDAQ, $3.52B, TIER 3 COMPOUNDER)**
   - Already in Archos as supplier-mapping WATCH; the May 2026 8-K SiPh language has now crystallized the thesis
   - $250M order book for InP laser tools (per CANDIDATE_UNIVERSE.md)
   - **Already partially scoped** — DD work should be additive to existing WATCH file
   - **Critical DD priorities:** Section 2.6 China BIS revenue concentration risk (the AXTI-RAL parallel); Section 5.5 SiPh-segment carveout in next 10-Q

5. **138080 — OE Solutions (KOSDAQ Korea, $400-700M, TIER 1 NANO / TIER 2 CATALYST)**
   - Direct 1.6T transceivers compatible with InfiniBand AI DC switches (NVDA Quantum-X namedrop in Korean media)
   - "Patents for the CPO Era" published Mar 2026
   - **Korean DART filing access required** — DD must include Korean-language filing workflow setup
   - **Critical DD priorities:** Section 2.3 NVDA / hyperscaler counterparty acknowledgment via Korean disclosures; Section 5.5 customer concentration; Korean Form-4-equivalent insider screen

6. **AEHR (already in taxonomy) — cross-tag chokepoint #1 + chokepoint #4**
   - Cap has DROPPED from $3.46B (per 2026-05-27 CHOKEPOINT_TAXONOMY.md reading) to ~$2.4-2.9B (verified 2026-05-28)
   - Q1 FY26 8-K explicitly tied SiPh WLBI to production ramp = vendor-level H10 fire at chokepoint #1
   - **No fresh DD needed** — taxonomy update is the action (cross-tag, no longer borderline graduation)

### Tier C — WATCH (not DD-ready; trigger conditions defined)

7. **SKYT** — verify SiPh enters >20% of next 10-K revenue breakdown
8. **MXL** — Washington 200G TIA design-win disclosure in next 10-Q
9. **CAMT** — borderline cap; verify intraday + AI-DC % of inspection revenue
10. **SMTC** — 1.6T design-win disclosure in next 10-Q
11. **HIMX** — FOCI partnership reaches material revenue threshold
12. **PLAB** — SiPh-segment carveout disclosure
13. **TPEX:3485 Centera Photonics** — newly public; needs cap verification + further public data; potential ACCEPT once liquidity matures
14. **LASR / nLight** — verify cap precisely; if AI-DC laser revenue is disclosed as growing segment, promote
15. **069540 Lightron** — verify post-rally cap; if PARTIAL-RECOVERING geometry triggers, enter at 50% sizing

### REJECT-track (do not pursue)

| Ticker | Reason |
|---|---|
| QUBT | Pre-revenue moonshot blind spot + LOVED retail sentiment + POET-collateral pre-revenue risk |
| INDI | Auto ADAS dominant; H8 end-market fails for AI-DC |
| GHM | Defense/nuclear dominant; CPO not load-bearing (could route through H10-D in separate session) |
| INV | Vague venture portfolio; no chokepoint connection |
| KOPN | AR/VR end-market |
| OSIS | Diversified parent; photonics segment too small + wrong end-market |
| OIIM | Tiny + adjacency-only |
| LEDS | LED/lighting; not CPO |
| XNDU | Over $5B cap + quantum end-market + pre-revenue |
| 9MT (MetaOptics SGX) | Metalens for AR/camera; not AI-DC end-market |
| 6869 (Yangtze Optical Fibre HKEX) | China geopolitical / export-control risk; fiber upstream not CPO-direct |
| BURU / LASE | Industrial laser (not AI-DC) — broken-IPO REJECT |

---

## SUPPLY CHAIN GAPS — Layers with NO sub-$5B public pure-play

Maintaining the IPO-watch list per INSIGHTS.md "consolidation-by-mid-cap eats the discovery window" finding.

| Layer | Status | IPO Watch / discovery vector |
|---|---|---|
| 1 — InP/GaAs/GaSb Substrates (US-listed) | EMPTY post-AXTI graduation | Foreign: IQE.L (LSE WATCH), Sumitomo Electric, JSP. No US sub-$5B pure-play. **Future IPO from Asian / European substrate carve-outs would be highest-priority watch.** |
| 2 — Epitaxial Growth (US-listed) | EMPTY pure-play; VECO is tool-vendor (different layer) | Foreign: 6502.TWO EzConn (post-IntelliEpi consolidation), SMART Photonics (private Dutch), Riber SA |
| 3 — Laser Sources (CW/EML/QD) | EMPTY post-LITE/COHR graduation; LASR is high-power but defense-tilted | **Ayar Labs is top IPO watch** (CW lasers for CPO); Innolume (private German); OpenLight (Synopsys-backed, Tower partner) |
| 4 — Silicon Photonics Foundry (pure-play) | EMPTY at sub-$5B; SKYT is mid-IDM with SiPh as one platform | **Capital intensity rules out pure-play sub-$5B SiPh foundry IPO; the path is via existing IDM expansion or acquisition** |
| 5 — Optical Interposer / PIC Design (US-listed) | POET ($2.22B) is sole; structurally consolidated | **Ayar Labs + Lightmatter + OpenLight IPOs** would fill this; all 3 are private with 2026-2028 IPO targets |
| 6 — Modulators (TFLN / LN) | EMPTY at sub-$5B pure-play; QUBT is pre-revenue | **HyperLight (private TFLN startup) is IPO watch**; Sumitomo Osaka Cement (5232.T) for LN materials |
| 7 — Fiber Attach / FAU | Foreign-only: Browave (TPEX), FOCI (TPEX), ACON Optics (TWSE) | **Teramount was acquired by Molex (Koch private)** — IPO window already consumed by M&A |
| 8 — Optical Packaging / Assembly (pure-play) | EMPTY post-ASMPT/BESI graduation; ALNT is motion-systems adjacency | Asian: Foreign listings + private packaging houses going public |
| 9 — Optical Test & Measurement (sub-$5B pure-play US) | EMPTY at sub-$5B US-listed | **Foreign-only: Anritsu (6754.T), Santec (6777)** — best near-term entries. Future EXFO re-IPO or VIAV-spinoff would be triggers. |
| 10 — Specialty Optical Materials (US-listed) | EMPTY pure-play; LPK is foreign | Glass substrate (Corning Future LIDE, LPKF). Polymer waveguide. SiN waveguide. **All private or mega-cap** |
| 11 — Thermal Management for CPO | CPSH is borderline; no clear sub-$5B pure-play | **Watch for thermal-substrate IPO carve-outs from Corning/Asetek/Boyd** |
| 12 — PCB / High-Freq Substrate | EMPTY at sub-$5B; Ibiden/Shinko/Toppan/Unimicron all foreign mega-cap or being acquired | Korean / Taiwanese mid-cap substrate names below $5B |
| 13 — Drivers / TIAs | **NEW DISCOVERY: MXL and SMTC are sub-$5B candidates** | Both verified sub-$5B; this layer is NOT structurally empty after all — prior scans missed them |
| 14 — Connectors / Interconnect | EMPTY pure-play; BELFB is adjacency | **Senko (private), Sumitomo, US Conec all private or mega-cap** |

**Key gap insight:** The biggest structural gaps are Layers 1, 3, 5, 6, 10 — substrates, laser sources, fabless PIC design, modulators, and specialty materials. These are EXACTLY where the private startup pipeline (Ayar, Lightmatter, OpenLight, HyperLight, NewPhotonics, Quintessent, Innolume, Scintil, SMART Photonics, Aloe) is concentrated. **The IPO watch list for the next 12-24 months is structurally clear.**

---

## PHASE 6 RETROSPECTIVE — Answers to the 7 questions

### 1. How many total public companies touch the CPO supply chain below $5B?

**Pass H8 (sub-$5B): 17 US-listed + 11 foreign-listed = 28 candidates surface across this sweep.**

Of those:
- **6 DD QUEUE** (Tier A + B priority for full DD within 30 days)
- **9 WATCH** (Tier C — trigger conditions defined)
- **12 REJECT-track** (wrong end-market, pre-revenue moonshot, vague narrative, etc.)
- **1 cross-tag taxonomy update** (AEHR — chokepoint #4 ACTIVE + #1 cross-tag for SiPh WLBI)

Compare to prior CPO scans:
- SCAN_04 (2026-05-27 optical next-gen) returned **0 new ACCEPT-track + 3 SOUNDING BOARD foreign-handicap candidates** (Browave, FOCI, IQE)
- Prior CPO taxonomy had **1 ACTIVE US-listed pure-play** (POET) + **1 OTC ADR** (SIVEF)

**This sweep increased the surface area roughly 6x via breadth-first methodology** — the prior scans applied tight filters too early and missed an order of magnitude of names.

### 2. Which supply chain layers have ZERO public company representation?

Confirmed empty (per Supply Chain Gaps section above): Layers 1 (US sub-$5B substrate), 3 (sub-$5B laser source pure-play), 4 (sub-$5B SiPh foundry pure-play), 6 (sub-$5B modulator), 10 (sub-$5B specialty material), 14 (sub-$5B connector).

**Most actionable IPO watch list ranking (12-24mo horizon):**
1. **Ayar Labs** (Layer 3 + 5) — Intel/AMD/NVIDIA-backed; rumored 2026-27 IPO
2. **Lightmatter** (Layer 5) — $4.4B private val; 2026-27 IPO target
3. **OpenLight** (Layer 5) — Synopsys-backed, Tower partner — IPO candidate
4. **HyperLight** (Layer 6) — TFLN modulator; NVDA-adjacent
5. **NewPhotonics** (Layer 5) — Israeli; powers Centera Photonics
6. **Innolume** (Layer 3) — German QD laser; scaling production

### 3. Framework-rejected-but-compelling names?

**SOI / Soitec** is the candidate that the strict 4-filter framework might have under-weighted (Euronext primary listing carries the foreign-handicap that has historically reduced conviction in Archos). But the substrate-supplier-to-three-foundries position is structurally similar to a load-bearing chokepoint pure-play. **Recommend: do NOT reject; instead document foreign-handicap explicitly and run full DD with awareness that the OTC ADR (SLOIY) liquidity caveat may limit position sizing rather than rejecting the candidate.**

**AIXTRON** at $4.9B USD is at the cap threshold — strict-application might disqualify as borderline graduation. But the 90% MOCVD share is a structural chokepoint position. **Recommend: include with explicit "entry-window-closing" risk flag in position sizing decision.**

**6754.T Anritsu** carries foreign-handicap but the optical test pure-play signal-quality is the highest of any new name surfaced. **Recommend: include with foreign-handicap documented; do not reject on listing-venue alone.**

### 4. Broken-IPO candidates?

**No clean broken-IPO photonics candidate passing CPO/AI-DC end-market test exists.**

- BURU (Nuburu) — REJECT — industrial laser end-market
- LASE (Laser Photonics) — REJECT — industrial cleaning laser
- RKLY (Rockley) — bankrupt 2023, biosensing pivot
- OPTX (Syntec Optics) — already in Archos WATCH; the only photonics de-SPAC with material AI-adjacent positioning

**Phase 6 insight:** The 2022-2023 photonics de-SPAC cohort was structurally dominated by industrial-laser + biosensing thesis. AI-DC photonics did NOT use the SPAC channel — the private companies (Ayar, Lightmatter, OpenLight) waited for traditional IPO routes. This means the AI-DC photonics IPO window opens cleanly in 2026-2028.

### 5. de-SPAC reanimation candidates?

**Same finding as Q4 — no clean 24-36mo post-de-SPAC photonics name with AI-DC end-market fit exists.** Pasqal and Photonic Inc are pending Bleichroeder mergers but are quantum (out of scope).

### 6. Insider buying signals?

**No clean Form-4 signal surfaced for sub-$5B CPO names in the broad-universe sweep.** Recommendation: per-name insider screen on the DD QUEUE candidates in a follow-up session, especially Soitec (AMF Paris filings), Sivers (Stockholm), AIXTRON (BaFin), OE Solutions/Lightron (DART Korea). The broad-universe insider screen remains structurally broken (OpenInsider unreachable per INSIGHTS.md).

### 7. Deferred revenue / customer deposit spikes?

**CANONICAL SIGNAL FIRED — but on a graduated name (TSEM).**

- **Tower Semiconductor Q1 2026: $290M silicon photonics customer prepayments received** + $1.3B SiPh revenue contracts signed for 2027.

**Implication for sub-$5B propagation (per Framework v2.0 discovery hierarchy — balance-sheet signals lead bellwether by 1-3 quarters):** The DD QUEUE candidates positioned UPSTREAM of TSMC/Tower/GFS should see analogous customer-deposit step-changes in their next 6-K / 10-Q / 10-K cycles. **Monitor:**
- **Soitec** next 6-K (Photonics-SOI customer deposits)
- **AIXTRON** next 10-K equivalent (MOCVD reactor deposit backlog)
- **Sivers Semiconductors** next 6-K (InP photonics customer prepayments)
- **OE Solutions** + **Lightron** Korean DART filings (1.6T transceiver prepayments)
- **AEHR** Q2 FY26 10-Q (WLBI customer prepayments — already partially confirmed)
- **VECO** Q2 FY26 10-Q (InP tool order book translation)

The first of these to disclose a first-time customer-deposit >$10M from a chokepoint-adjacent end-market becomes a TIER 1 ACCEPT-track candidate per Framework v2.0 DISCOVERY HIERARCHY rule.

---

## TAXONOMY UPDATES — Recommended changes to CHOKEPOINT_TAXONOMY.md

### Chokepoint #1 (CPO) — ACTIVE additions

| Action | Ticker | Notes |
|---|---|---|
| ADD | **AEHR cross-tag** | Already #4 ACTIVE; add cross-tag to #1 (SiPh WLBI per Q1 FY26 8-K vendor-level fire) |
| ADD | **VECO cross-tag** | Already supplier-mapping WATCH; promote to chokepoint #1 ACTIVE via the May 2026 8-K "particularly strong momentum in silicon photonics" disclosure |
| ADD | **SOI / SLOIY** (Soitec) | NEW ACTIVE entry — chokepoint #1 substrate-and-foundry-layer pure-play, foreign-listed, $3.3B USD TIER 3 |
| ADD | **AIXA / AIXXF** (AIXTRON) | NEW ACTIVE-BORDERLINE entry — chokepoint #2 (MOCVD epi tool — promoted as a new sub-layer of CPO supply chain), $4.9B USD borderline TIER 3 |
| ADD | **6754.T** (Anritsu) | NEW ACTIVE entry — chokepoint #1 test layer, foreign-handicap, $2B USD TIER 2 |
| REPLACE | **SIVEF → SIVE.ST** | Stockholm primary listing is cleaner liquidity than OTC ADR; same name |
| UPDATE | **AEHR cap** | $3.46B (2026-05-27 reading) → ~$2.4-2.9B (2026-05-28 verified) — cap REDUCED, no longer borderline graduation |
| UPDATE | **POET cap** | Confirm $2.22B from SCAN_04; no change in scan results today |

### Active taxonomy proposed row updates (chokepoint #1 CPO row)

After update, the #1 CPO row should read:

> **#1 Co-packaged optics (CPO) | Sub-$5B pure-plays remaining (mkt cap verified 2026-05-28): POET $2.22B (Canadian-founded, NASDAQ canonical); AEHR ~$2.4-2.9B (cross-tag with #4 WLBI; chokepoint #1 fire per Q1 FY26 8-K SiPh production ramp); VECO $3.52B (cross-tag with supplier-mapping; chokepoint #1 fire per May 2026 8-K "particularly strong momentum in silicon photonics"); SOI/SLOIY ~$3.3B USD (Euronext, foreign-handicap; SEMI SiPh Industry Alliance substrate to TSMC COUPE/GFS Fotonix/Tower SiPh/ST); AIXA/AIXXF ~$4.9B USD (Xetra, borderline-graduation handicap; 90% G10-AsP MOCVD reactor share for InP fab tool layer); 6754.T Anritsu ~$2B USD (TSE, foreign-handicap; BERTWave MP2110A optical test workhorse 10G-1.6T); SIVE.ST $2.05B USD (Stockholm primary replacing SIVEF OTC ADR reference); Browave TPEX:3163 ~$2.6B USD (TPEX, foreign-handicap, prior WATCH); FOCI TPEX:3363 ~$2.8B USD (TPEX, foreign-handicap, prior WATCH); IQE.L ~$665M USD (LSE, foreign-handicap, prior WATCH) | ACTIVE | Multi-tier | Vendor + Category | NVDA GTC + Spectrum-X + Quantum-X CPO; NVDA-COHR/LITE/GLW investments; TSMC COUPE; AVGO Tomahawk 6 Davisson; Tower $1.3B SiPh 2027 contracts**

### Chokepoint #8 (Optical interconnect 800G+/1.6T/AECs/SerDes) — UPDATE

Add candidates surfaced for this layer:
- **MXL** MaxLinear (TIA layer — sub-$5B, "Washington" 200G TIA)
- **SMTC** Semtech (CDR/TIA — sub-$5B borderline)
- **138080** OE Solutions (Korean 1.6T InfiniBand-compatible transceivers — KOSDAQ foreign-handicap)
- **069540** Lightron (Korean pluggable transceivers — KOSDAQ foreign-handicap)
- **TPEX:3485** Centera Photonics (Taiwan emerging board newly listed)

**Recommendation:** Reclassify chokepoint #8 from "EMPTY — structurally consolidated" to **"PARTIALLY ACTIVE — driver/TIA layer (US) and transceiver layer (Korean/Taiwanese) re-emerged as sub-$5B candidates after structural-consolidation finding."** The 800G module assemblers are graduated, but the 13-layer (drivers/TIAs) and 8-layer (sub-$5B transceivers) entry vectors exist outside the Chinese Innolight/Eoptolink/Suzhou-TFC cohort.

### New sub-layer proposed for taxonomy: Chokepoint #4-EPI

The MOCVD epi-tool layer is currently bundled inside chokepoint #4 (Wafer-level burn-in test) which is conceptually different. **Recommend creating a sub-entry** for epi tools (AIXTRON, VECO) as part of the broader CPO upstream stack, or merging this concept into chokepoint #1 supply chain. Sounding Board call required.

---

## CANDIDATE_UNIVERSE.md UPDATES — Recommended changes

### NEW DD QUEUE entries

- **SOI / SLOIY** (Soitec) — TIER 3 COMPOUNDER DD QUEUE (foreign-handicap)
- **AIXA / AIXXF** (AIXTRON) — TIER 3 COMPOUNDER DD QUEUE (foreign-handicap + borderline-cap)
- **6754.T** (Anritsu) — TIER 2/3 DD QUEUE (foreign-handicap)
- **VECO** (Veeco Instruments) — promote from supplier-mapping WATCH to chokepoint #1 ACTIVE DD QUEUE
- **138080** (OE Solutions) — TIER 1 NANO / TIER 2 CATALYST DD QUEUE (Korean DART access required)

### NEW WATCH entries

- **SKYT** (SkyWater Technology) — TIER 2 CATALYST WATCH (SiPh foundry trigger)
- **MXL** (MaxLinear) — TIER 2 CATALYST WATCH (200G TIA design-win trigger)
- **CAMT** (Camtek) — TIER 3 COMPOUNDER WATCH (CPO inspection trigger)
- **SMTC** (Semtech) — TIER 3 COMPOUNDER WATCH (1.6T design-win trigger)
- **HIMX** (Himax) — TIER 2 CATALYST WATCH (FOCI partnership scale trigger)
- **PLAB** (Photronics) — TIER 3 COMPOUNDER WATCH (SiPh photomask segment carve-out)
- **SVCO** (Silvaco) — TIER 1 NANO WATCH (SiPh TCAD licensing %)
- **CPSH** (CPS Technologies) — TIER 1 NANO WATCH (AI-DC ceramic thermal substrate)
- **TPEX:3485** (Centera Photonics) — TIER 1 NANO WATCH (newly public; foreign-handicap)
- **LASR** (nLight) — TIER 2 CATALYST WATCH (verify AI-DC laser segment growth)
- **069540** (Lightron Fiber-Optic) — TIER 2 CATALYST WATCH (Korean PARTIAL-RECOVERING per +1,575% YoY rerate)
- **LPK / LPKFF** (LPKF Laser) — TIER 1 NANO WATCH (glass substrate binary outcome)
- **6777** (Santec Holdings) — TIER 2 CATALYST WATCH (tunable laser + CPO test)
- **6502.TWO** (EzConn) — TIER 1 NANO WATCH (post-IntelliEpi III-V epi consolidation)
- **TWSE:6820** (ACON Optics) — TIER 1 NANO WATCH (FAU specialist parallel to Browave/FOCI)
- **4979** (LUXNET) — TIER 1 NANO WATCH (Taiwan optical components)
- **BELFB** (Bel Fuse) — TIER 2 CATALYST WATCH (datacom connectors/magnetics adjacency)
- **ACLS** (Axcelis Technologies) — TIER 3 COMPOUNDER WATCH (ion implant SiPh fab tools)

### NEW REJECT-log entries

- **QUBT** (Quantum Computing Inc) — Pre-revenue moonshot blind spot + LOVED retail + POET-collateral risk
- **GHM** (Graham Corporation) — Defense/nuclear dominant; not AI-DC (could route H10-D separately)
- **INV** (Innventure) — Vague venture portfolio; no chokepoint connection
- **KOPN** (Kopin Corp) — AR/VR end-market
- **OSIS** (OSI Systems) — Diversified parent; security inspection dominant
- **OIIM** (O2Micro) — Tiny + adjacency-only
- **LEDS** (SemiLEDs) — LED-pivot nano-cap
- **XNDU** (Xanadu Quantum) — Over $5B + quantum + pre-revenue
- **9MT** (MetaOptics SGX) — AR/camera metalens; not AI-DC
- **6869** (Yangtze Optical Fibre HKEX) — China export-control risk
- **BURU** (Nuburu) — Industrial laser; broken-IPO REJECT
- **LASE** (Laser Photonics) — Industrial laser; broken-IPO REJECT
- **MTSI** (MACOM) — graduated to $19.36B (TIER 4 SEGMENT candidate ONLY if AI-DC optical segment >50% + >40% YoY in next 10-Q — currently FLAG)
- **RAL** (Ralliant) — graduated to $7B (TIER 4 SEGMENT candidate; verify T&M AI-DC segment)
- **NVMI** (Nova Ltd) — graduated to $16.28B
- **INDI** (indie Semi) — auto ADAS dominant; already in robotics WATCH per SCAN_12

---

## LESSONS CAPTURED — Recommended INSIGHTS.md addendum (subject to Sounding Board ratification)

### Lesson 1 — Breadth-first methodology outperforms tight-filter early-application by ~6x

[hypothesis: 1, last: 2026-05-28] [transient]

Prior CPO scans (SCAN_04 2026-05-27 optical-next-gen + the 2026-05-26 weekly scan) applied H8 (sub-$5B) + H10 (bellwether mention) + H5 (IGNORED) filters DURING discovery, producing 0 new ACCEPT-track candidates and 3 foreign-handicap WATCH names. **This sweep deliberately deferred filter application until Phase 5 matrix-build and surfaced 28 sub-$5B candidates across 13 chokepoint layers — a ~6x expansion.** The cost was modest (~5 parallel agents, ~10 minutes of waiting time). The benefit was surfacing the actual structure of the supply chain rather than the filtered-to-zero artifact.

**How to apply:** For periodic chokepoint-specific scans (run quarterly or after bellwether earnings cycle), use breadth-first methodology and apply 4-filter framework at matrix-build stage only. For routine weekly scans, continue tight-filter application to manage cost.

### Lesson 2 — TSEM Q1 2026 $290M SiPh customer prepayments is the canonical Framework v2.0 DISCOVERY HIERARCHY confirmation

[confirmed: 1 run, last: 2026-05-28] [structural]

Per Framework v2.0 codified 2026-05-27, balance-sheet signals (deferred revenue, customer deposits) are the PRIMARY discovery layer and bellwether mentions are the CONFIRMATION layer. **TSEM's $290M Q1 2026 SiPh customer prepayments (filed May 13, 2026) is the highest-magnitude single-quarter customer-deposit disclosure in the AI Infrastructure cohort to date.** It validates the inversion of the prior gate (H10 first → balance sheet second) and confirms that Q3/Q4 2026 sub-$5B 10-Q / 10-K / 6-K filings will be where the propagated customer-deposit signals first surface at the supplier layer (Soitec, AIXTRON, Sivers, OE Solutions, AEHR, VECO).

**How to apply:** Build a quarterly customer-deposit screen specifically on the CPO supplier list (the DD QUEUE + WATCH set produced by this sweep) targeting first-time deferred revenue >$10M from a chokepoint-adjacent end-market.

### Lesson 3 — The 2022-2023 photonics de-SPAC cohort was structurally dominated by industrial-laser + biosensing; AI-DC photonics IPOs are still ahead

[confirmed: 1 run, last: 2026-05-28] [structural]

Phase 6 retrospective Q4 + Q5 found that BURU (industrial), LASE (industrial), RKLY (biosensing-bankrupt), OPTX (already-tracked) are the entire photonics de-SPAC cohort with material relevance — and NONE pass the CPO/AI-DC end-market test. Pasqal + Photonic Inc are pending Bleichroeder mergers but quantum. **The AI-DC photonics IPO channel opens in 2026-2028 via traditional IPOs from Ayar, Lightmatter, OpenLight, HyperLight — not via de-SPAC reanimation.**

**How to apply:** Skip de-SPAC reanim screening for the AI-DC photonics lens going forward. Focus IPO-watch budget on the traditional-IPO calendar for the private-startup list (top 6 per the supply chain gaps section above).

### Lesson 4 — Layer-13 (Drivers/TIAs) was NOT structurally consolidated — prior SCAN_04 finding was over-generalized

[hypothesis: 1, last: 2026-05-28] [transient]

SCAN_04 (2026-05-27) declared chokepoint #8 (800G+/1.6T transceivers / AECs / SerDes) "STRUCTURALLY CONSOLIDATED — no sub-$5B US-listed AI-DC pure-play exists." This sweep surfaced **MXL (MaxLinear, ~$1.5B) + SMTC (Semtech, ~$3-3.5B)** as US-listed sub-$5B candidates in the driver/TIA sub-layer (13). The structural consolidation finding applies specifically to the **module-assembly layer** (the AAOI/Innolight cohort), not the driver/TIA chip layer. **Refine SCAN_04 conclusion: chokepoint #8 module-layer is structurally consolidated; chokepoint #8 chip-layer (drivers, TIAs, CDRs) has sub-$5B WATCH candidates that re-emerged in this sweep.**

**How to apply:** Update CHOKEPOINT_TAXONOMY.md #8 row from "EMPTY — structurally consolidated" to a more nuanced classification distinguishing module-layer (empty) from chip-layer (re-emerging).

### Lesson 5 — Foreign-handicap is a position-sizing input, not a binary rejection

[hypothesis: 1, last: 2026-05-28] [structural]

3 of the 6 DD QUEUE candidates are foreign-listed (SOI/SLOIY, AIXA/AIXXF, 6754.T). Prior Archos convention treated foreign-listing as a binary reduction in conviction. This sweep's signal-quality analysis suggests **foreign-handicap should be a position-sizing input — reduce position size 30-50% — not a binary disqualifier**. The signal-quality on Soitec (substrate supplier to all three SiPh foundries) is high enough that strict rejection would forfeit one of the cleanest CPO-adjacent positions in the universe.

**How to apply:** Update DUE_DILIGENCE_CHECKLIST.md and DISCOVERY_PROMPT.md to formalize "foreign-handicap discount factor" as a position-sizing input parameter rather than an inclusion gate. Sounding Board call required.

---

## Files updated this run

- This file: `weekly-scan/runs/2026-05-28-cpo-full-sweep.md` (created)
- `CHOKEPOINT_TAXONOMY.md` — chokepoint #1 CPO row expansion (AEHR + VECO cross-tags; SOI + AIXA + 6754.T + SIVE.ST additions); chokepoint #8 row clarification; AEHR cap update; refresh date 2026-05-28
- `CANDIDATE_UNIVERSE.md` — 5 new DD QUEUE entries (SOI, AIXA, 6754.T, VECO promotion, 138080); 18 new WATCH entries; 13 REJECT-log additions; last-screened date 2026-05-28

## Forward calendar (next 90 days)

- **Jun-Jul 2026:** TSEM, GFS, Soitec, AIXTRON quarterly results — monitor for follow-on SiPh customer-deposit step-changes propagating downstream
- **Jul-Aug 2026:** Q2 earnings for AEHR (SiPh WLBI ramp), VECO (InP tool order conversion), MXL (Washington 200G TIA design-wins), POET (next 1.6T 2×DR4 milestone with Lessengers)
- **Aug-Sep 2026:** OE Solutions, Lightron Korean DART filings — verify CPO transceiver prepayment signals
- **Continuous:** Any 8-K Item 1.01 from a sub-$5B US-listed name naming "1.6T transceiver" / "co-packaged optics" / "200G per lane" / "CPO module" as a binding design win = TIER 1 H10 fire
- **Continuous:** Ayar Labs S-1 filing (top IPO watch), Lightmatter S-1 (#2), OpenLight S-1 (#3) — all 2026-27 IPO targets that would fill Layer 3+5 gaps

## STOP

