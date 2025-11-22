# From Rapid Growth to Reliable Forecasts: Solving Europe’s EV Adoption Challenges

#### ADS 506: Applied Time Series Analysis
#### Team: Luisa Gonzalez, Paul Matta, Kiara Paz


# Overview
This project analyzes electric vehicle (EV) adoption in Europe using time-series forecasting methods, including ETS, ARIMA, and TSLM models. The work follows a Problem–Solution storytelling structure to diagnose challenges in understanding EV growth and to develop reliable forecasting models.

# Situation
Electric vehicle adoption is accelerating globally, but growth patterns differ by region due to variations in policy, incentives, and market maturity. The original dataset covers multiple global regions, which introduces inconsistencies when comparing trends shaped by distinct policy environments.

To maintain consistency, we focused exclusively on Europe, one of the fastest-growing EV markets with strong regulatory support and extensive historical data. The European subset is complete with no missing values, making it ideal for exploratory analysis and forecasting.

# Problem 
Even though Europe’s EV market is expanding rapidly, several analytical challenges emerged:
- EV sales and stock values follow exponential, not linear growth.
- Raw values are heavily right-skewed, making interpretation difficult.
- Year-over-year volatility is high, especially in early years.
- BEVs, PHEVs, and FCEVs follow different adoption trajectories, adding complexity.
- Without addressing these structural issues, simple linear forecasting models fail to produce reliable results.


These issues make simple linear forecasting unreliable and limit the ability to plan policy, manufacturing, or infrastructure effectively.

# Solution
Our exploratory analysis revealed clear structural patterns:
- EV growth is multiplicative, benefiting from log-scale modeling.
- BEVs dominate long-term growth, while PHEVs plateau and FCEVs remain negligible.
- Log-transformed values yield smoother, more interpretable distributions.
- Growth rates indicate a shift from early-stage adoption to broader maturity.

Based on these insights, we apply forecasting models that reflect the true structure of the data:
- ETS (A, Ad, N) for exponential/damped trend behavior
- ARIMA models on log-transformed values
- TSLM models for trend-based forecasting comparisons

These methods generate more accurate and stable forecasts for EV sales and stock.

# Next Steps
- 1. Build Forecasting Models
  - Fit ETS and ARIMA models using log-transformed EV sales.
  - Use rolling time-series cross-validation for accuracy comparison.
- 2. Generate Forecasts
  - Produce 5–10 year forecasts for total EV sales and EV stock.
  - Model BEVs separately to project market share evolution.
- 3. Extend the Analysis
  - Compare adoption patterns across European countries.
  - Incorporate external regressors such as policy incentives or charging infrastructure growth.
- 4. Apply Insights
  - Support policymakers evaluating EV targets.
  - Assist manufacturers with demand and production planning.
  - Guide charging network investment decisions
