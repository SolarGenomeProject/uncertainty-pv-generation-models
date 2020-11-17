# Uncertainty in Solar PV Generation Models
This notebook illustrates the value of incorporating measured solar irradiance data, sourced from accurate radiometric station, to provide uncertainty analysis in solar photovoltaic (PV) generation models. Most of the PV design tools rely on TMY data (short for typical meteorological year) which is not designed with the solar energy applications in mind (it shows a typical meteorological year and not a typical solar year. Or, as Frank Vignola (2012) puts it:

"To develop a sound, bankable dataset, it is important to understand resource variability and the nature of uncertainties in the various constituents of the data ... TMY files may be suitable for initial evaluations, they generally do not constitute a bankable dataset." Moreover, "...if the TMY file is used to estimate the performance of a solar system, comparisons between the long-term dataset and the TMY averages should be carried out. This is especially true for TMY3 data files created from just 11 years of data."

Vignola, Frank E., Andrew C. McMahan, and Catherine N. Grover. "Bankable solar-radiation datasets." Solar Energy Forecasting and Resources Assessment (2013).

IF YOU ARE RUNNING THIS THROUGH THE WEB (USING BINDER) READ BELOW!
1) Do not download files from NOAA
2) When prompted to insert a start and end year, use 2015 and 2019
3) Load the data set at the end of section 4

For measuring the uncertainty in the solar PV generation modeling we need reliable solar irradiance data preferably sourced from a radiometric station located close to the site being modeled.

In this example we will be collecting and using data from the NOAA SURFRAD station in State College, PA.

"...the Surface Radiation Budget Network (SURFRAD) was established in 1993 through the support of NOAA's Office of Global Programs. The SURFRAD mission is clear; its primary objective is to support climate research with accurate, continuous, long-term measurements of the surface radiation budget over the United States."

Visit: https://www.esrl.noaa.gov/gmd/grad/surfrad/overview.html

Here we have:

5 years of data
Data sampled every minute
Data include the global horizontal irradiance (GHI), diffuse horizontal irradiance (DHI), direct normal irradiance (DNI), air temperature, and ambient pressure
IF USING BINDER: The data was averaged to 10 min to save storage and computational time.

To make the example possible I make use of the SANDIA PV Collab PVLib tool:
"...pvlib python is a community supported tool that provides a set of functions and classes for simulating the performance of photovoltaic energy systems. pvlib python was originally ported from the PVLIB MATLAB toolbox developed at Sandia National Laboratories and it implements many of the models and methods developed at the Labs. pvlib python is a community supported tool that provides a set of functions and classes for simulating the performance of photovoltaic energy systems. pvlib python was originally ported from the PVLIB MATLAB toolbox developed at Sandia National Laboratories and it implements many of the models and methods developed at the Labs."

For more information visit:
https://pvlib-python.readthedocs.io/en/v0.8.0/index.html

Use this code at your own discretion. The user must be aware that the results here are more illustrative than a precise solar design. 

Thank you and have fun! :)
