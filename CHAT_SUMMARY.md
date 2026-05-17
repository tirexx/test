# Chat Summary — Tesla Model S Plaid 2023

## Vehicle Info

- **Car:** Tesla Model S Plaid 2023
- **VIN:** 5YJSA1E65PF517234

---

## 1. SIM Card & Cellular Connectivity

- Tesla service installed a **new SIM card** in the car
- The Tesla app wakes the car by sending an **SMS to the SIM card's phone number** — this is the standard wake-up mechanism
- Initially, the car showed **only Wi-Fi, no LTE** connection
- Service Mode (Infotainment > Connectivity) showed:
  - Cell Link State: **Idle** (red)
  - Cell Connection: **Failed to connect** (red)
  - Valid SIM: **Grey** (not green)
  - Toggle SIM button was **locked** (requires Service Mode Plus / Tesla Toolbox)
  - Modem type: AG525RGL, antennas both Normal, IMEI valid
- Diagnosis: SIM was physically installed but **not properly toggled/activated in software**
- **Resolution:** User contacted Tesla service; LTE was fixed and is now working

## 2. Electrical Calculation

- DC 220V × 16A = **3.52 kW**; at 1 hour = 3.52 kWh
- Full Model S Plaid charge (~100 kWh) at this rate would take ~28.4 hours

## 3. Deep Sleep / Vampire Drain

- No single "deep sleep" button — requires disabling multiple features
- Key settings: disable Sentry Mode, Cabin Overheat Protection, Summon Standby
- Stop third-party apps from polling; avoid checking Tesla app frequently
- For maximum sleep: Controls > Safety & Security > Power Off
- Expected drain: 0.1–0.5% per day with everything disabled

## 4. Key Fob Functions

- Three touch areas: front (frunk), roof (lock/unlock), rear (trunk/charge port)
- Passive entry, walk-away lock, auto-present handles, drive-away lock
- Dead battery backup: scan on B-pillar card reader
- Up to 4 key fobs, 19 total keys
- **Previous owner's keys can be deleted** via Controls > Locks > trash icon (no service mode needed)

## 5. Climate System Noise

- Normal: humming/ticking from A/C compressor, fan noise varies by level
- Fan levels 1–3 ~30–35 dB, max 9–10 ~55–60 dB
- Abnormal: grinding, rattling, persistent clicking, whistling from vents

## 6. Fender Liner Clips

- User shared photo of a clip with visible red center pin (possibly not fully seated or wrong type)
- Tesla OEM part numbers: **1006521-00-A** (push-pull 8x18x20mm) and **1006535-00-A** (wheel arch)
- Known issue: original clips are too short and fall out; improved longer versions available
- Tesla service manual links:
  - [Front Wheel Arch Liner — Remove and Replace](https://service.tesla.com/docs/ModelS/ServiceManual/Palladium/en-us/GUID-C8630660-DD53-4CF1-9A41-5842A5632B87.html)
  - [Rear Wheel Arch Liner — Remove and Replace](https://service.tesla.com/docs/ModelS/ServiceManual/Palladium/en-us/GUID-83204DD0-19B1-4C53-B77D-879D769D6A95.html)
  - [Front Fender Assembly — Remove and Replace](https://service.tesla.com/docs/ModelS/ServiceManual/Palladium/en-us/GUID-B9E14414-F480-42DC-91DC-30F42706D3BE.html)

## 7. External Speaker / Boombox / PWS

- Boombox works **only when parked** (driving sound option removed after 2022 NHTSA recall)
- Available Boombox options: Lock Sound, Horn Sound, Replace Horn, Play Current Media, Megaphone
- **PWS (Pedestrian Warning System) sound while driving cannot be changed** — fixed in firmware
- PWS sound: white/pink noise going forward, sci-fi whine in reverse; auto-adjusts with speed up to ~32 km/h

## 8. Service Mode Battery Info (from screenshot)

- **LV Battery:** Li-Ion CATL, SOC 78%, Voltage 15.59V, Health OK
- **PCS DC-DC:** Target 15.56V, Output 15.53V, Current 26.20A
- SOC = State of Charge (of the 12V LV battery, not the main drive battery)

## 9. Jack Pads & Lifting

- 4 jack points, each with 3 holes — use **center hole**
- **Measure holes first** — Tesla changed sizes from 25mm to 20mm on some 2023 cars
- Recommended pads: T Sportline Ranger Series, Powerflex PF75-1001, EVANNEX, SVI International
- Recommended stands: RennStand 3-ton with Tesla pad included
- **Must enable Jack Mode** (Controls > Service > Jack Mode) before lifting — required for air suspension
- **Never lift from diagonal points simultaneously**

## 10. Part Numbers

### Windshield Wipers (Bosch) — Model S 2021+ Refresh/Plaid

- **Bosch Aerotwin A621S** (set) — Part # **3397007638**
- Driver: 26" (650mm), Passenger: 20" (500mm), direct fit, no adapters needed

### Cabin Air Filter — Model S 2022–2023 Plaid

- **Tesla OEM** — [shop.tesla.com](https://shop.tesla.com/product/model-s_x-air-filter) — ~$34
- **Pureflow** — Part # **PC99476X** — ~$25
- **BASENOR** — for Model S/X 2022–2026, activated carbon — ~$25
- Service manual: [Cabin Filter — Remove and Replace](https://service.tesla.com/docs/ModelS/ServiceManual/Palladium/en-us/GUID-E8D15D36-E8D7-4D36-B59B-1D3632E7E321.html)

### Fender Liner Clips

- **1006521-00-A** — RVT Push-Pull 8x18x20mm (inner fender well)
- **1006535-00-A** — Push pin retainer (wheel arch liner)

## 11. LTE Hotspot

- Tesla's LTE is for the car's own systems only — **cannot share as Wi-Fi hotspot** for other devices
- Alternatives: use phone hotspot, or buy a portable MiFi device

---

## Repository

- **Branch:** `cursor/general-coding-task-e167`
- **PR:** https://github.com/tirexx/test/pull/1 (draft)
- **TASKS.md** contains: questions for TSK, reminders, and part numbers
