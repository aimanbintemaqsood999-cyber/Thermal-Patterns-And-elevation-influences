# Post-Monsoon Nighttime Land Surface Temperature and Terrain Influences, Six Districts of Sindh, Pakistan (2022-2025)

![Post-monsoon nighttime LST maps](NightPostLST.png)

## Overview
Multi-year GIS analysis of post-monsoon (October and November) nighttime Land Surface Temperature (LST) and its relationship with terrain in six districts of Sindh: Larkana, Jacobabad, Dadu, Khairpur, Shaheed Benazirabad and Sukkur. Elevation, slope and hillshade were derived from a DEM to examine how topography relates to nighttime thermal patterns.

## Study area
Six districts of Sindh Province, Pakistan: Larkana, Jacobabad, Dadu, Khairpur, Shaheed Benazirabad and Sukkur.

![Study area map](StudyArea.png)

## Data
- Nighttime LST: [product, e.g. MODIS MOD11A2 / Landsat, and resolution], October and November, 2022-2025
- DEM: [USGS SRTM (GTOPO), e.g. SRTM, and 1km]
- District boundaries:

## Method
1. Prepared nighttime LST rasters for October and November of each year (2022-2025) [ Obtained LST data through code,
2. Used raster math in ArcGIS Pro to calculate monthly and seasonal mean composites]
3. Derived **slope** and **hillshade** surfaces from the DEM to describe terrain relief and roughness.
4. Organized all rasters and district boundaries in a standard geodatabase.
5. Built layout series showing elevation, slope, hillshade and nighttime LST for each of the six districts.

## Results

### Elevation
![Elevation maps of six districts](ElevationMap.png)

### Nighttime LST (post-monsoon mean)
![Nighttime LST maps](NightPostLST.png)

### Key findings
## Key Findings

### Nighttime Land Surface Temperature (Oct-Nov mean, 2022-2025)

- **Khairpur** shows the clearest spatial pattern: cooler in the far west, with a hot band through the center and a hot east and southeast. The very high LST zone appears largest in 2024 and 2025.
- **Sukkur** has a cooler northwest, a hot eastern and southeastern zone, and a very high LST strip along its western edge. The hot zone is most extensive in 2024.
- **Dadu** shows the same pattern every year: a very high LST band along the western margin and moderate to low LST across the eastern plains.
- **Jacobabad and Shaheed Benazirabad** appear cooler in 2023 and warmer in 2024, with scattered hot spots rather than one large zone.
- **Larkana** is relatively stable across all four years, with scattered high and very high patches.
- Overall, 2024-2025 look warmer than 2022-2023, though not uniformly across districts.

### Terrain (DEM, Slope, Hillshade)

- Most of the study area is flat, low-lying plain with very low slope.
- **Dadu** is the exception, with a high and steep western margin (Kirthar side) and low plains to the east.
- **Sukkur** has a narrow high strip along its western edge, and **Larkana** is highest in the north.

### Link Between LST and Terrain

- In **Dadu, Sukkur and Khairpur**, the highest and steepest terrain coincides with the hottest nighttime LST zones. This suggests that rocky, bare ridges retain heat after sunset.
- In **Larkana**, the match is weak and patchy.
- In the flat districts (**Jacobabad, Shaheed Benazirabad**), terrain does not explain the LST patterns. Land cover (crops, bare soil, water) is a more likely driver.

### Limitations.
- Class breaks should be identical across all years and districts for the LST maps to be comparable.
- DEM classes appear stretched per district, which exaggerates relief in some panels.
- Fine striping in slope and hillshade over the plains may reflect DEM noise or field patterns rather than real terrain.

### Next Steps

- Compute mean LST per district per year with Zonal Statistics.
- Test the relationship between LST and elevation and slope (correlation or regression).
- Overlay LULC classes to separate terrain effects from land cover effects.

## Tools
ArcGIS Pro (DEM, slope, hillshade, zonal statistics and layout design ) (https://code.earthengine.google.com/2fe343076c6df368bf81ea1a3e0f31ca) Code for LST data

## Files
- `StudyArea.png`: study area map
- `ElevationMap.png`: elevation maps for the six districts
- `NightPostLST.png`: post-monsoon nighttime LST maps
- `StudyArea.ppkx`, `Elevation_map.ppkx`, 'NIGHTPOSTLST.ppkg': ArcGIS Pro project packages (open in ArcGIS Pro only)

## Limitations
- Only October and November are covered, so results do not describe other seasons.
