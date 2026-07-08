# Electric Vehicle Population Analysis Dashboard

A Tableau dashboard analyzing the population of registered Battery Electric Vehicles (BEVs) and Plug-in Hybrid Electric Vehicles (PHEVs), built as part of a Data Visualization coursework project.

## Overview

Electric vehicle adoption has grown rapidly over the past few years, and this project explores that growth through the lens of official vehicle registration data. Using a dataset of 130,443 registered EVs, this dashboard examines who is buying electric vehicles, which manufacturers and models dominate the market, how adoption has trended over time, and how far these vehicles can typically travel on a single charge. The result is a clear, visual story of EV adoption in Washington State  from Tesla's overwhelming market lead, to the sharp rise in registrations over the last three years, to the balance between fully-electric and plug-in hybrid ownership.

## Data Source

**Electric Vehicle Population Data**, published by the Washington State Department of Licensing (DOL), via [data.wa.gov](https://data.wa.gov/Transportation/Electric-Vehicle-Population-Data/f6w7-q2d2). The dataset lists BEVs and PHEVs registered through Washington State DOL, with 17 fields per record including make, model, year, electric range, CAFV eligibility, and location.

The analysis uses the March 2025 release of the dataset (130,443 records). Because the Washington DOL regularly updates the data, the current online version may include more records than those analyzed in this project.

## Dashboard Views

- **Dashboard Overview** — combined summary view
- **Total Vehicles by State**
- **Top 10 Total Vehicles by Make**
- **Total Vehicles by Model Year**
- **Total Vehicles by Model**
- **Total BEV Vehicles / Total PHEV Vehicles**
- **Total Vehicles by CAFV Eligibility**
- **Avg Electric Range**

## Key Insights

- **Total registered vehicles**: 130,443
- **Vehicle type split**: 100,156 BEV (76.8%) vs. 30,287 PHEV (23.2%) - battery-electric vehicles dominate over plug-in hybrids
- **Top manufacturer**: Tesla, with 59,629 vehicles - 45.7% of all registrations, more than the next 4 manufacturers combined (Nissan: 13,023, Chevrolet: 11,251, Ford: 6,743, BMW: 5,696)
- **Geographic concentration**: 130,138 of 130,443 vehicles (99.8%) are registered in Washington State, with small numbers spread across other states (California, Virginia, Maryland, Texas)
- **Model years covered**: 1997–2023, with adoption peaking in recent years - 2022 alone accounts for 28,013 vehicles, followed by 2021 (18,445) and 2023 (18,217)
- **Average electric range**: ~130 miles (calculated only on vehicles with a recorded range - see data quality note below)
- **CAFV eligibility split**: 60,551 vehicles confirmed eligible, 53,446 "unknown - range not yet researched," 16,446 not eligible due to low battery range

## Data Quality Notes

- **`Base MSRP`** is 0 (unpopulated) for 97% of records (127,025 of 130,443) - this field is not reliable for price analysis in this dataset.
- **`Electric Range`** is 0 for 53,446 records (41%) - this doesn't mean zero range; it corresponds exactly to vehicles marked "eligibility unknown as battery range has not been researched." These zero values were excluded when calculating the average range above.
- A small number of records (3–305 rows) have missing values in minor fields (City, County, Postal Code, Model, Legislative District) - negligible relative to dataset size.
- No duplicate rows or duplicate vehicle IDs were found.

## Screenshots

### Dashboard Overview
![Dashboard Overview](Images/Dashboard%20overview.png)

### Total Vehicles by State
![Total Vehicles by State](Images/Total%20vehicles%20by%20state.png)

### Top 10 Vehicles by Make
![Top 10 Vehicles by Make](Images/Top%2010%20total%20vehicles%20by%20make.png)

### Total Vehicles by Model Year
![Total Vehicles by Model Year](Images/Total%20vehicle%20by%20model%20year.png)

## Files in This Repository
ev-population-dashboard/

├── DAV_25016654.twbx                           

├── Electric_Vehicle_Population_Data.csv         

├── Images/                                      

└── README.md

## How to View

1. Download `DAV_25016654.twbx`
2. Open with [Tableau Desktop](https://www.tableau.com/products/desktop) or [Tableau Reader](https://www.tableau.com/products/reader) (free)
3. Alternatively, view the screenshots above for a quick preview without installing Tableau

## Tools Used

- Tableau Desktop
- Dataset: Washington State DOL Electric Vehicle Population Data

*Data Visualization Coursework Project*
