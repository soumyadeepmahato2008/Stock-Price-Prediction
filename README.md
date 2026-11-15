# Stock Price Prediction using Machine Learning

A beginner-friendly machine learning and time-series project that studies historical **Tata Consultancy Services (TCS)** stock prices and predicts the next trading session's closing price using past market data.

This project demonstrates data collection, data cleaning, feature engineering, regression models, and time-series evaluation. It is an educational project, **not financial advice**.

## Project overview

The notebook downloads daily historical TCS data from Yahoo Finance with the `yfinance` library. It prepares the dataset, creates features from previous trading sessions, trains machine learning models, and compares their results with a simple baseline.

### Models

- **Linear Regression** — a simple regression model.
- **Random Forest Regressor** — an ensemble model that can learn non-linear relationships.
- **Previous-close baseline** — assumes the next closing price will equal the latest observed closing price.

### Evaluation metrics

- **MAE (Mean Absolute Error):** average absolute difference between actual and predicted prices.
- **RMSE (Root Mean Squared Error):** penalizes larger prediction errors more strongly.
- **R² score:** indicates how much variation in the test data is explained by the model.

The notebook also visualizes historical closing prices, actual versus predicted prices, and Random Forest feature importance.

## Dataset

| Item | Details |
|---|---|
| Company | Tata Consultancy Services |
| Yahoo Finance ticker | `TCS.NS` |
| Frequency | Daily |
| Start date | 1 January 2019 |
| Data source | Yahoo Finance via `yfinance` |

The dataset is downloaded when the notebook runs, so a separate CSV file is not required. Data availability depends on Yahoo Finance and your internet connection.

## Repository structure

```text
Stock-Price-Prediction/
├── Stock_Price_Prediction_TCS.ipynb
├── requirements.txt
├── README.md
└── .gitignore
```

## Requirements

- Python 3.9 or later
- Internet connection
- Jupyter Notebook or JupyterLab

## Installation and usage

### 1. Clone the repository

```bash
git clone https://github.com/soumyadeepmahato2008/Stock-Price-Prediction.git
cd Stock-Price-Prediction
```

### 2. Create a virtual environment (recommended)

**Windows PowerShell:**

```powershell
py -m venv .venv
.\.venv\Scripts\Activate.ps1
```

**Windows Command Prompt:**

```cmd
py -m venv .venv
.venv\Scripts\activate.bat
```

**macOS / Linux:**

```bash
python3 -m venv .venv
source .venv/bin/activate
```

### 3. Install the dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Launch Jupyter Notebook

```bash
jupyter notebook
```

Open `Stock_Price_Prediction_TCS.ipynb` and execute the cells in order, from top to bottom.

## Workflow

1. Import the required Python libraries.
2. Download historical TCS stock data.
3. Inspect and clean the dataset.
4. Plot the historical closing price.
5. Create lag features, rolling averages, daily returns, and volume-based features.
6. Set the next observed trading session's closing price as the prediction target.
7. Split the data chronologically into training and testing sets (80% / 20%).
8. Train Linear Regression and Random Forest models.
9. Compare model predictions with the previous-close baseline.
10. Evaluate the models and visualize the results.

## Limitations and responsible use

- This is an educational machine learning project, not an investment tool or financial advice.
- Stock prices are affected by many unpredictable factors. Historical patterns do not guarantee future performance.
- The data is split in chronological order to respect time-series structure; observations are not randomly shuffled.
- Any next-session estimate is experimental and may be inaccurate.
- Yahoo Finance data may be revised, delayed, or temporarily unavailable. Results can change when the notebook is run on a different date.
- Performance on TCS does not guarantee similar performance on other stocks.

## Ideas for further improvement

- Add walk-forward validation.
- Experiment with additional models such as Support Vector Regression or gradient boosting.
- Include more technical indicators and compare against a market index.
- Test the workflow on other stock tickers.
- Explore dedicated time-series methods such as ARIMA.

## Author

**Soumyadeep Mahato**  
GitHub: [@soumyadeepmahato2008](https://github.com/soumyadeepmahato2008)

## License

No license has been specified. Unless a license is added, the repository remains subject to the default copyright restrictions.
