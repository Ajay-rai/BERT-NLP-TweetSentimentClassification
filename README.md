# BERT-NLP-TweetSentimentClassification: Project Overview
* Determined the sentiment of public towards work from home by analyzing tweets.
* Scraped over 7000,000 tweets using snscrape. Performed text-preprocessing and EDA.
* Used AWS sagemaker/kaggle to get the sentiment from a pre-trained model based on DistillBert.
* Imported the pipeline from Hugging Face model hub.

## Code and Resources Used
* **Python Version:** 3.8.5
* **Packages:** pandas, tensorflow, transformers, matplotlib, seaborn, snscrape, nltk
* * **GitHub Repo Ref1:** https://github.com/debnsuma/Intro-Transformer-BERT/blob/main/BERT-Disaster-Tweets-Prediction.ipynb
* * **GitHub Repo Ref2:** https://github.com/Rohan2002/BERT-natural-disaster-tweet-prediction/tree/master/lib
* * **Medium article Ref:** https://python.plainenglish.io/scraping-tweets-using-snscrape-and-building-sentiment-classifier-13811dadd11d

## Web Scraping (snscrape_tweets.ipynb)
Scraped over 700,000 tweets using snscrape. 27 attributes were there, out of which only following were important.
* date
* tweets (content)
* hashtags

## Data Cleaning (NLP sentimental analysis.ipynb)
Cleaned the raw text tweets.
* Removed hashtags, @username and other non english words and punctuations from tweets.

## EDA
Plotted distribution of tweets (#WFH) before and after covid. Also observed the average words used per tweets:

![alt text](https://github.com/Ajay-rai/BERT-NLP-TweetSentimentClassification/blob/main/img/covidtweets.PNG)
![alt text](https://github.com/Ajay-rai/BERT-NLP-TweetSentimentClassification/blob/main/img/Wordstweets.PNG)

## Model Building (model_building.ipnyb)
* Used transformers to call a pre-trained model from Hugging Face model hub.
* The pipeline used has an autotokenizer and it's called sentiment-analysis.
* Trained the model in AWS sagemaker/Kaggle.

![alt text](https://github.com/Ajay-rai/BERT-NLP-TweetSentimentClassification/blob/main/img/pn.PNG)
![alt text](https://github.com/Ajay-rai/BERT-NLP-TweetSentimentClassification/blob/main/img/pnn.PNG)
![alt text](https://github.com/Ajay-rai/BERT-NLP-TweetSentimentClassification/blob/main/img/hashtags.PNG)
![alt text](https://github.com/Ajay-rai/BERT-NLP-TweetSentimentClassification/blob/main/img/content.PNG)

## Conclusion and Future Recommendation
* The sentiment of public is almost equally divided between positive and negative for 'work form home'.
* Pipeline was implemented to train the model from Hugging Face model hub
* The accuracy of model can be improved by further training it in a labellled data set of tweets and using other models.
