
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


![Block Flow Diagram (BFD)](images/BFD.png)
![Overall Process Flow Diagram (PFD)](images/PFD.png)

---

## 🧪 Reaction Chemistry

**Core Reaction:**

> Benzoic Acid + Methanol ⇌ Methyl Benzoate + Water

🔬 Key characteristics:

* Reversible, equilibrium-limited esterification
* Acid-catalysed (HCl)
* Liquid-phase operation
* Excess methanol used to shift equilibrium toward ester formation

![Reaction mechanism schematic](images/rxn-mech.png)

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


![VLE plots](images/VLE1.png)
![VLE plots](images/VLE2.png)
![VLE plots](images/VLE3.png)
![VLE plots](images/VLE4.png)

---

### 🔀 2. Flowsheeting & Separation Strategy (Report 2)

* Operating conditions fixed (25 °C, 1 bar, high methanol excess)
* Two distillation sequences developed and compared:

  * **Method 1:** Early methanol recovery
  * **Method 2:** Load-distributed separation
* Detailed Aspen shortcut column analysis performed
* Energy vs recovery trade-offs evaluated
* 🏆 **Method 2 selected** due to lower peak reboiler duty and improved utility integration

![separation flowsheets](images/sep1.png)
![Alternative separation flowsheets](images/sep2.png)
![Distillation column configuration diagrams](images/dist.png)

---

### 🔌 3. Process Integration & Cogeneration (Report 3)

* Complete material flowsheet developed including:

  * Mixer and equilibrium reactor
  * Four distillation columns
  * Multiple heat exchangers
* Cooling water loop designed with recycle and makeup streams
* ⚡ **Cogeneration (Rankine cycle)** integrated for on-site power generation with a cooling water loop
* Column-wise mass and energy balances validated
* Practical challenges documented (kinetics data, utility loop closure)

![Full Aspen flowsheet](images/fullasp.png)
![Cogeneration cycle schematic](images/cogen.png)
![Cooling water loop schematic](images/cwl.png)

---

### 🚀 4. Final Design & Optimisation (Combined Report)

* Reactor hydrodynamics analysed (turbulent PFR operation)
* Recycle strategy implemented to achieve **>99% overall conversion**
* Detailed **shell-and-tube heat exchanger design** using TEMA standards
* Aspen EDR results validated against hand calculations
* 🔥 **Pinch analysis** performed and heat exchanger network synthesised
* Cooling water loop optimised to minimise freshwater consumption
* Sensitivity analysis conducted for profit maximisation

![Heat exchanger network (HEN) diagram](images/HEN.png)
![Sensitivity plot1](images/sensi1.png)
![Sensitivity plot2](images/sensi2.png)
![Sensitivity plot3](images/sensi3.png)

---

## ⚙️ Key Technical Features

* Plug Flow Reactor (PFR) with recycle
* Four-column distillation train
* Heat exchanger network with ΔTₘᵢₙ = 10 °C
* Cogeneration-based utility integration
* Aspen Plus simulation supported by manual design validation

![full with HEN](images/final.png)

---

## 💰 Economic Highlights

💵 Capital and operating cost estimation performed
📊 Sensitivity analysis on key design variables
⏱ **Payback period ≈ 3 years**
✅ Process shown to be economically viable under realistic assumptions

---

## ⚠️ Limitations & Future Scope

⚠️ Limitations:

* Lack of detailed reaction kinetics limited reactor–HEN coupling accuracy
* Certain Aspen design settings could not be fully replicated manually

🔮 Future work may include:

* Kinetic parameter estimation
* Rigorous reactor modelling
* Centralised cooling utility design
* Dynamic simulation and process control studies

---

## 🎬 Endterm Presentation



---

## 👥 Team Members (Group 4)

* Aaditya Amlan Panda (220007)
* Abhijit Dalai (220030)
* Adarsh Pal (220054)
* Akash Kumar Gupta (220095)
* Kushagra Tiwari (220574)
* Saurabh Yadav (220991)
* Snehil Tripathi (221071)
* Tushar Verma (221147)

---

## 📚 Literary References
* **[A Study of the Esterification of Benzoic Acid with Methyl Alcohol Using Isotopic
Oxygen](https://pubs.acs.org/doi/10.1021/ja01277a028)**: Irving Roberts and Harold C. Urey, J. Am. Chem. Soc. 1938, 60, 10, 2391–2393
* **[The solubilities of benzoic acid and its nitro-derivatives, 3-nitro and 3,5-dinitrobenzoic acids](https://www.researchgate.net/publication/356654643_The_solubilities_of_benzoic_acid_and_its_nitro-derivatives_3-nitro_and_35-dinitrobenzoic_acids)**: Xiang Zhang, Jian Chen, Jinzhong Hu, Min Liu, Zhuoer Cai, Yang Xu and Baiwang Sun, 2021, Journal of Chemical Research
* **[Patent: CONTINUOUS PROCESS FOR PREPARING BENZOIC ACID ESTERS](https://patents.google.com/patent/US6235924B1/en)**:  Wesley Wayne McConnell, Bruce Edward Stanhope, Franz Joseph Luxem, 2001, United States Patent, McConell et al.

---

## 🛠 Tools & Software

🧪 Aspen Plus (Simulation & EDR)
📐 Excel (Design calculations)
💻 Fortran (Economic sensitivity analysis)

---

✨ *This repository documents the complete academic capstone journey — from conceptual process selection to final techno‑economic evaluation.*


