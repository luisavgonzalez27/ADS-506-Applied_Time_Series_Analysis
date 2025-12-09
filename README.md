# From Rapid Growth to Reliable Forecasts: Solving Europe’s EV Adoption Challenges

#### ADS 506: Applied Time Series Analysis
#### Team: Luisa Gonzalez, Paul Matta, Kiara Paz


# Overview
This project forecasts electric vehicle (EV) adoption in Europe using time-series models including ETS, ARIMA, and TSLM. The analysis follows a Problem–Solution storytelling framework to understand nonlinear EV growth, diagnose modeling challenges, and develop reliable forecasting methods that support industry and policy decision-making.

# Situation
EV adoption is accelerating globally, but the pace, stability, and policy context vary widely across regions. The original dataset includes 54 global regions, each shaped by different:
- EV incentives and subsidies
- Charging-infrastructure maturity
- Economic and regulatory environments

To maintain a consistent analytical foundation, we focused on Europe, because it:
- Has one of the fastest-growing EV markets worldwide
- Operates under aligned EU-level policy frameworks
- Contains a complete time series with no missing values
- Exhibits clear exponential adoption patterns suitable for time-series analysis

Cross-regional EDA showed China growing the fastest, followed by Europe and the U.S., reinforcing Europe as a meaningful and policy-coherent modeling target.

# Problem 
Despite strong growth, Europe’s EV market presents several modeling challenges:
### Structural Data Issues
- EV sales and stock grow exponentially, not linearly.
- Raw values are heavily right-skewed, complicating trend interpretation.
- Variance increases over time for all powertrains (BEV, PHEV, FCEV).
- Different technologies follow distinct adoption trajectories, requiring separate models.

# Solution
Key Insights From Exploratory Analysis:
- EV growth is multiplicative, benefiting from log-scale modeling.
- BEVs dominate long-term growth, while PHEVs plateau and FCEVs remain negligible.
- Log-transformed values yield smoother, more interpretable distributions.
- Growth rates indicate a shift from early-stage adoption to broader maturity.

## Forecasting Approach
Based on these findings, we selected models that align with nonlinear and variance-unstable behavior
- ETS (A, Ad, N) for exponential/damped trend behavior
- ARIMA models on log-transformed values
- TSLM models for trend-based forecasting comparisons

## Model Insights
- BEVs: Raw ARIMA produced the best forecasts
- PHEVs: Log-transformed ETS models were most accurate
- FCEVs: Raw TSLM outperformed other models
- Total Sales: Log-scale models yielded the most stable variance and cleanest signal


# Next Steps
- Build Forecasting Models
  - Fit ETS and ARIMA models using log-transformed EV sales.
  - Use rolling time-series cross-validation for accuracy comparison.
- Generate Forecasts
  - Produce 5–10 year forecasts for total EV sales and EV stock.
  - Model BEVs separately to project market share evolution.
- Extend the Analysis
  - Compare adoption patterns across European countries.
  - Incorporate external regressors such as policy incentives or charging infrastructure growth.
- Apply Insights
  - Support policymakers evaluating EV targets.
  - Assist manufacturers with demand and production planning.
  - Guide charging network investment decisions
