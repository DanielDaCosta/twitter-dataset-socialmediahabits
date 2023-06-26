# Stream Data

Tweeter data collected from the API: https://api.twitter.com/2/users/{userid}/tweets

## Data Summary
Total number of tweets: 430k
Total number of users: 889

PROVAX    401
AVAX      329
RANDOM    159

**Timeframe**
Start date: 2023-04-05
Last date: 2023-05-11

**Details**
The file includes a set of new columns that are indicated by the suffix *"_delta_until_next_tweet"*. The column *"target_tweet_id"* refers to the following tweet that the user posted.

For example, "public_metrics_retweet_count_delta_until_next_tweet" represents the number of retweets that a tweet had when the user published the "target_tweet_id".

Please note that every tweet in this dataset includes the metrics it received (likes, retweets, quotes) until the user's subsequent publication. As we only started collecting this data from **'2023-04-05'**, there will be many NaN values in the columns. Therefore, to perform any analysis, we need to filter the dataset. If we filter by this date there is only around 10% of data missing (one of this reason is that maybe the last tweet was posted more than 7 days ago).


## Statistics

If we filter the data by *'current_time' >= 2023-04-05*, we can analyze the percentage of tweets that don't have the columns *_delta_until_next_tweet*:

stream-0-tweets-previous-likes: 0.08003540202757067
stream-1-tweets-previous-likes: 0.022972191557588183
stream-2-tweets-previous-likes: 0.06788511749347259
stream-3-tweets-previous-likes: 0.0588464779501264
stream-4-tweets-previous-likes: 0.04606708656803867
stream-5-tweets-previous-likes: 0.01790369049252298
stream-6-tweets-previous-likes: 0.13942052471291666

# Analysis
