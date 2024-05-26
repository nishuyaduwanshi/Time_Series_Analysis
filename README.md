# Surface Water Extent Time Series

This Python script computes the surface water extent time series for a specified inland water body and time range using the Google Earth Engine Python API. It calculates the total surface water area within the specified water body for each image in the provided time range and creates a time series of the surface water extent values. 

## Table of Contents

- [Requirements](#requirements)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)
- [Results](#results)
- [Files](#files)
- [License](#license)


## Requirements

- Python 3.6+
- Jupyter Notebook
- [Google Earth Engine](https://earthengine.google.com/)
- Required Python packages:
  - `geemap`
  - `earthengine-api`
  - `folium`
  - `matplotlib`
  - `pandas`
  - `seaborn`
  - `geopandas`
  - `requests`

## Setup and Installation

1. **Install the Required Packages:**
    ```bash
    pip install geemap earthengine-api folium matplotlib pandas seaborn geopandas requests
    ```

3. **Authenticate and Initialize Google Earth Engine:**
    ```python
    import ee
    ee.Authenticate()
    ee.Initialize()
    ```

## Usage

1. **Run the Jupyter Notebook:**
    ```bash
    jupyter notebook aral_sea_analysis.ipynb
    ```

2. **Select Area of Interest (AOI):**
    Use the 'Draw a Rectangle' tool on the map to select the AOI.

3. **Save and Extract Coordinates:**
    The coordinates of the AOI will be saved to a GeoJSON file (`aoi_defined.geojson`).

4. **Process Satellite Images:**
    The script processes the images to calculate the water surface area for the specified years.

5. **Generate and Save Time Series Plot:**
    The script generates a time series plot of the water surface area and saves it as `water_surface_area.png`.

## Results

The results include:
- Side-by-side visual comparison of the Aral Sea in the years 2000 and 2014.
- A time series plot of the water surface area from 2000 to 2014.

![Water Surface Area Time Series](water_surface_area.png)

## Files

- `aral_sea_analysis.ipynb`: Jupyter Notebook containing the analysis code.
- `aoi_defined.geojson`: GeoJSON file containing the AOI coordinates.
- `water_surface_area.png`: Generated time series plot of the water surface area.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for more details.
