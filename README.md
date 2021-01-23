# Movie Recommender System
This repository contains the files for a Data Science project about recommender systems and machine learning. 
The project revolves around building a hybrid recommender system with collaborative and content-based filtering. 


## The Dataset
The dataset was provided through the course material for INF161 at the University of Bergen. It
consists of a somewhat customized version of the [MovieLens 1M Dataset](https://grouplens.org/datasets/movielens/1m/), 
which contains 1 million movie ratings given by 6000 users on 4000 movies in the years 2000-2003. 
The data provided through INF161 was translated to Norwegian and modified to be slightly more challenging to clean than the original. 

## The Process
In order to learn as much as possible about recommender systems and data science in general, 
I decided early on to follow the Data Science Process for this project:

![The Data Science Process](/data-science-process.png)

This project has largely been motivated by wanting to learn how to implement a recommender system in Python. 
I started with wondering whether I would be able to improve the root mean squared error (RMSE) of a superior recommender system 
by combining it with a different recommender system approach. I had read about the "cold start problem", and though it intuitively 
made sense to combine content-based and collaborative filtering models to improve recommendations, I was curious about how one would practically 
apply this to create a hybrid recommender system. After taking a look at the dataset for the first time, I also wrote down a string of questions which 
were only answerable through data wrangling and visualization. 

Cleaning the data was more difficult than I originally thought, as a lot of the data was missing or incorrect. 
I quickly came to learn the power of value imputations, especially using KNN. 
I also learned a surprisingly lot about the US postal code system...

Before I began modelling, I had to answer the questions I had about possible patterns in the data. 
After figuring out that I could potentially improve the training dataset through engineering three new features, 
I also wanted to know how much RMSE would improve from adding the new features to the training dataset. 
Therefore, I first created different content-based and collaborative filtering models using a variety of machine learning algorithms.
I then re-built and re-trained the most promising models using the new dataset with the engineered features. 

Finally, I ran the improved hybrid recommender a last time and predicted ratings from all users to all movies. 
Going forward, I'm considering whether I should implement the hybrid recommender in a simple website. 
I am hoping that I'll soon find the time to do so. 


## Explanation of files
* [raw data](https://github.com/SebastianRokholt/Hybrid-Recommender-System/tree/main/raw_data) - The raw data files.
* [Part 1: cleanup.ipynb](https://github.com/SebastianRokholt/Hybrid-Recommender-System/blob/main/cleanup.ipynb) - Cleaning the raw data files. 
* [cleaned data](https://github.com/SebastianRokholt/Hybrid-Recommender-System/tree/main/cleaned_data) - The resulting files after performing the data cleaning.
* [Part 2: analysis-and-modelling.ipynb](https://github.com/SebastianRokholt/Hybrid-Recommender-System/blob/main/analysis-and-modelling.ipynb) - Data Analysis, Exploration and Modelling.
* Part 3: predict.ipynb (Coming soon!) - Predicting ratings for all movies from all users.

