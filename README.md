Urban Heat Island (UHI), a phenomenon according to which urban areas have higher temperature compared to their surrounding rural areas. Some traditional studies are dependent on the retrospective analysis of satellite datasets, which causes limitation in immediate decision making and short-term planning. Meanwhile, some are using the real-time monitoring which limits the availability and accessibility and also increases the cost. This suggests the need for the near real-time model using the land surface temperature data calculated using the satellite datasets along with the meteorological data to do the ground level validation. The model gives weekly UHI prediction using the MODIS LST and ERA5. 

Implementation is done in 3 phases 

Phase 1: HISTORICAL BASELINE (2020-2024): using the MODIS MOD11A2 LST, ERA5 meteorological variables (2m air temperature, 10m wind speed, precipitation), MODIS NDVI for vegetation index, MODIS urban land cover, SRTM elevation and VIIRS nighttime lights.
Using this features on Random Forest model (trained on UHI using LST - air temperature).

Phase 2: NEAR REAL-TIME PREDICTION: 16 day lag and 30 day meteorological window to ensure that all data is available. 12 features pipeline where 7 base and 5 interactive features are used and they preserve Phase 1 model architecture.

Phase 3: VISUALIZATION AND VALIDATION: Interactive visuals, automated alerts ( indicators: >3 High, >5 Very High, >8 Extreme), thus detecting the hotspots and ground validation on the 10 major IMD cities.
