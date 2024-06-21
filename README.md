## Neutral Language Processing NLP

### Description of the dataset used:
This is a Python script performing sentiment analysis and similarity comparison on Amazon’s
product reviews dataset, the data set provides a row-structured information about products
contain 19 columns and 34660 rows.
The columns includes (id, name, asins, brand, categories keys, manufacturer, reviews date,
reviews dateadded, reviews date seen, reviews didpurchase, reviews doRecommend,
reviews id, reviews numHelpful, reviews rating, reviews sourceURLs, reviews text, reviews
title, reviewsuserCity).
Our target variable in this task is ‘reviews text’.

I will use pandas data frame, I will load the en_core_web_sm and en_core_web_md spacy model to
implement natural language processing tasks, these models will help analyse and classify the
sentiment of the product reviews, and compare them.

### **Note:**
- en_core_web_sm is a small English pipeline trained on written web text (blogs, news
and comments), that includes vocabulary, syntax and entities.
- En_core_web_md is a medium-sized English model trained on written web text
(blogs, news, comments), that includes a tagger, a dependency parser, a lemmatizer,
a named entity recognizer and a word vector table with 20K unique vectors.

### Pre-processing steps:
First, load the dataset in to pandas DataFrame. Then display the necessary information in order to
pre-process the data. Clean the defined text to use it for the following analysis by using lowercase
function then removing the null values and the stop_words.

### About python script steps:
- First, import the necessary libraries, Pandas, spacy.
- Second load the spaCy English model for sentiment and similarity analysis,
en_core_web_sm, and en_core_web_md.
- Add SpacyTextBlob as a pipeline component for sentiment analysis.
- Load the dataset into a pandas DataFrame.
- Display information about the dataset and the reviews.text column.
- Explore the data.
- Preprosessing: Drop rows where reviews are missing and print the new total.
- Preprosessing: we still need to remove stop words and punctuations.
- Create function ’prep_text’ to remove stop words and punctuations.
- Create function ‘product_review’ to perform polarity and sentiment analysis.
- Create function ‘compare’ to perform similarity comparison between two reviews.
- Comparing the similarity of two reviews, by calling ‘compare’ function to print the
similarity Score of 0.809 close to 1, which mean strong similarity.
- Test the sentiment analysis on a sample of product reviews, by calling the functions
Sentiment_A and prep_text with the first and second reviews in the dataset,
dataframe['reviews.text'][0], dataframe['reviews.text'][1].
- Apply text pre-processing and sentiment analysis to a subset of clean_data.
- Print the first rows of the resulting clean_data DataFrame.
- Print note to user to explain the reviews feelings using if-else.

### Evaluation of results:
The model fail to analyse the first review after the removal of the stop_words, which affect
the results of polarity.
The model successfully applied the sentiment analysis on the second review.
The model successfully applied on the similarity comparison.
The results was:
 
- Review 1: Negative polarity of -0.05 then, positive polarity of 0.325 and subjectivity of 0.783.
- Review 2: Positive polarity of 0.8 and subjectivity of 0.825.
