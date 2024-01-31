# Exploring Streaming Twitter Data (Optional)

By the end of this activity, you will be able to:

1. View the text of Twitter data streaming in real-time containing specific words.
2. Create plots of the frequency of streaming Twitter data to see how popular a word is.

NOTE: You must complete the instructions in the Reading Instructions for Creating a Twitter App before you begin this activity.

Step 1. Open a terminal shell. Open a terminal shell by clicking on the square black box on the top left of the screen.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/pYW6JQWREeabsxLXkMIYiw_f85b3afcf7b7a86decd2b0eb43764ecd_click-on-terminal.png?expiry=1706745600000&hmac=0pLx028xMjONEZZGZXSYAbSScaSPUzN3l_BSMm4tems)

Change into the json directory:

```
cd Downloads/big-data-2/json
```

Run ls to see the files:

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/MwPYphZVEea3RQoRNEpMkw_dfee01bfef295b4e2cd5f26168e7e86c_ls.png?expiry=1706745600000&hmac=au_lBh2a1FO7jpX-W5Xlx8JJXn54GwNmPAO04ahoYco)

The auth file must be contain the Twitter access keys and tokens. See the Reading Instructions for Creating a Twitter App for instructions how to create this file.

Step 2. View real-time tweets. We can view the contents of tweets in real-time by running the LiveTweets.py script. Run LiveTweets.py president to see the tweets containing the word president:

```
./LiveTweets.py president
```

The output displays two columns: the first is the timestamp of the tweet, and the second is the text of the tweet.

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/oYQyeRZXEeaHiBKWMgIXbw_8cae3f5265d4438cdc77ec4286376594_live-president.png?expiry=1706745600000&hmac=g6KV5nQm8TOQAd5Ri4Sj5d8f7PreI3WTkp22Kz3XXBM)

When you are done, enter Control-c to stop the script.

Let's run LiveTweets.py time to see the tweets containing the word time:

```
./LiveTweets.py time
```

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/uL5k9BZXEeaEhA5mDe1Caw_5f796f65c4b90196dbe5ff0cb471dd52_live-time.png?expiry=1706745600000&hmac=clKO54KW3z3D8yP1GEVDbnjP3RLlBdSVlS3uaSN_ZCM)

Based on the timestamps, the word time appears more often that president.

Step 3. Plot real-time frequency of tweets. We can create a plot showing the frequency of tweets containing a specific word. Run PlotTweets.py president to create the plot for the word president:

```
./PlotTweets.py president
```

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/puUKiRZYEea3kgpbcREV_w_7426c7f5e68f10c73236763817f9af29_plot-president.png?expiry=1706745600000&hmac=6wkelSpk7p2u4-Xz-LHle4x1fLgve1JDLbG_5g6ting)

In this plot, we can see the variation over time of the number of tweets per second containing the word president. Over this time period, the maximum was 11 tweets per second.

When you are done looking at the plot, click in the terminal window and press enter.

Now let's look at the frequency plot for the word time:

```
./PlotTweets.py time
```

![](https://d3c33hcgiwev3.cloudfront.net/imageAssetProxy.v1/tEy-KhZYEea3kgpbcREV_w_8b1304746b17747674eca0aa1542f74e_plot-time.png?expiry=1706745600000&hmac=kSE884OurlISPBw1aY8t6DiMENGfjUNwEO_Z0YNd_q0)

In this plot, we can see the maximum number of tweets per second containing the word time was about 55, which is much higher than the maximum for the word president.