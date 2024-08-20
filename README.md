# Analysis of Italian MICHELIN restaurants

## Project Overview

This project aims to predict the **Return on Assets (ROA) for 2022** using various machine learning techniques. 

- [Project Overview](#project-overview)
- [Data Description](#data-description)
- [Project Structure](#project-structure)
- [Feature Engineering](#feature-engineering)
- [Modeling Approaches](#modeling-approaches)
- [Results](#results)
- [License](#license)

## Data Description

The dataset used in this analysis includes various financial metrics and other relevant features. Key variables include:

- `ROA (%)`: Return on Assets from the year 2020 to 2022.
- `Indice_Liquidità`: Index of liquidity from 2020 to 2022.
- `Indice_Finanziario`: Index of financial independence from 2020 to 2022.
- `Follower_Restaurant and Follower_Chef`: Instagram follower for restaurant and chef from 2018 to 2022. It contains a lot of missing data so in the end we didn't use this data for our predictive analysis
- `Type of Structure`: Hotel, Catering, Guest house, Farmhouse
- `Star`: Number of star from 1 to 3
- `N. of employees`: to understand the size of the company
- `Social Capital`
- Dummies variables for regions.

## Feature Engineering
We created two new variables to summarize the effect of the two index previously calculated that are more statistically significant.
- `Delta_Liquidità_2022`: Change in liquidity in 2022.
- `Delta_Finanziario_2022`: Change in financial independence in 2022.

## Modeling Approaches
Several models were implemented and compared:

**OLS Regression**: The baseline model used for prediction.

**Ridge Regression with Spline Transformation**: To capture non-linearities.

**Polynomial Features**: To capture non-linear relationships between features.

**Simple Decision Tree**: Trying a tree based method to see how it performs.

**Random Forest**: Improving performance of tree base method using RF.

## Results

**Empirical Results**: R-squared is the metric used to evaluate the performance of each model

**Visual Results**: Visualizing the predicted y versus the actual y provided a clear view of how well the regression line corresponds with our data.

**Explanable AI**: SHAP was used to interpret the OLS model, understand feature importance and more importantly how much and how each variable influence the final result.

## License
I'd like to thanks my friend Simone Staiano to manually scrape data all over the web to provide me this Dataset, all the credits goes to him.
