

## 📈 Stock Market Prediction and Forecasting Using Stacked LSTM

A deep learning-based project to predict stock prices using a **Stacked LSTM (Long Short-Term Memory)** model. This notebook focuses exclusively on historical price data of **Apple Inc. (AAPL)** to demonstrate how deep learning can be applied to financial time series forecasting.

> ⚠️ **Disclaimer:** This project is for **educational and learning purposes only**. It is **not intended for financial or investment advice**.

---

### 🎯 Project Objective

To implement and explain a **Stacked LSTM neural network** for predicting future stock prices using historical data, showcasing how LSTM networks can learn temporal patterns in financial time series.

---

### 🛠️ Technologies Used

* **Python 3**
* `NumPy`, `Pandas` — Data manipulation
* `Matplotlib` — Data visualization
* `scikit-learn` — Feature scaling
* `TensorFlow / Keras` — Deep learning framework
* `pandas_datareader` — Stock price retrieval via Tiingo API

---

### 📊 Data Source

* **Provider:** [Tiingo API](https://api.tiingo.com/)
* **Stock:** `AAPL` (Apple Inc.)
* **Frequency:** Daily closing prices

> 🔑 You need a **Tiingo API key** to access the data. It’s free to sign up at [tiingo.com](https://www.tiingo.com/).

---

### 🔄 Workflow Summary

1. **Data Loading**

   * Fetch `AAPL` stock data using Tiingo API via `pandas_datareader`
2. **Preprocessing**

   * Handle missing values
   * Normalize prices using `MinMaxScaler`
   * Create time-based input sequences for LSTM
3. **Model Construction**

   * Build a Stacked LSTM architecture with multiple layers
   * Use `adam` optimizer and MSE loss
4. **Training & Evaluation**

   * Train the model and monitor loss
   * Visualize predicted vs actual prices



### 🚀 How to Run This Notebook

1. Open `Untitled.ipynb` in [Google Colab](https://colab.research.google.com/) or Jupyter Notebook.

2. Install required libraries if needed:

   ```bash
   pip install pandas_datareader tensorflow matplotlib scikit-learn
   ```

3. Set your Tiingo API key:

   ```python
   key = 'your_api_key_here'
   ```

4. Run each cell step-by-step and observe outputs.

---

### ⚙️ Troubleshooting

**Issue:**
`TypeError: concat() takes 1 positional argument but 2 were given`

**Fix:**
Update `pandas_datareader` to a compatible version:

```bash
pip install --upgrade pandas_datareader
```

Or, downgrade your `pandas` version:

```bash
pip install pandas==1.5.3
```

---

### 🚧 Limitations & Next Steps

* This is a **single-stock, single-feature** model (closing price only)
* Hyperparameters are basic — can be improved with tuning
* Could benefit from adding:

  * More technical indicators (e.g., RSI, MACD)
  * Sentiment analysis from financial news
  * Real-time forecasting interface (e.g., with Streamlit)

---

### 📚 Educational Purpose Only

This notebook is designed for **learning and experimentation** in deep learning and stock data analysis. The predictions are **not reliable for actual investment decisions**.

---

