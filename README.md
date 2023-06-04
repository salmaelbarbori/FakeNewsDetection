# FakeNewsDetection
<section align = "center">
  <a href = "https://github.com/salmaelbarbori/FakeNewsDetection/blob/main/20230522_220143_0000.png?raw=true">
    <img src = "https://github.com/salmaelbarbori/FakeNewsDetection/blob/main/20230522_220143_0000.png?raw=true" slt = "fakeDetection" width = "500" height ="400"/>
  </a>
</section>
</br>

## Situation 

Salma is an aspiring data scientist who is trying to stay up to date in the field of data science. She looks for articles that includes data science news every day, and she tries to understand technical aspects very well and in a detailed manner.
Unfortunately it happened that she learned from the news from a journal names .... but after verifying the informations learned from that article and trying to apply what she had learned she find herself confused 😕 and start worrying if the news that she read and decided to apply were true or fake. After verification she found out that the news were Fake.
since she is an aspiring data scientist and she is trying to aquire new skills in this field, she decided to build a classification model, that gives users the chance to enter a news and then the model will tell them based on lots of training if the news shared arr true and can be trusted or it is fake so they avoid it.

## Project goals

This project aims to classify news in one of the cotegories real news or fake ones.

## Pipeline

<section align = "center">
  <a href = "https://github.com/salmaelbarbori/FakeNewsDetection/blob/main/Pipeline_png.png">
    <img src = "https://github.com/salmaelbarbori/FakeNewsDetection/blob/main/Pipeline_png.png" slt = "fakeDetection" width = "500" height ="400"/>
  </a>
</section>
</br>

## Dataset

I scrapped my dataset from the website : PoliticFact.
My dataset contains more than 23 000 rows.
Here is the link to the dataset: https://github.com/salmaelbarbori/FakeNewsDetection/blob/main/POlitical_fact_chekcer_data_set.csv

## Pre-processing

```python
import nltk
```
### Removing punctuation, symbols and numbers
```python
import re
r'[^a-zA-z0-9.,!?/:;\"\'\s]' 
```
### Tokenization
```python
from nltk.tokenize import RegexpTokenizer
```
### Removing StopWords
```python
from nltk.corpus import stopwords
```
### Lemmatizing
```python
from nltk.stem import WordNetLemmatizer,PorterStemmer
```
## Vectorization
---
```python
from sklearn.feature_extraction.text import CountVectorizer
```

## Machine learning
### Spliting data by two(Training/Evaluation)
```python
from sklearn.model_selection import train_test_split
```
### Algorithms
Classification algorithms: 
I tested two algorithms the first one is 
#### Decision Tree Algorithm
```python
from sklearn.tree import DecisionTreeClassifier
```
The second one is 
#### Naive Bayes Classifier
```python
from sklearn.tree import DecisionTreeClassifier
```

## Evaluation
```python
#Confusion matrix
from sklearn import metrics
cm = metrics.confusion_matrix(y_test, model.predict(x_test))
```
