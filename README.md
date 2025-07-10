📈 Stock Market Price Predictor
A simple machine learning project that predicts the next day's closing stock price using historical data and Linear Regression. The model also supports multi-day forecasting using recursive predictions.

🎯 Objective
To forecast a stock's closing price using historical data. The model uses:

✅ Linear Regression for time-series forecasting

📉 Historical stock data (historicalquotes.csv)

🗂️ Project Structure
sql
Copy
Edit
stock_price_predictor/
│
├── historicalquotes.csv       # Historical stock data with Date, Open, Close/Last, High, Low, Volume
├── stock_predictor.ipynb      # Jupyter notebook with full code and analysis
└── README.md                  # This file
📚 Dataset Format
Ensure your historicalquotes.csv file has the following columns:

Date	Close/Last	Volume	Open	High	Low
02/28/2020	$273.36	106721200	$257.26	$278.41	$256.37

The notebook:

Cleans the $ symbols

Sorts by ascending date

Prepares Close as input and Target (next day's price) as output

🛠️ Tools & Libraries Used
Python

pandas, numpy for data processing

matplotlib for plotting

scikit-learn for model training and evaluation

🔄 Workflow
Read and clean historicalquotes.csv

Preprocess: Remove dollar signs, convert dates, sort chronologically

Create features: Close price → predict next day’s price (Target)

Split data into training and test sets (80-20)

Train a Linear Regression model

Predict and plot actual vs predicted closing prices

Evaluate model performance (MSE, R² Score)

Forecast the next 3–5 days using recursive prediction

✅ Example Results
sql
Copy
Edit
Linear Regression:
  MSE: 13.67
  R² Score: 0.99

Next 5-day forecast:
  Day +1: $187.43
  Day +2: $187.52
  Day +3: $187.61
  Day +4: $187.70
  Day +5: $187.78
📈 Sample Graph Output
Line plot showing actual vs predicted prices

Forecasted values shown as dashed lines

🚀 Optional Extensions
Add lag features like Close(t-1), Close(t-2) for smarter models

Use Random Forest Regressor or LSTM for better trend learning

Build a web app with Streamlit or Flask

Export predictions to CSV/Excel

🧠 Conclusion
This project gives you a simple but effective baseline for stock price prediction using only historical closing prices and linear regression. It's easy to improve with more data and smarter features.
