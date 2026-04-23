# Unified Methodology Application to Southeast Asia

**SEED2S+Reveal Global Consulting**  
Authors: Rutvi Karnik, Ken Wang, Pranjal Patel

---

## Project Overview
This project builds upon two previously established methodologies that examined U.S. critical mineral import patterns from Canada and East and Southeast Asia to assess trade relationships. We developed a unified methodology, and to test its reproducibility for any world region, we applied it to familiar data and unseen data and compared the results. This README is for navigating the Retrospective Team's work, who implemented the methodology on Southeast Asia data.

## Definition of Region
This project uses the regional classification framework defined by the United Nations Sustainable Development Goals (UN SDG). Under this definition, Southeast Asia is treated as a distinct subregion within Eastern and South-Eastern Asia. Our methodology can be applied to any subregion of the seven major regions as defined by UN SDG. If no subregion exists, as in the case of Sub-Saharan Africa, the major region would be appropriate instead. This allows for improved reproducibility across regions and follows widely used global datasets and methodologies.

The 11 countries included in Southeast Asia are: Brunei, Cambodia, Indonesia, Laos, Malaysia, Myanmar (Burma), Philippines, Singapore, Thailand, Timor-Leste, and Vietnam.

Source: [Our World in Data – World Region Map Definitions](https://ourworldindata.org/world-region-map-definitions)

## Why Southeast Asia?
The previous cohort's regions were Canada and East and Southeast Asia. Canada is not a subregion as per our chosen UN SDG definition, so the methodology could not be applied to Canada unless we considered the whole subregion of Northern America with three additional countries. East Asia as a subregion consists of China, which was previously excluded because its dominance over global critical mineral
processing can obscure patterns among other suppliers. 

Since our goal was to apply the methodology to familiar data, we chose Southeast Asia as our region because the two other potential regions would have included new data.

## Methodology
Please take a look at the project's [main README](../README.md) for information on the unified methodology.

## Results / Findings
* Total imports by both real and nominal values increased over the year range 2010 - 2025, with the sharpest increase occurring in 2022. The pattern shows a decline in 2023, followed by another increase in 2024.
* The top commodities included aluminum and copper, with the top 3 commodities composing almost 50% of U.S. imports from Southeast Asia.
* 70.3% of all imports from Southeast Asia were refined or processed materials. 26% were categorized as "Other" and 3% were raw materials.
* The top 3 countries were Thailand, Vietnam, and Indonesia, in that specific order.
* Thailand saw a spike in their exports of aluminum to the United States in 2022, while Vietnam's steadily rose. Indonesia's exports did not seem to increase in comparison.
* 2022 stands out as the strongest import year, with 2025 following close behind.
* For month-over-month volatility, aluminum is the top volatile commodity with repeated sharp fluctuations over time.
* Laos is the most volatile country for month-over-month analysis.
* For year-over-year volatility, the commodity "Natural Graphite" with HS Code 2504 is the most volatile.
* Brunei is the most volatile country for year-over-year analysis, displaying irregular spikes in imports.

## Repository Structure
```
└── 📁Retrospective Team                  # This folder
    ├── EDA.ipynb                               # Data Analysis and Visualizations 
    ├── inflation_rates.csv                     # CSV file of inflation rates from 2010-2025
    ├── main.ipynb                              # Data Preprocessing and Cleaning
    ├── README.md                               # This file - information about the Retrospective Team's work
    ├── retrospective_data_cleaned.csv          # Final cleaned dataset
    └── retrospective_raw_data.csv              # Raw dataset
```