# NVDA Stock Price Forecast Using Prophet

This repository contains a forecasting project that predicts the stock price movement of **NVIDIA Corporation (NVDA)**. By using **Prophet**, a powerful forecasting model designed to handle time series data, the project aims to capture long-term trends, seasonal effects, and changepoints in the stock price.

## Project Overview

NVDA is one of the most popular and volatile stocks in the technology sector. Investors and traders alike are keen on predicting its price movements to guide investment and trading decisions. The goal of this project is to provide a forecast of NVDA stock prices, focusing on:

- **Understanding Major Trends:** Identifying the long-term movement of NVDA stock prices to support investment decisions.
- **Supporting Trading Decisions:** Providing guidance for traders on potential future price movements.
- **Minimizing Investment Risks:** Helping investors reduce risk and increase profitability by understanding key trends.

This project uses Prophet to model the time series data and evaluate its accuracy using **Mean Absolute Error (MAE)** and **Root Mean Squared Error (RMSE)**.

## Table of Contents

- [Installation](#installation)
- [Dataset](#dataset)
- [Methodology](#methodology)
- [Results](#results)
- [Visualization](#visualization)
- [Recommendations](#recommendations)
- [Team](#team)
- [License](#license)

## Installation

To run the project locally, you'll need to set up the following dependencies:

```bash
pip install pandas
pip install fbprophet
pip install matplotlib
```

Once installed, you can run the Jupyter notebook or Python scripts to see the forecast results.

## Dataset

The dataset consists of NVDA's **stock closing prices** starting from 2024. The data is preprocessed for use in the Prophet model, with date formatting and column adjustments as needed for time series modeling.

## Methodology

### Forecasting Model: Prophet

Prophet is a robust forecasting model from Facebook designed for time series data with **seasonal components**, **trend changes**, and **holiday effects**. Here's how we approached the modeling:

1. **Data Preprocessing:** Historical stock prices are cleaned and formatted.
2. **Data Splitting:** The data is split into 80% for training and 20% for testing.
3. **Model Tuning:** We tune the following parameters to improve model sensitivity:
   - **changepoint_prior_scale (CPS):** Controls flexibility in detecting trend changes.
   - **seasonality_prior_scale (SPS):** Adjusts sensitivity to seasonal patterns.
   - **holidays_prior_scale (HPS):** Handles the effect of holidays on the stock price.
4. **Evaluation Metrics:** We use **MAE** and **RMSE** to measure model accuracy.

### Key Parameters:
- **CPS = 0.06**: Sufficiently flexible in capturing trend changes.
- **SPS = 0.15**: High sensitivity to seasonal patterns.
- **HPS = 1**: Minimal impact since holiday effects are not prominent in the dataset.

## Results

The model effectively captures the **long-term trends** of NVDA's stock price movements. While Prophet struggled with short-term volatility, the forecasted **trend direction** aligns with the actual data, making it useful for long-term investment strategies.

- **MAE:** Measures the average absolute deviation between predicted and actual values.
- **RMSE:** Highlights significant errors, offering more insight into large prediction deviations.

### Key Insights:
- **Rolling Mean and Changepoints:** Prophet successfully identifies key changepoints in the stock trend, aided by careful parameter tuning.
- **Residual Analysis:** The residuals (errors) show a fairly even distribution, indicating that the model captures most of the existing patterns without systematic bias.

## Visualization

The following visualizations are provided to illustrate the model's performance:

1. **Prediction vs. Actual:** Shows how well the model follows actual stock price movements.
2. **Residuals:** A visualization of the prediction errors, demonstrating the spread and patterns of error.

## Recommendations

### 1. Long-Term Investment Strategy:
- The model is useful for long-term investors, as it captures the general trend direction. Investors can leverage this forecast to decide the right time for buying or selling stocks over an extended period.

### 2. Trading Opportunities:
- Though short-term volatility prediction is not the strength of Prophet, the predicted trends can help traders align their strategies with the market momentum. Traders can combine this model with technical indicators for better decision-making.

### 3. Decision-Making Support:
- Overall, this forecast supports both **investment** and **trading strategies** by providing a reliable view of long-term trends.

## Team

This project was developed by the following contributors:

- [**Faizal Lutfi Yoga Triadi**](https://www.linkedin.com/in/faizallutfiyt/)
- [**Army Putera Silalahi**](https://www.linkedin.com/in/army-putera-silalahi/)
- [**Andy Hermawan**](https://www.linkedin.com/in/andy-hermawan/)

This full markdown document will ensure that the project is well-organized and clearly documented for users on GitHub.
