# Population Risk Analysis

This project analyzes population risk across countries using fertility rates, dependency ratios, and migration data. The goal is to identify countries at high risk of population decline and understand the main demographic factors contributing to this risk.

## Data Sources
- Cleaned population dataset (`clean_population_data.csv`)
- World Bank and UN demographic statistics

## Methodology
1. **Data Cleaning & Normalization**: Loaded the population data, handled missing values, and normalized key factors (fertility, dependency, migration) for comparability.
2. **Population Risk Score**: Calculated a combined risk score using: population_risk_score = dependency_norm + (1 - fertility_norm) + (1 - migration_norm)
3. **SQL Analysis**: Queried the top 10 countries for each factor and risk category.
4. **Visualizations**: Created bar charts for fertility, dependency, migration, and risk scores to highlight trends.
5. **Regression Analysis**: Used a linear regression to understand the relative contribution of each factor to population risk. Dependency ratio and fertility are highly correlated, while migration provides independent insight.

## Key Takeaways

- High-risk countries are mostly in Africa and parts of Asia, often with high dependency ratios.
- Low fertility (below replacement level of 2.1) affects 121 countries, indicating potential population decline.
- Negative net migration occurs in ~130 countries, contributing to population risk.
- Dependency ratio and fertility are strongly correlated, both contributing to risk. Migration adds independent insight.
- Overall, countries with high dependency, low fertility, and negative migration face the greatest population challenges.

## How to Run

1. Open the Jupyter/Colab notebook.
2. Upload the cleaned CSV if not already present.
3. Run cells in order: data loading → SQL queries → visualizations → regression.
