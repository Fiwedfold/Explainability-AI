Electricity Consumption Analysis and Prediction Project

Authors

Cavaliere Luca

Alan Casasnovas

Arthur Da Costa Vieira

Project Objective

The main goal of this project is to analyze and predict electricity consumption in a region (e.g., Nouvelle-Aquitaine) based on temporal data while identifying potential anomalies. Key aspects include:

Visualization of energy consumption and production trends.

Predictive modeling to anticipate hourly consumption.

Anomaly detection using unsupervised algorithms.

Model explainability to understand factors influencing consumption.

📊 Key Results

🔍 Exploratory Analysis

Electricity consumption exhibits daily variations (peaks during the day) and seasonal variations (higher in winter).

Renewable energy sources (wind, solar) contribute significantly but vary across periods.

Strong correlations between consumption and thermal/nuclear production.

🤖 Predictive Modeling

Model used: Ridge Regression

Explanatory variables: hour, day of the week, thermal production

Model performance in Nouvelle-Aquitaine region:

MAE (Mean Absolute Error): 655.66 MW

RMSE (Root Mean Square Error): 834.77 MW

⚠️ Anomaly Detection

Methods used: Isolation Forest and Local Outlier Factor

Results: About 1% of the data is marked as anomalies (abnormally high or low consumption).

📈 Interactive Visualizations

Time-series graphs (Plotly) showing the evolution of consumption and anomalies.

Comparison of energy production sources with customized color palettes.

📂 Data Sources

📊 Main Dataset

File Name: eco2mix-regional-tr.csv

Official Source: RTE (Réseau de Transport d’Électricité)

Link: ECO2Mix Data

Description: This dataset contains hourly data on electricity consumption and production by French region, including:

Consumption (MW)

Production by type: thermal, nuclear, wind, solar, hydro, bioenergy

Trade exchanges and CO₂ rates

Covered Period: Data updated daily

🛠️ Python Libraries Used

pandas, numpy for data manipulation

scikit-learn for modeling and anomaly detection

matplotlib, seaborn, plotly for visualizations

prophet for advanced time-series analysis

🔑 Dataset Details

Column

Description

Data Type

Date - Time

Hourly timestamp (YYYY-MM-DD HH:MM)

Datetime

Region

French region (e.g., Nouvelle-Aquitaine)

Categorical

Consumption (MW)

Total electricity consumption

Numeric

Thermal (MW)

Fossil-based production (gas, coal)

Numeric

Nuclear (MW)

Nuclear-based production

Numeric

Wind (MW)

Wind-based production

Numeric

Solar (MW)

Solar-based production

Numeric

Hydro (MW)

Hydroelectric production

Numeric

Bioenergy (MW)

Biomass-based production

Numeric

⚙️ Data Processing

Cleaning: Handling missing values using median imputation.

Feature Engineering:

Creating temporal variables (hour, day of the week, weekend).

Calculating the share of renewable energy in total production.

Normalization: Standardizing data for ML models.

🎯 Conclusion

This project demonstrates how AI and data analysis can support energy decision-making. The developed models enable consumption prediction and anomaly detection, facilitating a proactive management of power grids.

The RTE dataset provides a reliable and rich base for in-depth analysis while requiring rigorous preprocessing to ensure optimal usability.

📎 Attached Files

Source code: projet_explainability_ai.py

Processed dataset: donnees_finales.parquet

