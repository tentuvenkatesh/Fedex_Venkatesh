# 📘 Dataset Overview — `public_emdat_custom_Ind.xlsx`

This dataset contains disaster event records for India (2018–2024) sourced from EM-DAT.  
Each row corresponds to a **unique disaster event** with identifiers, taxonomy, geospatial metadata, temporal coverage, and impact indicators.

---

## 🔑 Event Identifiers & Taxonomy

### 1. DisNo.
- **Type:** string  
- **Description:** Unique identifier for each disaster event.  
- **Example:** `2018-0023-IND`  
- **Use:** Primary key for deduplication and joins.

### 2. Historic
- **Type:** boolean/string  
- **Description:** Indicates if the record is historic or current.  
- **Example:** `No`  
- **Use:** Filtering contemporary vs. historic events.

### 3. Classification Key
- **Type:** string  
- **Description:** Compact internal taxonomy key for subclass of disaster.  
- **Example:** `tec-ind-fir-fir`  
- **Use:** Programmatic grouping by subclass.

### 4. Disaster Group
- **Type:** string  
- **Description:** Top-level disaster group.  
- **Example:** `Natural`, `Technological`  
- **Use:** Broad hazard categorization.

### 5. Disaster Subgroup
- **Type:** string  
- **Description:** Secondary grouping within Disaster Group.  
- **Example:** `Meteorological`, `Geophysical`  
- **Use:** Mid-level taxonomy analysis.

### 6. Disaster Type
- **Type:** string  
- **Description:** Human-readable disaster type.  
- **Example:** `Flood`, `Cyclone`  
- **Use:** Standard hazard labeling.

### 7. Disaster Subtype
- **Type:** string  
- **Description:** More granular subtype of disaster.  
- **Example:** `Flash flood`, `Tropical cyclone — landfall`  
- **Use:** Fine-grained hazard classification.

### 8. External IDs
- **Type:** string/list  
- **Description:** External identifiers linking to other databases.  
- **Example:** `GLIDE: TC-2019-000041-IND`  
- **Use:** Cross-referencing.

### 9. Event Name
- **Type:** string  
- **Description:** Human-readable event name or title.  
- **Example:** `Cyclone Fani`  
- **Use:** Reports, readability.

### 10. ISO
- **Type:** string  
- **Description:** ISO 3-letter country code.  
- **Example:** `IND`  
- **Use:** Country-level joins.

### 11. Country
- **Type:** string  
- **Description:** Country name.  
- **Example:** `India`  
- **Use:** Geographical filtering.

### 12. Subregion
- **Type:** string  
- **Description:** UN subregion.  
- **Example:** `South Asia`  
- **Use:** Subregional grouping.

### 13. Region
- **Type:** string  
- **Description:** Continent-level grouping.  
- **Example:** `Asia`  
- **Use:** Macro-regional analysis.

### 14. Location
- **Type:** string  
- **Description:** Free-text location (states, districts, provinces).  
- **Example:** `Odisha, West Bengal`  
- **Use:** Localized event context.

### 15. Origin
- **Type:** string  
- **Description:** Descriptor of hazard origin (genesis).  
- **Example:** `Offshore (Bay of Bengal)`  
- **Use:** Hazard genesis classification.

---

## 🌍 Event Attributes & Humanitarian Context

### 16. Associated Types
- Other disaster types linked (e.g., earthquake + landslide).

### 17. OFDA/BHA Response
- US OFDA/BHA response flag/details.

### 18. Appeal
- Whether an international/local appeal was issued.

### 19. Declaration
- Official emergency declaration (Yes/No/text).

### 20. AID Contribution ('000 US$)
- Monetary aid (in thousands USD).

---

## ⚡ Hazard Characteristics

### 21. Magnitude
- Numeric measure of intensity (context-dependent).  

### 22. Magnitude Scale
- Scale of magnitude (e.g., Richter, km/h).  

### 23–24. Latitude & Longitude
- Event coordinates in decimal degrees.  

### 25. River Basin
- Basin name (flood-specific).

---

## 📅 Temporal Coverage

### 26–28. Start Year, Month, Day  
- Event start date.

### 29–31. End Year, Month, Day  
- Event end date.

---

## 👥 Human Impact

### 32. Total Deaths
- Total fatalities.  

### 33. No. Injured
- People injured.  

### 34. No. Affected
- People requiring assistance.  

### 35. No. Homeless
- People rendered homeless.  

### 36. Total Affected
- Aggregate affected population (may overlap).

---

## 💰 Economic Impact

### 37–38. Reconstruction Costs & Adjusted
- Rebuilding cost (raw & inflation-adjusted).  

### 39–40. Insured Damage & Adjusted
- Insured losses (raw & adjusted).  

### 41–42. Total Damage & Adjusted
- Reported economic losses (raw & adjusted).  

### 43. CPI
- Index used for inflation adjustments.

---

## 🗺️ Geospatial & Metadata

### 44. Admin Units
- JSON-like structure with adm1/adm2 codes/names.  

### 45. Entry Date
- Record entry date.  

### 46. Last Update
- Last revision date.  

---
**Note:**
Since data is quite less we are adding USA also into our dataset,so our main dataset is **public_emdat_custom_Ind_usa.xlsx**
---------------------------------------------------------------------------------------------------------------------------------------
# 📘 Dataset Overview — `US_PortCalls.csv`

This dataset contains **port call statistics** for different vessel types across economies/ports.  
Each row represents **port performance indicators** (time in port, vessel size, capacity, etc.) by year, economy, and ship type.

---

## 📅 Temporal & Economy Identifiers

### 1. Year
- **Type:** integer  
- **Description:** Calendar year of the record.  
- **Example:** `2018`  

### 2. Economy
- **Type:** integer/code  
- **Description:** Numerical code for the reporting economy/region.  
- **Example:** `0`  

### 3. Economy Label
- **Type:** string  
- **Description:** Human-readable name of the reporting economy.  
- **Example:** `World`, `United States`  

---

## 🚢 Market & Vessel Classification

### 4. CommercialMarket
- **Type:** integer/code  
- **Description:** Encoded market segment identifier.  
- **Example:** `7`  

### 5. CommercialMarket Label
- **Type:** string  
- **Description:** Ship market segment / vessel type.  
- **Example:** `All ships`, `Dry bulk carriers`, `Container ships`  

---

## ⚓ Port Time Indicators

### 6. Median time in port (days)
- **Type:** float  
- **Description:** Median turnaround time in port (in days).  
- **Example:** `1.02`  

### 7. Median time in port (days) Footnote
- **Type:** string  
- **Description:** Footnote/reference about the reported value.  

### 8. Median time in port (days) Missing value
- **Type:** string  
- **Description:** Notes missing or unreported values.  

---

## ⏳ Vessel Age Indicators

### 9. Average age of vessels (years)
- **Type:** float  
- **Description:** Average age of vessels in the segment.  
- **Example:** `13.0`  

### 10. Average age of vessels (years) Footnote
- Footnote for context/limitations.  

### 11. Average age of vessels (years) Missing value
- Notes missing values.

---

## 📦 Container Ship Indicators

### 12. Average container carrying capacity (TEU) per container ship
- **Type:** float  
- **Description:** Average TEU capacity per container ship.  
- **Example:** `21413.0`  

### 13. Average container carrying capacity (...) Footnote
- Footnote details.  

### 14. Average container carrying capacity (...) Missing value
- Missing/not reported notes.

---

## 🚢 Vessel Size Indicators

### 15. Maximum size (GT) of vessels
- **Type:** float  
- **Description:** Largest vessel gross tonnage (GT) recorded.  
- **Example:** `234006.0`  

### 16–17. Footnote & Missing value  
- Context and missing data notes.

---

## ⚖️ Cargo Carrying Indicators

### 18. Maximum cargo carrying capacity (dwt) of vessels
- **Type:** float  
- **Description:** Maximum vessel deadweight tonnage (dwt).  
- **Example:** `441561.0`  

### 19–20. Footnote & Missing value  
- Context and missing notes.

---

## 📦 Container Ship Capacity Indicators

### 21. Maximum container carrying capacity (TEU) of container ships
- **Type:** float  
- **Description:** Maximum TEU capacity of container ships.  
- **Example:** `21413.0`  

### 22–23. Footnote & Missing value  
- Context and missing notes.

---

## 📊 Notes
- **Footnote columns** = Explanatory remarks about methodology/coverage.  
- **Missing value columns** = Explicit flags for unavailable data.  
- **Units:**  
  - Time = days  
  - Age = years  
  - Capacity = TEU (Twenty-foot Equivalent Units)  
  - Size = GT (Gross Tonnage)  
  - Cargo capacity = dwt (Deadweight tonnage)  

------------------------------------------------------------------------------------------------------------------
# 📘 Dataset Overview — `US_PortCallsArrivals.csv`

This dataset provides **port call counts (arrivals)** by **year**, **economy**, and **vessel/market segment**.  
Each row is a combination of temporal, geographic, and market identifiers with the KPI **Number of port calls**.

---

## 📅 Temporal & Economy Identifiers

### 1) Year
- **Type:** integer  
- **Description:** Calendar year of observation.  
- **Example:** `2018`

### 2) Economy
- **Type:** integer/code  
- **Description:** Encoded identifier for the reporting economy/region group.  
- **Example:** `1`

### 3) Economy Label
- **Type:** string  
- **Description:** Human-readable economy/region name.  
- **Examples:** `United States`, `World`, `Individual economies`

---

## 🚢 Market & Vessel Classification

### 4) CommercialMarket
- **Type:** integer/code  
- **Description:** Encoded market segment / vessel-type identifier.  
- **Example:** `7`

### 5) CommercialMarket Label
- **Type:** string  
- **Description:** Market segment / vessel type label.  
- **Examples:** `All ships`, `Dry bulk carriers`, `Container ships`, `LPG carriers`, `LNG carriers`, `Oil tankers`, `Ro-Ro`, etc.

---

## 📈 Core KPI

### 6) Number of port calls
- **Type:** integer/float  
- **Description:** Count of **vessel arrivals (port calls)** within the specified year, economy, and market segment.  
- **Units:** count (calls)  
- **Example:** `15432`

### 7) Number of port calls Footnote
- **Type:** string  
- **Description:** Methodological or coverage notes specific to the KPI value (e.g., definitions, scope limitations).

### 8) Number of port calls Missing value
- **Type:** string  
- **Description:** Explicit indicator that the KPI is unavailable, not applicable, or not separately reported.  
- **Examples:** `Not applicable`, `Not available or not separately reported`
