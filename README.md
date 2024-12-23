# stock_price_prediction
Stock Price Prediction

# Table of Contents

1. [Stock Market Price Estimation](#stock-market-price-estimation)
2. [Data Collection](#data-collection)
3. [Installation](#installation)
4. [Usage](#usage)
5. [Data](#data)
6. [Model](#model)
7. [Deployment](#deployment)
8. [License](#license)
9. [Acknowledgements](#acknowledgements)


## Stock Market Price Estimation

Stock market price estimation is a crucial aspect of financial analysis that impacts investors, companies, and analysts alike. The goal is to achieve accurate and reliable results to guide decision-making and minimize risks.

Inaccurate estimations can lead to:

- **Investor Losses:** Misleading predictions may cause poor investment decisions.
- **Market Panic:** Overly pessimistic forecasts can trigger unnecessary sell-offs.
- **Reputational Risk:** Financial institutions or analysts may lose credibility.

My aim is to analyze stock market price data for Google, Meta, Apple, and NVIDIA between October 30, 2021, and October 30, 2024, and provide an estimator while deploying my model both locally and to the cloud.

## [Data Collection](https://github.com/f-kuzey-edes-huyal/stock_price_prediction/blob/main/downloading_relevant_data.ipynb)

I used the [ ```yfinance```](https://github.com/ranaroussi/yfinance/tree/main?tab=readme-ov-file) library to download stock market price data for four companies—Google, Meta, Apple, and NVIDIA—from October 30, 2021, to October 30, 2024. The yfinance library is a Python tool for accessing historical market data, financial metrics, and company information from [Yahoo!Ⓡ finance](https://finance.yahoo.com/).

You can download the data in two steps as outlined below:


1) Specify the companies.

```tickers = ['GOOGL', 'META', 'AAPL', 'NVDA']```

2) Decide on the start and end dates, then download the data.

```stock_data = yf.download(tickers, start="2021-10-30", end="2024-10-30", group_by="ticker")```



 " ```yfinance``` is not affiliated, endorsed, or vetted by Yahoo, Inc. It's an open-source tool that uses Yahoo's publicly available APIs, and is intended for research and educational purposes. You should refer to Yahoo!'s terms of use ([here](https://legal.yahoo.com/us/en/yahoo/terms/product-atos/apiforydn/index.html), [here](https://legal.yahoo.com/us/en/yahoo/terms/otos/index.html), and [here](https://policies.yahoo.com/us/en/yahoo/terms/index.htm)) for details on your rights to use the actual data downloaded."



## Stock Price Dataset Description

This dataset contains daily stock price information, which is useful for analyzing stock performance, predicting trends, or conducting financial research.

| **Column Name** | **Description**                                                                                         |
|------------------|-------------------------------------------------------------------------------------------------------|
| **Date**         | The date of the record in the format `YYYY-MM-DD`.                                                   |
| **Open**         | The stock's opening price at the start of the trading day.                                           |
| **High**         | The highest price the stock reached during the trading day.                                          |
| **Low**          | The lowest price the stock fell to during the trading day.                                           |
| **Close**        | The stock's closing price at the end of the trading day.                                             |
| **Adj Close**    | The closing price adjusted for corporate actions like stock splits, dividends, and rights offerings. |
| **Volume**       | The total number of shares traded during the trading day. This reflects market activity and liquidity.|


## Installation

```git clone https://github.com/f-kuzey-edes-huyal/stock_price_prediction.git```

__To-Do List:__

- Find a way to efficiently dockerize the TensorFlow model.
- Evaluate the Docker image.
- Get a smaller image and try AWS deployment before meeting with AJ!
