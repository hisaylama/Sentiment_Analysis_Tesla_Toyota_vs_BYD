# Sentiment Analysis of Financial News

This project performs sentiment analysis on financial news headlines for a list of stock tickers. The process involves web scraping, data parsing, sentiment scoring, and visualization. Below is the step-by-step workflow:

---

## Workflow

### 1. **Initialize Required Libraries**
   - Import necessary libraries such as `urllib`, `BeautifulSoup`, `nltk`, `pandas`, `matplotlib`, and `seaborn`.

### 2. **Download VADER Lexicon**
   - Use `nltk` to download the VADER sentiment lexicon, which is required for sentiment analysis.

### 3. **Define List of Stock Tickers**
   - Specify the stock tickers (e.g., `AAPL`, `MSFT`, `GOOGL`, `AMZN`, `TSLA`) for which financial news will be analyzed.

### 4. **Loop Over Each Ticker**
   - For each ticker:
     - Build the Finviz URL.
     - Send an HTTP request with appropriate headers.

### 5. **Fetch and Parse HTML Response**
   - Try to fetch the HTML response from the Finviz website.
   - If successful:
     - Locate the news table using the `news-table` ID.
     - If the news table is found, store it in a dictionary.
   - If an error occurs or no table is found:
     - Print a warning or error message and proceed to the next ticker.

### 6. **Extract News Data**
   - Loop over the rows in each news table:
     - Extract the title, date, and time from each row.
     - If the title exists, append the parsed data (`ticker`, `date`, `time`, `title`) to a list.
     - If row parsing fails, print an error message and proceed to the next row.

### 7. **Create a Pandas DataFrame**
   - Convert the parsed data into a Pandas DataFrame with columns: `ticker`, `date`, `time`, and `title`.

### 8. **Initialize VADER Sentiment Analyzer**
   - Use the VADER sentiment analyzer to score the sentiment of each news headline.

### 9. **Apply Sentiment Analysis**
   - Apply the VADER sentiment analyzer to the `title` column of the DataFrame.
   - Add a new column, `compound`, which contains the sentiment score for each headline.

### 10. **Convert Date Column to DateTime**
   - Convert the `date` column to a proper datetime format, handling any missing or invalid dates.

### 11. **Group Data by Ticker and Date**
   - Group the data by `ticker` and `date`.

### 12. **Compute Mean Compound Sentiment Score**
   - Calculate the mean compound sentiment score for each group.

### 13. **Plot Sentiment Analysis Results**
   - Create a bar chart to visualize the average sentiment scores for each ticker over time.

---

## Output
- A bar chart showing the average compound sentiment score for each stock ticker by date.

---

## Notes
- Ensure that the required libraries are installed before running the script.
- The script uses the Finviz website for scraping news headlines. Ensure compliance with their terms of service.
- Handle missing or invalid data gracefully to avoid runtime errors.

---

## Requirements
- Python 3.x
- Libraries: `nltk`, `pandas`, `numpy`, `matplotlib`, `seaborn`, `BeautifulSoup4`

---

## How to Run
1. Clone the repository.
2. Install the required libraries using `pip install -r requirements.txt`.
3. Run the script using `python main.py`.
4. View the generated bar chart for sentiment analysis results.

---

This ReadMe provides a clear overview of the project and its workflow, making it easier for others to understand and use the code.
