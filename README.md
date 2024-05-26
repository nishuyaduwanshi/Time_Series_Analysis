# Surface Water Extent Time Series
This Python script computes the surface water extent time series for a specified inland water body and time range using the Google Earth Engine Python API. It calculates the total surface water area within the specified water body for each image in the provided time range and creates a time series of the surface water extent values. 

## Table of Contents

- [Requirements](#requirements)
- [Setup and Installation](#setup-and-installation)
- [Usage](#usage)

## Requirements
- [Google Colab](https://colab.research.google.com/)
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


1. **Open Google Colab**:
   - Go to [Google Colab](https://colab.research.google.com/).

2. **Create a New Notebook**:
   - Click on "File" -> "New Notebook".

3. **Install Required Packages**:
   - In the first cell, enter the following code to install the required packages and authenticate Google Earth Engine:
     ```python
     !pip install earthengine-api
     !pip install geemap
     
     import ee
     ee.Authenticate()
     ee.Initialize()
     ```

4. **Clone the Repository**:
   - In the next cell, clone GitHub repository:
     ```python
     !git clone [https://github.com/nishuyaduwanshi/Time_Series_Analysis.git]
     %cd Time_Series_Analysis
     ```

5. **Run the Script**:
   - In the following cell, run the Python script:
     ```python
     !python Time_Series_Analysis.ipynb
## Workflow

1. **Select Area of Interest (AOI):**
    Use the 'Draw a Rectangle' tool on the map to select the AOI.
<img width="988" alt="step 1" src="https://github.com/nishuyaduwanshi/Time_Series_Analysis/assets/170518265/57043b2d-1317-47b5-9e56-548a55b9421a">

2. **Save and Extract Coordinates:**
    
<img width="1331" alt="step 2" src="https://github.com/nishuyaduwanshi/Time_Series_Analysis/assets/170518265/3b75c240-6bfe-4c5e-b064-24907c27eb19">

3. **Load Data**: Load the Global Surface Water data from Google Earth Engine.

4.  **Filter Data**: Filter the data for the specified time range and location.


5. **Process Satellite Images:**
    The script processes the images to calculate the water surface area for the specified years.

6. **Generate and Save Time Series Plot:**
    The script generates a time series plot of the water surface area and saves it as `water_surface_area.png`.
<img width="642" alt="step 7" src="https://github.com/nishuyaduwanshi/Time_Series_Analysis/assets/170518265/7fafb420-345e-4e68-be19-8a6010a4dc29">

### Example Images

Below are example images showing the Aral Sea in 2000 and 2014:

![Aral Sea 2000](https://eoimages.gsfc.nasa.gov/images/imagerecords/84000/84437/aralsea_tmo_2000238.jpg)
![Aral Sea 2014](https://eoimages.gsfc.nasa.gov/images/imagerecords/84000/84437/aralsea_tmo_2014231.jpg)



