# Water Data Retrieval & Summary

## 1. Source Selection
**Target Location**: [Gila River near Gila, NM](https://waterdata.usgs.gov/monitoring-location/09430500/) (Monitoring Location: **USGS-09430500**). <br>
**State**: New Mexico (FIPS Code: **35**).

## 2. Data Retrieved
**Parameter**: Discharge, cubic feet per second (Code: **00060**). <br>
**Timeframe**: Last 90 days (**P90D**). <br>
**Observation Count**: **5,000** data points. <br>

## 3. How to Run the Script
Ensure you have the following Python libraries installed: `requests`, `pandas`, `numpy`, and `matplotlib`. <br>
<br>
Copy the script provided below into a Jupyter Notebook or Python file and run the cells in order. The script will: <br>
**Query** the USGS OGC API for continuous streamflow data. <br>
**Clean** the data by converting timestamps to **UTC** and removing negative sensor error values. <br>
**Generate** a statistical summary (**Min, Max, Average**) and a time-series plot. <br>
**Save** the results to `cleaned_gila_river_data.csv` and `discharge_plot.png`. <br>

## 4. Future Improvements
**Dynamic Pagination**: With more time, I would implement a recursive pagination loop. Since the API often limits single responses (e.g., to 10 items default), a loop using the **next** link in the API response would ensure a complete record for very high-frequency or long-term requests.
