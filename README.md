# Predicting suicides from economic development indicators

This project aims at predicting suicide numbers of a given country in a given year from its economic development indicators.

## Dataset

Two datasets are at the foundation of this project
1. [Suicide statistics (SS)](https://www.kaggle.com/szamil/who-suicide-statistics) provided by the World Health Organization
2. [Economic development indicators (EDI)](https://www.kaggle.com/worldbank/world-development-indicators) provided by the World Bank

## Theoretical background

Four economic development indicators were chosen:

1. Adjusted GDP per capita
2. Consumer price index
3. Unemployment percentage of total population
4. Central government debt

These are known indicators of mental health and suicide numbers, as shown [here](https://bmjopen.bmj.com/content/2/3/e000785), [here](https://scielo.isciii.es/scielo.php?script=sci_arttext&pid=S0213-61632014000100004) and [here](https://pubmed.ncbi.nlm.nih.gov/20652218/)

## Status

Current Ridge model has a median absolute error of 500 people on the testing set.
As usual, more features, better data preprocessing and better model training are likely to yield better results.


## Current todos

- Investigate impact of introducing categorical and ordinal variables (country and year, respectively)
- Encapsulate preprocessing and model fitting in sklearn-style pipeline
- Grid search model fitting


## Possible improvements

- EDI includes many other economic development indicators, such as debt as percentage of GDP. With the right data treatment techniques, these too could be used for predictions.
- Missing values could be imput by regressing indicator values along time axis for each country, since numbers seem to linearly increase over time for most indicators.
- There are better ways to deal with skewed data during training. See https://scikit-learn.org/stable/auto_examples/inspection/plot_linear_model_coefficient_interpretation.html
- Find better ways of dealing with highly correlated data. Maybe models that boost smaller coefficients?
