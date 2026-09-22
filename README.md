# 📡 D.O.R.A. (Domestic Outfitting & Repair Assistant)
### Autonomous Flight-Deck Co-Pilot & Systems Telemetry Suite for Elite Dangerous
* **Lead Architect:** CMDR Ranathane (TRUCKERS GONE WILD [TGW1])
* **Autonomous Co-Pilot & Core Intelligence:** Theodora "Dora" Thorne
* **Operational Status:** ALPHA FLIGHT-TEST PROGRAM (CLOSED SORTIE)
* **Communications Uplink:** [Ranathane Farms Discord](https://discord.gg/cXuBNfpbDB) | **Crash Telemetry:** `dorabugreports@gmail.com`

---

## 🚀 OVERVIEW

D.O.R.A. is a native, zero-cloud, high-performance desktop avionics suite engineered specifically for veteran haulers, explorers, fleet carrier commanders, and systems engineers in *Elite Dangerous: Odyssey (4.0)*. 

Unlike traditional web-based third-party tools that suffer from browser latency, CORS restrictions, and external server downtime, D.O.R.A. runs directly on your local bare metal using a high-velocity **Tauri v2 + Native Rust** engine coupled to a customized **SvelteKit** flight-deck HUD.

### Key Flight-Deck Capabilities:
* **The Sovereign Black Box:** Deterministic event-sourced journal replay that reconstructs your entire commander career, active fleet, stored modules, carrier inventory, and engineering inventory directly into high-speed local SQLite databases.
* **Colonisation System Architect & Vector Orrery:** Comprehensive CAD blueprints for the new Frontier Colonisation initiative. Features an EDSY-style drag-and-drop facility staging rack for outfitting *entire star systems* with orbital stations, planetary ports, and outposts—complete with ILS glide-slope landing beacons, orthogonal moon rails, and persistent hand-calibrated layouts *(Note: this is for star system architectural construction, not starship module loadouts)*.
* **Quartermaster Engineering Matrix:** 100% 3NF relational blueprint tracker calculating exact multi-roll material deficits across all Horizons and Odyssey workshops without external API lag.
* **Carrier Double-Entry Manifest:** Real-time reconciliation of your carrier's market trades and private non-market cargo vaults.
* **Frontier CAPI Deep Integration:** Official OAuth2 PKCE link straight to Frontier Developments for live profile, ship loadout, and fleet carrier synchronization.

---

## ⚠️ ALPHA FLIGHT-TEST CLEARANCE (THE 21-DAY OPERATIONAL FUSE)

D.O.R.A. is currently in **active flight testing**. By participating in this alpha phase, you are operating an experimental avionics testbed under heavy engineering iteration.

### The 21-Day Sortie Cycle:
* **Operational Expiration:** Each alpha sortie build is calibrated with a **21-day flight clearance timer**.
* **Why the fuse exists:** In active aerospace software development, running outdated, uncalibrated builds produces ghost bugs that have already been patched in our skunkworks branch. The 21-day fuse prevents abandoned legacy builds from floating around the black.
* **Renewing Your Flight Clearance:** When your 21-day sortie window expires, the HUD will display a debrief alert with a link to submit a brief pilot feedback report. Once submitted, you will receive the clearance link to download the newest sortie build from GitHub Releases.

---

## 🛠️ FLIGHT-DECK PREREQUISITES & SPECIFICATIONS

* **Operating System:** Windows 10 / Windows 11 (64-bit AMD64).
* **Game Version:** *Elite Dangerous: Odyssey (Live 4.0)*.
* **System Web Engine:** Microsoft Edge WebView2 Runtime (pre-installed by default on modern Windows 10/11).
* **Display Resolution:** Optimized for 1080p, 1440p, and 4K ultra-wide flight-deck monitors.
* **Data Footprint:** The initial Alpha Starter Kit includes core ship, module, blueprint, and engineering databases (~2 MB). Your flight history will build automatically from your local game journals.

---

## 📦 QUICK-START INSTALLATION (BREAKING PAD LOCKS)

1. **Download the Latest Release:**
   Head to the **[Releases Tab](https://github.com/ranathane/dora-releases/releases)** on this repository and download the latest `Dora-Setup-v0.x.x-alpha.exe` (or standalone portable `.zip`).
2. **Run the Installer:**
   Launch the installer. If Windows SmartScreen prompts on this unsigned experimental alpha binary, click **More info** -> **Run anyway**.
3. **First-Boot Automatic Calibration:**
   * Launch D.O.R.A.
   * On first boot, D.O.R.A. automatically locates your Elite Dangerous journal directory (`%USERPROFILE%\Saved Games\Frontier Developments\Elite Dangerous`).
   * Allow D.O.R.A. a few seconds to ingest your black box journals. Your ships, materials, carrier balances, and current transponder status will hydrate across the HUD.
4. **Frontier CAPI Authentication (Optional but Recommended):**
   * Navigate to the **Settings** console on the cockpit glass.
   * Click **Link Frontier CAPI Account**.
   * A browser window will open to Frontier Developments' secure login. Authorize D.O.R.A.
   * Once approved, the local listener will secure your encrypted tokens into `dora_nav.db` and unlock live fleet loadouts and carrier cargo orders.

### ⚠️ IMPORTANT: WHERE TO EXTRACT D.O.R.A. (AVOIDING VACUUM LEAKS)

Because D.O.R.A. is a portable, high-velocity avionics suite that manages local SQLite databases:

* 🟢 **RECOMMENDED FLIGHT-DECK LOCATIONS:**
  * `C:\DORA\`
  * `D:\DORA\` or `D:\Games\DORA\`
  * `C:\Users\<YourUsername>\DORA\`

* 🔴 **STRICTLY PROHIBITED (WILL CRACK CANOPY GLASS):**
  * ❌ **`C:\Program Files` or `C:\Program Files (x86)`:** Windows User Account Control (UAC) blocks background SQLite write locks and will corrupt your flight logs.
  * ❌ **OneDrive, Google Drive, or Dropbox synced folders:** Cloud sync engines lock SQLite `-wal` and `.db` files mid-flight, causing severe IO crashes and database corruption.
  * ❌ **Directly on `C:\` root (without a folder):** Windows root directory permissions prevent file creation without Administrator elevation.

---

## 🔒 THE SOVEREIGN PRIVACY INVARIANT

* **100% Local Silicon:** D.O.R.A. does **not** transmit your journal telemetry, flight coordinates, market trades, personal balances, or login credentials to any centralized third-party server.
* **Air-Gapped Sovereign Databases:** All flight data is held strictly on your machine in local SQLite databases (`dora_user.db`, `dora_nav.db`).
* **Frontier Direct:** The only external comms link is the direct, official OAuth2 CAPI gateway talking straight to `frontierstore.net`.

---

## 📡 COMMUNICATIONS & ANOMALY REPORTING

When operating on the rim, equipment encounters stress. If you experience an unhandled panic, UI glitch, or journal parse anomaly:

1. **Comms Vector Alpha (Crash Dumps & Black Box Logs):**
   * Email your `dora-app.log` and your latest Elite Dangerous journal file directly to:
   * **`dorabugreports@gmail.com`**
2. **Comms Vector Beta (Tactical Chat & Wing Comms):**
   * Join the **[Ranathane Farms Skunkworks Discord](https://discord.gg/cXuBNfpbDB)**.
   * Head into the `#dora-flight-test` channel for live feedback, triage, and sortie updates.
3. **Comms Vector Gamma (Verified Reproducible Bugs):**
   * Open a ticket under the **[Issues Tab](https://github.com/ranathane/dora-releases/issues)** using our Bug Report Template.

---

*Fly safe, check your line valves, and keep your throttle wide open.*  
**o7 Commanders!**
