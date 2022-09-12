# chatbot_project

A company holds an event that has been given the deserved promotion through marketing in hopes of attracting as big an audience as possible. Now, it’s up to the customer support team to guide the audience and answer any queries. Providing high-quality support and guidance is the challenge. The chatbot is very helpful for its 24/7 presence and ability to reply instantly.  


![download](https://user-images.githubusercontent.com/94167271/189384486-98d627c2-5b2e-449f-8fa2-c47cf69822b9.png)

#### Objective: To develop a real-time chatbot to engage with the customers in order to boost their business growth by using NLP and Speech Recognition.

Domain:  Customer Support

 Analysis to be done: Create a set of prebuilt commands or inputs as a dataset. Here, we use command .json as Dataset that contains the patterns we need to find and the responses we want to return to the user.
 
### Prerequisites
 
 pip install tensorflow, keras, pickle, nltk
 
 Intents.json – The data file which has predefined patterns and responses.
 
 train_chatbot.py – In this Python file, we wrote a script to build the model and train our chatbot.
 
 Words.pkl – This is a pickle file in which we store the words Python object that contains a list of our vocabulary.
 
 Classes.pkl – The classes pickle file contains the list of categories.
 
 Chatbot_model.h5 – This is the trained model that contains information about the model and has weights of the neurons.

### import necessary packages

    import nltk
    from nltk.stem import WordNetLemmatizer
    lemmatizer = WordNetLemmatizer()
    import json
    import pickle

    import numpy as np
    from keras.models import Sequential
    from keras.layers import Dense, Activation, Dropout
    from keras.optimizers import SGD
    import random 
    import pandas as pd

    This is how our intents.json file looks like.

![image](https://user-images.githubusercontent.com/94167271/189677804-c07451ca-3d56-4154-a488-070a36cbf903.png)

###  Preprocess data

When working with text data, we need to perform various preprocessing on the data before we make a machine learning or a deep learning model. Based on the requirements we need to apply various operations to preprocess the data.

Tokenizing is the most basic and first thing you can do on text data. Tokenizing is the process of breaking the whole text into small parts like words.

Here  iterate through the patterns and tokenize the sentence using nltk.word_tokenize() function and append each word in the words list. We also create a list of classes for our tags.

Now we will lemmatize each word and remove duplicate words from the list. Lemmatizing is the process of converting a word into its lemma form and then creating a pickle file to store the Python objects which we will use while predicting.

![Screenshot (240)](https://user-images.githubusercontent.com/94167271/189691574-e5cbce50-ff66-498e-8367-4db9586cde68.png)


We have our training data ready, now we will build a deep neural network that has 3 layers. We use the Keras sequential API for this. After training the model for 200 epochs, we achieved 100% accuracy on our model. Let us save the model as ‘chatbot_model.h5’.

### Final result of chatbot 

![Screenshot (237)](https://user-images.githubusercontent.com/94167271/189680822-a581d3f6-9dd1-48ff-b0a8-9b822c576c3b.png)

Summary

In this project, we understood about chatbots and implemented a deep learning version of a chatbot in Python which is accurate. Can customize the data according to business requirements and train the chatbot with great accuracy. Chatbots are used everywhere and all businesses are looking forward to implementing bot in their workflow.
