# Web-APIs-Classification(Depression or Anxiety disorder)

## Problem Statement

To scape 2 subreddits(Anxiety & Depression) and using the scape data to build classification model which is based on Logistic Regression and MultinomialNB. The purpose of the model is to accurately predict the category of the words used in both subreddits. We hope that the model could be implemented in therapy session to distingush between an anxiety or depression patient.  

And at the end of the evaluation, the model with the best accuracy and least type 2 error would be selected as the final model. This would be based on score accuracy, ROC AUC score and confusion matrix.


## Executive Summary

Singapore has one of the highest depressive disorder cases among high-income nation around the world. And there is an increasing trend among Singapore youth to be diagnosed with depression or anxiety disorder. 

We hope that the model would provide insights on the common words used by depression or anxiety disorder patients during therapy. Therefore, mapping out a relationship between words used and sentiments of patients. Eventually the model could be utilize to help psychiatrist to make better deduction of depression or anxiety disorder patients. Thus, ensuring that the proper resources and treatments are allocated to individual patient. 

## Evaluation Summary

### Model Choice: TfidfVectorizer & LogisticRegression

#### **TfidfVectorizer & LogisticRegression** was the final choice of our model as it has one of the highest accuracy score as compared to other deployed methods. 


### Data collected from models

|Model      |Accuracy      |ROC AUC 
|---------    |------    |---------|
|**Logistic Regression** |0.8336    |0.907  |
|**MultinomialNB**        |0.8068    |0.882  |
|**CountVectorizer & LogisticRegression** |0.847  |0.91  |
|**CountVectorizer & MultinomialNB**    |0.831    |0.82  |
|**TfidfVectorizer & LogisticRegression** |**0.8546**  |**0.935**  |
|**TfidfVectorizer & MultinomialNB**    |0.8221    |0.908  |

**Accuracy:** TfidfVectorizer & LogisticRegression provided the highest accuracy of **0.8546**.  
**ROC AUC:** TfidfVectorizer & LogisticRegression has **0.935**. This mean that the positive and negative predictions are relatively distinct and there is not much overlapped between them. 

## Conclusion & Recommendation

In conclusion, the sentiment analysis of words used in both the subreddit post are pretty similar. Both are on the extreme side of the score in which their words are mostly very negative(-1) or positive(1). In this case it is possible as we are handling depression and anxiety issue thus, the sentiment within the posts would be relatively negative and at the same time people would be giving positive advise which would form the positive aspect of the posts.

And from the words comparison analysis, both subreddit posts have similar usage of words such as 'feel' and 'people' which are words used to describe feelings and human interactions. Individually, depression have distinct words such as 'friend' and 'life' which is relevant to this situation in which depression patients would normally be discussing about life issues and having friends support. Anxiety has distinct words such as 'feeling' and 'work' and it might be due to the emotional aspect of anxiety disorder patients feeling stress at work or engaging in social ineraction. 

With all the above analysis we decided to implement it into 4 different models and TfidfVectorizer & LogisticRegression gave us the best accuracy and ROC AUC score. Beside having the best score and accuracy the confusion matrix of the model gives the least type 2 error, in which psychiatrist fail to diagnosed an anxiety disorder patient. We feel that failling to diagnose an anxiety disorder patient would be more detrimental as opposed to diagnosing a patient wrongly for anxiety. This would further harm the patient mental health. In conclusion, the final model with TfidfVectorizer & LogisticRegression will be used and recommended for helping psychiatrist to make better deduction of depression or anxiety attack patients.

