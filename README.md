# sustainable-growth-decoupling
Analyzing global GDP growth vs. carbon emissions to evaluate the feasibility of absolute decoupling

## Project Overview
Historically, economic growth (GDP) has always gone hand-in-hand with environmental damage. This project looks at historical data to answer a massive question in climate economics: **Can countries actually decouple economic growth from carbon emissions?** 

Specifically, I want to see if wealthy nations are genuinely achieving "Absolute Decoupling" (growing their GDP while lowering their actual carbon footprint) or if they are just outsourcing their heavy manufacturing—and their emissions—to developing countries.

### Key Analytical Pillars:
1. **The Kaya Identity Decomposition:** Breaking down total carbon emissions into four main drivers: Population, Affluence ($GDP/\text{Capita}$), Energy Intensity ($\text{Energy}/GDP$), and Carbon Intensity ($CO_2/\text{Energy}$).
2. **Decoupling Classification:** Grouping countries into distinct categories: *Absolute Decoupling* (GDP goes up, emissions go down), *Relative Decoupling* (emissions are still rising, but slower than GDP), or *Expansive Coupling* (emissions are outstripping economic growth).
3. **The Energy Mix Transition:** Analyzing how fast shifting from fossil fuels to renewables (solar, wind, hydro, nuclear) impacts a country's total carbon output without tanking its economic productivity.

---

## Core Datasets Targeted
To build a unified data matrix for this analysis, I'm combining a few main global datasets:
*   **Our World in Data (OWID) CO2 Dataset:** Tracks annual territorial emissions, plus crucial consumption-based $CO_2$ records (to account for trade/imports).
*   **World Bank Open Data:** Provides constant GDP metrics, population sizes, and country income brackets.
*   **Energy Institute / EIA Metrics:** Gives the breakdown of global energy consumption by source (fossil fuels vs. low-carbon alternatives).

---

## The Mathematical Framework: The Kaya Identity
To figure out what is *actually* driving changes in emissions over time, I'm using the **Kaya Identity** framework to break down the data at the country level:

$$CO_2 = \text{Population} \times \left(\frac{\text{GDP}}{\text{Population}}\right) \times \left(\frac{\text{Energy}}{\text{GDP}}\right) \times \left(\frac{CO_2}{\text{Energy}}\right)$$

By calculating these factors, we can tell if a country's emissions dropped because they actually adopted cleaner tech (lowering carbon intensity) or if their economy just stalled out.

---

## Repository Structure
```text
├── data/                  <- Raw and processed datasets
├── notebooks/             <- Jupyter Notebooks for data cleaning, EDA, and plots
├── src/                   <- Helper Python scripts for data processing
├── .gitignore             <- Keeps heavy data files off GitHub
├── LICENSE                <- MIT Open Source License
└── README.md              <- You are here!
