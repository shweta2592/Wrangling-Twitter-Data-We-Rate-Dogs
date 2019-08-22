# Wrangling-Twitter-Data-We-Rate-Dogs

<h3>In Progress</h3>

<h3> Introduction </h3>

This project is a part of Udacity's curriculum on Data Wrangling using Twitter's API.The dataset used to wrangle is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. And the numerators almost always greater than 10, because "they're good dogs Brent." The tweet archive records using in this project contains basic tweet data (tweet ID, timestamp, text, etc.)

<h3>Tools Used</h3>  Python<br>

<h3>Project Steps:</h3>
1. Gather Data<br>
2. Assess Data<br>
3. Clean Data<br>
4. Storing<br>
5. Analyzing <br>
6. Visualizing <br>

<h4>Data Gathering</h4>
<b>twitter_archive:</b> The WeRateDogs Twitter archive, which is provides by the Udacity Course and we use pd.read_csv() to import them into dataframe.<br>
<b>image_predictions:</b> The tweet image predictions, i.e., what breed of dog (or other objects, animal, etc.) is present in each tweet according to a neural network. This file ('image_predictions.tsv') is hosted on Udacity's servers and downloaded programmatically using the requests library and the provided url.<br>
<b>tweet_data:</b> Using the tweet IDs in the WeRateDogs Twitter archive, query the Twitter API for each tweet's JSON data using Python's Tweepy library and store each tweet's entire set of JSON data in a file called 'tweet_json.txt' file. Each tweet's JSON data is written to its own line. <br>

<b>Steps to be continued since project is still in progress.
