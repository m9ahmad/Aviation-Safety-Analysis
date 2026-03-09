<h1 align="center">🛡️ AeroSafe: Forensic Aviation Risk Intelligence (1908–2025)</h1>

<p align="center">
  <img src="https://img.shields.io/badge/Dataset-Airplane_Crashes_117Y-red?style=for-the-badge&logo=aircanada" />
  <img src="https://img.shields.io/badge/NLP-Trigram_Extraction-green?style=for-the-badge&logo=pypy" />
  <img src="https://img.shields.io/badge/Viz-Interactive_Plotly-orange?style=for-the-badge&logo=plotly" />
  <img src="https://img.shields.io/badge/Metrics-Survival_Index-blue?style=for-the-badge&logo=dataiku" />
</p>

<p align="center">
  <strong>An Exploratory Data Analysis (EDA) and Predictive Risk Audit of global aviation incidents.</strong><br />
  Quantifying "The Safety Paradox," Operator Fragility, and NLP-driven Causal Discovery.
</p>

---

## 📖 Project Overview
This project performs an industrial-grade audit of aviation safety data to uncover hidden risks, patterns, and survival trends across over a century of flight records. By implementing **NLP-based feature extraction** and **survivability modeling**, this study provides a forensic view of how aviation risk has evolved from mechanical failures to systemic mass-fatality events.

---

## 🛠️ Tech Stack & Methodology

| Category | Tools & Libraries |
| :--- | :--- |
| **Data Engine** | `Pandas`, `NumPy` |
| **NLP Pipeline** | `NLTK`, `Scikit-Learn` (CountVectorizer) |
| **Visualization** | `Plotly` (Interactive), `Seaborn`, `Matplotlib` |
| **Environment** | `Google Colab` |

---

## 🔍 Key Technical Analyses & Findings

### 1. 🧬 The Survivability Index
Transitioned from raw counts to a normalized **Survival Rate** metric to evaluate crashworthiness across aircraft generations.
> $$Survival\_Rate = \frac{Aboard - Fatalities}{Aboard}$$

### 2. ⚖️ Crew vs. Passenger Risk Delta
* **Analysis**: Comparative fatality analysis between crew and passengers.
* **Finding**: Identified specific aircraft types (e.g., **Hawker Siddeley HS-125**) with statistical discrepancies, indicating higher crew vulnerability compared to passengers.

### 3. 📉 The Safety Paradox (2019 Case Study)
* **Hypothesis**: Are accidents rarer but deadlier?
* **Finding**: In 2019, while only 9 accidents occurred, **66% were Mass Fatality events** (including the Boeing 737 Max 8). This validates the paradox: modern aviation is safer in frequency, but higher in potential casualty volume.

### 4. 🧠 NLP: "The Why" Causal Mining
* **Extraction**: Top trigrams from accident summaries.
* **Finding**: Predominant causal themes identified: *"Poor weather conditions"*, *"Adverse weather conditions"*, and *"Cargo plane crashed"*.

### 5. 🏙️ Ground Zero & Third-Party Risk
* **Analysis**: Fatalities affecting individuals not aboard the aircraft.
* **Finding**: 242 incidents resulted in **8,513 ground fatalities**. The 9/11 attacks remain the most significant outlier in urban third-party risk.

### 6. 📅 Decadal Fatality-to-Aboard Trends
* **Trend**: High fatality rates in early aviation saw a steady decline through the mid-20th century (lowest in 1980s-90s).
* **Finding**: A recent slight uptick in the 2000s-2010s reflects the impact of high-capacity aircraft in mass-casualty events.

### 7. 🌡️ Operator Risk Signatures (Heatmap)
* **Competitive Intelligence**: Analyzed top 20 operators for failure types (Engine, Weather, Pilot, Landing).
* **Finding**: **Aeroflot** exhibited the highest cumulative frequency across all analyzed incident categories compared to global peers.

### 8. 🚁 High-Risk Airframe Identification
* **Analysis**: Calculating Mean Fatality Rate for AC Types with $>10$ incidents.
* **Finding**: Older/Specialized types like the **De Havilland DH-4** and **Mil Mi-8** helicopter exhibited the lowest historical survivability rates.

### 9. 📍 Interactive Vulnerability Diagnostics
* **Interactive Scatter Plot**: A Plotly-driven diagnostic mapping Crew vs. Passenger fatality rates.
* **Utility**: Highlighting aircraft where the risk profile deviates from the $1:1$ diagonal line, exposing role-specific design or operational vulnerabilities.


<p align="center">
<strong>Developed by Mahad Ahmad</strong><br />
<em>AI Software Engineer | Aviation Risk Analyst</em><br />


---
             # Heatmaps, Decadal Graphs, Scatter Plots
└── README.md               # Documentation
