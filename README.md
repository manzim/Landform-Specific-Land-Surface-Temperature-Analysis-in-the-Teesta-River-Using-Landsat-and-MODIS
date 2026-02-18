
# Title

<b> Landform Specific Land Surface Temperature Analysis in the Teesta River 2019 to 2024 Using Landsat and MODIS </b>

## Overview

This repository contains the full reproducible workflow used to analyse land surface temperature in the Teesta River region of Bangladesh. The study focuses on landform specific temperature behavior, especially sandbars, using Landsat 8 9 Collection 2 Level 2 and MODIS MOD11A2 products.

This repository is written as a transparent research diary so that students and researchers can follow each step and adapt it to their own river systems.

## Research Question
- How does sandbar land surface temperature vary seasonally in a large, braided river system, and what are the implications of spatial instability for landform-specific thermal analysis?”

The objective of the research questions was to evaluate the methodological constraints in dynamic braided river systems and to assess the reliability across different riverine landforms. 

## Study Area

Teesta River floodplain, Rangpur region, Bangladesh. Coordinate bounding box is defined in the script.

## Data Sources

Landsat 8 and Landsat 9 Collection 2 Level 2 Surface Temperature
Spatial resolution: 30 meters

MODIS MOD11A2 Land Surface Temperature
Spatial resolution: 1 kilometer

Temporal coverage: January 2019 to December 2024

## Workflow Summary

- Define Area of Interest in Google Earth Engine
- Download and preprocess Landsat images
- Apply cloud masking using QA_PIXEL
- Convert surface temperature band to Celsius
- Build monthly composites
- Extract mean LST for AOI
- Process MODIS monthly composites
- Merge Landsat and MODIS time series
- Perform correlation analysis
- Generate NDVI and NDWI indices
- Classify landforms into river sandbar and floodplain
- Extract landform specific LST
- Apply physical plausibility filtering
- Conduct pixel count diagnostics
- Perform seasonal aggregation
- Generate summary statistics and figures
- Important Methodological Decisions
- No interpolation was applied to missing months.
- Pixel count diagnostics were used to evaluate spatial support.
- Physical plausibility filter between 5 and 55 degrees Celsius was applied to sandbar LST values.
- Unrealistic values caused by cloud contamination were removed.

## Key Findings

Sandbar LST showed consistent seasonal variation.
River and floodplain classes often had insufficient valid pixels after masking.
Landsat and MODIS monthly LST showed weak but positive correlation.
Seasonal differences between dry and monsoon periods were observed.

### Reproducibility

All scripts are written in Python using:
- Google Earth Engine Python API
- geemap
- geopandas
- matplotlib
- pandas
- numpy

To reproduce:

- Authenticate Earth Engine
- Set your project ID
- Run the script sequentially

### License

BSD 3 Clause License.Free to use modify and distribute with attribution.

## Citation

If you use this workflow in academic work, please cite:
<b> Ahmed Manzim Ridwan. 2026. Landform Specific Land Surface Temperature Analysis in the Teesta River 2019 to 2024 Using Landsat and MODIS. GitHub Repository. </b>
