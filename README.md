# Bike-Sharing-Demand-Prediction


<img width="521" alt="bike sharing" src="https://github.com/kratikajawariya28/Bike-Sharing-Demand-Prediction./assets/124557001/cb679e1f-28b5-475b-948b-be89f1dd7b5b">



## Objective
The objective of this project is to predict bike-sharing demand at each hour for the stable supply of rental bikes in a city based on historical data. By building a predictive model, we aim to help bike-sharing companies optimize their bike allocation and better meet customer demand, ultimately improving the efficiency and user experience of their services.

## Dataset
The dataset used for this project contains historical information about bike rentals, includes features:
- **Date**: Current date
- **Rented Bike Count**: Dependent variable
- **Hour**: Hour of the day (0-23)
- **Temperature(°C)**: (Numerical) Temperature at the time of booking in °C.
- **Humidity(%)**: Humidity measure
- **Wind speed (m/s)**: (Numerical) Wind speed.
- **Visibility (10m)**: (Numerical) Visibility measure
- **Dew point temperature(°C)**: (Numerical) Dew point temperature measure
- **Solar Radiation (MJ/m2)**: (Numerical) Solar radiation measure
- **Rainfall(mm)** : (Numerical) Rainfall in mm
- **Snowfall (cm)** : (Numerical) Snowfall in mm
- **Seasons** : (Categorical) 4 seasons
- **Holiday** : (Categorical) Whether a holiday or not
- **Functioning Day** : (Categorical) Whether a functional day or not

## Data Wrangling
Data wrangling is an essential step in preparing the dataset for analysis and modeling. This phase involves cleaning, transforming, and structuring the data to make it suitable for further analysis.

## EDA (Exploratory Data Analysis)
Exploratory Data Analysis is a crucial step in understanding the dataset and gaining insights from it. By conducting thorough EDA, we aim to uncover valuable information about the dataset that will guide feature selection, engineering, and model building, ultimately leading to more accurate predictions of bike-sharing demand.

### Numerical Analysis
- Visualize numerical data using histograms, box plots to identify patterns and outliers.
- Assess the data distribution for each numerical feature to determine if there is skewness.
- Explore correlations between numerical variables to understand their relationships.

### Categorical Analysis
- Analyze the distribution of categorical variables using bar charts and count plots.
- Explore how categorical variables impact bike-sharing demand.

```
The following is a list of the types of plots we utilized during our analysis:
1. Histogram
2. Boxplot
3. lineplot
4. Q-Q plot
5. Scatter plot
6. Bar graphs
7. Correlation heatmap
8. Pair Plot
```

## Feature Engineering
The various steps involved in feature engineering:
- Handling Outliers: We managed outliers on column wind_speed by capping extreme values.
- Feature Selection: We selected key features using techniques like feature importance scores and correlation analysis.
- Categorical Encoding: We encoded categorical variables for effective model utilization.
- Data Transformation: We transformed data to meet linear model assumptions, including squareroot transformations.
- Multicollinearity: To ensure feature independence, we mitigated multicollinearity using VIF analysis.

## ML Model Implementation
The steps involved in implementing machine learning models for regression are:
- Data scaling: We standardized numerical features using StandardScaler.
- Data Preprocessing: The data was prepared for modeling, including train-test splitting
- Model Selection: Multiple machine learning models, including various regression algorithms (Linear, Ridge, Lasso and Elasticnet), as well as decision tree-based algorithms (Decision Trees, Random Forest, Gradient Boosting), were employed. The selection of the best-performing machine learning model was based on the evaluation using the R2 score.
- Model Evaluation: We assessed models using the R2 score, a suitable metric for regression tasks.

## Conclusion
### We opted for the XGBoost machine learning model as it demonstrated superior performance and yielded the best results.

### The dataset analysis leads to the following conclusions:
- During non-holidays, there is a substantial demand peak at 8 AM and 6 PM, aligning with typical work hours. This suggests that commuters and workers are the primary users during these times.
- On holidays, the dataset does not exhibit a significant daytime peak in demand. This suggests that usage patterns differ on holidays, potentially involving more leisure-oriented activities.
- The dataset shows that the highest booking activity occurs in the month of May, while January records the lowest. These monthly trends could be influenced by various factors, such as weath conditions or seasonal events.
- Seasonal analysis reveals that the summer months experience the highest booking rates, while the winter months show the lowest. These trends are likely related to weather and outdoor activities.
- Non-functioning days, characterized by reduced booking activity, present an opportunity for maintenance purposes. Organizations can utilize these periods to conduct maintenance and service improvements efficiently.
