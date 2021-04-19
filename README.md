# Predicting suicides from economic development indicators

This project aims at predicting suicide numbers from economic development indicators.

## Dataset

Two datasets are at the foundation of this project
1. [Suicide statistics (SS)](https://www.kaggle.com/szamil/who-suicide-statistics) provided by the World Health Organization
2. [Economic development indicators (EDI)](https://www.kaggle.com/worldbank/world-development-indicators) provided by the World Bank

Datasets should be placed in `data/` and are preprocessed in the form of:
+ Features: country, year, population, economic development indicators
+ Label: total # suicides


## Theoretical background

Four indicators were chosen:

1. Adjusted GDP per capita
2. Consumer price index
3. Unemployment percentage of total population
4. Central government debt

These are known indicators of mental health and suicide numbers, as shown [here](https://bmjopen.bmj.com/content/2/3/e000785), [here](https://scielo.isciii.es/scielo.php?script=sci_arttext&pid=S0213-61632014000100004) and [here](https://pubmed.ncbi.nlm.nih.gov/20652218/)


Based on the following papers

## Current todos

- Finish refurbishing sklearn preprocessing pipeline
- Grid search train linear model

## Possible improvements

- EDI includes many other economic development indicators, such as debt as percentage of GDP. With the right data treatment techniques, these too could be used for predictions.
- Missing values could be imput by regressing indicator values along time axis for each country, since numbers seem to linearly increase over time for most indicators.
-
