# Wrangling-Twitter-Data-We-Rate-Dogs

<h3>In Progress</h3>

<h3> Introduction </h3>

This project is a part of Udacity's curriculum on Data Wrangling, web scraping using Twitter's API.The dataset used to wrangle is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. And the numerators almost always greater than 10, because "they're good dogs Brent." The tweet archive records using in this project contains basic tweet data (tweet ID, timestamp, text, etc.)

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
<h4> Data Assessing </h4><br>
<b>Quality</b>
Datatype of timestamp column were strings.
<br>1.Some ratings in the numerator are in decimals. They need to be converted into float datatype.
<br>2.Sources of devices used to make a tweet were links.
<br>3. Only Original tweets need to be retained.
<br>4.Drop certain rows which are retweets and replies to retweets
<br>5.Drop columns not useful for analysis
<br>6.Some names were a, an, the etc. which didn't make sense.
<br>7.Some Numerator ratings were extremely high
<br>8.Denominator values range from 0 to 170
<br><b>Tidiness</b>
<br>1.Columns 'doggo', 'floofer','pupper' and 'puppo' are all one variable for Stages
<br>2.Columns p1_dog,p2_dog,p3_dog are all one variable for Dog breeds.

<br><h4>Clean Data</h4>
<br>1.Timestamp column was converted into datetime object
<br>2.Dog_breeds column created which merged p1_dog,p2_dog and p3_dogs
<br>3.Only original tweets retained.Duplicate rows were dropped.
<br>4.Columns not useful for analysis were dropped
<br>5.Denominator ratings not equal to 10 were dropped
<br>6.Very high numerator rating rows were removed
<br>7.Both numerator and denominator were converted into float type from integers.
<br>8.Name column consisting of a, an, the etc. were combined and replaced with None.
<br>9.Sources of devices which were links were converted into strings
<br>10.Stages column created by melting 'dogs','floofer','pupper' and 'puppo' columns
<br>11.The cleaned dataframe was then written to a .csv file and named as twitter_archive_master.csv.

<h4> Exploring and Assessing : The whole data was cleaned and explored. Visualizations were provided for a cleaer understanding of each variable and its uses.
