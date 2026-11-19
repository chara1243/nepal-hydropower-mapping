# Nepal Hydropower Mapping

![Python](https://img.shields.io/badge/Python-3.10%2B-blue)
![GeoPandas](https://img.shields.io/badge/GeoPandas-Spatial%20Analysis-green)
![Google Colab](https://img.shields.io/badge/Platform-Google%20Colab-orange)
![License](https://img.shields.io/badge/License-MIT-yellow)
![Project](https://img.shields.io/badge/Project-Geospatial%20Mapping-blueviolet)

## Overview

**Nepal Hydropower Mapping** is a geospatial mapping and visualization workflow designed to analyze and visualize the spatial distribution of hydropower stations across Nepal.

The project uses Python-based geospatial libraries to process hydropower station inventory data, classify projects according to installed capacity, and produce publication-quality cartographic outputs.

The workflow is designed for researchers, students, planners, and professionals working in hydropower development, renewable energy, and geospatial analysis.

## Objectives

1. Map the geographical distribution of hydropower stations across Nepal.
2. Classify hydropower stations according to installed generation capacity.
3. Examine provincial distribution and installed generation capacity.
4. Produce publication-quality static and interactive maps.
5. Export cleaned geospatial datasets for further GIS analysis.

## Key Features

### 1. Spatial data processing
- Import hydropower station inventory from CSV.
- Import Nepal administrative/geographical boundary shapefile.
- Convert station coordinates into point geometries.
- Reproject spatial datasets for accurate cartographic representation.
- Remove records with missing essential coordinates or capacity.

### 2. Hydropower capacity classification

The workflow uses four capacity classes:

| Classification | Installed capacity |
|---|---:|
| Micro | Below 10 MW |
| Small | 10–less than 25 MW |
| Medium | 25–less than 100 MW |
| Large | 100 MW and above |

These are visualization classes used in this project, not necessarily official regulatory categories.

### 3. Cartographic visualization

- Graduated point symbols.
- Capacity-based color classification.
- Station labels for large projects.
- North arrow.
- Scale bar.
- Custom legend.
- Publication-quality PNG export at 600 DPI.

### 4. Interactive mapping

The project also generates an interactive map using Folium, including:

- Hydropower station locations.
- Capacity-based marker colors.
- Station information popups.
- Nepal boundary.
- Interactive navigation.

### 5. Spatial data export

The workflow exports:

- GeoPackage (`.gpkg`)
- CSV (`.csv`)
- Static map (`.png`)
- Interactive map (`.html`)

### 6. Statistical analysis

The workflow generates:

- Total number of stations.
- Total installed capacity.
- Capacity-class distribution.
- Five largest hydropower stations.
- Province-wise station distribution.
- Province-wise installed capacity.

## Technology Stack

| Technology | Application |
|---|---|
| Python | Main programming language |
| Pandas | Tabular data processing |
| GeoPandas | Geospatial data processing |
| Shapely | Spatial geometry |
| Matplotlib | Cartographic visualization |
| Folium | Interactive mapping |
| NumPy | Numerical processing |
| AdjustText | Label placement |
| Matplotlib-Scalebar | Map scale bar |
| Google Colab | Cloud-based execution |

## Input Data Requirements

### Hydropower inventory CSV

The CSV should contain the following columns:

| Column | Description |
|---|---|
| `Name_of_station` | Hydropower station name |
| `Capacity_(MW)` | Installed capacity in MW |
| `Latitude` | Latitude in decimal degrees |
| `Longitude` | Longitude in decimal degrees |
| `Province` | Province name |
| `Commissioned` | Commissioning year/date |
| `Owner` | Project owner |

The first four columns are essential for the main mapping workflow. Province, commissioning date, and owner are optional.

### Nepal boundary shapefile

Required files:

- Nepal.shp
- Nepal.shx
- Nepal.dbf
- Nepal.prj

The coordinate reference system should be verified before processing.

## Installation

Install the required packages:

```bash
pip install -r requirements.txt
