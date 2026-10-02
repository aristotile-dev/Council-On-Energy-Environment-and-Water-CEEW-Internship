# 🌍 Delhi Air Quality Analysis (CEEW Internship Assignment)

![Python](https://img.shields.io/badge/Python-3.12-blue?logo=python&logoColor=white)
![Jupyter](https://img.shields.io/badge/Made%20with-Jupyter-orange?logo=jupyter&logoColor=white)
![Status](https://img.shields.io/badge/Status-Completed-success)
![CEEW](https://img.shields.io/badge/CEEW-Internship%20Assessment-green)

This repository contains the analysis and findings for the **Council on Energy, Environment and Water (CEEW)** internship assignment. The project focuses on assessing air quality trends in Delhi using remote sensing data and ground-based observations.

## 📂 Project Overview

The analysis is divided into two main assignments:

### **1. Nitrogen Dioxide ($NO_2$) Analysis (2019–2024)**
* **Objective:** Analyze the temporal and spatial distribution of $NO_2$ concentrations in Delhi during summer months (March–June) over a 6-year period.
* **Data Source:** Sentinel-5P OFFL data accessed via **Google Earth Engine (GEE)**.
* **Key Tasks:**
    * Fetched and processed satellite imagery for the Delhi region.
    * Clipped data to the Delhi state boundary using GADM shapefiles.
    * Visualized spatial changes in $NO_2$ levels year-over-year.
    * Identified pollution hotspots linked to industrial clusters and heavy traffic.

### **2. $PM_{2.5}$ Time-Series Analysis (2022)**
* **Objective:** Compare satellite-derived $PM_{2.5}$ estimates with ground-truth data from monitoring stations.
* **Data Source:**
    * Satellite-derived $PM_{2.5}$ (WUSTL, 1x1 km resolution).
    * Ground observations from 5 stations: **Narela, North Campus, Nehru Nagar, R K Puram, and ITO**.
* **Key Tasks:**
    * Performed spatial interpolation (KD-Tree) to map satellite pixels to station coordinates.
    * Conducted time-series comparison (Daily, Weekly, Monthly).
    * Calculated error metrics: **RMSE, MAPE, MAE, and $R^2$**.
    * Analyzed diurnal patterns and meteorological impacts (monsoon dip, winter inversion).

## 🛠️ Tech Stack & Libraries

* **Languages:** Python 3.12
* **Geospatial Analysis:** `Google Earth Engine (ee)`, `Geopandas`, `Rioxarray`, `Xarray`, `Shapely`
* **Data Manipulation:** `Pandas`, `Numpy`
* **Visualization:** `Matplotlib`, `Seaborn`
* **Statistical Analysis:** `Scikit-learn`, `Scipy`

## 📊 Key Insights

* **$NO_2$ Trends:** Significant fluctuations were observed, with a notable dip during the 2020 lockdown periods, followed by a rise in subsequent years. Hotspots remain persistent in industrial zones.
* **Satellite vs. Ground $PM_{2.5}$:** Satellite data showed a strong correlation with ground stations, proving it to be a viable tool for filling data gaps in areas without monitoring stations.
* **Seasonal Impact:** Meteorological conditions (rainfall, mixing layer height) play a dominant role in pollution peaks and troughs compared to minor variations in human activity.

## 🚀 How to Run

1.  **Clone the repository:**
    ```bash
    git clone [https://github.com/your-username/delhi-air-quality-analysis.git](https://github.com/your-username/delhi-air-quality-analysis.git)
    ```
2.  **Install dependencies:**
    Ensure you have the required Python libraries installed:
    ```bash
    pip install earthengine-api rioxarray xarray pandas geopandas matplotlib seaborn scikit-learn
    ```
3.  **Google Earth Engine Setup:**
    * The notebooks require a GEE account.
    * Run `ee.Authenticate()` within the notebook to link your Google account.
4.  **Run the Notebooks:**
    * Open `Assignment 1.ipynb` for the $NO_2$ spatial analysis.
    * Open `Assignment 2.ipynb` for the $PM_{2.5}$ statistical comparison.

## 📄 Files Included

* `Assignment 1.ipynb`: Code for Sentinel-5P $NO_2$ extraction and mapping.
* `Assignment 2.ipynb`: Code for $PM_{2.5}$ correlation and time-series plotting.
* `Result.pdf`: Detailed report summarizing methodologies and conclusions.
* `PM25_Satellite_vs_Ground_2022_CORRECTED.csv`: Processed dataset used for Assignment 2.

## 👤 Author

**Aristotile S**
*Submitted as part of the CEEW Internship Assessment.*
