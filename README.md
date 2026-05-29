---

# 🌸 Production of Methyl Benzoate via Esterification

<p align="center">
  <b>ChE453 – Capstone Project (Group 4)</b><br>
  Department of Chemical Engineering, Indian Institute of Technology Kanpur
</p>

---

## 📌 Project Overview

✨ This project presents the **design, simulation, and optimisation of a continuous industrial process** for the production of **Methyl Benzoate** via the esterification of **Benzoic Acid with Methanol**.

Methyl Benzoate is a high-value aromatic ester widely used in **fragrances, flavouring agents, solvents**, and as an **intermediate in pharmaceutical and agrochemical industries**.

🔁 The project evolves systematically from **process selection and thermodynamic validation** to **flowsheet development, separation sequencing, energy integration, cogeneration, and economic optimisation**, culminating in a **technically feasible and economically attractive plant design**.

<p align="center">
  <img src="images/BFD.png" alt="Block Flow Diagram (BFD)" width="750">
</p>

<p align="center">
  <img src="images/PFD.png" alt="Overall Process Flow Diagram (PFD)" width="780">
</p>

---

## 🧪 Reaction Chemistry

**Core Reaction:**

> Benzoic Acid + Methanol ⇌ Methyl Benzoate + Water

🔬 Key characteristics:

* Reversible, equilibrium-limited esterification
* Acid-catalysed (HCl); molar ratio Methanol : Benzoic Acid : HCl = **16.59 : 2.7 : 0.1215** (Roberts & Urey, 1938)
* Liquid-phase operation at **25 °C, 1 bar**
* Excess methanol used to shift equilibrium toward ester formation and act as solvent/carrier

<p align="center">
  <img src="images/rxn-mech.png" alt="Reaction mechanism schematic" width="550">
</p>

---

## 🎯 Project Objectives

✅ Identify and justify a suitable **industrial process route** for Methyl Benzoate production  
✅ Select and validate an appropriate **thermodynamic model**  
✅ Develop and compare alternative **separation sequences**  
✅ Integrate **reactor, distillation, heat exchangers, and utilities** into a unified flowsheet  
✅ Apply **pinch analysis** for heat exchanger network (HEN) design  
✅ Integrate a **cogeneration (Rankine cycle)** system for energy recovery  
✅ Perform **economic and sensitivity analysis** to maximise profitability  

---

## 📦 Feed & Product Specifications

| Stream | Component | Flow |
|--------|-----------|------|
| Feed | Methanol | 61.37 kmol/hr (fresh) |
| Feed | Benzoic Acid (0.5 mass% Phthalic Acid impurity) | 57.81 kmol/hr (fresh) |
| Product | Methyl Benzoate | **57.77 kmol/hr** |

Market prices (used in economic analysis):
- Methanol: **USD 370/MT** (Asia Pacific, 2025)
- Benzoic Acid: **USD 1,010/MT** (FOB Shanghai, Q1 2025)
- Methyl Benzoate: **USD 2,200/MT** (industrial-grade, Q4 2023)

---

## 🧱 Process Development Summary

### 🧩 1. Process Identification & Thermodynamics (Report 1)

* Esterification route selected based on industrial relevance
* Feed specified: Methanol (16.95k moles), Benzoic Acid (2.7k moles with 0.5 mass% Phthalic Acid)
* Reactor converts feeds to **~7,435 moles each** of Methyl Benzoate and Water at 80% single-pass conversion (assumed pending kinetics)
* Market study conducted — Methyl Benzoate market projected to reach **USD 2.26 billion by 2032** at 6% CAGR
* Preliminary break-even analysis: **k ≈ 437** (scaling factor), profit multiplier **≈ 1.74×**
* Thermodynamic models evaluated: NRTL, Peng–Robinson, UNIQUAC
* ⭐ **UNIQUAC selected** based on best fit to experimental Txy data for Water–Methanol binary
* Azeotrope analysis (UNIQUAC, 1 bar): **No azeotropes found** — confirms conventional distillation feasibility

<p align="center">
  <img src="images/VLE1.png" alt="VLE plot" width="620">
  <img src="images/VLE2.png" alt="VLE plot" width="620">
  <img src="images/VLE3.png" alt="VLE plot" width="620">
  <img src="images/VLE4.png" alt="VLE plot" width="620">
</p>

---

### 🔀 2. Flowsheeting & Separation Strategy (Report 2)

* Operating conditions fixed: **25 °C, 1 bar**, high methanol excess (molar ratio 16.59 : 2.7 : 0.1215)
* Two four-column distillation sequences developed and compared in Aspen (shortcut method):

**Method 1 — Early Methanol Recovery:**
- C1 strips methanol overhead; C2 removes water; C3 recovers MEB; C4 polishes benzoic acid/PTH
- Methanol recovery: **~99.0%** | MEB recovery: **~98.01%** | Benzoic acid recovery: **~98.01%**
- Total reboiler duty: **49,902 kW** (C1 bears ~80% of load at 40,099 kW)

**Method 2 — Load-Distributed Separation:**
- C1 sends MeOH+H₂O overhead; C2 is main methanol column; C3 and C4 target MEB and benzoic acid
- Methanol recovery: **~98.90%** | MEB recovery: **~98.01%** | Benzoic acid recovery: **~98.01%**
- Total reboiler duty: **48,931 kW** (~2% lower than Method 1, more evenly split between C1 and C2)

* 🏆 **Method 2 selected** due to ~971 kW lower total reboiler duty, reduced peak column load, and better utility integration potential

<p align="center">
  <img src="images/sep1.png" alt="Separation flowsheet" width="750">
  <img src="images/sep2.png" alt="Alternative separation flowsheet" width="750">
  <img src="images/dist.png" alt="Distillation column configuration" width="750">
</p>

---

### 🔌 3. Process Integration & Cogeneration (Report 3)

Complete material flowsheet developed in Aspen Plus with:

**Distillation Columns (all 20 trays, rigorous RadFrac):**

| Column | Separation | Feed Stage | Reflux Ratio | Reboiler Duty | Condenser Duty |
|--------|-----------|------------|--------------|---------------|----------------|
| C1 | MEB + Benzoic acid from MeOH + Water | 11 | 0.0187 | 22,532 kW | −17,596 kW |
| C2 | Methanol (distillate) from Water (bottoms) | 14 | 1.7256 | 38,340 kW | −38,109 kW |
| C3 | Methyl Benzoate (distillate) from Benzoic acid + PTH | 11 | 0.3033 | 4,291 kW | −4,436 kW |
| C4 | Benzoic acid (distillate) from Phthalic acid | 10 | 1.1913 | 25 kW | −19 kW |

**Heat Exchangers:**

| Unit | Duty | Hot Side → Cold Side |
|------|------|---------------------|
| HX1 | ~1,205 kW | Mixed water stream → Cooling water recycle |
| HX2 | 9,983 kW | Methanol distillate D2 (64 → 35 °C) → Rankine condensate |
| HX3 | ~2,792 kW | MEB distillate D3 (191 → 30 °C) → Cooling water recycle |

**⚡ Cogeneration (Rankine Cycle) — Three-stage steam turbine system:**

| Stage | Pressure Out | Power Generated |
|-------|-------------|-----------------|
| HP Turbine | 40 bar | 1,540 kW |
| MP Turbine | 10 bar | 7,013 kW |
| LP Turbine | 3 bar | 4,693 kW |
| LLP Turbine | 1 bar | 3,372 kW |
| **Total** | — | **~16,618 kW** |

* Mass balance verified across all columns and heat exchangers (total in = total out)
* Cooling water loop designed with recycle; makeup stream required to maintain 40 °C return temperature
* Practical challenges documented: lack of detailed reaction kinetics limited reactor–HEN coupling

<p align="center">
  <img src="images/cogen.png" alt="Cogeneration cycle schematic" width="700">
  <img src="images/cwl.png" alt="Cooling water loop schematic" width="700">
</p>

---

### 🚀 4. Final Design & Optimisation (Combined Report — Reports 4, 5, 6)

#### Reactor Hydrodynamics

* **Type:** Plug Flow Reactor (PFR) with recycle
* **Dimensions:** Length = 40 m, Diameter = 8 m
* **Operating temperature:** 63.4 °C (isothermal)
* **Heat duty:** −285.4 kW (exothermic)
* **Residence time:** 2.57 hr (within typical industrial range of 1–5 hr)
* **Average velocity:** 0.00433 m/s | **Reynolds number:** 36,961 → **Turbulent flow (Re ≥ 4,000)** ✅
* **Single-pass conversion:** 58% | **Overall conversion with recycle:** **99.63%**
* Fresh feeds: Methanol 61.37 kmol/hr, Benzoic Acid 57.81 kmol/hr | Product: 57.77 kmol/hr MEB

#### Detailed Shell-and-Tube Heat Exchanger (TEMA Standards)

| Parameter | Value |
|-----------|-------|
| Shell type | E-type (single pass) |
| Tube OD / ID | 20 mm / 16 mm |
| Tube length | 4.88 m (standard) |
| Number of tubes | 2,425 (triangular pitch, 25 mm) |
| Number of baffles | 5 (single segmental, 25% cut, 288 mm spacing) |
| Shell diameter | 1,441 mm |
| Tube-side fluid | Methanol (hot), 64.2 → 35 °C |
| Shell-side fluid | Cooling water, 25 → 40 °C |
| Heat duty | **9,983 kW** |
| HX area (calculated) | 735.3 m² | HX area (Aspen EDR) | 721.45 m² |
| UA (calculated) | 625 kW/K | UA (Aspen) | 613.24 kW/K |
| Tube material | CuNi 90/10 (TEMA Class B, ASME Code Sec VIII Div 1) |

Manual calculations closely matched Aspen EDR results (within ~2%).

#### Pinch Analysis & Heat Exchanger Network

* **ΔT_min chosen:** 10 °C
* **5 process streams** included:

| Stream | Type | mCp (kW/°C) | Tin | Tout | Duty (kW) |
|--------|------|------------|-----|------|-----------|
| D2 (Methanol distillate) | Hot | 341.89 | 64 °C | 35 °C | 9,915 |
| D3 (MEB distillate) | Hot | 4.668 | 191 °C | 35 °C | 728 |
| D4 (Benzoic acid distillate) | Hot | 1.733 | 248 °C | 35 °C | 369 |
| LIQOUT (Reactor outlet) | Cold | 374.54 | 50 °C | 54 °C | 1,498 |
| MIXOUT (Reactor inlet) | Cold | 348.69 | 25 °C | 50 °C | 8,717 |

* **Cascade diagram result: No pinch point** — net excess energy throughout; all surplus transferred to cold utility
* **Minimum heat exchangers required: 5** (= N_streams + N_utilities − 1)
* HEN designed with 5 exchangers (HEN1–HEN5); streams matched by mCp_hot ≤ mCp_cold rule
* Cooling water loop optimised with makeup block to achieve zero fresh cooling water requirement

#### Cooling Water Loop

* Makeup block targets: BACWH = 40 °C, MBCWH = 40 °C, net fresh water makeup = 0 tonne/hr
* Cooling tower simulated with air/water mass balance verified (total in = 25,082,416 kg/hr = total out)

#### Sensitivity Analysis for Profit Optimisation

Dominant design variables explored via Fortran-coded objective function in Aspen:

| Variable | Optimum Value | Observation |
|----------|--------------|-------------|
| Reactor diameter | **13.68 m** | Clear profit maximum |
| Reactor length | **59.46 m** | Broad optimum |
| Column 2 bottom purity | **0.95** | Higher purity reduces profit (higher reboiler duty) |
| Column 1 top purity | **0.95** | Same trend; minimum purity constraint applied |
| Column 2 top purity | **0.99** | Higher methanol recovery improves profit monotonically |

<p align="center">
  <img src="images/HEN.png" alt="Heat Exchanger Network" width="780">
</p>

<p align="center">
  <img src="images/sensi1.png" alt="Sensitivity plot" width="620">
  <img src="images/sensi2.png" alt="Sensitivity plot" width="620">
  <img src="images/sensi3.png" alt="Sensitivity plot" width="620">
</p>

---

## ⚙️ Key Technical Features

* Plug Flow Reactor (PFR) with recycle — turbulent regime (Re = 36,961), residence time 2.57 hr
* Four-column distillation train (Method 2 sequence)
* Shell-and-tube HX designed to TEMA Class B / ASME standards (CuNi 90/10, 2,425 tubes)
* Heat exchanger network with ΔT_min = 10 °C, 5 exchangers, no pinch point
* Three-stage Rankine cogeneration generating **~16,618 kW** of electricity
* Cooling water loop with zero freshwater makeup at steady state
* Aspen Plus simulation (UNIQUAC thermodynamics) supported by manual design validation

<p align="center">
  <img src="images/final.png" alt="Final integrated flowsheet with HEN" width="780">
</p>

---

## 💰 Economic Results

| Metric | Value |
|--------|-------|
| Total Capital Cost (TCC) | **$2.98 × 10⁷** |
| Yearly Operating Cost (YOC) | **$1.39 × 10⁸** |
| Raw Materials Cost | **$1.06 × 10⁸** |
| Annual Revenue | **$2.14 × 10⁸** |
| Total Annualised Cost (TAC) | **$1.49 × 10⁸** |
| **Total Annual Profit (TAP)** | **$6.46 × 10⁷** |
| **Payback Period** | **~3 years** |

The process is economically viable under realistic market assumptions (methanol at $370/MT, benzoic acid at $1,010/MT, methyl benzoate at $2,200/MT, operating 7,200 hr/yr).

---

## ⚠️ Limitations & Future Scope

**Limitations:**

* Lack of detailed reaction kinetics prevented accurate temperature-dependent reactor–HEN coupling; equilibrium reactor (R-Equil) used as approximation
* Some Aspen EDR settings could not be fully replicated in manual heat exchanger calculations
* Cooling water loop closure required simplifying assumptions (makeup block approach)

**Future work:**

* Kinetic parameter estimation (rate constant k, activation energy Ea) for Fischer esterification
* Rigorous PFR modelling with temperature profiles
* Dynamic simulation and process control studies
* Optimisation of HEN retrofit to incorporate reactor heat duties more accurately

---

## 🎬 Endterm Presentation

▶ [Watch Endterm Presentation video](https://drive.google.com/file/d/1FrWMKWWbhJXB8A-jbmuGOKWoEXzA9vmA/view)

---

## 👥 Team Members (Group 4)

| Member | Roll No. | Key Contributions |
|--------|----------|------------------|
| Aaditya Amlan Panda | 220007 | Block diagram, cogeneration integration |
| Abhijit Dalai | 220030 | Flowsheeting, method selection, cooling water loop |
| Adarsh Pal | 220054 | Block diagram, distillation column optimisation |
| Akash Kumar Gupta | 220095 | Flowsheeting, distillation column optimisation |
| Kushagra Tiwari | 220574 | Thermodynamic analysis, cogeneration integration |
| Saurabh Yadav | 220991 | Market & profitability analysis, cogeneration |
| Snehil Tripathi | 221071 | Market & profitability analysis, distillation optimisation |
| Tushar Verma | 221147 | Thermodynamic analysis, cooling water loop |

---

✨ *This repository documents the complete academic capstone journey — from conceptual process selection to final techno-economic evaluation.*

---
