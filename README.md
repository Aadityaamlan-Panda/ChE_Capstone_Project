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
* Acid-catalysed (HCl)
* Liquid-phase operation
* Excess methanol used to shift equilibrium toward ester formation

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

## 🧱 Process Development Summary

### 🧩 1. Process Identification & Thermodynamics (Report 1)

* Esterification route selected based on industrial relevance
* Feed and product specifications established
* Market study conducted for Methanol, Benzoic Acid, and Methyl Benzoate
* Thermodynamic models evaluated: NRTL, Peng–Robinson, UNIQUAC
* ⭐ **UNIQUAC selected** based on best phase-equilibrium fitting
* Azeotrope analysis confirmed separation feasibility

<p align="center">
  <img src="images/VLE1.png" alt="VLE plot" width="620">
  <img src="images/VLE2.png" alt="VLE plot" width="620">
  <img src="images/VLE3.png" alt="VLE plot" width="620">
  <img src="images/VLE4.png" alt="VLE plot" width="620">
</p>

---

### 🔀 2. Flowsheeting & Separation Strategy (Report 2)

* Operating conditions fixed (25 °C, 1 bar, high methanol excess)
* Two distillation sequences developed and compared:

  * **Method 1:** Early methanol recovery
  * **Method 2:** Load-distributed separation
* Detailed Aspen shortcut column analysis performed
* Energy vs recovery trade-offs evaluated
* 🏆 **Method 2 selected** due to lower peak reboiler duty and improved utility integration

<p align="center">
  <img src="images/sep1.png" alt="Separation flowsheet" width="750">
  <img src="images/sep2.png" alt="Alternative separation flowsheet" width="750">
  <img src="images/dist.png" alt="Distillation column configuration" width="750">
</p>

---

### 🔌 3. Process Integration & Cogeneration (Report 3)

* Complete material flowsheet developed including:

  * Mixer and equilibrium reactor
  * Four distillation columns
  * Multiple heat exchangers
* Cooling water loop designed with recycle and makeup streams
* ⚡ **Cogeneration (Rankine cycle)** integrated for on-site power generation
* Column-wise mass and energy balances validated
* Practical challenges documented (kinetics data, utility loop closure)

<p align="center">
  <img src="images/cogen.png" alt="Cogeneration cycle schematic" width="700">
  <img src="images/cwl.png" alt="Cooling water loop schematic" width="700">
</p>

---

### 🚀 4. Final Design & Optimisation (Combined Report)

* Reactor hydrodynamics analysed (turbulent PFR operation)
* Recycle strategy implemented to achieve **>99% overall conversion**
* Detailed **shell-and-tube heat exchanger design** using TEMA standards
* Aspen EDR results validated against hand calculations
* 🔥 **Pinch analysis** performed and heat exchanger network synthesised
* Cooling water loop optimised to minimise freshwater consumption
* Sensitivity analysis conducted for profit maximisation

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

* Plug Flow Reactor (PFR) with recycle
* Four-column distillation train
* Heat exchanger network with ΔTₘᵢₙ = 10 °C
* Cogeneration-based utility integration
* Aspen Plus simulation supported by manual design validation

<p align="center">
  <img src="images/final.png" alt="Final integrated flowsheet with HEN" width="780">
</p>

---

## 💰 Economic Highlights

💵 Capital and operating cost estimation performed
📊 Sensitivity analysis on key design variables
⏱ **Payback period ≈ 3 years**
✅ Process shown to be economically viable under realistic assumptions

---

## ⚠️ Limitations & Future Scope

**Limitations:**

* Lack of detailed reaction kinetics limited reactor–HEN coupling accuracy
* Certain Aspen design settings could not be fully replicated manually

**Future work:**

* Kinetic parameter estimation
* Rigorous reactor modelling
* Centralised cooling utility design
* Dynamic simulation and process control studies

---

## 🎬 Endterm Presentation

▶ [Watch Endterm Presentation video](https://drive.google.com/file/d/1FrWMKWWbhJXB8A-jbmuGOKWoEXzA9vmA/view)

---

## 👥 Team Members (Group 4)

Aaditya Amlan Panda · Abhijit Dalai · Adarsh Pal · Akash Kumar Gupta ·
Kushagra Tiwari · Saurabh Yadav · Snehil Tripathi · Tushar Verma

---

✨ *This repository documents the complete academic capstone journey — from conceptual process selection to final techno-economic evaluation.*

---
Just say 👍
