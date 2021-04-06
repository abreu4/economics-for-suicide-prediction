# Predicting suicides from economic development indicators

This project aims at predicting suicide numbers purely from economic development indicators.

## Phases

The project is divided in 2 sprints with 3 phases each:
1. Preprocessing the economic indicators dataset
2. Preprocessing the suicide statistics dataset
3. Developing the model


## Sprints

Each sprint will differ only in the number of unique indicators.
1. st sprint: 
  * GDP per capita (constant LCU)
  * Unemployment percentage, total population
  * Consumer price index
2. nd sprint:
  * To be determined. The idea is to add more promising indicators and use a self-regularized model, such as Lasso regression


## Dataset

Two datasets are at the foundation of this project
1. [Suicide statistics (SS)](https://www.kaggle.com/szamil/who-suicide-statistics) provided by the World Health Organization
2. [Economic development indicators (EDI)](https://www.kaggle.com/worldbank/world-development-indicators) provided by the World Bank

Datasets should be placed in `data/`. Only `Indicators.csv` is required from the EDI dataset

The datasets will be preprocessed to the form of:
+ Features: country, indicator, indicator value, year
+ Label: total # suicides

## Current todos

- Interpolate missing values in the EDI dataset
- Find out which years are available for which countries in the SS dataset
- Combine both datasets into a new dataset for sprint 1.
- Build simple regression models