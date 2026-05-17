# Tesla Model S Plaid 2023 — Discovered Vehicle Info

Information collected from the car's touchscreen (Controls → Software and Controls → Software → Additional Vehicle Information) and validated against public sources.

## Identity

| Field | Value |
|---|---|
| Profile name | `tirexx-car` |
| Model | Model S |
| Variant | **Plaid** (tri-motor: 1× front permanent magnet + 2× rear permanent magnet) |
| Model year | **2023** (VIN position 10 = `P`) |
| VIN | `5YJSA1E65PF517234` |
| Plant of manufacture | Fremont, CA, USA (VIN position 11 = `F`) |
| Market region | **Europe** (Navigation Data set is `EU-...`) |
| Odometer at capture | 31,908 km |

VIN decode reference: `5YJSA1E6` corresponds to a 2023 Model S Plaid, 1,020 hp, 1-speed direct drive.

## Driver-assistance / Autopilot

| Field | Value |
|---|---|
| AI Computer (formerly "FSD Computer") | **Full Self-Driving Computer 4 (HW4 / AI4)** |
| Autopilot package licensed | **Full Self-Driving Capability — Included package** (owned outright with the car, not a subscription) |
| SAE level | **Level 2** — driver supervision required at all times (per NHTSA classification of FSD Beta / FSD Supervised) |
| FSD stack version on installed software | **FSD v14.2.2.5** (bundled with vehicle software 2026.2.9.3) |
| EU regulatory status (May 2026) | FSD (Supervised) city-streets approved in the Netherlands only; EU-wide approval expected Q3–Q4 2026. Highway features (TACC, Autosteer, Navigate on Autosteer, Auto Lane Change, Autopark, Summon) are available now. |

## Hardware / equipment (from Additional Vehicle Information)

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

## Software / connectivity

| Field | Value |
|---|---|
| Vehicle software | **2026.2.9.3** (released 22 March 2026) |
| Bundled FSD version | v14.2.2.5 |
| Navigation map data | `EU-2019.20` (older revision — recommend a Wi-Fi-connected idle to pull the latest EU map cycle) |
| Premium Connectivity | Active, **expires 1 Aug 2026** |
| Last "up to date" check | 17 May at 12:39 |

### Notable changes introduced in 2026.2.9 / 2026.2.9.3 that affect this car's UI

- The **Controls → Autopilot** menu was renamed to **Controls → Self-Driving** (regulator-driven cosmetic rename pushed by California DMV; behavior unchanged).
- "FSD Computer" was renamed to **"AI Computer"** in the UI (hence the label seen on this car's screen).
- "Navigate on Autopilot" was renamed to **"Navigate on Autosteer"**.
- The Autosteer steering-wheel icon next to the speed was removed; the engaged state now shows the text **"Self-Driving"** in blue under the speed.
- New **Brake Confirm** toggle (default off) added under Self-Driving.
- Adds Active Road Noise Reduction, Grok with Navigation Commands (Beta), Arrival Options, charge-cable unlatch via rear-left door handle, and various cosmetic/UX features.

## Available driver-assist features on this specific car (today)

Available now (EU + HW4 + FSD owned + 2026.2.9.3):

- Traffic-Aware Cruise Control (TACC)
- Autosteer (highway / divided road lane keeping)
- Auto Lane Change (with optional confirmation)
- Navigate on Autosteer (motorway interchanges and exits) — Mild / Average / Mad Max profiles
- Autopark
- Summon (Smart Summon availability is country-dependent in the EU)
- Forward Collision Warning, Automatic Emergency Braking, Lane Departure Avoidance, Blind Spot warning

Region-gated (present on the car but only unlocked once the user's EU country approves FSD Supervised):

- Traffic Light and Stop Sign Control
- Autosteer on City Streets
- Full Self-Driving Profile (Chill / Average / Assertive)

## Where this info was found on the car

- **Controls → Software** — model, VIN, AI computer, FSD package status, Premium Connectivity expiry, software version, navigation data version.
- **Controls → Software → Additional Vehicle Information** — detailed hardware spec list (motors, brakes, suspension, audio, infotainment, modem, MAC, IMEI, charging, garage door).
- **Controls → Self-Driving** (formerly **Controls → Autopilot** before software 2026.2.9) — live list of toggles available, gated by package + region.
- **Controls → Upgrades** — purchase / subscription status (not needed here, FSD is already included).

## Sources used for validation

- Tesla Model S Owner's Manual (Controls and Autopilot sections) — <https://www.tesla.com/ownersmanual/models/en_us/GUID-29A7E205-A689-41D1-B69C-3AE821CB70E7.html>
- Tesla support — Full Self-Driving (Supervised) Subscriptions — <https://www.tesla.com/support/full-self-driving-subscriptions>
- NHTSA recall report 23V-085 (FSD Beta classified as SAE Level 2) — <https://static.nhtsa.gov/odi/rcl/2023/RCLRPT-23V085-9893.PDF>
- Not a Tesla App — Official 2026.2.9.3 release notes — <https://www.notateslaapp.com/software-updates/version/2026.2.9.3/release-notes>
- Teslascope — 2026.2.9.3 / FSD 14.2.2.5 mapping — <https://teslascope.com/software/2026.2.9.3>
- VIN Inspect — 2023 Model S VIN decoder — <https://vininspect.com/vin/tesla/model-s/2023/5yjsa1e65pf>
- 17vin — `5YJSA1E6` = 2023 Model S Plaid 1,020 hp — <https://en.17vin.com/model/df7c2.html>
- Tesla FSD Europe regulatory tracker — <https://fsdtracker.eu/>
- Wards Auto — Netherlands type approval of FSD Supervised (April 2026) — <https://www.wardsauto.com/news/tesla-fsd-supervised-approved-the-netherlands/817279/>
- Drive Tesla Canada — Swedish Transport Agency on EU-wide rollout 2026 — <https://driveteslacanada.ca/news/tesla-fsd-europe-approval-sweden-2026/>
- Tesla North — Single Pull vs. Double Pull Autosteer on stalkless yoke — <https://teslanorth.com/2023/11/15/tesla-debuts-single-pull-autosteer-feature-for-cars-with-stalks>
- Not a Tesla App — Tesla removes "Autopilot" name; menu becomes "Self-Driving" in 2026.2.9 — <https://www.notateslaapp.com/news/3719/tesla-kills-the-autopilot-name-in-new-software-update>
- Tessie — 2026.2.9 release notes (Controls → Self-Driving, Brake Confirm, AI Computer rename) — <https://stats.tessie.com/versions/2026.2.9>
