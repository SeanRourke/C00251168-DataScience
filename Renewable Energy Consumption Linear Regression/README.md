# Linear Regression on Renewable Energy Consumption

## Introduction

This project involved developing a machine learning model using linear regression to analyse and predict renewable energy consumption levels as a percentage of total energy consumption levels across various countries over the past 32 years.

## Data Sources

The dataset used for this project was obtained from World Bank Group, available here: https://data.worldbank.org/indicator/EG.FEC.RNEW.ZS?. This dataset contained a column holding different countries and regions of the world, and columns representing each year from 1960 to 2023.

## Pre-Processing

The original dataset contained columns from 1960, but no data was present until 1990. I removed the columns for the years 1960 - 1989. The data for 2023 was also empty so I also removed it.

## Tools and Tech Used

This project is written in Python in a Jupyter Notebook.
Excel was used for the pre-processing of the dataset.

## Findings

From performing operations on this data set, I have found that a linear regression model fits the data accurately for many of the countries and regions. 
For example, linear regression fits accurately on the data for Denmark.
There are countries however where this model does not work, such as Azerbijan.

This information could still be uselful, as countries that do not fit a linear model can be compared to see similarities that are perhaps the cause of the volatile nature of their renewable energy consumption.
Similarly, countries that the linear regression model works for can be compared to establish similarities between countries that have seen linear growth in renewable energy consumption, and similarities between countries that have seen linear decline in renewable energy consumption.