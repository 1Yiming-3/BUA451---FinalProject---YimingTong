# BUA451---FinalProject---YimingTong

**Yiming TONG** | Business Data Analytics & Finance, Syracuse University  
**Dataset**: bigquery-public-data.covid19_nyt.us_counties  
**Date**: 2025-04-29 

# 1. Executive Summary


### This project focuses on the county-level COVID-19 epidemic in the United States, extracts and analyzes the "cumulative confirmed cases" and "daily new" trends from the public BigQuery dataset, and then constructs a binary classification model to predict whether the next day will enter the "high incidence" state.
** - Business problem ** : Help public health departments prioritize medical resources and provide early warning of new spikes.

** - Key findings - ** :
1. As of the latest date, the five most affected counties are Los Angeles, New York City, Cook, Miami-Dade, Maricopa.
2. The new peak in Los Angeles County is mainly concentrated in July 2020 and January 2021.

** Model performance ** : ~74% precision and 70% + recall on the test set based on Logistic Regression with data added in the last 7 days.

** Management implications ** : This can be used to dynamically deploy care and supplies and to develop intervention strategies in advance of high-risk periods.

# 2. Dataset Description

Data Source: Google BigQuery Public Dataset

Table ID: bigquery-public-data.covid19_nyt.us_counties

Origin: The New York Times COVID-19 repository (county-level daily counts of cases and deaths)

Created: April 9, 2020 Last Modified: April 28, 2025

Location: US (no table expiration)

Schema

 Column	 Type	 Description

-date	DATE	Report date

-county	STRING	County name

-state_name	STRING	State name

-county_fips_code	STRING	FIPS geographic identifier for the county

-confirmed_cases	INTEGER	Cumulative number of confirmed COVID-19 cases to date

-deaths	INTEGER	Cumulative number of confirmed COVID-19 deaths to date

- Table Description: County-level time series of COVID-19 confirmed cases and deaths published by The New York Times (source: https://github.com/nytimes/covid-19-data).

- Record Count: ~2.7 million rows (all U.S. counties, daily from 2020-01-21 through 2025-04-28).

This dataset supports both exploratory analysis and time-series predictive modeling.

# 3. EDA Results and Visuals
### 3.1 - Insight 1: Top 5 Counties for “Cumulative Number of Confirmed Diagnoses” by Latest Date
#### Business Implications: Helps decision makers quickly target counties with the worst outbreaks and most need for resource investment.

# 4. Predictive Modeling

# 5. Managerial Insights and Takeaways
1. ** Prioritizing resources ** : The Top 5 counties with the highest risk of severe illness and death are prioritized to receive medical supplies and human support.

2. ** Dynamic early warning ** : High incidence early warning based on model prediction, which can start emergency response 1-2 days in advance and optimize emergency material allocation.

3. ** Monitoring and Strategy ** : Combined with interactive visualization, real-time monitoring of peak periods and adjusting epidemic prevention policies (such as restricting aggregation and expanding detection) to cut peaks.

4. ** Future expansion ** : Integrate socioeconomic, population density, vaccination rate and other multi-dimensional features to build a more refined prediction and intervention framework.



