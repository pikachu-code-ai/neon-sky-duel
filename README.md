# neon-sky-duel# ⚔️ NEON SKY DUEL 3D — Aerial Squad Battle

**NEON SKY DUEL 3D** is a high-octane, fast-paced 3D cyberpunk aerial starfighter squad-combat game built in a single self-contained HTML5 file using **Three.js** and procedural **Web Audio API** sound synthesis. 

Pilot your high-tech **Valkyrie-X Starfighter** across high-altitude sky decks, lock onto hostile interceptor squadrons, perform high-speed roll dashes, deflect incoming fire with your Aegis Shield, and vaporize enemies with devastating Hyper Nova Beams!

---

## ✨ Key Features

* **Sleek 3D Aerodynamic Starfighters:** Detailed 3D fighter models featuring swept-delta wings, needle noses, faceted canopy glass, V-tail fins, and rear nozzles with animated afterburner exhaust cones.
* **Unrestricted 360° Flight Engine:**
  * **360° Continuous Horizontal Steering:** Smooth yaw rotation with visual wing-banking dynamics.
  * **Unrestricted Forward & Backward Flight:** Thrust forward at 80 m/s with afterburner flames and ambient speed particles, or backpedal at 55 m/s.
  * **Plane-Level Altitude Lock:** Ascend (+Y) and descend (-Y) at 52 m/s while keeping pitch locked strictly level (`pitch = 0`).
* **High-Visibility Spatial Orientation:**
  * **Y=0 Holographic Sky Deck:** Glowing grid floor with concentric compass distance rings.
  * **Y=110 Upper Sky Ceiling:** Translucent ceiling grid.
  * **8 Perimeter Boundary Pillars:** Glowing neon pillars at $R = 140\text{m}$ defining arena limits.
  * **Dynamic Altitude Drop-Lines & Ground Shadows:** Real-time vertical projection lines drawn under every active starfighter down to floor level.
* **Tactical Target Tracking & Radar:**
  * **2D Tactical Sky Radar:** Real-time top-down radar displaying player heading cone, all active enemies (with `+`/`-` altitude indicators), and highlighted target lock.
  * **3D Target Lock Frame:** On-screen target tracking frame displaying hostile unit name, dynamic numeric HP readout, distance in meters, and action prompts (`BLADE RANGE` vs `PLASMA RANGE`).
  * **Off-Screen Target Pointer Arrow:** Directional arrow guiding vision toward locked targets when out of view.
* **5 Multi-Wave Squad Missions + Boss Battle + Endless Swarm:**
  * Fight through escalating multi-enemy waves across 5 structured missions.
  * Face **THE APEX OMEGA ARCHON** in Level 5—a triple-delta golden celestial dreadnought with orbital laser pylons.
  * Test your endurance in **Endless Swarm** mode with scaling hostile health (+12% per wave).
* **Deep Combat Mechanics:**
  * **Spacebar Dual Plasma / Blade Lunge:** Fires continuous twin plasma bolts at range (with 40° magnetic aim-assist within 180m) or triggers a 60-damage point-blank blade lunge when within 34m.
  * **Sonic Z-Vanish Roll Dash (`Shift` / `L`):** Invulnerable roll dash leaving wireframe afterimages, teleporting behind the locked enemy for counter-strikes.
  * **Aegis Bubble Shield (`G` / `X`):** Active spherical shield to block and parry incoming plasma bolts and melee strikes.
  * **Hyper Overdrive Nova Beam (`Q` / `V`):** Piercing 3D laser beam fired at 100% charge across the sky.
* **Zero-Lag 60 FPS Performance Architecture:** Object-pooled projectiles (90), spark particles (75), wireframe trail afterimages (8), and DOM floating popups (10). Zero per-frame memory heap allocations.
* **Procedural Web Audio API SFX:** Zero external sound assets required. Synthesizes plasma bolts, railgun blasts, blade slashes, roll dashes, shield parries, explosions, and victory fanfares directly via Web Audio API.

---

## 🎮 Controls

### Desktop Controls

| Key / Input | Action |
| :--- | :--- |
| **`W` / `S`** | Fly Forward (80 m/s) / Fly Backward (55 m/s) |
| **`A` / `D`** or **`←` / `→`** | 360° Continuous Turn Left / Right (with Wing Banking) |
| **`R` / `↑`** | Ascend UP (+Y) at 52 m/s (Plane-Level) |
| **`C` / `Ctrl` / `↓`** | Descend DOWN (-Y) at 52 m/s (Plane-Level) |
| **`Spacebar` / Left-Click** | **Primary Weapon:** Dual Plasma Volley (2x14 Dmg) / Close-Range Blade Lunge (60 Dmg when <34m) |
| **`Tab` / `E`** | Cycle Target Lock across active hostiles |
| **`Shift` / `L` / Right-Click** | **Sonic Z-Vanish Roll Dash** (Invulnerable Teleport) |
| **`G` / `X`** | **Aegis Shield** (Block / Parry) |
| **`Q` / `V`** | **HYPER NOVA BEAM** (Piercing Laser Beam at 100% charge) |
| **`P` / `Esc`** | Pause / Resume Battle |
| **`M`** | Toggle Sound FX On / Off |

### Mobile Touch Controls

* **Left Virtual Joystick:** 360° Turning & Forward/Backward Acceleration.
* **`🔥 [SPACE] SHOOT PLASMA` Button:** Continuous primary fire / close-range blade lunge.
* **`▲ ASCEND` / `▼ DESCEND` Buttons:** Vertical altitude movement.
* **`🎯 TARGET` Button:** Cycle target lock across active enemies.
* **`⚡ ROLL DASH` Button:** Execute Z-Vanish Dash.
* **`🛡️ AEGIS` Button:** Raise Aegis Shield.
* **`💥 NOVA` Button:** Activate Hyper Nova Beam.

---

## 🛸 Hostile Starfighter Roster

| Enemy Class | Model Visual | Base HP | Speed | Combat Behavior |
| :--- | :--- | :--- | :--- | :--- |
| **Viper Interceptor** | Crimson/Magenta Forward-Swept Stealth Fighter | 240 HP | 28 m/s | Fast dogfighting, close-range strafing & plasma bursts. |
| **Rail-Hawk Sniper** | Slender Needle-Wing Craft with Dual Rail Booms | 320 HP | 20 m/s | Long-range positioning, telegraphed high-speed railgun beams (28 Dmg). |
| **Juggernaut Gunship** | Broad Heavy Armored Bomber with Quad Thrusters | 540 HP | 15 m/s | Heavy armored hull firing 3-way spread plasma volleys. |
| **Apex Omega Archon** | Triple-Delta Golden Dreadnought with Rotating Pylon | 1,400 HP | 26 m/s | Multi-phase boss with orbital laser strikes & escort swarms. |

---

## 🏁 Mission Overview

| Level | Mission Name | Structure | Squad Breakdown | Primary Threat |
| :--- | :--- | :--- | :--- | :--- |
| **LVL 1** | **Cyber Patrol** | 2 Waves | 2 Vipers ➔ 2 Rail-Hawks | Scout Interceptors & Snipers |
| **LVL 2** | **Viper Squadron** | 2 Waves | 3 Vipers ➔ 2 Rail-Hawks + Viper Leader | Rapid Interceptors & Squadron Leader |
| **LVL 3** | **Orbital Fortress** | 3 Waves | 3 Vipers ➔ 3 Rail-Hawks ➔ 2 Juggernauts | Telegraphed Rail Beams & Heavy Gunships |
| **LVL 4** | **Crimson Armada** | 3 Waves | 4 Vipers ➔ 3 Snipers + Heavy ➔ 2 Commanders | Crossfire Snipers & Heavy Commanders |
| **LVL 5** | **Apex Throne Assault** | 3 Waves | 4 Interceptors ➔ 4 Heavy/Snipers ➔ Apex Archon | Multi-Phase Archon Boss & Royal Escorts |
| **ENDLESS**| **Endless Swarm** | Infinite | Continuous Recycling Squads | Escalating Health (+12%/wave) |

---

## 🛠️ Technical Setup

1. **File Format:** Single self-contained HTML5 document (`neon_sky_duel_3d.html`).
2. **Library Dependency:** Three.js (`r128`) loaded via CDN.
3. **Execution:** Double-click `neon_sky_duel_3d.html` or open it in any standard web browser (Chrome, Edge, Safari, Firefox). No build step, node modules, or web server required!
