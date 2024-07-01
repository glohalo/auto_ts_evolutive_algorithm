### Implementation Details

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

Source: https://winedarksea.github.io/AutoTS/build/html/source/tutorial.html
