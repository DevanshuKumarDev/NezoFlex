
#Nezoflex

![Python](https://img.shields.io/badge/Python-3.8-blueviolet)

![Framework](https://img.shields.io/badge/Framework-Flask-red)

![Frontend](https://img.shields.io/badge/Frontend-HTML/CSS/JS-green)

![API](https://img.shields.io/badge/API-TMDB-fcba03)

A movie recommendation system that uses content based filtering to recommend movies.
The details of the movies like title, genre, runtime, rating, poster, etc. are fetched using an API by TMDB.


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

## Architecture

![flow_diagram](https://github.com/DevanshuKumarDev/NezoFlex/blob/main/flow.png)
