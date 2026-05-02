# T-Mobile Cellular Coverage Optimization Report
**Target Area:** Los Angeles County, California  
**Budget:** $750,000  

## 1. Executive Summary
T-Mobile has allocated a capital improvement budget of $750,000 to maximize cellular network coverage within Los Angeles County. The objective is to identify the most efficient use of this budget among three proposed development scenarios. Based on advanced GIS Viewshed analysis utilizing 1-arcsecond high-resolution SRTM DEM data, **Scenario C (Adding 3 New Towers)** is recommended as it yields the highest absolute increase in coverage area (a 4.23% net increase over the status quo).

## 2. Methodology
To ensure accurate calculations, the following spatial analysis procedures were applied:
*   **Data Sources:** T-Mobile tower locations (`TMOSites.csv`), Los Angeles County boundary (`lacounty.shp`), and five 1-arcsecond SRTM Void Filled DEM tiles downloaded from USGS Earth Explorer.
*   **Data Preparation:** The 5 DEM tiles were mosaicked into a single seamless elevation raster. All geographic data (towers, DEM, county boundary) were reprojected to the **NAD 1983 UTM Zone 11N (EPSG:26911)** coordinate system to ensure accurate metric area calculations.
*   **Viewshed Parameters:** The analysis was performed assuming an observer (tower) height based on existing structure heights, a receiver (user phone) height of 1.5 meters, and a default line-of-sight transmission radius of 25,000 meters (25 km) under ideal atmospheric conditions.
*   **Coverage Calculation:** The resulting viewsheds were masked to the exact boundary of Los Angeles County. Coverage area was calculated by summing the area of all visible 30m x 30m pixels and dividing by the total land area of the county.

## 3. Scenario Analysis and Results

The table below illustrates the changes in coverage area across the status quo and the three proposed scenarios:

| Development Scenario | Coverage Area (Sq. Meters) | % of LA County Covered | Net Gain over Status Quo |
| :--- | :--- | :--- | :--- |
| **Status Quo (Baseline)** | 4,929,452,100 m² | 40.08% | - |
| **Scenario A (+10m Height)** | 5,008,313,700 m² | 40.72% | + 0.64% |
| **Scenario B (+5km Range)** | 5,237,206,200 m² | 42.58% | + 2.50% |
| **Scenario C (3 New Towers)** | 5,449,495,500 m² | 44.31% | **+ 4.23%** |

*(Refer to `Coverage_Comparison_Chart.png` for a visual comparison of these results.)*

### 3.1 Status Quo (Current State)
Currently, T-Mobile's network covers approximately **40.08%** of Los Angeles County's total land area. Coverage is heavily concentrated in the densely populated urban basin, while mountainous regions and northern peripheral areas remain significantly underserved due to line-of-sight terrain obstruction.

### 3.2 Scenario A: Increase Existing Tower Height by 10m
Raising all existing towers by 10 meters yields only a marginal improvement (**40.72%** total coverage, a 0.64% increase). Because most existing towers are located in relatively flat urban areas, adding height does not effectively overcome the massive topographic barriers (like the San Gabriel Mountains) that block signals from reaching underserved valleys.

### 3.3 Scenario B: Increase Transmission Range by 5km
Extending the range of all existing towers from 25km to 30km provides a moderate improvement (**42.58%** total coverage). While existing towers can push signals slightly further into valleys, the signal is still fundamentally blocked by major mountain ranges.

### 3.4 Scenario C: Add 3 New Towers in Underserved Areas
By strategically placing three completely new towers in the largest "dead zones" (areas currently outside the 25km radius of any existing tower), the network overcomes existing geographic barriers entirely. This scenario maximizes the return on investment, bringing total coverage to **44.31%** (a 4.23% absolute increase).

## 4. Final Recommendation
Based on the spatial analysis, **Scenario C (Adding 3 New Towers)** is unequivocally the most effective approach for expanding T-Mobile's cellular footprint in Los Angeles County. While improving the range (Scenario B) or height (Scenario A) of existing infrastructure provides diminishing returns due to the county's mountainous terrain, establishing new points of origin in unserved regions successfully bypasses these physical obstructions. It is recommended that the $750,000 budget be allocated to the construction of these three new cellular towers.