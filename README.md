# NLP Competition Hosted by DataHack in Analytics Vidhya 
[Janatahack: Independence Day 2020 ML Hackathon](https://datahack.analyticsvidhya.com/contest/janatahack-independence-day-2020-ml-hackathon)
## Problem Statement:
Given the abstract and title for a set of research articles, predicting the topics for each article included in the test set.\
There are six tags - 
### Computer Science, Physics, Mathematics, Statistics, Quantitative Biology, Quantitative Finance
NOTE: It is multi-label classification problem.

## Evaluation Metric - micro F1 Score 

## About Data
Training data - \
Columns = ['ID','TITLE','ABSTRACT','Computer Science','Physics','Mathematics','Statistics','Quantitative Biology','Quantitative Finance'] \
Shape   = (20972, 9)\
non-null values  = 20972 (There are no null/none values) 

Testing data - \
Columns = ['ID', 'TITLE', 'ABSTRACT']
Shape   = (8989, 3) \
non-null values  = 8989 (There are no null/none values) 

# MY APPROACH
* Preprocessing data - cleaning data by stripping off extra/white spaces, replacing escape characters and punctuation with spaces. 
* Tools used for modelling - Pytorch,GPU,transformer models (BERT-base-uncased,allenai/scibert_scivocab_uncased) and tokenizers
* final model - model worked best was allenai/scibert_scivocab_uncased from huggingface, transformer based models
* To improve further -  feature engineering and text augmentation, tuning hyper-parameters etc.
              
**max f1-score - 0.84** 



[allenai/scibert_scivocab_uncased](https://huggingface.co/allenai/scibert_scivocab_uncased)

Thanks to [Prithvi Jaunjale](https://www.kaggle.com/prithvijaunjale/scibert-multi-label-classification)
