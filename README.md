# Threshold-Autoregressive-Model

Overview

This project demonstrates the implementation of a Threshold Autoregressive (TAR) Model using Apple stock prices (Close) as the dependent variable and Gross Domestic Product (GDP) as an exogenous variable. The model identifies regime changes in stock price behavior based on thresholds in GDP values.

**Key Steps**

**Data Collection:**

Gathered Apple stock price data (Close) and GDP data.

Ensured time consistency by aligning both datasets.

**Data Preprocessing:**

Converted Date columns into datetime format and set them as indices.

Merged the Apple stock and GDP datasets on their date indices.

Applied logarithmic transformations to stabilize variance and reduce skewness.

Created lagged variables for stock prices as predictors.

**Threshold Selection:**

Determined a threshold for GDP using the mean or a specified percentile value.

Segmented the data into two regimes: one below or equal to the threshold and one above it.

**Model Specification:**

Defined separate linear regression models for each regime using Ordinary Least Squares (OLS).

Included lagged stock prices (apple_lag) and GDP as predictors for both regimes.

**Model Training and Evaluation:**

Split the dataset into training and testing subsets.

Trained the TAR model on the training data, estimating parameters for each regime.

Calculated metrics like Mean Squared Error (MSE) and Mean Absolute Error (MAE) for training and testing sets.

**Visualization:**

Plotted residuals to evaluate model fit for each regime.

Compared actual vs. predicted values for both training and test sets to assess model performance.

**Results and Insights:**

Analyzed the effect of GDP on stock prices in different regimes.

Highlighted how the relationship changes based on economic conditions.

**Applications**

Financial Modeling: Capture stock price behavior under different economic scenarios.

Macroeconomic Analysis: Explore how macroeconomic indicators influence market trends.
