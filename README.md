# Sentiment Analysis in Natural Language Processing

This repository houses a predictive classification model that analyzes **reviews** or **comments**
and **predicts** its class as either **POSITIVE** or **NEGATIVE** review.

The dataset used for this project is a labelled dataset found on Kaggle with this 
[link] (https://www.kaggle.com/datasets/columbine/imdb-dataset-sentiment-analysis-in-csv-format/data)
The dataset had separate data for training, validating and testing.
The **training** data set had a shape of **(40000, 2)**, while the **testing** has a shape of 
**(5000, 2)**

The model was developed using Google Colab Notebook.

## STEPS
Various steps were used in order to make this model come out as expected. The steps used 
are as follows:

1. **PREPROCESSING**
    This step, the data was cleaned, stop words were removed using the stopwords library
    in NLTK. HTML tags and other noise data were removed using **REGEX**.

    Also, during the preprocessing, **LEMMATIZATION** technique was used to cut down words back
    to it base form whilst retaining its meaning. Example: going is returned to go and so on.
    
2. **VECTORIZATION**
    This step entails converting the preprocessed texts into vectors that can be understood by the 
    machine learning model.
    **TF-IDF** was used to make this possible

3. **MODELLING**
    This is the actual model creation. Since it is a binary problem, Classification algorithms were used
    and the end result gives either of **POSITIVE (1)** or **NEGATIVE (0)**

    Different models were used to find out which of them gives a better result. Overall the
    **Linear Simple Vector Classification (Linear SVC)** proved to be the better algorithm with 
    **2222 TP** points, **2272 TN** points, **233 FP** points and **273 FN** points