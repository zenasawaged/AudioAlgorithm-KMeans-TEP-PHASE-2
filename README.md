# AudioAlgorithm-KMeans-TEP-PHASE-2

In this project, I am aiming for the best clusters needed to find the type of song characteristics this user enjoys. 

DATA
The dataset had approximately 28362 data points. This would be a good beginning data set for proof of concept.

METHOD
Hypotheses:

Since there is not a target variable, I had simply hypothesized that there was a correlation with the genre of the users songs.

The goal was to first clean the data and choose our ideal features. There are a number of general types of models that could be used for predicting clusters.

I utilized:

KMeans clustering and calculate within-cluster sum of squares (WCSS) for different values of K and plot the elbow method curve

Then I created a Means object with this optimal number of clusters. 

Upon finding optimal clusters, I re-train our model by generating labels for the dataset and output the centroids of your clusters

EDA Report

We explored the dataset by utilizing describe, head, and columns functions. I then started creating histogram to determine distribution of artists selected:
![image](https://github.com/zenasawaged/AudioAlgorithm-KMeans-TEP-PHASE-2/assets/75915150/23ab53ff-b4fb-44cd-b08f-af60d58023dc)

Then I compared the genre of her most popular selected artists- we found pop and country to be most selected genre
![image](https://github.com/zenasawaged/AudioAlgorithm-KMeans-TEP-PHASE-2/assets/75915150/a83624b5-d2d1-467c-ad22-3c8cd27d89ce)

Then I compared the topic of her most popular selected artists- we found sadness and violence were most popular
![image](https://github.com/zenasawaged/AudioAlgorithm-KMeans-TEP-PHASE-2/assets/75915150/9e41fa12-37d2-44b2-a986-101fa553a87e)

Since Sadness was the most popular topic, i found it to still be a small portion of the topics
![image](https://github.com/zenasawaged/AudioAlgorithm-KMeans-TEP-PHASE-2/assets/75915150/2bc75794-dd76-43b4-945f-3f3d2ce96b18)

The i created subplots for each genre with its topic and I still found no correlation.
![image](https://github.com/zenasawaged/AudioAlgorithm-KMeans-TEP-PHASE-2/assets/75915150/d7e20f1f-7304-4a35-8104-29e5bfcc8d9d)

CLEANING
Cleaning Report

We want to make sure the data is clean and usable. That means removing things like missing data-sets and columns that are not necessary. I started by checking for null values and dropping columns that were not so useful such as "Unnamed: 0','lyrics'" and since this is unsupervised learning, I removed non-numerical variables ['artist_name','track_name','genre','topic']. 

# To do Kmeans we have to drop all non-numerical columns 
numerical_df=df_f.drop(['artist_name','track_name','genre','topic'], axis=1)

We moved on to deeper exploration after this and created a new csv file.

MODELING
Pre-Processing Report Modeling Report

I chose to utilize non-numerical dataset in order to perform the kmeans cluster modeling.

![image](https://github.com/zenasawaged/AudioAlgorithm-KMeans-TEP-PHASE-2/assets/75915150/1b25dc01-99e4-492e-a5dd-e5b67a263c4f)

According to the elbow plot, best number of clusters is 3

So I create a Means object with this optimal number of clusters. I Named this object 'kmeans' and fit this Means object using my "numerical_df" data, I used variable sadness and dating to test out my model and outputted the centroids of its clusters.

New Sample Predication

Lastly, I fit this KMeans object using my "newsampleprediction" data.


