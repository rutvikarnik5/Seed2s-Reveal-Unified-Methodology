# Critical Minerals and International Trade: Harmonized Methods and Analysis

**SEED2S+Reveal Global Consulting**  
Authors: Rutvi Karnik, Ohm Patel, Pranjal Patel, Michelle Thomas, Ken Wang, Edwin Zheng

---

## Project Overview
This project builds upon two previously established methodologies that examined U.S. critical mineral import patterns from Canada and East and Southeast Asia to assess trade relationships. Our goal was to develop a robust and reproducible unified methodology. To test its reproducibility for any world region, a Retrospective Team applied it to familiar data (Southeast Asia) and a Prospective Team applied it to unseen data (South America), comparing the results. This README is for summarizing our project, and further work by the Retrospective Team and Prospective Team can be found by navigating to their appropriate folders.

## Key Findings
* Thailand, Vietnam, and Indonesia account for 81.4% of U.S. critical mineral imports from Southeast Asia. This concentration increases strategic vulnerability, as disruptions in any of these suppliers could threaten supply chain stability.
* Refined materials and manufactured articles account for 70.3% of total real import value from Southeast Asia. This indicates strong reliance on processed industrial inputs, increasing exposure to external production disruptions and trade shocks.
* The largest import commodity from Southeast Asia (aluminum) accounts for 17.8% of total real import value. This concentration increases vulnerability to price volatility, export restrictions, and supply disruptions in a single commodity market.
* 3 countries (Chile, Peru, Brazil) supply 93.8% of all U.S. critical mineral imports from South America. Simultaneous disruptions in any one country could severely impact U.S. supply chains
Limited fallback options among remaining 9 South American countries (<7% combined).
* Refined copper alone accounts for 71.6% of total real import value ($51.6B over 2010–2025). Over 74% of imports arrive as refined/processed materials, meaning the U.S. depends on foreign processing capacity. Disruptions to copper supply or refining would have outsized national security consequences.
* Real import value grew 158% from 2020 ($3.1B) to 2025 ($7.9B) — a 15-year high. Growth driven by clean energy and EV expansion, making South American minerals increasingly critical. Demand trajectory suggests supply concentration risk will intensify, not diminish.
* Nominal values overstate real import growth by up to 48% in 2025 ($11.6B nominal vs. $7.9B real). Without inflation adjustment, policymakers may overestimate trade stability and underestimate vulnerability. Harmonized methodologies CPI adjustment is essential for accurate, reproducible supply chain analysis.

## Unified Methodology
After assessing the strengths and weaknesses of the two separate methodologies utilized by the previous Fall 2025 cohort, our team established a unified methodology framework. The goal was to make it robust and reproducible, easily applied to any world region for gathering trade and national security insights.

### Definition of Region
This project used the regional classification framework defined by the United Nations Sustainable Development Goals (UN SDG). Our methodology can be applied to any subregion of the seven major regions as defined by UN SDG. If no subregion existed, as in the case of Sub-Saharan Africa, the major region would be appropriate instead. This allows for improved reproducibility across regions and follows widely used global datasets and methodologies.

Source: [Our World in Data – World Region Map Definitions](https://ourworldindata.org/world-region-map-definitions)

### Data Collection
Critical mineral trade data was exported from the U.S. Census Bureau's USA Trade Online database which provides Harmonized System (HS) code classifications for all commodities. The data was exported as CSV files.

### Data Preprocessing and Transformation
The following variables were retained or created:
* 4-digit HS Code
* Commodity
* Year
* Month
* Real Value (USD)
* Nominal Value (USD)
* Annual Inflation Rate
* Consumer Price Index (CPI)
* Category Type


**Commodity Classification**  
For category type, each commodity was classified based on its processing stage. The approach followed the same function that was developed by the previous cohort with some changes such as incorporating additional keywords within the classification. The four possible categories were:
* Ore / Raw - minimally processed
* Compound - chemical forms such as oxides or salts
* Refined / Articles - processed products
* Advanced Product - downstream products such as batteries

**Nominal to Real Value Conversion**  
The chosen base year was 2010 and 100 was its consumer price index. The following equation was used to compute CPI values for all observations.

$$\mathrm{CPI}_{\text{current}} = \mathrm{CPI}_{\text{past}} \left( \frac{\text{inflation rate}}{100} + 1 \right)$$

Then we converted to real values using:

$$\mathrm{\text{Real Value}} = \left(\frac{\text{Nominal Value}}{\text{CPI}} \right) * 100$$

**Data Validation and Cleaning**  
We identified missing values and checked for duplicate rows. We also removed negative values in variables where they did not make sense such as year, month, real value, etc. We ensured numerical variables were of type numeric. Lastly, we evaluated for outliers and explored whether they had been caused by false reporting or code error.

### Data Analysis
We produced various visualizations to aid our analyses. We wished to see whether certain patterns would reveal implications for supply chain risk or trade vulnerability. The following is a non-comprehensive list of visualizations we utilized:
* Total Imports per Year in Real and Nominal value
* Top 10 Commodities by Real Value
* Percent Share of the Total Real Imports for the Top 5 Commodities
* Time-series for Top 3 Commodities over Month-Year by Real Value
* Pie Chart of Category Type by Total Real Value
* Percent Share of the Total Real Imports for the Top 3 Countries
* Line Plot of Monthly Average Real Import
* Heatmap of Real Imports by Month and Year
* Top 5 Most Volatile Commodities (monthly and yearly)
* Top 3 Most Volatile Countries (monthly and yearly)

For a full list, please consult our manuscript.

## Application of Unified Methodology
In order to test the methodology’s usefulness, a Retrospective and Prospective team were formed. The Retrospective team’s purpose was to apply the methodology to a familiar world region. They picked Southeast Asia as their region. On the other hand, the Prospective team applied the methodology to a new region with unseen data. They picked South America, a subregion under Latin America and the Caribbean.

Once both teams had applied the methodology to their separate regions, they reconvened to discuss their results and evaluate the reproducibility of the unified methodology.

Both teams found similar key indicators: import concentration, refined material dependency, country level vulnerability. The methodology was successful because of three key parts:
1) Universal HS Codes: allows the methodology to be similarly applied to any world region data.
2) Standardized Pipeline: clear outlined steps for data preprocessing and analysis makes the methodology reusable.
3) Cross Region consistency: no matter the region, the methodology is able to produce consistently formatted findings that directly connect to trade insights and national security.

## Repository Structure
```
└── 📁Retrospective Team                    # Retrospective Team
└── 📁Seed2s-Reveal-Unified-Methodology     # Prospective Team
└── README.md                               # This file - information about the project
```