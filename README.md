# Analysis of Carbon Emissions and Public Health Outcomes

This project processes and visualizes carbon emissions by county in Illinois and tracks their relationship to public health outcomes across the state, including cancer, COPD, asthma, and worsening complications for Covid-19, stroke, and heart failure.

> University of Chicago Harris School of Public Policy, Winter 2026
> 
> **Authors**: Micah Slaughter and Jonathan Kacvinsky

# Research Question

> How do rates of carbon emissions and air quality impact rates of cancer incidence, mortality, and climate change in the state of Illinois?

### Sub-Questions

1. Do carbon emission rates exacberate health outcomes?
2. How does particulate matter contribute to air pollution via air quality index?
3. Is there variation in carbon emissions to cancers correlated with lung infections?

**Key Findings**


# Setup

```bash
conda env create -f environment.yml
```

# Project Structure

```
data/
  raw-data/           # Raw data files
    ghgp_data_2021.xlsx    # Carbon emissions data
    bladder_cancer.csv		# Bladder cancer data
    heart_stroke_mortality.csv  # Heart failure and stroke mortality data
    breast_cancer.csv		# Breast cancer data
    Illinois_Counties.geojson # Illinois county geo data
    colorectal_cancer.csv		# Colorectal cancer data
    kidney_cancer.csv # Kidney cancer data
    crude_asthma.csv	#	Asthma data
    lung-bronch_cancer.csv  # Lung and bronchus cancer data
    crude_COPD.csv			# COPD data
    population_illinois.xlsx  # Illinois population data
    daily_aqi_by_county_2025.csv	# US AQI data
    us-counties.csv #
  derived-data/       # Filtered data and output plots
    fire_filtered.gpkg  # Fire data filtered to post-2015
    cpi_filtered.csv    # CPI data filtered to 2020 onwards
code/                 # Data processing and plot creation 
  preprocessing.qmd   # Organizes health data and cleans emissions and AQI data
  cancer_graph.py			# Plots cancer incidence bar graph
  county_map.py			  # Maps cancer incidence and emissions maps
  emissions-cancer_scatter.py   # Plots cancer incidence and emissions scatter plot
environment.yml	      # Defines required packages
README.md             # Explains project structure
```


# Usage

1. Run preprocessing to filter data:
   ```bash
   python code/preprocessing.py
   ```

2. Generate the fire perimeter plot:
   ```bash
   python code/plot_fires.py
   ```

# Streamlit Dashboard
**Please note** that dashboard may need time to wake up, be patient on first load.
The interactive dashboard allows users to:
+ Choose which graphs to explore, focusing on air quality index or carbon emissions
+ Isolate and compare how health outcomes vary with carbon emissions across the 20 highest polluting counties in Illinois
+ Compare how particulat matter contributes to air quality per county

# Data Sources



# Data Processing

# Usage

1. Run preprocessing to filter data:
   ```bash
   python code/preprocessing.py
   ```

2. Generate the fire perimeter plot:
   ```bash
   python code/plot_fires.py
   ```
# Limitations and Future Research

+ Data Reporting and Measurement
  + Reporting standards for cancer data can be uneven
  + Limitations on emissions reporting
+ Established standards for for emissions type and tracking
  + This project identified patterns of health outcomes and scope 1 carbon emissions, but scope 2 and scope 3 are reported less frequently
+ Climate Corporate Accountability Act
  + Starting in January 1st, Illinois industries will be required to report scope 3 emissions. Using this data, we will haveh a better idea of how carbon emissions influence health outcomes.
  
> Data Analytics and Visualization for Public Policy, 2026
