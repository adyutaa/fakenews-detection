# Detecting Fake News with Machine Learning (using TfidVectorizer & PassiveAggresiveClassifier)

# What is TfidVectorizer?

TF (Term Frequency): number of times a word appears in a documents. The higher the value, means that a term appears more often than the others/
And so, the document is a good match when the term is part of the search terms.

IDF (Inverse Document Frequency): Words that occur many times in a document but also occured many times in many others document, is probably irrelevant.
IDF measures how significant a term is in the entire corpus.

so the what TfidVectorizer do is converting a collection of raw docs unto a matrix of TF-IDF features.

# PassiveAgressiveClassifier?
Such an algorithm remains passive for a correct classification outcome, and **turns aggressive** in the event of a **miscalculation, updating and adjusting**.
Unlike most other algorithms, it does not converge.
Its purpose is to make updates that correct the loss, causing very little change in the norm of the weight vector.

Using sklearn, we build a TfidfVectorizer on our dataset.
Then, we would initialize a PassiveAggressive Classifier and fit the model.
In the end, the accuracy score and the confusion matrix tell us how well our model fares.

# Dataset
the dataset we use for this project has the shape of 7796x4.
The first column identifies the news, second and third are the title and text, the fourth column has labels denoting whether the news is REAL or FAKE.

**Data Preview**
<img width="986" alt="image" src="https://github.com/adyutaa/fakenews-detection/assets/44364705/6eb9a7f8-fca6-408b-92ae-9b9659fd076c">

**Applying TfidVectorizer and fitting the data**
<img width="1125" alt="image" src="https://github.com/adyutaa/fakenews-detection/assets/44364705/c59e763f-6796-43f4-8f56-b3f69e2633ab">

**PassiveAgressive Vectorizer,Score and Results**
<img width="1154" alt="image" src="https://github.com/adyutaa/fakenews-detection/assets/44364705/f65fbb8c-78f6-4d19-9ac6-c75407822c0b">



