## Stock Data Fetching and Visualization

## Overview
This project is a Python script to fetch stock market data using the Alpha Vantage API and visualize it using Matplotlib and Plotly. The script supports fetching both daily and intraday stock data and provides tools for analyzing and visualizing stock price trends.

## Features
Fetch stock market data (daily or intraday) for a given symbol using the Alpha Vantage API.

Parse and clean the retrieved data into a Pandas DataFrame.

Plot stock closing prices using Matplotlib.

Create interactive candlestick charts using Plotly.

## Prerequisites
Libraries
The following Python libraries are required:

json

requests

pandas

matplotlib

plotly

# API Key
You will need an API key from Alpha Vantage to access the stock market data. Store the API key in a file named key.txt in the following format:

{ "TWITTER_SECRET": "your_alpha_vantage_api_key" }

# Usage
Step 1: Prepare the Environment

Install the required Python libraries if not already installed:

pip install requests pandas matplotlib plotly

Ensure the key.txt file is in the same directory as the script and contains your Alpha Vantage API key.

Step 2: Script Configuration

Update the symbol variable with the stock ticker symbol you want to analyze (e.g., GOOGL for Google).

Update the api_key variable with the name of your API key file (default: key.txt).

Step 3: Run the Script

Run the script using Python:

python script_name.py

Step 4: Visualize the Data

The script will fetch stock data and display it in the console.

A line chart of the stock's closing prices will be shown using Matplotlib.

An interactive candlestick chart will be displayed using Plotly in your web browser.

# Code Explanation
Fetching Data

The fetch_stock_data function retrieves stock data using the Alpha Vantage API. It supports the following:

Symbol: The stock ticker symbol (e.g., GOOGL).

Interval: The time interval for the data (daily or intraday).

Parsing and Cleaning
The fetched JSON data is converted into a Pandas DataFrame for easier analysis and visualization. Columns are renamed for readability, and the index is sorted by date.

#Visualization
Matplotlib Line Chart: A simple line chart to show closing prices over time.

Plotly Candlestick Chart: An interactive candlestick chart displaying open, high, low, and close prices.

#Notes
The script fetches the entire dataset (outputsize=full). For smaller datasets, update the parameter to outputsize=compact.

Ensure the key.txt file contains a valid Alpha Vantage API key to avoid errors.

#Troubleshooting
Invalid API Key: Check the contents of key.txt and ensure the API key is correct.

Unsupported Symbol: Verify the stock ticker symbol is valid and supported by Alpha Vantage.

API Call Limits: Alpha Vantage imposes rate limits on free API keys. Refer to their documentation for details.

Future Improvements
Add support for fetching additional stock metrics.

Implement error handling for network or API issues.

Extend the script to save visualizations as image files.
