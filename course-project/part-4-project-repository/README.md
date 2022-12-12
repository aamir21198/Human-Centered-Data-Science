# Course Project

## Part 4 - Project Repository

**DATA 512: Human-Centered Data Science**

[![MIT License](https://img.shields.io/apm/l/atomic-design-ui.svg?)](https://github.com/aamir21198/Human-Centered-Data-Science/blob/main/LICENSE)

### Goal:
During the last three years we all have been experiencing a global pandemic. This has been tragic and disruptive to many countries and has taken a deep personal toll on many individuals and their families.
One aspect that has been hard to miss in the last three years is the datafication of the pandemic. That is, many aspects of the individual toll of the pandemic have been collected, aggregated and re-represented as data. This datafication gives us the privilege to examine the pandemic from potentially many different perspectives to understand how it has changed lives and how it has changed society. To be honest, we are actually at the very beginning of understanding and comprehending these impacts.
During this Course Project you are going to begin taking a look at some of the social aspects of the pandemic by conducting a human centered data science analysis of some available COVID-19 data.

#### Assigned County: Hudson, New Jersey 

### Research Questions
1. How did the increase in COVID-19 cases in Hudson County affect its unemployment rate?
2. How did the increase in COVID-19 deaths in Hudson County affect its unemployment rate?
3. Does the employment rate in Hudson County depend more on the number of COVID cases or the number of deaths due to COVID-19?

### Data Sources:
- [John Hopkins University COVID-19 data](https://www.kaggle.com/datasets/antgoldbloom/covid19-data-from-john-hopkins-university). ([License](https://creativecommons.org/licenses/by/4.0/))
- [Masking Mandates by County](https://data.cdc.gov/Policy-Surveillance/U-S-State-and-Territorial-Public-Mask-Mandates-Fro/62d6-pm5i)
- [Mask Compliance Survey](https://github.com/nytimes/covid-19-data/tree/master/mask-use) ([License](https://github.com/nytimes/covid-19-data/blob/master/LICENSE))
- [The unemployment rate in Hudson County, NJ](https://fred.stlouisfed.org/series/NJHUDS7URN)

### Input Data Files
- Data/RAW_us_confirmed_cases.csv
- Data/RAW_us_deaths.csv
- Data/mask-mandate.csv
- Data/mask-use-by-county.csv
- Data/unemployment-rate-hudson-nj.csv

### Data Description for RAW_us_confirmed_cases.csv

| Feature        | Data type | Description                                                         |
|----------------|-----------|---------------------------------------------------------------------|
| Province_State | String    | The name of state                                                   |
| Admin2         | String    | The name of the county                                              |
| UID            | int       | Unique ID of the county                                             |
| Country Region | String    | The country that the county belongs to                              |
| Lat            | float     | The county latitude                                                 |
| Long_          | float     | The county longitude                                                |
| Combined Key   | String    | Unique key by combining the county, state and country               |
| \<date>        | int       | Confirmed number of cases for each day from 1/22/2020 to 10/30/2022 |

### Data Description for RAW_us_deaths.csv

| Feature        | Data type | Description                                                    |
|----------------|-----------|----------------------------------------------------------------|
| Province_State | String    | The name of state                                              |
| Admin2         | String    | The name of the county                                         |
| UID            | int       | Unique ID of the county                                        |
| Country Region | String    | The country that the county belongs to                         |
| Lat            | float     | The county latitude                                            |
| Long_          | float     | The county longitude                                           |
| Combined Key   | String    | Unique key by combining the county, state and country          |
| Population     | int       | The population of the county                                   |
| \<date>        | int       | The number of deaths for each day from 1/22/2020 to 10/30/2022 |

### Data Description of unemployment-rate-hudson-nj.csv

| Feature        | Data type | Description                                                              |
|----------------|-----------|--------------------------------------------------------------------------|
| Date           | String    | The first date of the month for which the unemployment rate was recorded |
| NJHUDS7URN     | String    | The unemployment rate for that month                                     |


### Final Visualization (Part 1):
![Hudson county daily cases](./Images/Hudson%20county%20daily%20cases.png)

### Visualizing the correlation between the COVID Cases and Unemployment Rate
![Covid Cases vs Unemployment Rate](./Images/cases_vs_unemployment.png)

### Visualizing the correlation between the COVID Deaths and Unemployment Rate
![Covid Cases vs Unemployment Rate](./Images/deaths_vs_unemployment.png)