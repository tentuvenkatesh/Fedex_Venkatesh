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

✅ **Tip for Usage:**  
- For **time-series joins** → use Start Year/Month/Day + End Year/Month/Day.  
- For **economic comparisons across years** → always use inflation-adjusted fields.  
- For **mapping/geo-analysis** → prefer Admin Units over free-text `Location`.
