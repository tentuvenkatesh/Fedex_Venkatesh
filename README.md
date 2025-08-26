****Data sets Overview****

**1.public_emdat_custom_Ind**

**1.DisNo.:**
Unique event identifier (string). Example format: 2018-0023-IND. Use this as the primary key for an event/record.

**2.Historic:**
Flag indicating whether the record is historic (e.g., Yes/No). Your samples show No for contemporary events.

Classification Key
A compact coded taxonomy key for the event (internal classification code, e.g., tec-ind-fir-fir). Useful for programmatic grouping by very specific subclass.

Disaster Group
Top-level group of the disaster (e.g., “Natural” or “Technological”). High-level category.

Disaster Subgroup
A second-level grouping within the group (e.g., “Meteorological”, “Climatological”, “Geophysical”, etc.).

Disaster Type
The named disaster type (human-readable) such as Flood, Cyclone, Earthquake, Drought, etc.

Disaster Subtype
More granular subtype where available (e.g., “riverine flood”, “flash flood”, “tropical cyclone — landfall”, etc.).

External IDs
Identifiers/references to external sources or other databases (may be a JSON list or semicolon-separated IDs). Use to crosswalk with other datasets.

Event Name
Free-text event name or title (e.g., “Cyclone Fani”). Helpful for human-readable reports and matching.

ISO
ISO country code (likely IND for India in your file). Good for joins and country-level grouping.

Country
Country name (e.g., India).

Subregion
Geographic subregion (e.g., parts of Asia; sometimes UN subregion names).

Region
Larger region or continent-level label (e.g., South Asia, Asia).

Location
Free-text place description — states, districts, provinces, or locality descriptions describing where the event affected.

Origin
Short descriptor of event origin (e.g., where hazard originated or the causal source). The exact semantics can vary; sometimes indicates whether the hazard originated offshore, inland, etc.

Associated Types
Other disaster types associated with the event (e.g., an earthquake that triggered landslides — a list of associated hazards).

OFDA/BHA Response
Indicator or note about response by OFDA/BHA (US Agency for International Development Office of U.S. Foreign Disaster Assistance / Bureau for Humanitarian Assistance). Could be a flag, note, or response amount.

Appeal
Whether an international/local humanitarian appeal was issued (and possibly the appeal amount if recorded).

Declaration
Whether an official declaration (e.g., national emergency, state of calamity) was made. Might be a yes/no or textual description.

AID Contribution ('000 US$)
Monetary aid contribution recorded (units: thousands of US dollars). Check whether this is donor-specific or total aid.

Magnitude
Numeric magnitude measure relevant for the disaster (earthquake magnitude, maximum wind speed, etc.). The meaning depends on Magnitude Scale.

Magnitude Scale
The scale used for the magnitude (e.g., Richter, Saffir-Simpson, MMI, km/h etc.). Read together with Magnitude.

Latitude
Latitude coordinate (decimal degrees) for the event location/epicenter/affected area.

Longitude
Longitude coordinate (decimal degrees) for the event location/epicenter/affected area.

River Basin
Name of river basin if relevant (mainly for floods).

Start Year
Integer year when the event started.

Start Month
Start month (1–12) when the event began.

Start Day
Start day of month (1–31) when the event began.

End Year
Integer year when the event ended (may equal Start Year for short events).

End Month
End month (1–12).

End Day
End day of month (1–31).

Total Deaths
Total number of fatalities attributable to the event. (Dataset may or may not distinguish direct vs indirect deaths — check metadata if you need that breakdown.)

No. Injured
Number of injured people as recorded.

No. Affected
Number of people “affected” (usually people who require immediate assistance — definitions vary between datasets). Often includes displaced, homeless, injured, etc.

No. Homeless
Number of people rendered homeless by the event (people without shelter/housing due to the disaster).

Total Affected
Another measure of affected population. In some schemas this is a derived/aggregate field (or overlaps with No. Affected) — treat cautiously and inspect row-level values to understand the exact meaning in your file.

Reconstruction Costs ('000 US$)
Estimated reconstruction costs (in thousands of USD) — the cost of rebuilding infrastructure, houses, etc.

Reconstruction Costs, Adjusted ('000 US$)
Reconstruction costs adjusted for inflation (CPI) to a reference year (units: thousands of USD).

Insured Damage ('000 US$)
Portion of damage that was insured (in thousands of USD).

Insured Damage, Adjusted ('000 US$)
Insured damage adjusted for inflation (thousands of USD).

Total Damage ('000 US$)
Total economic damages (direct losses) reported, in thousands of USD.

Total Damage, Adjusted ('000 US$)
Total damage adjusted for inflation (thousands of USD). Use this for cross-year comparisons.

CPI
Consumer Price Index (or an index/factor used to adjust monetary values). Likely the factor or index year used to compute the “Adjusted” columns.

Admin Units
Structured information about administrative units affected (your samples show JSON-like lists containing adm1_code, adm1_name, adm2_code, adm2_name, etc.). Good for mapping to subnational polygons or for granular spatial joins.

Entry Date
Date the record was entered into the database (YYYY-MM-DD). Useful to track ingestion time.

Last Update
Date the record was last updated (YYYY-MM-DD). Helpful to know whether values (e.g., damage or deaths) were revised later.
