# Wrangling and Analyzing Data-Udacity-Project---We-Rate-Dogs

## Overview
Real-world data rarely comes clean. Using Python and its libraries, you will gather data from a variety of sources and in a variety of formats, assess its quality and tidiness, then clean it. This is called data wrangling. You will document your wrangling efforts in a Jupyter Notebook, plus showcase them through analyses and visualizations using Python (and its libraries) and/or SQL.

The dataset that you will be wrangling (and analyzing and visualizing) is the tweet archive of Twitter user @dog_rates, also known as WeRateDogs. WeRateDogs is a Twitter account that rates people's dogs with a humorous comment about the dog. These ratings almost always have a denominator of 10. The numerators, though? Almost always greater than 10. 11/10, 12/10, 13/10, etc. Why? Because "they're good dogs Brent." WeRateDogs has over 4 million followers and has received international media coverage.

WeRateDogs downloaded their Twitter archive and sent it to Udacity via email exclusively for you to use in this project. This archive contains basic tweet data (tweet ID, timestamp, text, etc.) for all 5000+ of their tweets as they stood on August 1, 2017.

## Context
Your goal: wrangle WeRateDogs Twitter data to create interesting and trustworthy analyses and visualizations. The Twitter archive is great, but it only contains very basic tweet information. Additional gathering, then assessing and cleaning is required for "Wow!"-worthy analyses and visualizations.

### The Data
In this project, I worked on the following three datasets.

#### Enhanced Twitter Archive
The WeRateDogs Twitter archive contains basic tweet data for all 5000+ of their tweets, but not everything. One column the archive does contain though: each tweet's text, which I used to extract rating, dog name, and dog "stage" (i.e. doggo, floofer, pupper, and puppo) to make this Twitter archive "enhanced." Of the 5000+ tweets, I have filtered for tweets with ratings only (there are 2356).

Extracted data from tweet text The extracted data from each tweet's text

I extracted this data programmatically, but I didn't do a very good job. The ratings probably aren't all correct. Same goes for the dog names and probably dog stages (see below for more information on these) too. I assessed and cleaned these columns to use them for analysis and visualization (see the Act_Report file).

#### Additional Data via the Twitter API
Back to the basic-ness of Twitter archives: retweet count and favorite count are two of the notable column omissions. I gathered this additional data from Twitter's API. Well, "anyone" who has access to data for the 3000 most recent tweets, at least. But you, because you have the WeRateDogs Twitter archive and specifically the tweet IDs within it, can gather this data for all 5000+. I had to query Twitter's API to gather this valuable data.

#### Image Predictions File
One more cool thing: I ran every image in the WeRateDogs Twitter archive through a neural network that can classify breeds of dogs*. The results: a table full of image predictions (the top three only) alongside each tweet ID, image URL, and the image number that corresponded to the most confident prediction (numbered 1 to 4 since tweets can have up to four images).


## Analysis Insights
- Common dog breeds

- Top rated dog(s)

- Top common name for dogs

- Top beloved dog stages (doggo, pupper, puppo or floofer)

- Top beloved dogs

- Top retweeted dogs

#### Distribution of dog stages

The following insights were gottten from the analyses codes ran on the twitter_archive_master dataset (see wrangle_act notebook)
1. Common dog breeds
The Top 5 common dog breeds are: Golden Retriever; Labrador Retriever; Pembroke, Chihuahua and Pug

2. Top rated dog(s)
The top 5 rated dog breeds are: Pembroke, Labrador Retriever, Golden Retriever, French Bulldog, and Soft-Coated Wheaten Terriere

3. Top common name for dogs
The top 5 common names for dogs are: Charlie; Lucy; Cooper; Oliver; and Penny

4. Top beloved dog stages (doggo, pupper, puppo or floofer)
The top 4 beloved dog stages are: 'pupper'; 'doggo'; 'puppo'; and 'floofer'

5. Top beloved dogs
The top 5 beloved dog breeds are: Golden Retriver; Labrador Retriever; Pembroke; Chihuahua; and French Bulldog

6. Top retweeted dogs
The top 5 retweeted dog breeds are: Golden Retriever; Labrador Retriever; Pembroke; Chihuahua; and Samoyed



## Conclusion
From the analyses and visualizations conducted (see act_report document), the following can be concluded from this project:

Golden Retriever has the highest predicted popularity/commonnest rating amongst all the dog breeds with 152 counts

The most retweeted dog_breed is Golden Retriever, which also happened to be the most favorite dog_breed

puppo seems to by the most favorited stage. then comes doggo and floofer. however, pupper seems to be the least popular.

There is a positive correlation between retweet_count and favorite_count. Please note that correlation does not mean causation. There may be other reason(s) for this positive correlation.

Pembroke is the highest rated dog breeds

The top 5 common names for dogs are: Charlie; Lucy; Cooper; Oliver; and Penny

The top 4 beloved dog stages are: pupper, doggo, puppo, and floofer
