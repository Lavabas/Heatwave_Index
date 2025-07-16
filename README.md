# Heat Wave Index Analysis over Central-Southeastern Sri Lanka (2000–2020)
Climate extremes like heat waves are becoming more frequent and severe, especially in tropical countries like Sri Lanka. Monitoring and mapping these events is vital for:
  - Water resource management
  - Disaster preparedness
  - Agricultural planning

This project investigates the spatiotemporal dynamics of heat waves in Central-Southeastern Sri Lanka (80.0°–81.5°E, 6.5°–8.5°N) over the past two decades. By combining real-world reanalysis climate data and open-source tools, I quantify the Heat Wave Index (HWI) to identify years and regions at greatest risk from extreme heat.

## Workflow
1. Download Climate Data (ERA5)
  - Variable: maximum_2m_air_temperature
  - Time range: 2000–2020
  - Region: Central-Southeastern Sri Lanka

2. Preprocessing
  - Convert from Kelvin to Celsius
  - Resample to 0.025° (~2.75 km) spatial resolution
  - Prepare xarray.Dataset using xee

3. Calculate Heat Wave Index
  - Threshold: 31°C
  - Duration: ≥5 consecutive days
  - Method: xclim.indices.heat_wave_index

4. Temporal Aggregation
  - Summarize annual maxima (YS)
  - Aggregate 5-year block maxima for visualization

5. Visualization
  - Faceted spatial heat maps
  - Time series at selected location: Lat 7.2°N, Lon 80.5°E

### Spatial distribution of annual Heat Wave Index (HWI) from 2000 to 2020 over Central-Southeastern Sri Lanka
  - Each panel represents a single year, showing the number of days that exceeded the heat wave threshold (≥31°C for ≥5 consecutive days). 
  - Higher intensity is shown in yellow, indicating greater heat wave occurrence in those grid cells.

<img width="1468" height="1190" alt="image" src="https://github.com/user-attachments/assets/f470c88a-9056-4fac-b358-b744ed3ee85e" />


### Maximum Heat Wave Index (HWI) over 5-year intervals from 2000 to 2020 across Central-Southeastern Sri Lanka
  - The maps show the spatial distribution of the most intense heat wave event within each period, based on the maximum number of consecutive days exceeding 31°C.
  - Yellow regions indicate areas most affected by prolonged extreme heat.

<img width="928" height="590" alt="image" src="https://github.com/user-attachments/assets/8f8afe8d-a213-407f-b567-f781d314ef93" />


### Annual time series of heat wave days (2000–2020) at a representative location in Central-Southeastern Sri Lanka(approximately 7.2°N, 80.5°E) 
  - The plot highlights interannual variability in extreme heat, with significant peaks in 2009, 2011, and 2016, reaching over 50 heat wave days in 2016, indicating increasing heat stress consistent with regional      climate change trends.

<img width="543" height="432" alt="image" src="https://github.com/user-attachments/assets/92f71f88-5997-4156-b173-a7eaaad39833" />


## Limitations & Considerations
1. The analysis is based on reanalysis data (ERA5), not direct weather station observations.
2. The heat wave definition used here is simple and may not reflect local health thresholds.
3. Pixelated visual output can be smoothed using finer ROI or post-processing interpolation.


 







Accordingly, this project also showcases how open datasets and reproducible code can support climate risk research in data-scarce regions.













