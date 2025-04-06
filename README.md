## Title: **Forecasting UK National Electricity Demand Using Public Data**

Project Overview:
This project focuses on developing a high-resolution, long-term forecast of UK National Electricity Demand using publicly available data from the National Grid. The objective is to predict half-hourly demand over the next five years, leveraging data accessible to standard users through open online sources.

The initial phase of the project involves a comprehensive data exploration and feature engineering exercise, aimed at identifying the most informative variables to improve forecast accuracy. Advanced data preprocessing and transformation techniques are employed to prepare the data for modeling.

In later stages, the project expands into probabilistic forecasting—estimating upper and lower bounds of national demand under varying weather conditions. This allows for the development of a robust forecasting model that captures a realistic range of possible outcomes, which is especially relevant for planning under uncertainty in the evolving energy landscape.

## Data source description:
**1. Historical National Electrcity Demand Data** from National Grid website:
<br> https://www.neso.energy/data-portal/historic-demand-data
<br> Historic electricity demand, interconnector, wind and solar outturn data for 2025. 
<br> Brief summary of some of the columns in the dataset:
<br> ND = National Demand is the sum of metered generation, but excludes generation required to meet station load, hydro storage pumping and interconnector exports
<br> FORECAST_ACTUAL_INDICATOR = Indication of whether data is out-turn (A) or forecast (F)
<br> I014_ND = Equivalent to ND but calculated using settlement metered generation data from the I014 file where available
<br> TSD = Demand is equal to the ND plus the additional generation required to meet station load, pump storage pumping and interconnector exports
<br> I014_TSD = Equivalent to TSD (above), but calculated using settlement metered generation data from the I014 file where available
<br> **2. Calendar information**
<br> https://www.api.gov.uk/gds/bank-holidays/#bank-holidays
<br> **3. UK Population split**
<br> Source: https://www.statista.com/statistics/716499/population-figures-by-country/#:~:text=The%20UK%20population%20was%2068.3%20million%20in%202023%2C,5.5%20million%2C%203.16%20million%2C%20and%201.92%20million%20respectively.
<br> The UK population was 68.3 million in 2023, with 57.69 million people living in England, by far the most populous constituent country of the UK. In this year, Scotland, Wales, and Northern Ireland had populations of 5.5 million, 3.16 million, and 1.92 million respectively.
<br> **4. GDP data**
<br> Data Source: https://www.ons.gov.uk/economy/grossdomesticproductgdp/datasets/gdpmonthlyestimateuktimeseriesdataset
<br> **5. Covid data**
<br> https://www.google.com/covid19/mobility/?hl=en
<br> **6. Weather Data**
There is few different free weather data sources avaliable in the Internet:
* Python Libraries for Historical Weather Data Meteostat (pip install meteostat) Climate Data Store API (for ECMWF ERA5 data)
* **Open-Meteo API**
<br> Source: https://open-meteo.com/en/docs/historical-weather-api?hourly=relative_humidity_2m,apparent_temperature,precipitation,pressure_msl,cloud_cover,wind_speed_10m&start_date=2019-01-01&end_date=2025-03-17&latitude=51.508&longitude=-0.1257
