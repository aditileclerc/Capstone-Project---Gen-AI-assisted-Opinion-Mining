# Capstone-Project---Gen-AI-assisted-Opinion-Mining-for-Financial-Stability-Prediction

**ABSTRACT**

Many individual investors face challenges in accessing timely and relevant investment insights, often missing critical information about a company’s financial stability. Traditional investment models, focused on historical financial data, frequently overlook qualitative factors like public sentiment and market reactions, which significantly influence stock performance. This lack of a blended approach—incorporating both quantitative and qualitative data—has created demand for tools that provide a more comprehensive analysis. Existing financial forecasting tools primarily emphasize structured financial data without effectively integrating real-time sentiment analysis from sources like social media and news. Consequently, investors are often left with incomplete insights into how external factors, like public sentiment, may impact their decisions.

To address these gaps, we propose a solution that utilizes Generative AI and Opinion Mining to enhance financial stability predictions. By combining traditional financial data with real-time sentiment analysis from social media and news sources, our model delivers a holistic view of the factors affecting stock performance. Our Time-Series Transformer Model captures shifts in sentiment and links them with stock price trends, stored in a Vector Database to allow real-time updates and efficient data retrieval. This innovative approach empowers investors by blending sentiment-driven insights with financial indicators, offering a more nuanced understanding of market trends and stock stability. Through the integration of advanced AI and sentiment analysis, our model provides individual investors with actionable, data-driven insights to support more informed investment decisions and opens up new possibilities for financial forecasting in an ever-evolving market landscape.

**Keywords** - Generative AI, Opinion Mining, Financial Stability Prediction, Sentiment Analysis, Time-Series Transformer Model, Stock Price Prediction, Vector Database, Real-Time Financial Forecasting


To predict a company’s financial stability (by analyzing various metrics) using Generative AI and sentiments (curated through opinion mining).

- We will be using a vector database of company data, public sentiments, financial statements to perform opinion mining.
- Based on the sentiments, features will be determined, and the generative model will be built to predict different stability measures, such as stock prices.
- Filling this gap will help from the consumer point of view, for example, when investing in a public company’s shares.

**Progress**

*Step 1: Data Collection*

- Extracting discussions from Reddit and Twitter resulted in irrelevant or noisy data, such as off-topic posts and biased opinions, which may not accurately reflect broader market sentiment.
- Both Reddit and Twitter have rate limits on API requests, restricting the volume of data collected, especially during peak stock market activity.
- Gathering past stock data from Yahoo Finance revealed inconsistencies and gaps in historical data for some companies, complicating accurate comparisons between stock performance and online sentiment.

*Step 2: Data Preprocessing*

Reddit and Twitter Data (Unstructured Text)
- Text Cleaning and Tokenization: Clean out unrelated posts, advertisements, links, and spam. Remove special characters and URLs. Break the text into words or tokens for easier analysis (tokenization).
- Handling Stop Words: Remove common words (e.g., "the", "and", "is") that do not carry sentiment but appear frequently.
- Lemmatization/Stemming: Reduce words to their base or root form (e.g., "running" becomes "run") to group similar words together.
- Remove Noise: Identify and remove posts/tweets that are irrelevant, sarcastic, or misleading to prevent skewed sentiment.
- Handle Duplicate Posts: Eliminate duplicate posts or comments (especially from bots or retweets) to avoid bias in sentiment or opinion trends.

Yahoo Finance Data (Historical Stock Data)
- Data Cleaning: Handle missing or inconsistent values: Stocks may have missing days due to holidays or incomplete trading days, which must be addressed (e.g., forward/backward filling missing data).
- Outlier detection: Identify abnormal fluctuations or errors in the stock data (such as drastic, unexplained drops or spikes)

*Step 3: Opinion Mining*
Sentiment Analysis:
- FinBERT Transformer Model: Analyze sentiment (positive, negative, neutral) from financial-related text.
- Sentiment Labeling: Assign sentiment labels with confidence scores to each post, tweet, or news article.







