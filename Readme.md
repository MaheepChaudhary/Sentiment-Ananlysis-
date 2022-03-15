# Sentiment Analysis
This project focus on building a Sentiment Classifier using [IMDB_Dataset](https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews) usig BERT and Tfidf encodings.

## Table of Contents
* Introduction
* Technologies
* Launch
* Inspiration
  
## Introduction
 Our Sentiment analysis model gives us the interpretation and classification of emotions (positive, negative) within text data using text analysis techniques. It can allows businesses to identify customer sentiment toward products, brands or services in online conversations and feedback. 
The model is built by using the [IMDB_Dataset](https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews). After the model is loaded that HTML tags are cleaned using BeautifulSoup and the punctuations, Stopwords using NLTK library. The obtained text is then encoded to vectors using BERT in Sentiment_Analysis_BERT file and Tfidf in Sentiment_Analysis_Tfidf file. The model is then trained using Dense layer and also LogisticRegression for more anaysis. 

## Technologies
The languages and libraries used are :-
* Python: 3.7
* Tensorflow
* Sklearn
* Numpy
* Pandas
* BeautifulSoup
* NLTK

## Launch
Further the from kaggle the dataset can also be downloaded directly by including the code in the files by using the code 
```python
!pip install kaggle
!mkdir .kaggle

import json
#In username enter your username obtained from kaggle and key obtained
token = {"username":"ENTER YOUR USERNAME","key":"ENTER YOUR KEY"}
with open('/content/.kaggle/kaggle.json', 'w') as file:
    json.dump(token, file)
    
!cp /content/.kaggle/kaggle.json ~/.kaggle/kaggle.json
!kaggle config set -n path -v{/content}
!chmod 600 /root/.kaggle/kaggle.json
!kaggle datasets download -d lakshmi25npathi/imdb-dataset-of-50k-movie-reviews    

!unzip {/content}/datasets/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews/imdb-dataset-of-50k-movie-reviews.zip
```
Or it can be uploaded directly by downloading the file through the [link](https://www.kaggle.com/lakshmi25npathi/imdb-dataset-of-50k-movie-reviews) and unzipping it. For further knowlege to download the dataset directly from kaggle in colab can be found through this [article](https://towardsdatascience.com/setting-up-kaggle-in-google-colab-ebb281b61463).

## Inspiration
The model was inspired by the Coursera rhyme project of Sentiment Analysis and also for more insipartion you can refer this [link](https://towardsdatascience.com/sentiment-analysis-with-python-part-1-5ce197074184).For explanation of BERT you can prefer this [link](https://www.youtube.com/playlist?list=PLbMqOoYQ3Mxw1Sl5iAAV4SJmvnAGAhFvK, ) and for BERT research paper this [link](https://arxiv.org/pdf/1810.04805.pdf) would be sufficient.
