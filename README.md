Water Data Retrieval & Summary
1. Source Selection

Target Location: Gila River near Gila, NM (Monitoring Location: USGS-09430500).
State: New Mexico (FIPS Code: 35).

2. Data Retrieved
Parameter: Discharge, cubic feet per second (Code: 00060).
Timeframe: Last 90 days (P90D).
Observation Count: 5,000 data points.


3. How to Run the Script
Ensure you have the following Python libraries installed: requests, pandas, numpy, and matplotlib. 
Copy the script provided below into a Jupyter Notebook or Python file and run the cells in order. The script will:
Query the USGS OGC API for continuous streamflow data.
Clean the data by converting timestamps to UTC and removing negative sensor error values.
Generate a statistical summary (Min, Max, Average) and a time-series plot.
Save the results to cleaned_gila_river_data.csv and discharge_plot.png.


4. Future Improvements
Dynamic Pagination: With more time, I would implement a recursive pagination loop. Since the API often limits single responses (e.g., to 10 items default), 
a loop using the next link in the API response would ensure a complete record for very high-frequency or long-term requests.
