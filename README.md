# RealEstate_EDA
Exploratory data analysis for world real estate data

1. **Exploratory Data Analysis (Data Info)**: Initial diagnostic assessment mapping schema boundaries, memory footprint, data distributions, and extreme underlying anomalies.
2. **Data Handling & Cleaning**: Advanced regular expression parsing to clean raw measurement labels (`" m²"` suffixes), multi-criteria logical masking to neutralize physical anomalies (e.g., properties with 43 bathrooms, 2009 bedrooms, 1 m^2 apartment area, or negative floor levels), and schema type casting using Pandas' specialized **Nullable Integer Types (`Int64`)** to ensure mathematical integrity.
3. **Feature Engineering**: Calculation of secondary valuation metrics—including price per square meter (`price_per_sqm`) and building age metricsto unlock deep behavioral insights. 
4. **Targeted Analysis**: Executing segmented boolean filters, multi-axis groupings, and structural aggregations to map out market cost-effectiveness, layout efficiency, liquidity thresholds, and optimal city-level spatial yields.
5. **Interactive Dashboarding**: Porting the analytical boundaries into a highly responsive, interactive Streamlit deployment tailored for on-the-ground corporate acquisition teams.

---

## Core Analytical Objectives

*   **Objective 1 (Market Selection)**: Identify the top five most cost-effective international nations based on average purchase price per square meter ($USD/\\text{Area}$) for contemporary real estate assets (built $\\ge 2011$).
*   **Objective 2 (Asset Optimization)**: Evaluate how average valuations scale across various bedroom and bathroom layouts within the target nations to uncover the optimal, value-maximizing asset profile.
*   **Objective 3 (Liquidity & Volume Evaluation)**: Assess active listing density across selected regions to ensure scalable corporate capital deployment without inducing localized market price inflation.
*   **Objective 4 (Capital Allocation Strategy)**: Isolate specific micro-markets/cities that yield the maximum usable square footage under an institutional budget cap of $500,000 to $1,500,000 USD per property.

---

## Key Data Insights

*   **The Cost Effectiveness Frontier**: Georgia, Russia, Thailand, and Northern Cyprus offer elite contemporary entry points, exhibiting base valuations under **$3,000 USD per square meter**. Conversely, the UAE represents an ultra-premium tier, averaging over **$8,000 USD per square meter**.
*   **The Luxury Premium Trap**: Properties with standard layouts scale predictably between **$1,937 and $8,791 USD/sqm**. However, high-density 5-bedroom, 4-bathroom luxury configurations reflect massive speculative inflation, surpassing **$12,137 USD/sqm**.
*   **Liquidity Concentrations**: Russia possesses extreme market depth with over **17,500 active listings**, providing maximum insulation against price distortion. Northern Cyprus presents heightened structural liquidity risk, restricting inventory to **fewer than 1,000 active units**.
*   **Spatial Yield Optimization**: Under the designated $500K–$1.5M corporate budget, administrative micro-markets around Moscow, Russia (Pervomayskoe and Marushkinskoe) yield maximum space (**400–550 sqm**), while Ban Kata (Phuket, Thailand) and Batumi (Georgia) provide top-performing lifestyle/coastal diversification alternatives (**300–335 sqm**).

---

## Directory Structure
```text
├── Data/
│   ├── worlds_real_estate_data.csv       # Original raw dataset
│   └── worlds_real_estate_cleaned.csv    # Pristine, optimized dataset
├── Notebooks/
│   └── Real_Estate_EDA_Notebook.ipynb    # Interactive EDA and full analytical pipeline
├── App/
│   └── dynamic_market_dashboard.py       # Streamlit interactive application script
├── Deliverables/
│   └── Executive_Strategy_Deck.pdf       # presentation slides
└── README.md                             # Comprehensive technical documentation
