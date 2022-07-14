
# Project Title

Book-Recommendation-System

# Problem Description

During the last few decades, with the rise of YouTube,
Amazon, Netflix, and many other such web services, 
recommender systems have taken more and more place in our
lives. From e-commerce (suggest to buyers articles that 
could interest them) to online advertisement (suggest to 
users the right contents, matching their preferences),
recommender systems are today unavoidable in our daily
online journeys. By analyzing the problems with ‘Book 
Recommendation System’ feature, how we can predict the 
best recommendation for users according to their items 
approach.

A recommendation system helps an organization to create
loyal customers and build trust by them desired products 
and services for which they came on your site. The 
recommendation system today is so powerful that they
can handle the new customer too who has visited the site for the first time. They recommend the products which
are currently trending or highly rated and they can also 
recommend the products which bring maximum profit to the
company. Providing specific data analysis and prediction to done 
with this data. The main objective is to built a predictive
recommender model, which could help in predicting –  how
we can predict the best recommendation for users according 
to their items approach. This would help us in providing 
better recommendation item to a right specific users.

# Data Description

We've three dataset - 

•	Book data – (ISBN, Book-Title, Book-Author,
Year-Of-Publication, Publisher, Image-URL-S, Image-URL-M, 
Image-URL-L)

•	Users data -  (User-ID, Location, Age)

•	Ratings data -  (User-ID, ISBN, Book-Rating) 

The users interaction is very vital role for recommendation.
 To successful build collaborative filtering model in 
 recommender system, data preparation is important. 
 Beginning with book data – dropping URL features 
 (i.e 'Image-URL-S', 'Image-URL-M', 'Image-URL-L'). 
 We have some extra columns which are not required for 
 our task like image URLs. And we rename the columns of 
 each file as the name of the column contains space and 
 lowercase letters so we will correct as to make it easy 
 to use. The features depict great analysis by feature 
 engineering.  

# Attribute information

•	Book data – (ISBN, Book-Title, Book-Author,
Year-Of-Publication, Publisher, Image-URL-S, Image-URL-M, 
Image-URL-L)

•	Users data -  (User-ID, Location, Age)

•	Ratings data -  (User-ID, ISBN, Book-Rating) 

# Summary of Project

A book recommendation system is a type of recommendation 
system where we have to recommend similar books to the 
reader based on his interest. We’ve all record and data
 with three different dataset –  Book dataset (ISBN, 
 Book-Title, Book-Author, Year-Of-Publication, Publisher,
  Image-URL-S, Image-URL-M, Image-URL-L); Users dataset 
  (User-ID, Location, Age); Ratings dataset (User-ID, ISBN,
   Book-Rating). Providing specific data analysis and 
   prediction to done with this data. The main objective
is to build a predictive recommender model, which could help
 in predicting –  how we can predict the best recommendation
for users according to their items approach. This would help
 us in providing better recommendation item to a right
  specific user.

As the first step, I performed data preparation 
(i.e data cleaning and feature engineering) and EDA part.
 The book_data, users_data and ratings_data dataset was an
  important dataset to gets smaller insights from its. 
  Analysis feature like book_title, book_author, publisher,
   year_of_publication, age, book_rating were important to 
get some insights. Some of the null values were present in 
feature data, we replaced with mean of that particular 
feature. Deal with mismatch feature like book_title, 
book_author, year_of_publication, publisher. 
Only considering age between 5-90 we took users data to 
analysis and perform recommendation on it.

After data preparation, building recommendation system based 
on popularity (i.e ratings). These recommendations are
 usually given to every user irrespective of personal 
 characterization. Merged book_data dataset and 
 ratings_explicit. Considering ISBNs that were explicitly 
 rated for this recommendation system.

The third step was to do Collaborative Filtering - Memory 
based approach was our first trial on train and test dataset
 which uses the memory of previous users interactions to 
 compute users similarities based on items they’ve interacted
  (i.e user-based approach) or compute items similarities 
based on the users that have interacted with them 
(i.e item-based approach). Applying cosine similarity to make
 item-item similarity need to take transpose of matrix. 
 This matrix would help in manage train-test matrix. After 
all views predictions based on similarity, we find 
recommendation on it based on score. Model-based 
collaborative filtering algorithms provide item 
recommendation by first developing a model of user ratings. 
We use Latent Factor Model called Singular Value Decomposition
(SVD). SVD made dimensionality reduction technique in machine
learning. SVD is a matrix factorization technique. It made us
reduces the number of features of a dataset by reducing the 
space dimension from N-dimension to K-dimension (where K<N). 
SVD uses a matrix structure where each row represents a user,
and each column represents an item. The elements of this matrix
are the ratings that are given to items by users.

Model evaluation metrics is important to distinguish the 
best collaborative filtering – either by memory based or 
model based approach. The memory based approach – Cosine 
Similarity shows RMSE score for item based CF is 7.99 and 
for user based CF it shows 7.99. The score is slightly 
similar. Model based collaborative filtering made it better
score with Latent Factor Model called SVD. The score 
improved to 1.63 for both SVD RMSE and accuracy score.


# Machine Learning (Unsupervised) Data Pipeline

1.	Data Preparation (Data Cleaning and Feature Engineering)

2.	Exploratory Data Analysis

•	Univariate Analysis on numeric and categorical features

•	Analysis from categorical variables
                                
3. Got top ten books as per ratings

4. Collaborative Filtering 

•	Memory Based approach - Cosine Similarity

•	Model Based approach – Singular Value Decomposition (SVD)


5. Model Evaluation Metrics

•	RMSE score with each collaborative filtering approach

6.  Getting top recommendation of books and ratings


# Conclusion


* Among top 20 Authors the highest number of books has been hold by Agatha Christie. Agatha Christie is leading at top with more than 600 counts, followed by William Shakespeare.

* Harlequin has most number of books published, followed by Silhouette.

* Number of Books published in yearly are between 1950 - 2005.

* Most of the users are between 30-40 prefer more books and somewhat we can also view between 20-30.

* As per ratings "Selected Poems" has been rated most followed by "Little Women". The countplot shows users have rated 0 the most, which means they haven't rated books at all.

* The top 10 books recommendation as per ratings with top "The lovely Bones: A novel" with 707 book ratings. But this are not based on some recommendation system. They are top 10 books as per ratings. 

* As we perform by cosine similarity in recommendation system it gives 7.94 RMSE score and SVD improved score it to 1.63 RSME score by Singular Value Decomposition model (SVD).

* The evaluation metrics for SVD is best RMSE score for all dataset (i.e users_data, ratings_data and books_data).

* As model based approach was best to signify and at last we got top 10 recommended books and ratings respectively.


