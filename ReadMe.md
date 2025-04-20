# Sentiment Analysis from Financial News data for BYD, Toyota and Tesla

This project performs sentiment analysis on financial news headlines for a list of stock tickers (BYD, TM and TSLA). 

# Description
- **Data Source:**
    - News headlines are scraped from [Finviz](https://finviz.com/), a popular financial news and stock screener platform.
    -  **Key Libraries Used:**
    - `BeautifulSoup`: For parsing and extracting news headlines from HTML (web scraping).
    - `urllib.request.Request`: For making HTTP requests to retrieve webpage content.
    - `nltk (VADER)`: For performing sentiment analysis on news headlines.
- **Output:**
Generates visualizations that show sentiment score patterns over time for selected tech company stocks using heatmaps, and interactive line plots.

- **Methodoloy**
  - Import important libraries
  - Scrape News Headlines from Finviz
  - Parse News Headlines and Build DataFrame
  - Perform Sentiment Analysis and Prepare Data
  - Visualize Sentiment Analysis Results

# Requirements
``` beautifulsoup4  
    nltk  
    numpy  
    matplotlib  
    pandas  
    urllib3  
```
Install them via: 
```
pip install beautifulsoup4 nltk numpy matplotlib pandas urllib3

```
# Usage
Check out the [tutorial](https://nbviewer.org/github/hisaylama/Sentiment_Analysis_Tesla_Toyota_vs_BYD/blob/main/tutorial_play.ipynb) to visualise the data.

# License
This project is licensed under the `MIT License`. Feel free to use, modify, and distribute the content with attribution.


