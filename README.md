# MOSQUITO-DISTRIBUTION-MAPPING-


# Geospatial & Climate-Driven Mosquito Distribution Mapping (SDM)

## Project Overview
This project presents an automated computational pipeline designed to fetch, process, and visualize spatial occurrence data for *Aedes aegypti* (a primary vector for dengue, yellow fever, and zika viruses). 

By integrating programmatic biodiversity data extraction with spatial heatmapping, this study models vector distribution hotspots. The goal is to provide an accessible, reproducible data-driven framework for understanding vector disease ecology and human-environmental interactions within biological anthropology and public health contexts.

---

## Why This Project?
Vector-borne diseases are heavily influenced by climate dynamics, human settlement patterns, and land-use changes. Understanding where disease vectors thrive is essential for predicting transmission risks. 

This project was built to achieve three primary objectives:
1. **Programmatic Data Access:** Eliminate manual CSV downloads by fetching live occurrence records directly from global biodiversity repositories.
2. **Interactive Spatial Visualization:** Generate clear, interactive heatmaps to identify geographical distribution clusters effectively.
3. **Data Preprocessing & Quality Control:** Clean geospatial data (filtering invalid or missing coordinates) to ensure accurate spatial modeling.

---

## Dataset Source
* **Primary Source:** [GBIF (Global Biodiversity Information Facility)](https://www.gbif.org/)
* **Taxon Studied:** *Aedes aegypti* (Linnaeus, 1762)
* **Extraction Method:** Programmatically fetched using the `pygbif` API wrapper in Python.
* **Fields Extracted:** Latitude, Longitude, Country/Region, and Year of occurrence.

---

## Methodology & Workflow

1. **Environment Setup & Dependency Loading**
   Installed essential Python libraries for geospatial processing and data visualization (`pygbif`, `geopandas`, `folium`, `matplotlib`, `seaborn`).

2. **API Data Ingestion**
   Queried the GBIF database for *Aedes aegypti* records restricted to entries with valid geospatial coordinates (`hasCoordinate=True`, `hasGeospatialIssue=False`).

3. **Data Cleaning & Filtering**
   Converted coordinate data into standardized numerical formats and removed records with incomplete geospatial attributes to avoid plotting errors.

4. **Spatial Mapping & Heatmap Generation**
   Utilized `folium` and its `HeatMap` plugin to map geographic hotspots. The interactive map enables smooth zooming and geographical exploration across regions.

5. **Analytical Distribution Visualizations**
   Built statistical visualizations using `seaborn` and `matplotlib` to evaluate latitudinal frequency distributions and highlight top contributing geographic regions.

---

## Project Structure & File Outputs
* `mosquito_sdm_pipeline.ipynb`: Complete executable Google Colab notebook containing code, documentation, and rendered plots.
* `aedes_cleaned_data.csv`: Cleaned occurrence dataset exported for further statistical or spatial modeling.
* `mosquito_interactive_heatmap.html`: Standalone interactive HTML map rendering spatial vector density hotspots.

---

## How to Run

1. Open the project notebook in **Google Colab**.
2. Run all cells sequentially. The pipeline will automatically fetch the latest available records from GBIF and display interactive plots directly within the notebook interface.
3. (Optional) Mount your Google Drive in the final step to export the generated `.csv` and `.html` output files locally or to your Drive storage.

---

## Dependencies & Requirements
* Python 3.x
* `pandas` & `numpy`
* `pygbif`
* `geopandas`
* `folium`
* `matplotlib` & `seaborn`

---

**Author:** Saira Akram Mughal  
*Focus:* Computational Biology, Biological Anthropology & Disease Ecology
