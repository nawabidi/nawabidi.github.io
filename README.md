# Bidita's Portfolio
Welcome to my GitHub Pages Portfolio! I’m Bidita, an Economics-Mathematics major at Whitman College, expected to graduate in May 2025.

## About Me
I'm passionate about data analysis and financial consulting. This is my [Linkedin](https://www.linkedin.com/in/biditanawar/)

## Skills
- Programming: Python, R
- Data Visualization: Tableau, Power BI, ggplot2, Matplotlib

# Political Market Volatility 

## Market Movements and Election Day: Analyzing Stock Price Volatility in the U.S. Presidential Election Days
## Authors: Bidita and Pure
## [Link to my code](https://colab.research.google.com/drive/1OXswCV-9xePKnib8qQQutd4Qlz_taD8k?usp=sharing)

## Introduction:
This project examines stock price volatility for the S&P 500, Dow Jones Industrial Average (DJI), and Nasdaq Composite during U.S. presidential elections, focusing specifically on the changes in closing prices from October to November of each election year. Using historical data from Yahoo Finance and election dates, we analyze stock market behavior during these pivotal moments. Instead of paying $20 to access and download the data, we copied and pasted the data directly into Excel and downloaded it into a CSV file. Fortunately, there were no missing cells and the data was complete. However, there were some minor issues when we tried to clean the data and convert the data to the datetime format. It filtered out some parts of the data and probably got confused with the other relevant column, e.g., volume. Later on, we figured out a way to fix it using column selections by choosing only the Date and Close columns instead, we then had the clean data in the right format for the visualizations.
During the election periods, the stock market is always hard to predict how the investors react in regards to the election polls, the uncertainty of the future policies between the two opposing parties, and economic forecasts from the news. Hence, we want to analyze the volatility of the stock market and observe the movement through the visualization, seeking to answer the question: How volatile is the stock market during these swinging times of the year? By isolating election-specific data, we calculate the percentage change in closing prices to identify patterns of volatility and market reaction. The visualizations include line graphs highlighting the overall trends in stock prices over the period of time for which data is collected and bar graphs showcasing the percentage change in stock prices during each election year. The bars are color-coded to reflect political affiliation, with blue bars representing Democratic terms and red bars representing Republican terms. This provides additional context to assess the relationship between political leadership and market trends.This approach offers a focused perspective on how elections influence short-term market performance, revealing insights into the interplay between political events and financial market stability.

## Methods & Results
## Data Preparation
The dataset included closing prices and dates, which were prepared for analysis by converting the Date column to datetime format and cleaning the Close column to remove commas and convert values into numeric format. It is highly recommended to open the CSV file on Excel and click save once, then close the tab and reopen it again. By that, Excel will automatically format the Date column on the CSV file that would work perfectly with the datetime format. The Date column was then set as the index, enabling efficient time-series operations such as filtering by year and month. The date format conversion has to be done carefully during the data cleaning process and checked regularly to make sure that the conversion does not filter out some portion of the full dataset that could distort the visualizations.

## Analysis
We analyzed the percentage change in S&P 500 closing prices between October and November during U.S. presidential election years. For each election year, the last closing prices of October and November were identified, and the percentage change was calculated using:

Percent Change = (November Closing Price − October Closing Price) /October Closing Price × 100

The changes were visualized using matplotlib, with purple (cool tone) showing positive changes and yellow/orange (hot tone) showing negative ones. A reference line at 0% was added to indicate no change.

## Results

### S&P 500

The line plot gives an overview of the stock market in terms of its closing price from 1985 to 2024 to give a sense of how the market has changed over time overall. This is showing a consistent long-term upward trend. From 1985 to 2000, the market experienced steady growth with occasional minor dips. A significant downturn is visible around 2008, corresponding to the global financial crisis, followed by a recovery phase. Since 2020, there has been a notable surge, reflecting strong post-COVID-19 market recovery and growth in key sectors like technology. Overall, the chart highlights the stock market's resilience and sustained growth over the decades.

![image](https://github.com/user-attachments/assets/f7d97941-f106-43ec-b856-6343bc18158d)

The bar chart revealed how the market behaved during election years, with purple bars showing market growth and yellow bars indicating decline from October to November. The graph contains the presidential terms from 1988 to 2024. Positive changes are highlighted during the elections of Clinton (1992, 1996), Bush (2004), Trump (2016), and Biden (2020), indicating market gains during these periods. Negative changes are seen during Bush's reelection (2000) and Obama's first election (2008), reflecting market downturns tied to economic uncertainty or crisis. The data suggest that market performance during election years can vary significantly depending on broader economic conditions 

{% include_relative fig1.html %}

The bars also provide further details when hovered on with the year, percentage change, and the presidential term. Positive changes occurred after the elections of Clinton (1992, 1996), Bush (2004), Trump (2016), and Biden (2020), indicating market confidence. Conversely, negative changes followed Bush's reelection (2000) and Obama's first term (2008), reflecting economic uncertainty or ongoing crises. The market often responds differently after elections based on the outcome and prevailing economic conditions. For instance, significant positive shifts, such as Biden in 2020, may reflect optimism about recovery strategies, while declines, like in 2008, indicate responses to broader financial instability.

{% include_relative fig2.html %}

### DOW Jones 

The graph shows the Dow Jones Industrial Average's closing prices over time, highlighting long-term growth with periods of volatility. From the early 1990s to the early 2000s, the index experienced steady growth, followed by a dip during the dot-com bubble burst. A significant drop is visible around 2008 due to the global financial crisis, after which the index steadily recovered. Post-2016, there is a sharp upward trajectory, with notable growth following the 2020 pandemic recovery. The overall trend demonstrates resilience and long-term upward movement despite periodic economic downturns.

![image](https://github.com/user-attachments/assets/ee6c86b1-2662-4010-9521-485134b1953a)

Positive percent changes are observed after Clinton's elections in 1992 and 1996, Bush's reelection in 2004, Trump's election in 2016, and Biden's election in 2020, reflecting market optimism. Negative changes occurred after Bush's election in 2000 and Obama's election in 2008, highlighting market concerns during periods of economic uncertainty. The data suggests that the DJIA's performance varies based on prevailing economic conditions and election outcomes.

{% include_relative fig3.html %}

Positive changes are evident after Bush's elections in 2000 and 2004, Trump's election in 2016, and Biden's election in 2020, reflecting strong market confidence during these transitions. However, negative or minimal changes occurred during Clinton's elections in 1992 and 1996 and Obama's elections in 2008 and 2012, indicating less optimistic market responses during those periods. The changes demonstrate that the DJI's performance post-election varies depending on market sentiment and prevailing economic conditions.

{% include_relative fig4.html %}

### NASDAQ

The graph shows the NASDAQ's closing prices over time, illustrating significant long-term growth. The sharp rise around 2000 reflects the dot-com bubble, followed by a steep decline as the bubble burst. After a period of recovery, another drop occurred during the 2008 financial crisis. From 2010 onward, the index shows a strong upward trajectory, particularly post-2015, driven by rapid growth in technology and innovation sectors. The surge after 2020 highlights recovery and expansion following the COVID-19 pandemic. Overall, the NASDAQ demonstrates resilience and exceptional growth, largely fueled by tech industry performance.

![image](https://github.com/user-attachments/assets/d7796d85-740d-4b3c-8f26-c86e887bdab5)

The chart shows the percent change in the NASDAQ from October to November during U.S. presidential election years. Positive changes are observed after Clinton's elections in 1992 and 1996, Bush's reelection in 2004, Trump's election in 2020, and Biden's election in 2020, indicating market optimism during these periods. Notably, there were significant negative changes after Bush's election in 2000 and Obama's election in 2008, reflecting market concerns during economic downturns or crises. The data highlights the NASDAQ's sensitivity to economic and political conditions surrounding elections.

{% include_relative fig5.html %}

Positive percent changes are observed after Bush's elections in 1988 and 2004, Clinton's reelection in 1996, and Biden's election in 2020, suggesting post-election market optimism. Minimal or negative changes occurred after Clinton's first election in 1992, Bush's election in 2000, and Trump's election in 2016. These variations reflect how market reactions differ based on election outcomes and prevailing economic conditions at the time.

{% include_relative fig6.html %}


## Above & Beyond
For our above and beyond, we decided to explore further how the volatility changed a month after elections to see the shift of market sentiment. This gives us perspective of how the investors perceived the election results and reacted to the president elect. This way we also concluded that political parties (e.g republican, democratic, etc.) have no significant influence on the volatility of the stock prices. rather other factors may also influence. 

## Conclusions 
Market Behavior During Elections:
The analysis revealed significant variations in stock price changes across different election years, suggesting that elections can influence short-term market performance.
While some years exhibited positive changes, others showed declines, reflecting differing market sentiments and responses to political transitions. The graph consists of all types of bars: big positive change, significant decline, almost to little or no change. This is attributed to many factors; e.g. the tightness of election polls, if the election results are not tight and easy to predict the winner, the market might not have high volatility. The significant decline might also not result from the election, but rather economic crisis. However, most of the bars reflect the big positive changes, which suggest that the market tends to be very active and show that the election does motivate the investors to jump in and make an investment in a variety of sectors hoping for the changes made by the policies as advertised during the election campaigns.

## Political Context and Market Trends:
By color-coding bar graphs based on party affiliation, we didn’t observe any pattern linking political party and market performance. Other factors, such as economic conditions or global events, play a more substantial role in influencing stock prices, election periods may have a short term effect on the volatility of prices. 

## Limitations and Areas for Further Study
We only accounted for the data from October to November and defined these two months to be the election periods. However, we did not get specific on the date of the unofficial results day that is typically the second Tuesday of November. So, it might not thoroughly reflect the market sentiment before and after the election results. 

Additionally, external factors with significant influence on the stock market, such as economic crises, geopolitical events, or monetary policy decisions, were not accounted for in this study. As these external influences were not isolated, the bar in the graph might not reflect the volatility that arises from the election alone,  but rather results from other confounding factors instead.

If we were to explore the study further, we would address such limitations by incorporating the economic indicator such as GDP growth rate during election periods. Including this metric, it would help isolate market movements driven by economic fundamentals from those influenced by elections, driving a more relevant result to the question of interest. Furthermore, we could also explore sector-specific stock indices to determine how different industries respond to elections. For example, industries that are likely to be volatile to the government policies, such as healthcare or renewable energy, may exhibit more pronounced reactions compared to less regulated sectors.	


## References
Yahoo Finance. (n.d.). S&P 500 Historical Data. Retrieved from https://finance.yahoo.com/quote/%5EGSPC/history/ Encyclopedia Britannica. (n.d.). 

Presidents of the United States. Retrieved from https://www.britannica.com/topic/Presidents-of-the-United-States-1846696
  




