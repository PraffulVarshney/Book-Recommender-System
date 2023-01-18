# Book-Recommender-System
## 1. Description:
<p>A Book Recommendation System which recommends the users a selection of books based on their interests.</p>

Dataset Used -- https://www.kaggle.com/datasets/arashnic/book-recommendation-dataset/




## 2. Algorithms Implemented:
#### 2.1 Popularity Based Recommendation :

* ##### Popular in the Whole Collection <br>
Sorted the dataset according to the total ratings each of the books have received in non-increasing order and then recommended top n books.

* ##### Popular at a Given Place <br>
The dataset was filtered according to a given place (city, state, or country) and then sorted according to total ratings they have received by the users in decreasing order of that place and recommended top n books.

* ##### Books By the Same Author, Publisher of Given Book Name <br>
For this model, I sorted the books by rating for the same author and same publisher of the given book and recommended top n books.

* ##### Popular Books Yearly <br>
This is the most basic model in which we have grouped all the books published in the same year and recommended the top-rated book yearly.

 	
#### 2.2 User-Item Collaborative Filtering Recommendation
Collaborative Filtering Recommendation System works by considering user ratings and finds cosine similarities in ratings by several users to recommend books. To implement this, we took only those books' data that have at least 50 ratings in all and users who reviewed more than 100 books. If there are m-books and n-users then each book is a point in N-user coordinate system and we find eucladian distance of each vector with each other vector and give top 20 book based on this similarity score.


#### 2.7 Hybrid Approach (Collaborative+Content) Recommendation
A hybrid recommendation system was built using the combination of both popularity-based and collaborative filtering systems. A percentile score is given to the results obtained from both popularity and collaborative filtering models and is combined to recommend top n books.



## 3. Webpage:
Built a webpage using Bootstrap and pickle that would take input from user and recommend 5 books based on collorative filtering and 50 most popular books across the platform.



## 4. Libraries Used:

* ipython-notebook - Python Text Editor
* sklearn - Machine learning library
* seaborn, matplotlib - Visualization libraries
* numpy, scipy- number python library
* pandas - data handling library
* bootstrap - bulid the webpage
* pickle - to deploy ML model
* gunicorn - to deploy webpage on heroku
