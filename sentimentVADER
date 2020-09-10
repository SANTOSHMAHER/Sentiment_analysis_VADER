#!/usr/bin/env python3
# Refrence Monkylearn
"""
 Extract the sentiment score (-1 for negative, 0 for neutral and 1 for positive) from any given text using the vaderSentiment library. 

VADER stands for Valence Aware Dictionary and sEntiment Reasoner, which is a lexicon and rule-based sentiment analysis tool that is specifically attuned to sentiments expressed in social media, and works well on text from other domains.

Installing the requirements for this tutorial:

pip install vaderSentiment
Created on Thu Sep 10 19:20:00 2020

@author: santoshmaher
"""


from vaderSentiment.vaderSentiment import SentimentIntensityAnalyzer

# init the sentiment analyzer
sia = SentimentIntensityAnalyzer()
##
sentences = [
    "I don’t find the app useful: it’s really slow and constantly crashing",
    "Exoplanets are planets outside the solar system",
    "This is sad to see such bad behavior"
]

for sentence in sentences:
    score = sia.polarity_scores(sentence)["compound"]
    print(f'The sentiment value of the sentence :"{sentence}" is : {score}')
##
for sentence in sentences:
    print(f'For the sentence "{sentence}"')
    polarity = sia.polarity_scores(sentence)
    pos = polarity["pos"]
    neu = polarity["neu"]
    neg = polarity["neg"]
    print(f'The percententage of positive sentiment in :"{sentence}" is : {round(pos*100,2)} %')
    print(f'The percententage of neutral sentiment in :"{sentence}" is : {round(neu*100,2)} %')
    print(f'The percententage of negative sentiment in :"{sentence}" is : {round(neg*100,2)} %')
    print("="*50)
