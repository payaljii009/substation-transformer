# Substation Transformer Bushing Maintenance and Insulation Resistance Testing (Megger)

**B.Tech Electrical Engineering Mini Project — Safe Interactive Educational Web Simulation**

> **IMPORTANT SAFETY DISCLAIMER**
> This application is an **educational software simulation only**. All voltages, resistance readings, and curves are **synthetic values** created for academic demonstration—not actual field measurements. Never connect this software to real electrical equipment. It intentionally provides no practical instructions for operating a Megger, performing high-voltage tests, discharging apparatus, or handling substation equipment. Real testing and maintenance must **only** be performed by trained, authorized electrical professionals under approved utility procedures.

---

## Project Objective

Develop a beginner-friendly, interactive web-based engineering dashboard that helps B.Tech students understand:
1. High-voltage (HV) and low-voltage (LV) transformer bushing construction in 3D.
2. The conceptual principle of Insulation Resistance (Megger) testing and dielectric absorption over time.
3. How insulation condition, ambient temperature, and humidity influence insulation resistance in `MΩ` and `GΩ`.
4. Conceptual substation bushing maintenance considerations and documentation practices.

---

## Technology Stack

- **HTML5** — Semantic multi-view dashboard structure
- **CSS3** — Clean blue, slate-grey, and white responsive engineering UI
- **JavaScript (ES6+)** — Modular simulation engine, UI controller, and verification suite
- **Three.js (r128 + OrbitControls)** — Interactive 3D substation transformer and bushing visualization
- **Chart.js (v4)** — Live Resistance vs. Time (`R–t`) and multi-condition comparison charts

---

## Project Files

| File | Description |
| :--- | :--- |
| `index.html` | Dashboard layout with Simulation, Results, Theory (12-section report), and Verification views |
| `style.css` | Responsive engineering theme styling, cards, tables, virtual LCD readout, and safety banners |
| `script.js` | 3D scene builder, raycasting inspector, synthetic IR math model, Chart.js graphs, and self-tests |
| `README.md` | Project documentation, run guide, and safety notice |

---

## Core Features Implemented

1. **Interactive 3D Transformer Bushing Model**
   - Main transformer tank, cooling radiator fin banks, conservator tank, 3 HV bushings (`HV-A`, `HV-B`, `HV-C`), and 4 LV bushings (`LV-a`, `LV-b`, `LV-c`, `LV-n`).
   - Switchable **Porcelain** vs. **Composite** insulator surfaces.
   - Rotate, pan, zoom (`OrbitControls`), toggleable 3D labels, and clickable parts with educational descriptions.

2. **Virtual Megger Testing Simulation**
   - Simulated DC voltage reference (`500 V`, `1000 V`, `2500 V`, `5000 V`), virtual `0–60 s` timer, `MΩ`/`GΩ` auto-formatted digital readout, and `15s` / `30s` / `60s` sample readings.
   - Interactive controls for bushing selection, simulated insulation condition (`Healthy`, `Aged`, `Contaminated`, `Severe Fault`), temperature (`10–60 °C`), humidity (`20–95%`), Start, Instant Sample, Log Run, and Reset.

3. **Insulation Resistance Analysis & Graphs**
   - Live Resistance vs. Time (`R–t`) graph with optional Healthy Reference overlay.
   - Logarithmic-scale Comparison Graph comparing all four simulated insulation conditions.
   - Results table (pre-seeded sample baselines + saved user runs) and automated educational interpretation.

4. **Conceptual Maintenance Module & 12-Section Educational Report**
   - Covers visual inspection concepts, surface contamination, cracks/damage, oil leakage indicators, fittings, general insulation condition, and documentation.
   - Built-in Theory report covering Introduction through References.

5. **In-App Verification Suite**
   - Dedicated **Verification** tab checking calculation bounds, unit formatting, temperature/moisture laws, dielectric absorption curve trend, Chart.js bindings, Three.js scene objects, and reset behavior.

---

## Running Locally

1. Ensure you have an active internet connection so the browser can load Three.js and Chart.js from jsDelivr CDN (graceful fallbacks are included if offline).
2. Open `index.html` directly in any modern browser (Chrome, Edge, Firefox), **or** serve the folder locally:
   ```bash
   python -m http.server 8000
   ```
   Then visit `http://localhost:8000`.
3. Explore the **Simulation**, **Results**, **Theory**, and **Verification** tabs.
