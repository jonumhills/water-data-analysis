# Water Data Retrieval & Summary

## 1. Source Selection
* [cite_start]**Target Location**: [Gila River near Gila, NM](https://waterdata.usgs.gov/monitoring-location/09430500/) (Monitoring Location: **USGS-09430500**). [cite: 89, 91]
* [cite_start]**State**: New Mexico (FIPS Code: **35**). [cite: 20]

## 2. Data Retrieved
* [cite_start]**Parameter**: Discharge, cubic feet per second (Code: **00060**). [cite: 31, 32]
* [cite_start]**Timeframe**: Last 90 days (**P90D**). [cite: 111]
* [cite_start]**Observation Count**: **5,000** data points. [cite: 126]

## 3. How to Run the Script
[cite_start]Ensure you have the following Python libraries installed: `requests`, `pandas`, `numpy`, and `matplotlib`. [cite: 3, 4, 5, 6] Copy the script provided below into a Jupyter Notebook or Python file and run the cells in order. The script will:
* [cite_start]**Query** the USGS OGC API for continuous streamflow data. [cite: 106, 120]
* [cite_start]**Clean** the data by converting timestamps to **UTC** and removing negative sensor error values. [cite: 135, 140]
* [cite_start]**Generate** a statistical summary (**Min, Max, Average**) and a time-series plot. [cite: 167, 168, 169, 186]
* [cite_start]**Save** the results to `cleaned_gila_river_data.csv` and `discharge_plot.png`. [cite: 192, 210]

## 4. Future Improvements
* **Dynamic Pagination**: With more time, I would implement a recursive pagination loop. Since the API often limits single responses (e.g., to 10 items default), a loop using the **next** link in the API response would ensure a complete record for very high-frequency or long-term requests.
