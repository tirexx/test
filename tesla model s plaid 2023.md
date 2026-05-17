# Tesla Model S Plaid 2023 — Discovered Vehicle Info

Information collected from the car's touchscreen across multiple sessions and validated against public sources. Owner is based in **Kyiv, Ukraine** (gray-market import of an EU-spec car), which materially affects connectivity and feature availability — see the **Ukraine-specific notes** section.

---

## 1. Identity

| Field | Value |
|---|---|
| Profile name | `tirexx-car` |
| Model | Model S |
| Variant | **Plaid** (tri-motor: 1× front permanent magnet + 2× rear permanent magnet, 1,020 hp) |
| Model year | **2023** (VIN position 10 = `P`) |
| VIN | `5YJSA1E65PF517234` |
| Plant of manufacture | Fremont, CA, USA (VIN position 11 = `F`) |
| Market region (build-spec) | **Europe** (Navigation Data set is `EU-...`) |
| Country of operation | **Ukraine (Kyiv)** — gray-market import |
| Odometer at capture | 31,908 km |

VIN decode reference: `5YJSA1E6` corresponds to a 2023 Model S Plaid, 1-speed direct drive, ~396 mi EPA range.

---

## 2. Driver-assistance / Autopilot package

| Field | Value |
|---|---|
| AI Computer (formerly "FSD Computer") | **Full Self-Driving Computer 4 (HW4 / AI4)** |
| Autopilot package licensed | **Full Self-Driving Capability — Included package** (owned outright with the car, transfers with VIN, **not** a $99/mo subscription) |
| SAE level | **Level 2** — driver supervision required at all times (per NHTSA classification of FSD Beta / FSD Supervised) |
| FSD stack version on installed software | **FSD v14.2.2.5** (bundled with vehicle software 2026.2.9.3) |
| EU regulatory status (May 2026) | FSD (Supervised) city-streets approved in **Netherlands only**; EU-wide approval expected **Q3–Q4 2026**. Highway features (TACC, Autosteer, Navigate on Autosteer, Auto Lane Change, Autopark, Summon) are available now. **Ukraine is not on the EU type-approval roadmap**, so city-streets autonomy is not expected here in the near term. |

---

## 3. Hardware / equipment (from Additional Vehicle Information)

| Field | Value |
|---|---|
| AI computer | Full Self-Driving Computer 4 |
| Air suspension | Adaptive |
| Audio system | Premium |
| Brake package | Base (not the Plaid Track Package carbon-ceramic brakes) |
| CCS and 3rd-party NACS DC charging | Enabled |
| Cabin heater | Heat pump |
| Cell IMEI | `35 134049 804599 1` |
| Garage door opener | HomeLink 5 (Opt 2) |
| Infotainment RAM | 16 GB |
| Infotainment processor | AMD Ryzen |
| Low-voltage battery | Lithium-ion |
| Modem capabilities | 2G / 3G / 4G |
| Motor — front | Permanent magnet |
| Motor — rear | Dual permanent magnet |
| Wi-Fi MAC address | `4C:FC:AA:99:B1:B3` |
| Yoke / stalkless steering | Yes (refresh-era Model S) |

---

## 4. Software / connectivity

| Field | Value |
|---|---|
| Vehicle software | **2026.2.9.3** (released 22 March 2026) |
| Bundled FSD version | v14.2.2.5 |
| Navigation map data | `EU-2019.20` (**older revision** — needs a Wi-Fi-connected idle to pull the latest EU cycle; affects Autopark spot detection and Traffic Light & Stop Sign Control activation) |
| Premium Connectivity | Active, **expires 1 Aug 2026** (subscription is paid but largely wasted in Ukraine — see Ukraine notes) |
| Last "up to date" check | 17 May at 12:39 |

### Notable changes introduced in 2026.2.9 / 2026.2.9.3 that affect this car's UI

- The **Controls → Autopilot** menu was renamed to **Controls → Self-Driving** (regulator-driven cosmetic rename pushed by California DMV; behavior unchanged).
- "FSD Computer" was renamed to **"AI Computer"** in the UI (hence the label seen on this car's screen).
- "Navigate on Autopilot" was renamed to **"Navigate on Autosteer"**.
- The Autosteer steering-wheel icon next to the speed was removed; the engaged state now shows the text **"Self-Driving"** in blue under the speed.
- "Smart Summon" was rebranded **"ASS — Actually Smart Summon"** in 2024 (still labeled this way in 2026.2.9.x).
- New **Brake Confirm** toggle (default off) added under Self-Driving (only appears once city-streets is unlocked).
- Adds Active Road Noise Reduction, Grok with Navigation Commands (Beta), Arrival Options, charge-cable unlatch via rear-left door handle, and various cosmetic/UX features.

---

## 5. Current Self-Driving menu settings (as observed on the car)

Captured live from **Controls → Self-Driving** on this car:

| Setting | Current value | Notes |
|---|---|---|
| Strikeout counter | "This vehicle has not had any such events." | Clean record — Autosteer disables after 5 strikeouts; reset on next park. |
| Cruise Follow Distance | **2** | Scale 1–7. Fairly close — recommend **3–4** for normal driving. |
| Autosteer Activation | **Single Click** | One press of the right scroll button engages Autosteer + TACC. |
| Navigate on Autosteer (Beta) | **ON** | Highway feature — handles motorway interchanges/exits. "Customize Navigate on Autosteer" sets lane-change profile (Mild / Average / Mad Max). |
| Traffic Light and Stop Sign Control (Beta) | **OFF** with note "requires updated maps. Connect to WiFi to download latest maps." | Toggle present (licensed on car) but blocked by stale `EU-2019.20` maps and EU regional gating. |
| Set Speed | **Speed Limit** | Engaging cruise sets target = detected limit + offset. |
| Offset (Set Speed) | **Fixed** = **+19 km/h** | High — at 100 km/h limit the car will Autosteer at 119 km/h. Recommend dropping to **+0 to +10 km/h** or switch to **Percentage +5–10%**. |
| ASS (Actually Smart Summon) | **ON** | Driving the empty car to the user via the Tesla app on private property. |
| Speed Limit Warning | **Display** | Visual-only nag when exceeding limit by the offset below. |
| Speed Limit (warning mode) | **Relative** | Warns based on how far over the detected limit you are. |
| Offset (Speed Limit Warning) | **+0 km/h** | Warns the moment you cross the limit. |
| Forward Collision Warning | **Medium** | Default. Late = lazy; Early = twitchy; Medium is the right choice. |
| Lane Departure Avoidance | **Warning** | Visual + yoke vibration. **Recommend switching to "Assist"** for active correction. |
| Emergency Lane Departure Avoidance | **ON** | Auto-corrects steering away from oncoming traffic / off-road edges. Keep on. |
| Automatic Emergency Braking | **ON** ("Disable Autosteer to modify") | Mandatory in EU under GSR; cannot be disabled while Autosteer is enabled. Keep on. |
| Obstacle-Aware Acceleration | **ON** | Limits motor torque if an object is detected ahead at low speed. Critical on a 1,020 hp car. Keep on. |
| Green Traffic Light Chime | **ON** | Sounds when the light ahead turns green / car ahead moves. Personal preference. |

### Toggles that are **NOT** present on this car (diagnostic — they tell us what's gated)

- ❌ **Autosteer on City Streets** — not present → FSD Supervised city-streets driving is not unlocked for the user's country.
- ❌ **Speed Profile / Chill / Average / Assertive** — only appears once city-streets is unlocked.
- ❌ **Brake Confirm** — only appears with city-streets driving active.

So: **the car is fully ready** (HW4, FSD owned, latest software, FSD v14.2.2.5 stack). Regulators haven't switched on the city-streets piece for the user's country.

### Recommended changes (for this owner)

1. **Cruise Follow Distance → 3 or 4** (less tailgaty on motorway).
2. **Cruise Offset +19 km/h → +5 km/h Fixed**, or **+5–10% Percentage** (cameras across EU/UA enforce well below +19).
3. **Lane Departure Avoidance: Warning → Assist**.
4. **Update maps over Wi-Fi** (required to ever turn on Traffic Light & Stop Sign Control).
5. (Optional) **Speed Limit Warning → Chime** for stricter camera enforcement zones.
6. **Customize Navigate on Autosteer → Mild or Average** for lane-change aggressiveness on motorway.

---

## 6. Available driver-assist features on this specific car (today)

### Available now in EU markets (HW4 + FSD owned + 2026.2.9.3)

- Traffic-Aware Cruise Control (TACC)
- Autosteer (highway / divided road lane keeping)
- Auto Lane Change (with optional confirmation)
- Navigate on Autosteer (motorway interchanges and exits) — Mild / Average / Mad Max profiles
- Autopark (vision-based, square "P" icon)
- Actually Smart Summon (ASS)
- Forward Collision Warning, Automatic Emergency Braking, Lane Departure Avoidance, Emergency Lane Departure Avoidance, Obstacle-Aware Acceleration, Blind Spot warning

### Region-gated (present on the car but only unlocked once the user's country approves FSD Supervised)

- Traffic Light and Stop Sign Control
- Autosteer on City Streets
- Full Self-Driving Profile (Chill / Average / Assertive)
- Brake Confirm toggle

---

## 7. How to engage Autopilot on this car

Because the car is HW4 + stalkless yoke + Autosteer Activation = **Single Click**:

1. Set a destination in the map (only required for Navigate on Autosteer, not plain Autosteer).
2. Drive onto a **motorway / dual carriageway** with clear lane markings.
3. Press the **right scroll button** on the yoke **once**. Autosteer + TACC engage simultaneously.
4. With Navigate on Autosteer ON and a destination set, the car handles interchanges and exits.
5. Keep light torque on the yoke and eyes on the road — the cabin camera enforces this.
6. Disengage by **pushing the right scroll button up**, **tapping the brake**, or **torque-overriding the steering**.

### What the car will and will NOT follow on a navigation route

| Phase of a trip | Who drives |
|---|---|
| Surface streets / city → motorway on-ramp | **Driver** (no autonomous turning available in Ukraine) |
| Merging onto motorway | Engage Autosteer once in a marked lane |
| Motorway with NoA on, destination set | **Car follows the route** — lane keeping, overtaking lane changes, takes interchange splits and exits |
| Off-ramp / road class drops | Banner *"Take over now"* — driver resumes |
| Surface streets / arrival | **Driver** |

Plain Autosteer cannot turn at intersections. Navigate on Autosteer is **motorway-only**. City-streets autonomy is not unlocked in Ukraine. For city trips like the 1.5 km Воскресенська St. example, **the user must drive manually**.

---

## 8. Autopark — usage on this car

### Conditions for the **P icon** to appear

- Crawl past a row of empty bays at **< 13 km/h** (perpendicular) or **< 21 km/h** (parallel).
- Bay must be ≥ 2.2 m wide with at least three visible lines or distinct curbs.
- Flat, paved surface — not cobblestone, brick, or gravel.
- Cameras clean and calibrated.

### Where the P appears on screen

- On the **left half of the touchscreen**, inside the 3D driving visualisation.
- Hovering **over the detected bay** in the rendered scene, near the rendered car.
- Square translucent badge with a white "P" inside.
- Multiple Ps may appear simultaneously for several detected bays — any can be tapped.

### Procedure

1. Crawl past the row of bays.
2. Stop ~one car length past the chosen bay.
3. Tap the **P icon** on the touchscreen.
4. Shift to **Reverse**.
5. Tap **Start Autopark**, hands off, foot near brake.
6. Car steers/accels/brakes itself, completes parking, shifts to Park.

Abort with: touching the wheel, pressing the brake, or tapping Cancel.

---

## 9. Where to find each piece of info on the car

| Goal | Path on touchscreen |
|---|---|
| Which Autopilot package the VIN owns | **Controls → Software** (top of the page; this is where "Full Self-Driving Capability — Included package" was confirmed) |
| Hardware spec details | **Controls → Software → Additional Vehicle Information** |
| Buy/manage subscription | **Controls → Upgrades** (or in the Tesla app) |
| Driver-assist toggles | **Controls → Self-Driving** (formerly Controls → Autopilot before 2026.2.9) |
| Change Autosteer engagement gesture | **Controls → Self-Driving → Autosteer Activation** (Single Click / Double Click) |
| Wi-Fi networks & "Remain Connected in Drive" | **Controls → Wi-Fi** (or the Wi-Fi icon in top-right status bar) |
| Power off / soft reboot | **Controls → Safety → Power Off**, or hold **both yoke scroll wheels** for 10 s for soft reboot |
| Suspension ride height | **Controls → Suspension** |
| Acceleration mode (Standard/Sport/Plaid/Drag Strip) | **Controls → Pedals & Steering** |

---

## 10. Connectivity — Ukraine-specific notes (CRITICAL)

This car operates day-to-day in Kyiv, which materially changes how connectivity works.

### What's broken in Ukraine

- **Tesla doesn't operate in Ukraine** — no Superchargers, no service centers, no Tesla roaming agreements with Ukrainian carriers.
- The **factory eSIM/SIM gets no usable cellular data** in Ukraine (Tesla Premium Connectivity works only in Tesla's official markets — US/CA/EU/EEA/UK/etc.).
- Tesla has **deprioritized / removed Ukraine from its EU online routing service** since ~2024. As a result, even with internet access, the in-car nav banner shows **"Navigating without connectivity"** while the offline routing engine still produces a valid blue-line route from the local map data.
- Map updates (`EU-2019.20` is stale) are intermittent because Tesla's EU map cycle no longer includes full Ukraine coverage.

### What still works

- **Offline turn-by-turn navigation** using the locally stored `EU-2019.20` map data — distances, ETAs, voice prompts, route line on screen.
- **All driver-assist features** — they don't require Tesla cloud connectivity (TACC, Autosteer, Navigate on Autosteer on motorways, Autopark, Lane Departure, FCW, AEB).
- **Vehicle software updates** — once the car has Wi-Fi, OTA still works.
- **Tesla app remote control** — works as long as the car has Wi-Fi.

### Practical workarounds (what local Tesla owners actually do)

| Option | What | Effort | Result |
|---|---|---|---|
| **A. Phone hotspot** | Phone's Personal Hotspot, connect car via **Controls → Wi-Fi**, toggle **"Remain Connected in Drive" ON** | 2 minutes | Live traffic / search / Grok / streaming work; "Navigating without connectivity" banner may still appear because Tesla's online routing has dropped Ukraine, but everything else is online. |
| **B. Permanent in-car 4G router** | Mobile router (Huawei E5577, GlocalMe, Netgear M6, etc.) with a **Kyivstar / Vodafone UA / lifecell** SIM, USB-C powered, in glovebox | 1 hour setup | Same as Option A, but no phone-hotspot dance. ~₴1500–3500 hardware, ~₴100–200/month data. |
| **C. Custom SIM in TCU** | Open headliner, insert local SIM in the Telematics Control Unit, switch from built-in eSIM to external SIM via Tesla Toolbox 3 (Service+ subscription, VPN required to purchase) | Half-day, technical | Native cellular like a non-gray car. Risks reverting on software updates; voids any goodwill. |

### Why "Navigating without connectivity" persists even after Wi-Fi is connected with Remain Connected in Drive ON

Verified during this owner's session:

1. Wi-Fi connected, working internet, "Remain Connected in Drive" toggled ON.
2. Banner still appears.

Cause: Tesla's **online routing backend** (separate from general internet) no longer serves Ukraine reliably. The car's offline routing engine produces the route from local maps, but Tesla flags this as "without connectivity" to indicate live traffic / charging-stop planning / online rerouting are unavailable.

**Mitigations:**

- **Soft reboot** (hold both yoke scroll wheels 10 s) — sometimes clears a stale cached state if the banner pre-dated Wi-Fi coming up.
- **Ignore the banner** — offline route still functions correctly.
- **Use Google Maps / Waze on a phone** for current Ukrainian POIs, road closures, live traffic. Most Kyiv-based Tesla owners do this.
- **Account region change** to a neighboring EU country (Poland) via the Tesla app sometimes restores online routing — mixed reports.
- **Periodically connect to home Wi-Fi** for several hours to give the car a chance to download newer maps when available.

### Configurable Wi-Fi options on this car

- **Controls → Wi-Fi** → select network → toggle **"Remain Connected in Drive"** (without this, Wi-Fi drops the moment the car is shifted out of Park, and "Navigating without connectivity" returns).

---

## 11. Sources used for validation

- Tesla Model S Owner's Manual (Controls and Autopilot sections) — <https://www.tesla.com/ownersmanual/models/en_us/GUID-29A7E205-A689-41D1-B69C-3AE821CB70E7.html>
- Tesla support — Full Self-Driving (Supervised) Subscriptions — <https://www.tesla.com/support/full-self-driving-subscriptions>
- Tesla support — Wi-Fi connectivity for Model S — <https://www.tesla.com/ownersmanual/models/en_us/GUID-1FE9620C-3D7F-4FD3-BBD9-28DD342AC150.html>
- NHTSA recall report 23V-085 (FSD Beta classified as SAE Level 2) — <https://static.nhtsa.gov/odi/rcl/2023/RCLRPT-23V085-9893.PDF>
- Not a Tesla App — Official 2026.2.9.3 release notes — <https://www.notateslaapp.com/software-updates/version/2026.2.9.3/release-notes>
- Not a Tesla App — Tesla removes "Autopilot" name in 2026.2.9 — <https://www.notateslaapp.com/news/3719/tesla-kills-the-autopilot-name-in-new-software-update>
- Teslascope — 2026.2.9.3 / FSD 14.2.2.5 mapping — <https://teslascope.com/software/2026.2.9.3>
- Tessie — 2026.2.9 release notes (Controls → Self-Driving rename, Brake Confirm, AI Computer rename) — <https://stats.tessie.com/versions/2026.2.9>
- VIN Inspect — 2023 Model S VIN decoder — <https://vininspect.com/vin/tesla/model-s/2023/5yjsa1e65pf>
- 17vin — `5YJSA1E6` = 2023 Model S Plaid 1,020 hp — <https://en.17vin.com/model/df7c2.html>
- Tesla FSD Europe regulatory tracker — <https://fsdtracker.eu/>
- Wards Auto — Netherlands type approval of FSD Supervised (April 2026) — <https://www.wardsauto.com/news/tesla-fsd-supervised-approved-the-netherlands/817279/>
- Drive Tesla Canada — Swedish Transport Agency on EU-wide rollout 2026 — <https://driveteslacanada.ca/news/tesla-fsd-europe-approval-sweden-2026/>
- Tesla North — Single Pull vs. Double Pull Autosteer on stalkless yoke — <https://teslanorth.com/2023/11/15/tesla-debuts-single-pull-autosteer-feature-for-cars-with-stalks>
- Tesla North — FSD 14 UI redesign / Autosteer icon removal — <https://teslanorth.com/2025/10/10/tesla-fsd-14-drops-autosteer-icon-in-ui-redesign/>
- TeslaDB — Autopark P icon visualisation — <https://tesladb.dev/releases/2024.20/autopark>
- Tesla MOTORS Club — "P icon appears briefly on display" thread (location of Autopark P on screen) — <https://teslamotorsclub.com/tmc/threads/saw-a-p-icon-appear-briefly-on-display-whats-that.182172/>
- Oleg Kutkov — Custom SIM in Tesla Model 3 2024+ / Model Y 2025+ / Cybertruck (Ukrainian Tesla connectivity workaround) — <https://olegkutkov.me/2025/05/12/custom-sim-card-in-tesla-model-3-2024-tesla-model-y-2025-and-cybertruck/>
- Oleg Kutkov — Tesla Model 3 US LTE modem replacement and reverse engineering — <https://olegkutkov.me/2021/06/10/tesla-model-3-us-lte-modem-replacement-and-some-reverse-engineering/>
- Tesla Motors Club — LTE connection interrupts crossing borders in EU — <https://teslamotorsclub.com/tmc/threads/lte-connection-interrupts-by-crossing-borders-in-eu.305562/>
- Change.org — petition to reinstate Ukraine on Tesla EU navigation maps — <https://www.change.org/p/request-to-reinstate-ukraine-on-tesla-s-navigation-maps-for-the-eu-region>
- DRIVER.TOP (UA) — Tesla Model 3 region change NA → EU for Ukrainian users — <https://driver.top/exp/583583/>
- Tesla DIY Repair — "Tesla LTE not working" troubleshooting (soft reboot / power cycle procedure) — <https://tesladiyrepair.com/posts/tesla-lte-connectivity-issues/>
