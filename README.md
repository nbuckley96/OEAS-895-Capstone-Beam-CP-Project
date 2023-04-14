# OEAS 895 Capstone Beam CP Project

This project was built at an attempt to estimate beam attenuation from chlorophyll fluorescence in the upper water column to use as another potential proxy for phytoplankton biomass. 

The packages used in this project can be found beamcp_chl.yml file

# Data

The data used in this project was extracted from the 2021 GEOTRACES Intermediate Data Product (IDP) webODV tool and downloaded as an ASCII spreadsheet.
More information can be found at on the GEOTRACES webstie:  https://www.geotraces.org/geotraces-intermediate-data-product-2021/

CTD sensor data that contained beam attenuation and either chlorophyll or fluorescence data were extracted from webODV.  Other CTD parameters pulled were:  cruise identifiers, station identifiers, dat/time, latitude, longitude, pressure, temperature, salinity, oxygen, and photosynthetically active radiation.  

The ASCII spreadsheet used in this project is placed in the 'Raw Data' folder where 'Data Processing Info' can also be found that was included with the ASCII spreadsheet upon download.  

# Notebooks

These still need to be cleaned up and automated but included are the following notebooks:  

CTD data at a glance
* This is a notebook that includes a map of plotting initial data locations and some exploratory data visualization to look at vertical distributions of the                 parameters imported from the ASCII spreadsheet.

Beam CP predicted from Chlorophyll Fluorescence - 14 April 2023
* This notebook includes applying the data corrections where necessary and then applies the KNeighborsRegressor from scikit learn.  
