# 📈 Stock Market Price Predictor

A simple machine learning project that predicts the **next day's closing stock price** using historical data and **Linear Regression**. The model also supports **multi-day forecasting** using recursive predictions.

---

## 🎯 Objective

To forecast a stock's closing price using historical data. The model uses:
- ✅ Linear Regression for time-series forecasting  
- 📉 Historical stock data from `historicalquotes.csv`

---

## 🗂️ Project Structure

stock_price_predictor/
│
├── historicalquotes.csv # Historical stock data (Date, Close/Last, Open, High, Low, Volume)
├── stock_predictor.ipynb # Jupyter notebook with full code and analysis
└── README.md # This file

yaml
Copy
Edit

---

## 📚 Dataset Format

Your `historicalquotes.csv` file should have columns like:

| Date       | Close/Last | Volume     | Open     | High     | Low      |
|------------|------------|------------|----------|----------|----------|
| 02/28/2020 | $273.36    | 106721200  | $257.26  | $278.41  | $256.37  |

The notebook:
- Cleans `$` symbols
- Converts strings to float
- Parses dates and sorts chronologically

---

## 🛠️ Tools & Libraries Used

- Python 3.x
- `pandas`, `numpy` for data preprocessing
- `matplotlib` for plotting
- `scikit-learn` for training and evaluation

---

## 🔄 Workflow

1. **Load and clean** the data
2. **Preprocess**: Remove dollar signs, sort by date
3. **Create features**: `Close` price → `Target` (next day's price)
4. **Train-test split** (80-20)
5. **Train** Linear Regression model
6. **Predict and plot** actual vs predicted prices
7. **Evaluate** with MSE and R² Score
8. **Forecast** next 3–5 days (recursive predictions)

---

## ✅ Sample Results

Linear Regression:
MSE: 13.67
R² Score: 0.99

Next 5-day forecast:
Day +1: $187.43
Day +2: $187.52
Day +3: $187.61
Day +4: $187.70
Day +5: $187.78

yaml
Copy
Edit

---

## 📈 Visual Output

- Line plot showing **actual vs predicted** closing prices
- Dashed orange line for predicted future values

---

## 🚀 Extensions

- Add lag features: `Close(t-1)`, `Close(t-2)` for improved modeling
- Try `RandomForestRegressor` or `LSTM` for better non-linear trend prediction
- Build a UI with **Streamlit** or **Flask**
- Export predictions to CSV or Excel

---

## 🧠 Conclusion

This project builds a baseline stock price predictor using just historical closing prices and Linear Regression. While simple, it sets a strong foundation for more advanced time-series forecasting projects.

---
