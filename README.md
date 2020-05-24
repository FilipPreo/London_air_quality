# London_air_quality
Project analysing changes to levels of pollutants in Central and Greater London before and after the introduction of the Ultra-Low Emissions Zone (ULEZ)

The purpose of our project is to retrieve data on London's air quality and assess the impact of the LEZ and ULEZ zones in anticipation of the expansion of the ULEZ zone in October 2021. Our data source will be from London Air (https://www.londonair.org.uk/LondonAir/API/) and OpenAQ (https://openaq.org/#/?_k=86pokr). We might choose to supplement this with additional data from TfL (tfl.org.uk). 

Our target audience is TfL and the office of the Mayor of London. This analysis is being conducted in order to peer review previous assessments of the impact of the two low-emission zones and also to attempt to answer whether the upcoming expansion of ULEZ to include Inner London is economically sound. 

The proposed effect sizes below are partially taken from the TfL consultation on ULEZ (TfL, 2015).

We are defining impact on air quality using the amount of Nitrogen Oxides (NOx) and particulate matter (PM10) as detected by automatic air sensors. We will select multiple sensor sites in London zone 1 that are inside the current ULEZ radius for our data. These levels are reported in miligrams per cubic meter. Here is a snapshot of the initial data:

/fig/no2_2007_08.jpg

/fig/pm10_2018_19.jpg

Our hypotheses are:
1. The introducton of ULEZ decreased the amount of NOx in Zone 1 of Central London by an effect size of at least 0.3. 
Null hypothesis - ULEZ did not reduced the amount of NOx in Zone 1 by any significant effect size.
2. The introduction of ULEZ was at least 1.25 as effective than the introduction of LEZ in reducing NO2 levels in Central London.
Null hypothesis - The effect of ULEZ on NO2 levels was not significantly more effective than LEZ in reducing NO2 levels in Central London. 
3. The introducton of ULEZ decreased the amount of PM10 in Zone 1 of Central London by an effect size of at least 0.4. 
Null hypothesis - ULEZ did not reduce the amount of PM10 in Zone 1 of Central London by any significant amount. 
4. The introduction of ULEZ was at least 1.5 as effective as the introduction of LEZ in reducing PM10 levels in Central London. 
Null hypothesis - The effect of ULEZ on PM10 was not significantly more effectve than LEZ in reducing PM10 levels in Central London. 

Our alpha values are set at 0.05.
Here is the result for the first and third tests:

/fig/hypothesis_test_1.jpg

/fig/hypothesis_test_2.jpg


Repo index:
* LondonAirQuality_final_notebook.ipynb - main notebook containing our detailed report and findings
* London Air Quality.pdf - final presentation of findings
* ulez_six_month_evaluation_report_final_oct.pdf - Mayor of London report on Cetral London's progress from ULEZ. Part of our research literature, included here for your convenience
* visualizations.py - functions for plotting our distributions
* hypothesis_tests.py - .py file for our null-hypothesis significance testing functions and for plotting visuals of those tests


* raw_data - data as downloaded / obtained via API; pre-cleaning
* clean_data - data files after merging and cleaning; data as used in statistical tests
* fig - images and visualizations saved directly from notebook
* archive_nb - additional notebooks that were generated as part of the cleaning or modelling process; not included in the final product

_________________________________________________________________________
References:
Ultra Low Emission Zone: Report to the Mayor; March 2015. Mayor of London; Transport for London. Accessed on: 11/11/2019. Link:
https://consultations.tfl.gov.uk/environment/ultra-low-emission-zone/user_uploads/tfl-ulez-consultation-report_final.pdf
