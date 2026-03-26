# reveal-australia-minerals
U.S - Australia Critical Mineral Supply Chain Analysis - Reveal Global Consulting
# U.S.–Australia Critical Mineral Supply Chain Analysis
**Reveal Global Consulting**  
**Analysts:** Ohm Patel, Michelle Thomas, Edwin Zheng

---

## Project Overview
This project analyzes U.S. dependence on Australian critical mineral 
exports using trade data from the U.S. Census Bureau USA Trade Online 
(DataWeb) platform. The dataset covers 19 HTS-6 commodity codes across 
10 mineral categories, spanning 2015–2025. The objective is to uncover 
supply chain insights that can inform U.S. economic security and 
policy decisions.

---

## Why Australia?
Australia is one of the world's most important exporters of strategic 
minerals critical to batteries, renewable energy systems, defense 
technology, and advanced manufacturing. It holds the world's largest 
reserves of several key minerals including lithium, titanium minerals, 
zirconium, and nickel.

Beyond raw resource wealth, Australia is a close U.S. ally operating 
under frameworks including the Australia–United States Free Trade 
Agreement (AUSFTA) and the AUKUS trilateral defense pact. As the U.S. 
seeks to reduce supply chain dependence on China — which dominates 
processing of most critical minerals — Australia represents one of the 
most viable and trusted alternative sources.

---

## Why These Commodities?
The 19 commodities selected represent Australia's most strategically 
relevant mineral exports to the United States across four supply chain 
stages: raw ore, chemical compounds, intermediate products, and refined 
metals. Selection criteria included:

- Confirmed trade flow from Australia to the U.S. (2015–2025)
- Strategic relevance to batteries, clean energy, aerospace, or defense
- Australia's position as a top global producer or reserve holder
- U.S. policy prioritization under the IRA, CHIPS Act, or DoD 
  critical mineral designations

---

## Commodities Covered

| HTS Code | Description | Mineral | Supply Chain Stage |
|---|---|---|---|
| 253090 | Mineral Substances NESOI | Lithium (Spodumene) | Ore |
| 260600 | Aluminum Ores & Concentrates | Bauxite | Ore |
| 261400 | Titanium Ores & Concentrates | Titanium | Ore |
| 261510 | Zirconium Ores & Concentrates | Zirconium | Ore |
| 261590 | Niobium/Tantalum/Vanadium Ores | Tantalum | Ore |
| 281820 | Aluminum Oxide (Calcined Alumina) | Aluminum | Compound |
| 281830 | Aluminum Hydroxide | Aluminum | Compound |
| 282300 | Titanium Oxides | Titanium | Compound |
| 282520 | Lithium Oxide & Hydroxide | Lithium | Compound |
| 284690 | Rare Earth Compounds NESOI | Rare Earths | Compound |
| 740311 | Refined Copper Cathodes | Copper | Refined |
| 750120 | Nickel Oxide Sinters | Nickel | Intermediate |
| 750210 | Unwrought Nickel, Not Alloyed | Nickel | Refined |
| 750220 | Unwrought Nickel Alloys | Nickel | Refined |
| 760110 | Unwrought Aluminum, Not Alloyed | Aluminum | Refined |
| 760120 | Unwrought Aluminum Alloys | Aluminum | Refined |
| 810520 | Cobalt Mattes & Unwrought Cobalt | Cobalt | Intermediate/Refined |
| 810820 | Unwrought Titanium; Powders | Titanium | Refined |
| 810920 | Unwrought Zirconium; Powders | Zirconium | Refined |

---

## Data Source
- **Platform:** U.S. Census Bureau USA Trade Online (DataWeb)
- **Trade Flow:** U.S. General Imports
- **Partner Country:** Australia
- **Years:** 2015–2025
- **Measures:** General Customs Value (USD), First Unit of Quantity, 
  CIF Imports Value (USD)
- **Commodity Level:** HTS-6

---

## Repository Structure
- `data/` — Cleaned trade dataset (DataWeb export, manually cleaned)
- `context/` — Australia background and commodity selection rationale
- `query-parameters/` — DataWeb query methodology and parameter log
