# Hacklytics'23: Angela the ChatBot

## Inspiration
We knew we wanted to do something in the healthcare track and were inspired to focus on mental health when we saw the problem statements from Elevance Health. Mental health is such a pressing issue that can have major effects on a person and is unique in that it can be something that people feel to embarrassed to speak about or don't take as seriously as their physical health. 

## What it does
Angela is a chatbot that determines if it's time for a person to reach out for help based on conversations it has with the person. Angela will ask you to explain where you are mentally, and the details surrounding how you might have gotten to this state. She then uses this information to decide if you aren't doing well and need to talk to someone or maybe even just helps you feel better herself. 

## How we built it
The dataset we chose identifies 15 different cognitive distortions but because we had such limited data, we decided to combine them into one category called the presence of cognitive distortion. Since most of the data pointed to the presence of cognitive distortions, we decided to augment our data with twitter data from the Twitter API. We then cleaned the data and built a Long Short-Term Memory (LSTM) model to help us classify the presence of cognitive distortion. Finally, we combined this model with Python's Tkinter library to create the chatbot interface.

## Challenges we ran into
The accuracy of the model is high but when we combined it with the Tkinter interface it started taking a long time to identify if something was a cognitive distortion. Basically, it takes Angela a very long time to tell someone if they need to reach out for help when responding through the chatbot interface.
There is a scarcity of annotated data to help identify each sort of cognitive distortion. As a result, we combined all cognitive distortions into a single category that shows the presence of cognitive distortion. The absence of cognitive distortion was indicated by the other target column. We detect a class imbalance due to the dominance of cognitive distortion courses. So, utilising an API and sentiment analysis, we created positive cases from a Twitter database. To address the data imbalance issue, we consolidated and produced the final dataset. Several studies have indicated that data from Twitter and other social media platforms can be used to detect depression, anxiety, and other mental health concerns.

## Accomplishments that we're proud of
By examining multiple research articles and performing analysis and visualisations on datasets, we were able to identify the problem area, which is the requirement for anonymity and trust in helping people seeking treatment and therapy for mental health difficulties. Then, we explored many methods to determine the best method for detecting the presence of cognitive dysfunction with little data. It was novel and difficult to train a dataset and then use the results to develop a chatbot in 36 hours. Furthermore, our team's two members are practically oceans away and in different time zones.

## Datasets used:
1. Mental Health Tech Survey 2014
Source: Kaggle
2. Dataset_Cognitive_Distortions.tsv 
Authors: Mariama C. Djalo D.
Source: GitHub
3. Twitter Dataset

## What's next for Angela the Chatbot
We would like to make Angela more robust by making it so she can handle even more categories than just a negative or positive assessment of the person she's talking to. We'd also like to speed up the UI to better meet the purpose of a self-assessment chatBot.
