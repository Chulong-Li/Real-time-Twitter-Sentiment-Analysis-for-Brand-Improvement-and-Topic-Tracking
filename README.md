# Twitter Sentiment Analysis for Brand Improvement
Dive into the industry and get my hands dirty.

## Inspiration
The solution for evaluating Twitter data to perform better business decisions is to keep tracking all relevant Twitter content about a brand in real-time and perform analysis as topics or issues emerge. By monitoring brand mentions on Twitter, brands could inform enagement and deliver better experiences for their customers across the world.

## Interesting facts from exploratory data analysis
- Less 0.01% users will push tweets with their locations.
- Tweets grabbed from streaming data won't have more than 0 LIKE or RETWEET, since you have already captured them even before others press buttons :p
- More than 65.6% users will write the locations in their profile, although very few of them don't live on Earth according to that fact.
- The numbers of positive and negative tweets are relatively close and stay low compared with neural tweet number. Unless emergency events happen, lines won't fluctuate acutely.

## Technical Approach v1 (~ Aug 15)
1. Extract streaming Twitter Data, preprocess data in Python, and load data into MySQL for storage
2. Perform exploratory data analysis with Seaborn to explore the insights
3. Connect with Plotly & Dash for real-time interactive front-end web app based on time series (In Progress)
4. Publish the visualization on github.io (In Progress)

## Next Version v2 ( ~ Aug 22)
Build ETL pipelines based on stream processing using Kafka, and perform sentiment analysis using Spark Streaming

## Quick Demo 

### Sentiment Tracking on Airbnb Brand
<img src="https://github.com/Chulong-Li/Twitter-Data-Sentiment-Analysis/blob/master/demo" alt="Sentiment Tracking" width="100%" height="100%">

### Tracking hot topic trends
<img src="https://github.com/Chulong-Li/Twitter-Data-Sentiment-Analysis/blob/master/Figures/LineChart.png" alt="LineChart" width="1000" height="600">
<img src="https://github.com/Chulong-Li/Twitter-Data-Sentiment-Analysis/blob/master/Figures/FreqDist.png" alt="FreqDist" width="1000" height="600">
<img src="https://github.com/Chulong-Li/Twitter-Data-Sentiment-Analysis/blob/master/Figures/GeoDist.png" alt="GeoDist" width="90%" height="90%">
## Get Started
### Pre-installation
```
pip install -r requirements.txt
```
### Set-up
Create a file called ```credentials.py``` and fill in the following content
```
# Go to http://apps.twitter.com and create an app.
# The consumer key and secret will be generated for you
API_KEY = "XXXXXXXXXXXXXX"
API_SECRET_KEY = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"

# After the step above, you will be redirected to your app's page.
# Create an access token under the the "Your access token" section
ACCESS_TOEKN = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
ACCESS_TOKEN_SECRET = "XXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXXX"
```

Create local MySQL Database with info below
```
host="localhost"
user="root"
passwd="password"
database_table="TwitterDB\"
```
### Run
Run ```Main.ipynb``` to start scraping data on Jupter Notebook. 

Run ```Analysis.ipynb``` to perform data analysis for brand improvement.

Run ```Analysis_for_Topic_Trend.ipynb``` to track hottest topic trends on Twitter

Note: Since streaming process is always on, press STOP button to finsih.

## What's next?
In the future, I'll write a tech blog on Towards Data Science to elaborate details under the hood. So stay tuned.
