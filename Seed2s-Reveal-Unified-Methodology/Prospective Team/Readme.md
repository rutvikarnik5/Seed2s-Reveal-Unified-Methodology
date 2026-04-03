# Reproducibility of Unified Methodology in Latin America America


# U.S.Latin America Critical Mineral Supply Chain Analysis
**Reveal Global Consulting**  
**Analysts:** Ohm Patel, Michelle Thomas, Edwin Zheng

---

# Project Overview
This project aims to test the reproducibility of a unified methodology by analyzing US critical mineral imports from Latin America, specifically the subregion of South America. This analysis is done using trade data from the U.S. Census Bureau USA Trade Online(DataWeb) platform. The analysis focuses on 12 countries within the subregion of South America and covers data spanning from 2010 - 2025. The objective is to uncover supply chain insights that can inform U.S. economic security and policy decisions.


## Definition of Region
This project uses the regional classification framework defined by the United Nations Sustainable Development Goals (UN SDG).
Under this definition, **South America** is treated as a distinct subregion within Latin America and the Caribbean. This allows for improved reproducibility across regions and follows widely used global datasets and methodologies.

The countries included in South America under this definition are:
Argentina, Bolivia, Brazil, Chile, Colombia, Ecuador, Guyana, Paraguay, Peru, Suriname, Uruguay, and Venezuela.

Source: Our World in Data – World Region Map Definitions  
https://ourworldindata.org/world-region-map-definitions


## Why Latin America?
Latin America, specifically the subregion of South America was chosen to evaluate the reproducibility of the methodology because the region plays a significant role in the global supply of critical minerals, including lithium, copper, and other resources essential for emerging technologies and clean energy systems. Several South American countries are key contributors to these supply chains, making the region highly relevant for analysis.

Additionally, Latin America has strong trade relations with the US and this makes them an important component of U.S. supply chains. The U.S. is aggressively strengthening critical mineral trade with South America, launching a $billion+ investment push in 2026 to secure supply chains for lithium, copper, and rare earths. Key agreements are focusing on Argentina and Brazil to reduce dependency on China which makes researching this region crucial. 

The diversity of economic structures, resource endowments, and trade patterns across countries in South America serves as a perfect test case in order to evaluate whether the unified methodology can produce reproducible and consistent insights. Furthermore, the availability of international trade and resource datasets for this region supports reproducible analysis. 

---

# Methodology

## Data Sources

Data for this analysis was obtained from U.S. Census Bureau's USA Trade Online database. 
URL: https://usatrade.census.gov/

Each record contains:
HS Code: Harmonized System commodity classification code
Commodity Description: Detailed product description
Country: Country of origin
Year/Month: Temporal dimension
Customs Value: Import value in U.S. dollars

## Data Limitations

## Data Preprocessing

### Data Formatting
- Multiple CSV files containing different critical minerals (e.g., copper, lithium, nickel, tin) were combined into a single dataset  
- Key variables were extracted and standardized, including:
  - HS Code (4-digit)
  - Commodity Name
  - Year
  - Country
  - Nominal Trade Value (USD)
- - The dataset is annual, therefore, a `Month` column was included but set to null for all entries  


### Data Cleaning
- Aggregate regional entries (e.g., “South America”, “South/Central America”) were removed to avoid double counting  
- Data was filtered to include only South American countries  
- Nominal values were cleaned by removing formatting (e.g., commas) and converted to numeric types  
- Columns such as Year, Value, and CPI were explicitly cast to numeric formats  
- Missing values were identified and documented  
- Duplicate rows were removed, and unique combinations of HS Code, Country, and Year were verified  


### Inflation Adjustment
To enable consistent comparisons over time, nominal trade values were converted to real values:
- Base Year: 2010 (CPI = 100)  
- Annual CPI values were calculated using U.S. inflation rates  
- Real values were computed using the formula:  
  **Real Value = (Nominal Value / CPI) × 100**

This adjustment accounts for inflation and allows for meaningful time-series analysis.


### Data Validation
- Negative or invalid values were checked across key variables  
- Duplicate time entries for each (HS Code, Country) pair were identified and resolved  
- Outliers were detected using the interquartile range (IQR) method  
  - Outliers were not removed but flagged for interpretation during analysis 

---

## Repository Structure

## Project Structure

```
.
├── data/
│   ├── raw/
│   │   ├── Copper & Graphite.csv
│   │   ├── Lithium, Cobalt, Sliver.csv
│   │   ├── Nickel, Manganese, Niobium.csv
│   │   └── Tin, Zinc.csv
│   │
│   └── processed/
│       └── south_america_cleaned.csv

├── main.ipynb
├── README.md
```

---

## Results/ Findings


## Why These Commodities?
The 14 commodity codes selected represent Australia's most strategically 
relevant mineral exports to the United States across four supply chain 
stages: raw ore, chemical compounds, intermediate products, and refined 
metals. Selection criteria included confirmed trade flow from Australia 
to the U.S. between 2015 and 2025, strategic relevance to batteries, 
clean energy, aerospace, or defense, Australia's position as a top 
global producer or reserve holder, and U.S. policy prioritization under 
the IRA, CHIPS Act, or DoD critical mineral designations.

---

## Commodities Covered
| HS Code | Description | Mineral | Supply Chain Stage |
|---|---|---|---|
| 2530 | Mineral Substances NESOI | Lithium (Spodumene) | Ore |
| 2606 | Aluminum Ores & Concentrates | Bauxite | Ore |
| 2614 | Titanium Ores & Concentrates | Titanium | Ore |
| 2615 | Zirconium/Niobium/Tantalum Ores | Zirconium, Tantalum | Ore |
| 2818 | Aluminum Oxide & Hydroxide | Aluminum | Compound |
| 2823 | Titanium Oxides | Titanium | Compound |
| 2825 | Lithium Oxide & Hydroxide | Lithium | Compound |
| 2846 | Rare Earth Compounds | Rare Earths | Compound |
| 7403 | Refined Copper | Copper | Refined |
| 7502 | Nickel Products | Nickel | Intermediate/Refined |
| 7601 | Unwrought Aluminum | Aluminum | Refined |
| 8105 | Cobalt Mattes & Unwrought Cobalt | Cobalt | Intermediate/Refined |
| 8108 | Unwrought Titanium & Powders | Titanium | Refined |
| 8109 | Unwrought Zirconium & Powders | Zirconium | Refined |

---

## Data Source
- **Platform:** U.S. Census Bureau USA Trade Online (DataWeb)
- **Trade Flow:** U.S. General Imports
- **Partner Country:** Australia
- **Years:** 2015–2025
- **Measures:** General Customs Value (USD), First Unit of Quantity, 
  CIF Imports Value (USD)
- **Commodity Level:** HS-4

---

## Repository Structure
- `data/raw/` — Unmodified DataWeb exports
- `data/cleaned/` — Processed and cleaned trade data
- `scripts/` — Python or R analysis scripts
- `outputs/` — Charts, visualizations, and summary tables
- `context/` — Australia background and commodity selection rationale
- `query-parameters/` — DataWeb query methodology and parameter log