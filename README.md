# Reddit Economy Analysis
This program scrapes Reddit data and Federal Reserve Economic Data (FRED) and investigates possible correlation.

The [Federal Reserve Bank of St. Louis](https://fred.stlouisfed.org/) and [Reddit](https://www.reddit.com/r/Economics/) both provide APIs for accessing their data. The St. Louis API is used to get employment data across time, and the Reddit API is used to gather posts from r/Economics that include "unemploy" in their title. Using the VaderSentiment library, the program assigns each Reddit post a "sentiment score", classifying the post as positive or negative. It then calculates the average sentiment of each month in the dataset. Then the data from both APIs are merged into a single data frame. To make comparison possible, the employment rate and sentiment scores are converted to Z-scores.

Finally, the employment rate and Reddit sentiment are graphed together and their correlation is calculated. The surprising result is that there is no correlation. Their Pearson correlation score is -0.0467.
