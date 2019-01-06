# Pytorch Challenge Side Project

## Text Classification for Yelp review - A sentiment analysis

it is common to see the practical use of text classification in email spam filtering. Basically, you are given a number of emails and then you train a classification model that automatially flags spam emails. It is just an idea and the uses of text classification are actually countless. To move one step forward from the spam filter, we can build a model that extracts the meaning/sentiment from the text and then try to figure out if the text shows a sign of positiveness or negativeness. 

In the Pytorch Challenge course, RNN with embedding and hidden LSTM layers are proposed to predict the sentiment of a given movie review. Inspired by it, I decide to try to conduct a sentiment analysis using CNN instead. In this side project, I use CNN to build a classification model that predicts the review stars from Yelp. By feeding the model with reviews from Yelp, the model automatically determines whether or not the user is satisfied with the service and returns a score, ranging from 0 (*extremely unsatisfied*) to 5 (*extremely satisfied*) based on the predicted satisfaction. The data is from Yelp website and it is free to download. The original dataset is in json format and each line has a form of:


    {'review_id': '1234',
 
    'user_id': 'abcd',
 
    'buisiness_id': 'abc123',
 
    'stars': 5,
 
    'date': '2019-01-01',
 
    'text': 'I enjoy the food a lot',
 
    'useful': 0,
 
    'funny': 0,
 
    'cool': 0}

To me, only __'stars'__ and __'text'__ matter in the project as the input will be the review text and the output is the review star. Here are the steps to prepare data, train the model and test the result. The script can be found in the notebook.

1. Load the dataset from my local folder and transform the dataset to csv format and split the dataset
2. Build vocabulary and load pre-trained language model 
3. Define CNN for text classification
4. Deine the training process
5. Define network init function
6. Predict the test data

So the project is done on my own laptop and I just uploaded the notebook that I used for this project. The repo only contains the notebook and there is no command line needed. The main purpose of the project is to build a text classification CNN to accurately predict the review score. I understand the format and structure of the notebook can be improved and I will continue to work on it after the course.
