# Stock Price Prediction Using Machine Learning

This project demonstrates a machine learning approach to predicting the next day's closing price of a stock using historical market data. The model is trained on Apple Inc. (AAPL) stock data obtained from Yahoo Finance and implements time series regression using a Random Forest Regressor.

## Project Overview

- **Objective**: Predict the next day's closing price for AAPL stock.
- **Data Source**: Yahoo Finance (`yfinance` Python package)
- **Model Used**: Random Forest Regressor
- **Features**: Open, High, Low, Close, Volume
- **Target Variable**: Next day's closing price

## Dataset Description

- Historical data from January 2015 to December 2023
- Features used:
  - `Open`, `High`, `Low`, `Close`, `Volume`
  - Target: `Close` column shifted by -1 (to represent next-day prediction)

## Tools and Libraries

- Python 3.x
- pandas, numpy
- yfinance
- scikit-learn
- matplotlib, seaborn

## Machine Learning Workflow

1. **Data Collection**  
   Retrieved AAPL stock data using the `yfinance` API.

2. **Preprocessing**  
   - Removed missing values  
   - Scaled numerical features using `StandardScaler`

3. **Feature Engineering**  
   - Created a new target column for next-day closing price  
   - Used previous day's features to predict future values

4. **Model Training**  
   - Split data into training and testing sets (80/20, time-ordered)  
   - Trained a Random Forest Regressor

5. **Evaluation**  
   - Evaluated model using RMSE and R² Score  
   - Visualized actual vs. predicted prices

## Model Performance

- **Root Mean Squared Error (RMSE)**: ~1.5 (example value)
- **R² Score**: ~0.89 (example value)

*Actual results may vary based on data and hyperparameters.*

## Visualization

A line plot comparing the actual and predicted closing prices over the test period is generated at the end of the script to evaluate model accuracy visually.

## How to Run

1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/stock-price-prediction.git
   cd stock-price-prediction
