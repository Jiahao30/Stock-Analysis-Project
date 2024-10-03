# S&P500 Stock Analysis Project

![Python](https://img.shields.io/badge/Python-FFD43B?style=for-the-badge&logo=python&logoColor=blue)
![Pandas](https://img.shields.io/badge/Pandas-2C2D72?style=for-the-badge&logo=pandas&logoColor=white)
![Numpy](https://img.shields.io/badge/Numpy-777BB4?style=for-the-badge&logo=numpy&logoColor=white)
![Plotly](https://img.shields.io/badge/Plotly-239120?style=for-the-badge&logo=plotly&logoColor=white)
![Microsoft Excel](https://img.shields.io/badge/Microsoft_Excel-217346?style=for-the-badge&logo=microsoft-excel&logoColor=white)
![Kaggle](https://img.shields.io/badge/Kaggle-20BEFF?style=for-the-badge&logo=Kaggle&logoColor=white)
![GitHub](https://img.shields.io/badge/github-%23121011.svg?style=for-the-badge&logo=github&logoColor=white)

## Project Overview
This project aims to conduct an in-depth analysis of the stock prices of companies listed in the S&P 500 index, focusing on four major technology companies as examples: **Apple (AAPL)**, **Amazon (AMZN)**, **Google (GOOG)**, and **Microsoft (MSFT)**. The objective is to understand long-term trends in stock prices, calculate moving averages, and analyse the correlation between price movements.

## Project Structure

    ├── LICENSE
    ├── README.md                             <- README.
    ├── data_resources
    │   │
    │   ├── sp500_stocks.csv                  <- Information for each one of the stocks that compose de S&P 500 index.
    │   ├── sp500_index.csv                   <- S&P index value from 2014 to date.
    │   └── sp500_companies.csv               <- Company metadata for S&P 500 companies.
    │ 
    └── S&P500_Stock_Analysis.ipynb           <- Code of the analysis.

### Problem Description

This project aims to analyse the stock price movements over the past decade, using four major technology companies from the S&P 500 index as example — *Apple, Amazon, Google, and Microsoft*. The objective is to identify trends, patterns, and correlations in their stock performance through various statistical and visualisation techniques. By applying time series analysis, moving averages, and correlation analysis, the project seeks to uncover insights into the long-term growth, short-term volatility, and inter-company relationships that could help investors and analysts make informed decisions about these technology giants.

### Dataset Information

The Standard and Poor's 500 or S&P 500 is the most famous financial benchmark in the world.

This project primarily utilises the [sp500_stocks.csv](https://www.kaggle.com/datasets/andrewmvd/sp-500-stocks/data?select=sp500_stocks.csv) dataset for analysis, which contains stock data for 503 listed companies in the S&P 500 index, spanning from 2010 to the present, amounting to over 1.86 million rows. Additionally, the `sp500_index.csv` and `sp500_companies.csv` datasets are used to supplement the main data with information on the S&P 500 index and specific company details. The key attributes of the main dataset include:

- **Date:** Date.
- **Symbol:** Company Symbol/Ticker.
- **Adj Close:** Similar to the price at market closure, yet also takes into account company actions such as dividends and splits.
- **Close:** Price at market closure..
- **High:** Maximum value of period.
- **Low:** Minimum value of period.
- **Open:** Price at market opening.
- **Volume:** Volume traded.

### Project Workflow
**1. Data Collection**
- The dataset includes stock data for 503 companies from the S&P 500 index, focusing on Apple, Amazon, Google, and Microsoft. The dataset was loaded and cleaned, ensuring no missing values, and data types were converted where necessary (e.g., date to datetime format).

**2. Stock Price Trends**
- The stock prices of the selected companies were plotted over time to visually inspect price movements. Subplots were created to display individual stock trends over the selected period (from 2010 to 2024). The analysis demonstrated steady upward trends in all four companies’ stock prices, with notable peaks and troughs representing periods of market volatility.

**3. Moving Average Calculations**
- The project calculated simple moving averages (SMA) for different window sizes (10-day, 20-day, and 50-day) to smooth out stock price fluctuations and identify longer-term trends. Moving averages for all four companies were plotted, showing consistent growth with minor fluctuations, reflecting overall positive trends in the tech sector.

**4. Stock Price Change and Daily Returns**
- Daily percentage price changes were calculated for each stock to analyse daily volatility. Line plots were generated to visualise the daily returns for each company, highlighting periods of high volatility and stable growth. The analysis identified various periods of significant price changes, especially during events like market corrections or economic downturns.

**5. Resampling Data**
- Resampling techniques were applied to better understand stock price trends on different time scales (monthly, quarterly, and yearly). These resampled plots provided insights into longer-term trends and helped smooth out daily noise. The quarterly and yearly resampling showed substantial growth in stock prices for all companies, particularly after 2020.

**6. Correlation Analysis of Closing Prices**
- A correlation matrix was created to analyse the relationships between the closing prices of the selected companies. The matrix indicated strong positive correlations between all four companies, with the highest correlations seen between Microsoft and Apple. A heatmap visualisation further illustrated these correlations, confirming that these tech giants often move in tandem due to their similar market drivers.

**7. Daily Return Correlation Analysis**
- The percentage changes in daily closing prices were also correlated to evaluate the relationship between daily returns for the four companies. The results showed moderate to strong correlations between daily percentage changes, indicating that the tech sector’s daily price movements are somewhat synchronised. Pairwise scatter plots were generated to visualise these relationships, highlighting similar trends in daily price movements across the companies.

### Conclusion
This project effectively analysed stock price movements for major tech companies in the S&P 500 index. By calculating moving averages, analysing daily returns, and performing correlation analysis, the project provided valuable insights into the trends and relationships in the stock prices of Apple, Amazon, Google, and Microsoft. The strong correlations between these stocks reflect the interconnected nature of the tech industry and its market trends.

## Improvement
In this project, I have introduced several improvements and innovations beyond the original tutorial, enhancing both the depth and accuracy of the analysis:

**1.	Extended Time Frame with Real-Time Updated Data:**
- While the original tutorial only utilised data from 2013 to 2018, I worked with a dataset spanning from 2010 to the present. This extended time frame, coupled with real-time updated data, provided a more comprehensive view of stock performance and market trends. The inclusion of more recent data enabled me to derive deeper insights and identify long-term trends that were previously inaccessible in the original analysis.

**2.	Code Error Corrections and Enhancements:**
- **Accurate Moving Average Calculations:** In the original tutorial, there was an issue when setting up the moving average windows. The tutorial did not account for different stocks when setting the window size, leading to anomalies in the moving average charts. I corrected this by using the **groupby and transform functions** to ensure the window size was applied correctly for each stock. This adjustment allowed for the generation of accurate moving average trend charts, reflecting the true price movements of each individual stock.
- **Correct Handling of Missing Values in PairGrid Plot:** Another significant issue in the tutorial was the treatment of missing values when plotting the PairGrid. The original code reset the index for the four stocks without addressing the impact of missing values, which resulted in incorrect relationship plots. To rectify this, I **used the ‘Date’ column as the index**, ensuring a consistent time series alignment across all stocks. This adjustment allowed for an accurate analysis of the relationships between the stocks, eliminating any discrepancies caused by missing values and ensuring the integrity of the correlation analysis between the four stocks.

These improvements not only addressed existing issues in the tutorial but also enhanced the overall accuracy and comprehensiveness of the project. By expanding the time frame and correcting technical errors, I was able to produce more reliable and insightful analysis outcomes.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) for details.

## Acknowledgements
This project is an adaptation of the concepts and methodologies taught by [Shan Singh](https://www.udemy.com/user/shantanu-singh-54/) on Udemy. Special thanks to Shan Singh for their guidance and instructional videos.

### Original Tutorial
[Data Analytics Real-World Projects in Python](https://www.udemy.com/course/data-analytics-projects-python/)

### Disclaimer
Please note that this project is an adaptation of the concepts and methodologies taught by Shan Singh. Any code, data, or content not directly from Shan Singh is original work created for this project and is covered under the MIT License.

## Contact Me!
For any questions or feedback regarding this project, feel free to reach out:
- Email: jiahao.shao30@gmail.com
- LinkedIn: <b>[Jasper Shao](https://www.linkedin.com/in/jasper-shao/)</b>
- GitHub: <b>[Jasper Shao](https://github.com/Jiahao30)</b>
