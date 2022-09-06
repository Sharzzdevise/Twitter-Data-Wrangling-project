# Twitter-Data-Wrangling-project
<img width="466" alt="gazer" src="https://user-images.githubusercontent.com/102169299/187760679-eb167609-1c05-4a77-8058-ea9ca4a6129c.png">

This a data wrangling project by Udacity on the ratings of dogs from a Twitter handle @WeRateDogs. The twitter account used consists of pictures of various dogs and their ratings which are most times rated over 10.Why? Because "they're good dogs Brent." WeRateDogs has over 4 million followers and has received international media coverage. The goal of the project was to wrangle WeRateDogs Twitter data to create excellent and accuarate analysis and visualizations. This is done using Python and it's frameworks; from collecting the data to cleaning and analysing it, and finally visualizing trends from the data.  This project is on data wrangling and is one of the many projects to be completed in partial fulfillment of the Udacity Data analysis nanodegree.  The task carried out are:  Gathering Data Assessing Data Cleaning and storing Data Analyzing and Visualizing Data
## Data Gathering

These three pieces of data described below were gathered in this jupyter notebook

1) twitter_archive_enhanced.csv: 
this file was downloaded manually from an URL provided by Udacity.

2) The tweet image prediction:
This comprises of what breed of dog (or other object, animal, etc.) is present in each tweet according to a neural network. This file (image_predictions.tsv) hosted on Udacity's servers was downloaded programmatically using the Requests library and the following URL: [https://d17h27t6h515a5.cloudfront.net/topher/2017/August/599fd2ad_image-predictions/image-predictions.tsv]

2) JSON file from Twitter API:
This file contains each tweet's retweet count and favorite (i.e. "like") count at minimum, and any additional data. Using the tweet IDs in the WeRateDogs Twitter archive, query the Twitter API for each tweet's JSON data using Python's Tweepy library and stored each tweet's entire set of JSON data in a file called tweet_json.txt file. Each tweet's JSON data was written to its own line, after which this .txt file was read line by line into a pandas DataFrame with (at minimum) tweet ID, retweet count, and favorite count.
## Assessing Data

After gathering the three data, the next step was assesing the data. 

The data were properly assessed using the two major assessment methods; quality and tidiness issues. 

1) Data quality issues: Data that have quality issues have issues with content like missing, duplicate, or incorrect data. This is called dirty data.

2) Data tidiness issues: Data that has specific structural issues that slow you down when cleaning and analyzing, visualizing, or modeling your data later.

Also the dataset was assessed in two ways; 
1) Visual assessment
2) Programmatically using code
### Quality Issues

1. Dataframe 1: Some observations are retweets, Only tweets are needed.drop retweets 

2. Dataframe 3: Drop retweet columns in the dataframe scrapped using twitterAPI

3. Dataframe 1: Convert timestamp column to datetime

4. Dataframe 1: Convert tweet_id column to string

5. Dataframe 1: Create a list to contain all the names that starts with lowercase

6. Dataframe 1: Replace the names that start with lower case with the word "None

7. Dataframe 2: Convert the tweet_id column in image_prediction dataframe to string for image prediction data

8. Dataframe 2: Covert the tweet_id column in image_prediction dataframe to string
### Tidiness issues

1. Dataframe 1: The doggo, fluffer, pupper, poppo should be on one column.

2. Dataframe 2: The p1, p2 and p3 columns are merged to get the most likely breed of dog.

3. Merge the three dataframes to become one dataframe and merge them on tweet_id column
## Cleaning Data

The data was cleaned to improve its quality and tidiness.

The data used the three cleaning processes which are Define, Code, and Test.

Define: the issues that were gotten in the assessment were converted into cleaning tasks.
Code: the cleaning task is converted into code and then run.
Test: codes are tested to ensure they worked.
### Conclusion
The detailed analyzed data set showed generally the dog tweets from the @weratedogs twitter account had really good ratings,majority of the ratings recorded over 10, with the highest ratings of 12/10 showing how loved and admired the dog tweet were perceived before viewers.
The data also showed how much the tweets were loved and rated by people who viewed them.This will undoubtedly increase social interactions for the @weratedogs twitter page, bring more followers/connections to the page thereby promoting growth and publicity for the page.
Statistics showed About 25% of the dogs have no name, also the above graph shows that the most occcuring image number that corresponds to each tweet's most confident prediction is 1.
The pupper breed had the most likes and rating, which shows how admirable these breeds were to the viewers. It will be encouraged that the we rate dogs twitter page post more dogs in the pupper category.

### Limitations

1)The dog stage had some missing values.
2)Some rating denominators had wrong values.
