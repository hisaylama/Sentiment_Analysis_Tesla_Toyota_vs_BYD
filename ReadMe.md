# Sentiment Analysis from Financial News data for BYD and Tesla

This project performs sentiment analysis on financial news headlines for a list of stock tickers. The process involves web scraping, data parsing, sentiment scoring, and visualization. 

- **Data Source:**
- News headlines are scraped from [Finviz](https://finviz.com/), a popular financial news and stock screener platform.
  
- **Key Libraries Used:**
  - `BeautifulSoup`: For parsing and extracting news headlines from HTML (web scraping).
  - `urllib.request.Request`: For making HTTP requests to retrieve webpage content.
  - `nltk (VADER)`: For performing sentiment analysis on news headlines.
    
- **Notebook Outcome:**
Generates visualizations that show sentiment score patterns over time for selected tech company stocks using heatmaps, and interactive line plots.

- **Methodoloy**
  - Import important libraries
  - Scrape News Headlines from Finviz
  - Parse News Headlines and Build DataFrame
  - Perform Sentiment Analysis and Prepare Data
  - Visualize Sentiment Analysis Results
