# OEAS 895 Capstone Beam CP Project

This project was built at an attempt to estimate beam attenuation from chlorophyll a concentrations in the upper water column to use as another potential proxy for phytoplankton biomass. 
In the future, hopefully this model will be adapted to incorporate fluorescence with chlorophyll a as a predictor for beam attenuation.  However, this could not be attempted at this time as the scaling of the of the fluorescence data varies depending on the sensor used for each cruise.

The packages used in this project can be found beamcp_chl.yml file
The following packages were installed in this conda environment:
* Scikit Learn 1.2.2
* Pandas 1.5.3
* Numpy 1.23.5
* Matplotlib 3.7.1
* Seaborn 0.12.2
* Cartopy 0.21.1
* CMOcean 3.0.3

# Data

The data used in this project was extracted from the 2021 GEOTRACES Intermediate Data Product (IDP) webODV tool and downloaded as an ASCII spreadsheet.
More information can be found at on the GEOTRACES webstie:  https://www.geotraces.org/geotraces-intermediate-data-product-2021/

CTD sensor data that contained beam attenuation and either chlorophyll or fluorescence data were extracted from webODV.  Other CTD parameters pulled were:  cruise identifiers, station identifiers, dat/time, latitude, longitude, pressure, temperature, salinity, oxygen, and photosynthetically active radiation.  

The ASCII spreadsheet used in this project was too large (730 MB) to be placed on GitHub so it was placed in a Google drive folder that can be accessed from the following link:  https://drive.google.com/drive/folders/121quulvUFnAvhx-pjFLY6Aylj8F8iCJY?usp=sharing.  
'Data Processing Info' on the ASCII spreadsheet used in this project can be found within the 'Raw Data' folder and was included with the ASCII spreadsheet upon download.  

Though unrelated to the model an ODV Collection file, 'IDP2021_GEOTRACES_IDP2021_Seawater_Sensor_Data_v1_fWAsARBb', has been placed in the 'Raw Data' folder and can be useful for initial data visualization.


# Notebooks

Included are the following notebooks:  

cruise_transect_profiles
* This is a notebook that includes a map of plotting initial data locations and some exploratory data visualization to look at vertical distributions of the                 parameters imported from the ASCII spreadsheet.

predict_beamcp_CHL_ONLY
* This notebook applied a K Nearest Neighbors Regression (frm scikit learn) to the chlorophyll and beam attenuation data.  This covers the following:  applying offsets where necessary, finding the optimal k value and then applying that to an initial KNN regression, and then applying a 5-fold cross validation to further validate the results from the train/test (70/30) split used in the initial KNN regression. 
