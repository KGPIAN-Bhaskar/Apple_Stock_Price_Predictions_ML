
# 📈 AAPL Stock Price Prediction using LSTM

A deep learning project that predicts Apple (AAPL) stock prices using Long Short-Term Memory (LSTM) neural networks. This project demonstrates an end-to-end machine learning workflow including data collection, preprocessing, model training, evaluation, and visualization.

---

## 🚀 Project Overview

Stock price prediction is a challenging time-series problem. In this project, we use historical stock data and an LSTM model to predict future closing prices.

### Key Highlights:

* 📊 Real-world stock data using Yahoo Finance
* 🔄 Time-series preprocessing using sliding window
* 🤖 Deep Learning model using LSTM
* 📉 Visualization of actual vs predicted prices
* 🧪 Train/Test split with performance evaluation

---

## 🧠 Technologies Used

* Python
* NumPy & Pandas
* Matplotlib
* Scikit-learn
* TensorFlow / Keras
* yFinance API

---

## 📂 Project Structure

```
├── data/
├── outputs/
│   └── aapl_price_chart.png
├── preprocess.py
├── train_model.py
├── README.md
```

---

## 📥 Data Collection

We use the **yFinance API** to download 5 years of Apple stock data:

```python
df = yf.download("AAPL", period="5y", auto_adjust=True)
```

---

## ⚙️ Data Preprocessing

* Extract only closing prices
* Normalize data using MinMaxScaler
* Create sequences of 60 days

### Sliding Window Concept:

```
Past 60 days → Predict next day price
```

---

## 🏗️ Model Architecture

* LSTM Layer (50 units, return sequences)
* Dropout (0.2)
* LSTM Layer (50 units)
* Dropout (0.2)
* Dense Layer (Output)

---

## 🧪 Training Details

* Optimizer: Adam
* Loss Function: Mean Squared Error (MSE)
* Epochs: 20
* Batch Size: 32

---

## 📊 Results

The model predicts stock prices based on historical patterns.


---

## 📏 Evaluation Metric

Root Mean Squared Error (RMSE):

```python
rmse = np.sqrt(mean_squared_error(y_test_actual, predictions))
```

---

## ⚠️ Limitations

* Does not consider external factors (news, economy)
* Works only on historical patterns
* Not suitable for real financial decision-making

---

## 🔥 Future Improvements

* Add technical indicators (Moving Average, RSI)
* Use GRU or Transformer models
* Hyperparameter tuning
* Multi-feature input (Volume, Open, High, Low)

---

## 💼 Use Cases

* Time-series forecasting
* Financial data analysis
* Deep learning practice project
* Resume / portfolio project

---

## 👨‍💻 Author

## Bhaskar Mandal ##
Data Analyst | Machine Learning Enthusiast

---

## ⭐ If you like this project

Give it a star ⭐ on GitHub and share!

---
