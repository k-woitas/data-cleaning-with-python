# Data Cleaning with Python

## Inhaltsverzeichnis

- [Files](#files)
- [Setup](#setup)
- [Contents](#contents)

Workshop prepared for University of Bern's [Transferable Skills Program for (Post)Docs](https://www.unibe.ch/research/promotion_of_early_career_researchers/ts/ts/index_eng.html). 

Covering data quality concepts including data validity and discussion of insufficient data. Working through a cleaning process of example tabular data using various methods of analysing (EDA), visualizing, correcting, transforming, imputing data.

## Files

* `data_cleaning.ipynb` – the workshop notebook
* `data_cleaning.html` – the executed notebook as HTML, to read without Python
* `bank.csv` – example dataset (abridged and adjusted version of the [Bank Marketing Data Set](https://archive.ics.uci.edu/dataset/222/bank+marketing))
* `environment.yml` / `requirements.txt` – the packages needed

## Setup

Tested with Python 3.12, pandas 2.3, scikit-learn 1.9, seaborn 0.13 and fg-data-profiling 4.20 (October 2026).

With conda:

    conda env create -f environment.yml
    conda activate cleaning-env
    jupyter lab

Or with pip (in a virtual environment):

    pip install -r requirements.txt
    jupyter lab

Note: [fg-data-profiling](https://github.com/Data-Centric-AI-Community/fg-data-profiling) is the current name of the former *pandas-profiling* / *ydata-profiling* package. It does not support pandas 3 yet, therefore pandas is kept at version 2.3.

## Contents

    1  Prerequisites
    2  Data quality aspects
        2.1  Data validity constraints
    3  Data cleaning workflow
    4  Data
        4.1  Load the example dataset
    5  Data inspection
        5.1  Checking variable validity
            5.1.1  General overview
            5.1.2  Data-types
            5.1.3  Duplicate items
            5.1.4  Ranges (of numerical variables)
            5.1.5  Set memberships (of categorical variables)
            5.1.6  Unique values
            5.1.7  Missing values
        5.2  Basic statistics
            5.2.1  Bivariate statistics
            5.2.2  Pivot tables
            5.2.3  Correlations
        5.3  Data inspection by visualizations
            5.3.1  Categoricals
            5.3.2  Numerics
            5.3.3  Bi-/Trivariate
            5.3.4  Heat maps
        5.4  Data inspection with data-profiling
    6  Explore cleaning
        6.1  Dealing with insufficient data
        6.2  Removing data
        6.3  Correcting data
            6.3.1  Change data-types
                6.3.1.1  Change data-type of "age" into integer
                6.3.1.2  Transforming "999" in 'pdays' to NA/None
            6.3.2  Unify inconsistent, but equal values or aggregate variable levels
                6.3.2.1  Aggregate levels of 'job' and 'education'
        6.4  Imputing data
        6.5  Transforming data
            6.5.1  Recode nominals into dummy variables
            6.5.2  Recode ordinals as numeric
        6.6  Standardize
    7  Define & verifying pipeline
    8  Implementing & reporting
