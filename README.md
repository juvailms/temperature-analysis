# Temperature Analysis

## Overview

This project involves analyzing temperature data from NOAA (National Oceanic and Atmospheric Administration) to visualize historical temperature records and anomalies. The main tasks include:

- Visualizing record high and low temperatures from 2005 to 2014.
- Highlighting 2015 temperature records that exceeded historical highs or lows.
- Addressing leap day (February 29th) considerations.
- Mapping station locations near Ann Arbor, Michigan.
- Summarizing 2015 temperature data for Ann Arbor, Michigan.

## Dataset Description

### `temperature.csv`
- **id**: Station identification code.
- **date**: Observation date (YYYY-MM-DD).
- **element**: Temperature type (TMAX/TMIN).
  - TMAX: Maximum temperature (tenths of degrees Celsius).
  - TMIN: Minimum temperature (tenths of degrees Celsius).
- **value**: Recorded temperature value (tenths of degrees Celsius).

### `BinSize.csv`
Contains metadata on station locations and other details.

## Tools and Libraries Used

- **Pandas**: Data manipulation and analysis.
- **NumPy**: Handling numerical operations.
- **Matplotlib**: Data visualization.
- **Seaborn**: Enhanced visualizations.
- **Geopandas**: For mapping and geospatial analysis.
- **Folium**: Interactive map visualization.

## Task Breakdown

### Record High and Low Temperatures (2005-2014)
- **Objective**: Plot a line graph showing the record high and low temperatures for each day of the year (excluding leap days) from 2005 to 2014.
- **Implementation**:
  - Data filtered for 2005–2014.
  - Grouped data by day of the year.
  - Aggregated max and min values.
  - Shaded the area between high and low records for clarity.

### Broken Records in 2015
- **Objective**: Overlay scatter points for 2015 temperatures that broke historical records.
- **Implementation**:
  - Filtered 2015 data.
  - Compared 2015 temperatures with historical records.
  - Plotted breaking points as scatter plots on the same graph.

### Leap Day Removal
- **Objective**: Exclude February 29th to maintain consistency in year comparisons.
- **Implementation**:
  - Filtered out leap day records from both datasets.

### Mapping Weather Stations
- **Objective**: Plot station locations near Ann Arbor, Michigan.
- **Implementation**:
  - Used Geopandas for station coordinates.
  - Mapped the stations using Folium for an interactive visualization.

### 2015 Temperature Summary for Ann Arbor
- **Objective**: Visualize and summarize 2015 temperature trends near Ann Arbor.
- **Implementation**:
  - Generated box plots and trend lines for 2015 data.

## Why These Tools Were Used

- **Pandas & NumPy**: Efficient data handling.
- **Matplotlib & Seaborn**: Customizable and aesthetically pleasing plots.
- **Geopandas & Folium**: Essential for geospatial analysis and interactive mapping.

## Challenges

- Handling leap years.
- Ensuring smooth integration of multiple datasets.
- Optimizing visual clarity with legends and labels.

## Results

- Visualized historical temperature trends with anomalies.
- Mapped weather station data.
- Summarized temperature data, highlighting record-breaking patterns.

## Instructions for Running the Project

1. Ensure all dependencies are installed:
   ```bash
   pip install pandas numpy matplotlib seaborn geopandas folium
