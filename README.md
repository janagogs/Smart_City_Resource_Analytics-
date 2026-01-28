# Project for Smart City Resource Analytics in Portugal (2006-2010)

## 1. Data Collection and Cleaning

The project used real household electricity consumption data from the UCI Machine Learning Repository, covering minute-level readings over several years. Initial steps included combining date and time into a datetime column, converting all features to numeric types, and removing missing values. This created a clean and consistent dataset suitable for analysis and modeling.

## 2. Data Aggregation and Feature Selection

Data was resampled to an hourly level to simplify analysis, with mean consumption calculated per hour. Key features selected for analysis included Global_active_power, Global_reactive_power, Voltage, and Global_intensity. Additional context-specific features were added to simulate a smart city environment: synthetic water consumption, hour of the day, day of the week, and month. These features allowed for a deeper understanding of energy and water usage patterns.

## 3. Exploratory Data Analysis (EDA)

EDA involved examining distributions, correlations, and temporal patterns in energy and water consumption. Visualizations showed significant variation across hours, days, and months, indicating strong seasonal and daily trends. Correlation analysis confirmed relationships between energy consumption metrics and synthetic water consumption, providing insights into household usage behavior.

## 4. Clustering of Household Patterns

KMeans clustering was applied to group households based on energy and water consumption, voltage, and intensity. The silhouette score of 0.402 indicated moderate cluster separation. Three distinct clusters were identified, representing different types of consumers, which can inform targeted energy and water management strategies.

## 5. Time-Series Forecasting

Time-series forecasting was implemented using XGBoost regression models for both energy and water consumption. Lag features from the previous four hours were used as predictors. The models achieved RMSE values of 0.567 for energy and 15.411 for water, showing that the models were able to capture consumption trends with good accuracy. Feature importance analysis highlighted the most influential variables for forecasting.

## 6. Smart Alerts Simulation

A smart alert system was simulated using thresholds based on mean plus standard deviation. Alerts were triggered when energy or water consumption exceeded these thresholds. Visualization of alerts across clusters identified high-consumption households, highlighting where interventions could reduce resource use effectively.

## Conclusion

This project successfully integrated data cleaning, feature engineering, exploratory analysis, clustering, time-series forecasting, and smart alert simulation. The results demonstrate how machine learning and data analytics can support resource optimization in smart cities, identify high-consumption households, and improve energy and water management strategies.
