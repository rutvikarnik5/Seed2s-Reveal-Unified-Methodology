# reveal-australia-minerals
U.S.–Australia Critical Mineral Supply Chain Analysis - Reveal Global Consulting

# U.S.–Australia Critical Mineral Supply Chain Analysis
**Reveal Global Consulting**  
**Analysts:** Ohm Patel, Michelle Thomas, Edwin Zheng

---

## Project Overview
This project analyzes U.S. dependence on Australian critical mineral 
exports using trade data from the U.S. Census Bureau USA Trade Online 
(DataWeb) platform. The dataset covers 14 HS-4 commodity codes across 
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