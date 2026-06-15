<div align="center">
  <img src="https://via.placeholder.com/150/000000/FFFFFF/?text=Jalachara" alt="Jalachara Logo">
  
  # 🌊 Project Jalachara
  **AI‑Powered Predictive Water Governance for Canal Command Areas**
  
  *“Jalachara: Sanskrit for ‘Water Wanderer’ – flowing where it’s needed most, fairly and efficiently.”*

  [![ISRO Hackathon 2026](https://img.shields.io/badge/ISRO_Hackathon-2026-orange.svg)](#)
  [![Problem Statement 6](https://img.shields.io/badge/Problem_Statement-6-blue.svg)](#)
  [![License](https://img.shields.io/badge/License-MIT-green.svg)](#)
</div>

---

## 📌 Executive Summary

India’s agricultural water demand exceeds supply by 40%. Current systems detect crop stress *after* the damage is done. **Jalachara** is a predictive water governance system that forecasts field-level water deficits 8 days ahead, optimises canal water allocation under **fairness** and **yield‑protection** constraints, and delivers actionable irrigation advisories. 

Built on **ISRO’s EOS-04 (C‑band SAR)** and **LISS‑III/IV optical data**, with a clear upgrade path to the systematically imaged **NISAR** 100m soil moisture data available through the Bhoonidhi Portal.

---

## 💎 The Three Transformative Upgrades

What makes Jalachara a national policy tool, not just an AI project?

1. ⭐ **Yield Loss Prevention Score**
   - *Shift:* From predicting "Water Deficit = 30mm" ➡️ "Expected yield loss = 14% without action in 3 days."
   - *How:* Calculates expected yield loss using FAO‑56 dual Kc principles combined with crop‑specific stress‑yield relationships.

2. ⭐ **Water Equity Index (WEI)**
   - *Shift:* From "Maximise total production" ➡️ "Optimise allocation while protecting tail‑end farmers."
   - *How:* A fairness constraint in our multi-objective genetic algorithm ensures that tail-end farmers receive no less than their minimum survival water requirement (WEI ≥ 0.8).

3. ⭐ **8-Day Early Warning System**
   - *Shift:* From detecting visible stress ➡️ Predicting stress 8 days *before* visible symptoms.
   - *How:* Adapts a RegCDI‑style framework using MODIS surface reflectance, EOS‑04 soil moisture, and Sentinel‑1 SAR backscatter.

---

## 🔬 Core AI Innovations

- **SITS-Former for Crop & Growth Stage Classification:** A Satellite Image Time Series Transformer fine-tuned on AgriFieldNet India, achieving >85% accuracy in crop type and phenological stage classification.
- **Hybrid AI‑Physics Water Deficit Forecaster:** Embeds neural networks into FAO‑56 water balance equations to respect mass conservation while learning nonlinear corrections from satellite observations.
- **MOGA‑Based Water Allocation Optimiser:** Uses NSGA‑II to simultaneously optimise for yield, economic returns, water equity, and waste minimisation.
- **Explainable AI + What‑If Simulator:** SHAP force plots reveal the *why* behind stress classifications, while a counterfactual simulator allows canal managers to test policy scenarios (e.g., "What if we release only 70% of normal canal water?").

---

## 📁 Data Sources & Stack

All data used in Jalachara is **100% free and open-access**.

| Component | Technology / Source |
| :--- | :--- |
| **High-Res Optical** | LISS‑IV (ISRO Bhoonidhi) |
| **Vegetation & Phenology** | LISS‑III, Sentinel‑2 (10m) |
| **SAR / Soil Moisture** | EOS‑04 (500m), Sentinel‑1 |
| **Future Integration** | **NISAR** (100m soil moisture every 12 days) |
| **Meteorology** | ERA5‑Land (GEE) |
| **AI / ML Stack** | PyTorch, XGBoost, Scikit-learn, Optuna |
| **Optimisation** | `pymoo` (NSGA-II) |
| **Physical Models** | `pyfao56` |
| **Dashboard** | Streamlit, Plotly, leafmap |

---

## 🚀 Quick Start (Prototype)

### 1. Clone the Repository
```bash
git clone https://github.com/bhargavatejagolla/Jalachara-ISRO-BAH2026.git
cd Jalachara-ISRO-BAH2026
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
```

### 3. Launch Dashboard
```bash
streamlit run app.py
```

---

## 📊 Validation Targets

- **Crop Classification Accuracy:** >85% (Target: 87-92%)
- **Water Deficit Forecast RMSE:** <15 mm
- **Yield Loss Prediction Error:** <10%
- **Water Equity Index (WEI):** ≥0.85
- **Early Warning Accuracy:** >80% at 8-day lead time

---

<div align="center">
  <i>"Transitioning from an observational model into a physical strategy."</i><br>
  Built for <b>Bharatiya Antariksh Hackathon 2026</b>
</div>
