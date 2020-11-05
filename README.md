# Financial-Tweets-Sentiment-Analysis

Objective: The aim of this project is to conduct sentiment analysis on financial tweets by making use of polarity scores. Through this attempt, we can classify different tweets as having a Positive/Negative/Neutral sentiment.
Dataset: The dataset used is outsourced from Kaggle.com. It contains tweets posted by a number of publicly listed companies, for example, Morgan Stanley and YahooFinance. There is a total of 28,878 tweets.

Methodology:
  1) Sourcing the data – The data is directly sourced from a .csv file obtained from Kaggle.
  2) Cleaning & pre-processing the data – For this mini project, only the text of the tweets was utilized. Other attributes like id, timestamp, company name, etc. were not required. All URLs, ‘@’ signs and other characters apart from ‘a-z’ or ‘A-Z’ had to be dropped to make sure the data was clean and formatted. Furthermore, all the letters were converted to lowercase and a space was inserted between each word in a sentence. The Natural Language Tool Kit was used to import the Porter Stemming Algorithm and stop words of the English language. The PS Algorithm removed the common morphological and in flexional endings from words. All the stop words that were imported from the library were also dropped. Both these techniques helped reduce noise in the data in order to make the sentiment analysis more accurate and reliable.
converted to
  3) Analysing the sentiment of all tweets – The polarity of each cleaned tweet was calculated using the VADER algorithm imported from the NLTK package. VADER maps the lexical features to sentiment scores. This sentiment score for any text is calculated by adding up the intensities of the words in that text. The SentimentIntensityAnalyser function takes a string as a parameter and returns the string’s positive, negative, neutral scores. It also returns a compound score which is calculated by normalizing the previous three scores. After studying similar models on the internet, I decided to categorize the sentiments based on the following compound values;
· Negative: <= -0.2
· Positive: >= 0.2
· Neutral: > 0.2 & < -0.2

Results: Calling the ‘findSentiment’ function prints the positive, negative, neutral, compound sentiment scores and returns the sentiment of the text.
