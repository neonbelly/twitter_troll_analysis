# Russian Twitter Troll Classification

## Technologies Used:
TwitterScraper: https://github.com/taspinar/twitterscraper/blob/master/twitterscraper/query.py (Data scraping)
Tableau (Visualization)
CountVectorizer and Tfidif Vectorizer (Text Features)
scikit-learn (Modeling)
XGBoost (Modeling)

## Purpose
Classification of troll accounts at either account level or individual tweet level

## Data Sources
Positive Case: FiveThirtyEight Twitter bot data (https://github.com/fivethirtyeight/russian-troll-tweets/)
Negative Case: Scraped tweets from verified users in 2018

# Motivation/Objective
The Russian Internet Research Agency (IRA) deployed "troll" Twitter accounts to misinform the American populace and cause political divides. FiveThirtyEight released 3 million verified tweets from these troll accounts from 2848 accounts for research. These accounts are fully capable of disguising as real accounts as they have a substantial amount of followers and follow other users, retweet Tweets, comment on Tweets, etc. Some troll accounts pose as legitimate news sources and link fake news articles that could miscontrue the truth when a user glances through their social media. Being able to quickly classify these fake accounts from real accounts and accurately removing them before they cause more damage and discord is a pertinent goal for social media sites like Twitter.

# The Data
The content of the tweets are not necessarily the same amongst troll accounts either; FiveThirtyEight was able to identify four types of bot accounts: right-wing, left-wing, newsfeed, fearmongerers, and gamer accounts. I removed non-English tweets to standardize the positive and negative case for comparison. I scraped verified users from 2018 from this article (https://medium.com/@bansalsamarth/this-espn-analyst-comes-closest-to-what-the-median-twitter-verified-user-looks-like-c1818aafc6e7) of a variety of backgrounds (not necessarily only political) in order to best approximate what a standard Twitter feed would look like to the average user. From the user handles in this dataset, I was able to pull past tweets from these users with information such as post date, retweets, links, etc.

When comparing the troll accounts to the verified users, trolls have several distinct behaviors. Troll accounts have an unusually high number of posts and have an unusual amount of accounts that they follow. It is uncommon for an average user who uses Twitter for light social media usage to follow so many accounts and tweet so frequently. Also in the dataset, troll accounts have a tendency to quote tweet, which is a retweet with one's own input added. These bots quote tweet on legitimate account tweets to bring attention to their own content and fake news sources. 

# This part is under construction
