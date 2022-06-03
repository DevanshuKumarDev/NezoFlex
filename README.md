
## Nezoflex

![Python](https://img.shields.io/badge/Python-3.8-blueviolet)

![Framework](https://img.shields.io/badge/Framework-Flask-red)

![Frontend](https://img.shields.io/badge/Frontend-HTML/CSS/JS-green)

![API](https://img.shields.io/badge/API-TMDB-fcba03)

A movie recommendation system that uses content based filtering to recommend movies.
The details of the movies like title, genre, runtime, rating, poster, etc. are fetched using an API by TMDB.

Youtube demo link: https://www.youtube.com/watch?v=8EEIJ50EXYs&ab_channel=DEVANSHUKUMARDEV

## How to run the project ?

1. Clone or download this repository to your local machine.
2. Install all the libraries mentioned in the requirements.txt file with the command `pip install -r requirements.txt`
3. Register yourself on TMDB and get your API key
4. Open your terminal/command prompt from your project directory and run the file `app.py` 

## How it works ?
In this project we use content based similarity to suggest movies to the user. However there are various other methods which are explained in the reference link given above.

### Similarity scores.

It is a numerical value ranges between zero to one which helps to determine how much two items are similar to each other on a scale of zero to one. This similarity score is obtained by measuring the similarity between the text details of both of the items. So, similarity score is the measure of similarity between given text details of two items. This can be done by cosine-similarity.

### Cosine similarity

Cosine similarity is a metric used to measure how similar the documents are irrespective of their size. Mathematically, it measures the cosine of the angle between two vectors projected in a multi-dimensional space. The cosine similarity is advantageous because even if the two similar documents are far apart by the Euclidean distance (due to the size of the document), chances are they may still be oriented closer together. The smaller the angle, higher the cosine similarity.

### Levenshtein Distance

The Levenshtein distance is a string metric for measuring difference between two sequences. Informally, the Levenshtein distance between two words is the minimum number of single-character edits (i.e. insertions, deletions or substitutions) required to change one word into the other.
We use a hybrid of both the methods in our application. The primary reason for this to improve the accuracy.

### The bigger picture

You might be wondering how do we use the words entered by the user. We convert the words to vectors and use the vector to classify and get the appropriate feature.
There are many ways in which we convert words to vectors. Some of them are bag of words and tfidf vectorizer. Since bag of words doesnot preserve the semantic meaning of the meaning. We use tfidf vectorizer.

#### Td-Idf vectorizer

TF-IDF for a word in a document is calculated by multiplying two different metrics:

##### 1 The term frequency of a word in a document
There are several ways of calculating this frequency, with the simplest being a raw count of instances a word appears in a document. Then, there are ways to adjust the frequency, by length of a document, or by the raw frequency of the most frequent word in a document.

##### 2 The inverse document frequency of the word across a set of documents
This means, how common or rare a word is in the entire document set. The closer it is to 0, the more common a word is. This metric can be calculated by taking the total number of documents, dividing it by the number of documents that contain a word, and calculating the logarithm.

So, if the word is very common and appears in many documents, this number will approach 0. Otherwise, it will approach 1.
Multiplying these two numbers results in the TF-IDF score of a word in a document. The higher the score, the more relevant that word is in that particular document.

## Architecture

![flow_diagram](https://github.com/DevanshuKumarDev/NezoFlex/blob/main/flow.png)

So when you enter the name of a movie
### 1. 
The details regarding the movie are fetched using TMDB API.TMDB is a famous site which has all the detailed information regarding movies. We use their API service and get the required details.

### 2.
Movies are recommended to the user by comparing the levenshtein distance between the current movie and the movies present in the TMDB dataset. The ones with close levenshtein distance are suggested.

## Technologies and concepts used

1.Similarity score and levenshtein distance

2.Html,css,js for front end 

3.Flask for backend

4.TMDB API to get the data regarding movies.

There are many more, which are mentioned in requirements.txt

## Screenshots
![Alt Text](https://github.com/DevanshuKumarDev/NezoFlex/blob/main/static/screenshots/11.JPG)

![Alt Text](https://github.com/DevanshuKumarDev/NezoFlex/blob/main/static/screenshots/12.JPG)

![Alt Text](https://github.com/DevanshuKumarDev/NezoFlex/blob/main/static/screenshots/13.JPG)

![Alt Text](https://github.com/DevanshuKumarDev/NezoFlex/blob/main/static/screenshots/14.JPG)


