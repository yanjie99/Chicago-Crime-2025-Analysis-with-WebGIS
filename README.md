# Chicago-Crime-2025-Analysis-with-WebGIS
📖 ## Project Overview
This project investigates the spatial distribution of crime incidents in Chicago (2025) and examines their relationship with urban activity indicators, including business density, transportation accessibility, and policing infrastructure.

The study integrates GIS analysis, spatial statistics, and WebGIS visualization to:

- Identify crime hotspots
- Explore correlations between crime and urban features
- Diagnose spatial patterns through statistical modeling
- Deliver interactive WebGIS outputs for interpretation

🎯 ## Objectives
- Analyze spatial patterns of crime incidents in 2025
- Examine relationships between crime and:
- - Business activity
- - Public transport accessibility (CTA stations)
- - Police station distribution
- Identify hotspots using Kernel Density Estimation (KDE)
- Perform statistical diagnostics (correlation + OLS)
- Produce WebGIS-ready outputs for visualization

🗂️ ## Project Structure

```
├── data/                         # (Not included) Raw datasets, raw dataset can be found on Chicago Data Portal
├── outputs/                      # Generated GIS layers & results
├── notebooks/
│   ├── 01_build_spatial_layers_and_filter_crime_business.ipynb
│   ├── 02_aggregate_to_community_areas.ipynb
│   ├── 03_hotspot_and_stats.ipynb
│   └── 04_community_area_diagnostic_analysis.ipynb
├── webgis/                       # (Optional) ArcGIS / Web outputs
└── README.md
```

⚙️ ## Methodological Workflow

1. Spatial Data Preparation

- Load and preprocess:
- - Crime incidents (2025)
- - Business locations
- - CTA stations
- - Police stations
- - Community area boundaries
- - Convert to spatial formats (GeoDataFrames)
- - Filter and clean datasets

📄 **Notebook**:
`01_build_spatial_layers_and_filter_crime_business.ipynb`

2. Spatial Aggregation

- Aggregate point data into community areas
- Compute key indicators:
- - crime_count_2025
- - crime_density_sqkm
- - business_count
- - business_density_sqkm
- - cta_count
- - police_count

📄 **Notebook**:
`02_aggregate_to_community_areas.ipynb`

3. Hotspot Detection & Statistical Analysis

- Generate Kernel Density Estimation (KDE) maps:
- - Bandwidths: 250m and 500m
- Compute:
- - Pearson correlation
- - Spearman correlation
- Visualize statistical relationships

📄 **Notebook**:
`03_hotspot_and_stats.ipynb`

4. Diagnostic Spatial Analysis

- Perform OLS regression (diagnostic purpose):

$$log(crime density)∼log(business density)+cta count+police count$$

- Analyze:
- - Model residuals
- - Spatial clustering patterns
- Identify unexplained spatial variation

📄 **Notebook**:
`04_community_area_diagnostic_analysis.ipynb`

📊 ## Key Results

- Strong positive relationship between: Crime density and business density; Crime density and transit accessibility
- KDE reveals: Concentrated hotspots in central urban areas
- OLS diagnostics indicate: Remaining spatial structure (non-random residuals); Suggesting additional unobserved factors

🌐 ## WebGIS Outputs

The results are further visualized using:

- ArcGIS Online
- - Interactive maps
- - Dashboards
- - Choropleth layers

Key layers include:
- Crime density
- Business density
- Crime-business interaction profiles
- KDE hotspot rasters

🧰 ## Technologies Used
**Python Libraries**
`geopandas`
`pandas`
`matplotlib`
`seaborn`
`statsmodels`

**GIS Software**

- ArcGIS Pro
- ArcGIS Online

**Spatial Analysis**

- Kernel Density Estimation (KDE)
- Spatial aggregation
- Correlation analysis
- OLS regression


