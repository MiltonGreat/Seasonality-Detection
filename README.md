# Stock Market Seasonality Detection

## Overview

This project aims to identify and analyze seasonal patterns in stock market prices by applying Fourier Transform and Wavelet Analysis techniques. These methods help detect cyclic behavior in stock prices over time, providing insights into potential periodic trends that can inform trading strategies.

### Objective

The primary goal of this project is to detect cycles or seasonality in stock price data using advanced mathematical methods, specifically Fourier Transform and Wavelet Analysis. By identifying dominant cycles and their strengths, we can assess whether the stock exhibits meaningful periodic behavior.

### Dataset

The analysis focuses on Apple Inc. (AAPL) stock data, specifically its Adjusted Close price, which is adjusted for splits and dividends. The dataset includes the following columns:

- Ticker: Stock symbol (e.g., AAPL)
- Date: Date of the stock price
- Open: Opening price for the day
- High: Highest price for the day
- Low: Lowest price for the day
- Close: Closing price for the day
- Adj Close: Adjusted closing price (used in the analysis)
- Volume: Number of shares traded
### Key Methods

1. Fourier Transform (FFT)

Fourier Transform is used to analyze the frequency spectrum of stock price data. This method allows the detection of dominant frequencies or cycles in the price series. By identifying the frequency with the most energy, we can estimate the dominant cycle length (in days).

2. STL Decomposition

The STL (Seasonal and Trend decomposition using Loess) is used to decompose the time series into three components:

- Trend: The underlying long-term movement.
- Seasonal: The repeating cycle component.
- Residual: The noise or random variation.

STL helps validate and cross-check the seasonality detected using Fourier Transform, providing additional confidence in the analysis.

### Outputs

When you run the detect_seasonality function, it will:

- Detect the dominant seasonal cycle for the stock price.
- Measure the strength of the cycle.
- Provide a verdict on whether the cycle is statistically significant.

Additionally, if visualize=True, the function will generate three plots:

1. Price and Seasonal Component: A plot comparing the stock prices with the seasonal component obtained from STL decomposition.

2. Frequency Spectrum: A plot of the frequency spectrum from the Fourier Transform, showing the dominant cycle.

3. Autocorrelation: A plot of the autocorrelation of the price series, highlighting repeating patterns over time.

### Interpretation

- Dominant Cycle: The detected length of the most prominent cycle in the stock prices (in days).
- Strength: The proportion of the total price movement explained by the detected cycle.
- Significant: A boolean indicating whether the cycle is statistically significant (based on predefined criteria like cycle strength and validity).

This output indicates that the most dominant cycle lasts for 2246 days, but its strength is 36.7%, and it is not statistically significant (meaning that while the cycle exists, it might not be reliable for trading decisions).

### Conclusion

This project enables the detection of seasonality in stock market data using advanced techniques such as Fourier Transform and STL decomposition. While the analysis identifies potential cycles, it is essential to validate the results and interpret them within the context of the stock's historical data and market conditions.

### Source

![S&P 500 Stock Data From Listing Day to 2023 from Kaggle](https://www.kaggle.com/datasets/pavankrishnanarne/s-and-p-500-stock-data-from-listing-day-to-2023)
