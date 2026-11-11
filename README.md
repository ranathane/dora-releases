# 📡 D.O.R.A. (Domestic Outfitting & Repair Assistant)
### Autonomous Flight-Deck Co-Pilot & Systems Telemetry Suite for Elite Dangerous
* **Lead Systems Architect & Builder:** CMDR Ranathane
* **Autonomous Flight Co-Pilot & Sentinel:** Theodora "Dora" Thorne
* **Operational Cycle:** Sortie 0.3 Alpha Baseline
* **Distribution Gateway:** [GitHub Releases](https://github.com/ranathane/dora-releases)
* **Communications Uplink:** Ranathane Farms Discord | **Crash Telemetry:** dorabugreports@gmail.com

---

> **"Spansh is the source of truth for the galaxy. D.O.R.A. is the engine that drives you through it."**  
> *"Ranathane built the frame. Dora flies the ship. Shen checks the torque. Jax sells the iron."*

---

## 🚀 OVERVIEW

D.O.R.A. is a sovereign, local-first, zero-cloud desktop avionics suite engineered specifically for veteran haulers, deep-space explorers, combat wings, and fleet carrier commanders in *Elite Dangerous*. 

Unlike traditional third-party web tools that suffer from browser lag, API rate limits, CORS overhead, and server downtime on Thursday maintenance ticks, D.O.R.A. runs directly on your local silicon. Compiled native in C++ and Rust under **Tauri v2** (~90,000 lines of code) with a customized **SvelteKit aerospace MFD glass**, D.O.R.A. operates completely offline during flight.

### Game Version Support:
* **Elite Dangerous: Odyssey (Live 4.0)**
* **Elite Dangerous: Horizons (Legacy 3.8 Multi-Universe Parity)**  
  *(Strict database segregation ensures Legacy sessions never cross-contaminate live galactic data).*

---

## 🛠️ CORE SUBSYSTEMS & CAPABILITIES

### 1. 108 GB Offline 10-Database Partition (3NF SQLite)
* **Zero Playtime Web API Dependencies:** Following an initial one-time freight haul to populate your local partition (via monthly deltas or full galactic archives), all astrogation, market queries, mining appraisals, and cartography lookups execute 100% locally from your own NVMe.
* **The Cartography Vault:** Indexes 601M celestial bodies, 845k starports, 101.7M commodity prices, 3.58M pulsars, and 1.11M mineral rings cold on disk with nanosecond B-Tree seeks.
* **4-Lane Turbo Spansh Depot:** High-velocity parallel WAN downloader with authentic Lockout/Tagout (LOTO) runway hazard interlocks active across the flight glass during hot database writes.

### 2. Sovereign Offline Neural Speech (Kokoro-82M ONNX)
* **Pure Local CPU Execution:** Shipped cold in `data/kokoro` with `model.onnx` (<60 MB memory footprint, <20 ms inference latency). Completely purged of external AI server daemons (no Ollama).
* **Closed Voice Manifold:** 13 distinct pilot personas with runtime phonetic dictionary compilation (`lexicon.tab`) and sub-millisecond contextual heteronym disambiguation (`live`, `permit`, `lead`, `close`, `read`).
* **Margaret Hamilton AGC Audio Dispatcher:** 3-tier prioritized audio pipeline ensuring critical warnings (canopy breach, shield collapse, heat runaway) instantly pre-empt tactical or ambient barks.

### 3. Star Caster P2P Astrogation (Nav Engine V2)
* **Direct CMDR-to-CMDR Routing:** Export routes as raw system ID64 integer streams. Copy a 22,000 Ly route to your clipboard with one click and hand it to a wingmate without waiting for any third-party database to sync.
* **Gate Zero O(1) Short-Circuit:** Sub-millisecond routing (0.0002s) for single-hop targets within jump range.
* **Ranathane’s Line & Compass:** High-speed commuter vector projection solving short routes (50–500 Ly) in **2 to 5 seconds**.
* **Trans-Galactic Highway Solver:** Exhaustive, branch-and-bound local A* solver. Tested across 23,311 Ly (Exphiay to Colonia) producing a razor-sharp **73-hop master corridor** (69 neutron leaps) completely offline.

### 4. Frontline Operations & Wingman Accountability
* **Operational Dropship State Machine:** Full combat sortie tracking across departure, planetary insertion, combat zone triage, and dropship extraction.
* **Hybrid Loot Harvester:** Live capture of Frontline victory drops, segregating 13 Odyssey on-foot microresources from 3 Horizons ship engineering materials.
* **Mercenary Coin Ledger:** Monitors the 1,000 Merc Coin weekly allowance cap, strictly synchronized to the Thursday 07:00 UTC Powerplay reset.
* **Table 17 Wingman Reliability Index:** 3-strike persistent ledger logging wingman disconnections, desertions, and combat efficacy with solid gold-star flight badges.

---

## 🎛️ THE 13 FLIGHT-DECK CONSOLES

1. **Tactical Flight Deck & HUD:** 3-column glass MFD with port kinetics, center command viewport, and starboard sector reconnaissance.
2. **Starship Hangar & Chassis Kinetics:** 4-cluster avionics, 57 canonical ship hulls, 16:9 cinematic widescreen portraits, and slide-out Engineering Forge Drawer.
3. **Quartermaster Inventory & Odyssey Locker:** Horizons G1–G5 materials, Odyssey microresources with liquidation valuation, and unified 1,000-unit carrier storage tracking.
4. **Operations, Frontline & Combat:** BGS contracts, CG rewards, Frontline raid state machine, Table 17 Wingman Roster, and "The Looker" 4-wide pirate massacre stacking radar.
5. **Quartermaster Workshop & Engineering:** 38 canonical engineer workshops with live unlock referral chains, 3-vector pilot profiling, and cumulative deficit shopping lists.
6. **Galaxy Explorer:** Unified astrogation workspace combining Route Calculator, 2-Opt Road to Riches Surveyor, Procedural Ghost Probes, Exobiology Radar, and Surface GPS.
7. **Expedition Route Planner:** 3-way route parser (Spansh JSON, ID64 streams, or plain-text) with anti-snapback latches and dual 2D/3D holotank portals.
8. **Freight Dispatcher & Trade Radar:** 500 Ly bubble freight radar and 3-Leg Triangular Trade Route Solver with 3D spatial voxel acceleration.
9. **Mining & Prospecting Radar:** In-RAM vector matcher querying 1.11M rings in <1 ms, 4-bit nibble hotspot overlap counters, and live pure-ore extraction stopwatch (T/hr).
10. **Powerplay 2.0 War Room:** 13-leader territory advisor, reverse-engineered mining merit calculators, and native EICAS combat directive hardpoint sniffer.
11. **Sovereign Colony Logistics & CAD Orrery:** Multi-commodity procurement radar and 15 Ly frontier expansion candidate scout.
12. **Flagship Bridge & Carrier Deck:** Discrete 37-field CarrierDetail model, 25,000T displacement bar, upkeep runway clock, and visitor market sales.
13. **Cockpit Settings & Spansh Depot:** 5-chamber Spansh cartography depot with 4-Lane Turbo WAN controls, theme palettes, and sovereign telemetry gateways.

---

## 📦 QUICK-START INSTALLATION & DEPLOYMENT (SOP)

D.O.R.A. is a portable, zero-installer aerospace suite.

1. **Download:** Grab the latest `DORA-Sortie-0.3-Alpha.zip` from [GitHub Releases](https://github.com/ranathane/dora-releases).
2. **Extract:** Unzip the archive directly into a dedicated root folder on a fast drive.
3. **First Boot:** Launch `dora-app.exe`. On startup, the event-sourced engine automatically locates your local Elite Dangerous journal directory (`%USERPROFILE%\Saved Games\Frontier Developments\Elite Dangerous`), building your local black box state in seconds.
4. **Populate Cartography:** Open `Settings -> Spansh Cartography Depot` to pull your database partition via 4-Lane Turbo.
5. **Flight Covenant:** Click **ENGAGE FLIGHT DECK / PILOT & SENTINEL COVENANT** to hydrate the 13 cockpit consoles.

### ⚠️ WHERE TO EXTRACT D.O.R.A. (AVOIDING VACUUM LEAKS)

Because D.O.R.A. manages high-throughput local SQLite databases running in WAL mode with memory-mapped I/O, directory placement is critical:

🟢 **RECOMMENDED FLIGHT-DECK LOCATIONS:**
* `C:\DORA\`
* `D:\DORA\` or `D:\Games\DORA\`
* `C:\Users\<YourUsername>\DORA\`

🔴 **STRICTLY PROHIBITED (WILL CRACK CANOPY GLASS):**
* ❌ `C:\Program Files` or `C:\Program Files (x86)`: Windows User Account Control (UAC) blocks SQLite background write locks and will corrupt your flight logs.
* ❌ `OneDrive`, `Google Drive`, or `Dropbox` synced folders: Cloud sync engines hook into SQLite `-wal` and `.db` files mid-flight, causing severe I/O crashes and catastrophic database corruption.
* ❌ Root drive directory directly (`C:\` without a subfolder): Windows root security permissions prevent proper file creation without elevated Administrator privileges.

---

## 🔒 THE SOVEREIGN PRIVACY & TELEMETRY BOUNDARY

* **100% Local Silicon:** D.O.R.A. runs entirely on your own hardware. Your flight history, system visits, trade profits, material inventories, and credit balances are stored locally in SQLite and are never transmitted to any commercial or third-party server.
* **Strict EDDN Community Relay:** Verified system cartography and market prices are forwarded to the community EDDN network strictly when your vessel physically arrives in the system. **We never forward unvisited math.**
* **Frontier CAPI Direct:** The optional Frontier Companion API gateway connects directly to Frontier Developments' secure OAuth2 PKCE servers. Encrypted access tokens are held strictly on your machine in `dora_nav.db`.

---

## 📡 COMMUNICATIONS & ANOMALY TRIAGE

When operating on the rim, equipment encounters stress. If you experience an unhandled panic or journal parse anomaly:

* **Vector Alpha (Tactical Chat & Wing Comms):** Join the [Ranathane Farms Discord](https://discord.gg/) `#dora-flight-test` channel for live triage and sortie updates.
* **Vector Beta (Verified Reproducible Defects):** Open a ticket under the repository's **Issues Tab**.
* **Vector Gamma (Crash Dumps & Black Box Logs):** Forward your `dora-app.log` and active journal file to: `dorabugreports@gmail.com`

---

*Fly safe, check your line valves, and keep your throttle wide open.*  
**o7 Commanders!**
