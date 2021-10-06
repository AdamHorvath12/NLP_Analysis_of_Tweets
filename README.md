# NLP Analysis of Tweets Project 2021 - Adam Horvath-Reparszky
(Kaggle challenge: https://www.kaggle.com/c/nlp-getting-started)

## Installation
```bash
git clone https://github.com/AdamHorvath12/NLP_Analysis_of_Tweets.git
```

Create a virtual environment (or in your base environment) with Anaconda or any virtual environment manager (see Anaconda example below): 

```bash
conda create -n nlp_tweets_project python=3.8
conda activate nlp_tweets_project
pip install -r requirements.txt
```

## Project description

Twitter has become an important communication channel in times of emergency.
The ubiquitousness of smartphones enables people to announce an emergency they’re observing in real-time. Because of this, more agencies are interested in programatically monitoring Twitter (i.e. disaster relief organizations and news agencies).

In this project, you’re challenged to build a machine learning model that predicts which Tweets are about real disasters and which one’s aren’t. You’ll have access to a dataset of 10,000 tweets that were hand classified.

## Solution

To tackle this problem, first I did basic exploratory data analysis and data visualization for a better understanding. Before the modeling part, tweets have to be cleaned first, therefore I defined two tweet processing functions to remove stopwords, emojis, URLs, hashtags, punctuations, etc.., also use lemmatization and stemming to create our cleaned corpus. The last step before modeling was to convert our raw text data into numerical values which the model can understand, for this step I used a pre-trained model tokenizer (distill bert tokenizer fast). Regarding the model selection, I decided to fine-tune a pre-trained BERT model, since it provides good results and does not require too much time and computational power.

## Future steps

In the dataset, we can find information (most of the time missing) about the location and keywords. However, by collecting more data or using external datasets and adding extra features to extend this dataset, we can improve our model. Regarding the model selection, we can think about other models, but we have to take into consideration the requisite time and computational power.

## References / Related articles (can be useful if someone do not have prior knowledge)

* https://www.kaggle.com/vbmokin/nlp-eda-bag-of-words-tf-idf-glove-bert
* https://www.kaggle.com/shahules/basic-eda-cleaning-and-glove
* https://www.kaggle.com/arthurtok/spooky-nlp-and-topic-modelling-tutorial
* https://github.com/jess-data/Twitter-2020-Sentiment-Analysis
* https://towardsdatascience.com/bert-explained-state-of-the-art-language-model-for-nlp-f8b21a9b6270
* https://medium.com/@gabriel.mayers/sentiment-analysis-from-tweets-using-recurrent-neural-networks-ebf6c202b9d5
* https://towardsdatascience.com/lstm-vs-bert-a-step-by-step-guide-for-tweet-sentiment-analysis-ced697948c47
* https://towardsdatascience.com/how-to-train-bert-aaad00533168
* https://towardsdatascience.com/how-transformers-work-6cb4629506df


