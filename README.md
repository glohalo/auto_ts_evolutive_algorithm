### Explanation Forecasting metrics:

1. **Validation Accuracy (SMAPE):**
   - **Symmetric Mean Absolute Percentage Error (SMAPE)** is a metric used to measure the accuracy of a forecast. It is calculated as:
     \[
     \text{SMAPE} = \frac{100\%}{n} \sum_{t=1}^{n} \frac{|F_t - A_t|}{(|A_t| + |F_t|)/2}
     \]
     where \(F_t\) is the forecasted value and \(A_t\) is the actual value.

2. **Prediction Interval Probability:**
   - The **Prediction Interval** is a range within which future observations are expected to fall with a certain probability.

**Forecasting Details:**
- **Forecast Length:** 60 periods
- **Frequency:** Automatically inferred
- **Prediction Interval:** 90%

**Optimization Strategy:**
- **Model Selection:** Using "fast_parallel" for quick and efficient model selection
- **Transformer List:** Optimized with the "fast" transformer set

**Genetic Algorithm Configuration:**
- **Max Generations:** 8 generations for thorough exploration
- **Validations:** 2 validation steps to ensure robustness
- **Constraint:** Set at 2.0 for optimal performance
- **Validation Method:** Backwards validation for reliable results

**Model Selection Process:**
The genetic algorithm explores a wide range of models and evaluates them based on:
- **Validation Accuracy:** Using Symmetric Mean Absolute Percentage Error (SMAPE) as the metric. The mean SMAPE of the validations is calculated to assess the model's accuracy.
- **Prediction Interval Probability:** Ensuring that the prediction intervals cover the true values with the specified probability (90%).

**Key Benefits:**
- **Efficiency:** Fast parallel processing reduces time
- **Accuracy:** High prediction interval ensures confidence
- **Scalability:** Suitable for various time series data applications

Implementing AutoTS with these configurations helps us achieve accurate and reliable forecasts while minimizing computational time. The genetic algorithm ensures we explore a wide range of models to find the best fit for our data.
