# Sentimental-Analysis-using-LSTM-
## Objective:
Given a review, determine whether the review is positive (Rating of 4 or 5) or negative (rating of 1 or 2).

<br>
[Q] How to determine if a review is positive or negative?<br>
<br> 
[Ans] We could use the Score/Rating. A rating of 4 or 5 could be cosnidered a positive review. A review of 1 or 2 could be considered negative. A review of 3 is nuetral and ignored. This is an approximate and proxy way of determining the polarity (positivity/negativity) of a review.

## [1] Data Cleaning: 

It is observed (as shown in the table below) that the reviews data had many duplicate entries. Hence it was necessary to remove duplicates in order to get unbiased results for the analysis of the data.Also we are sorting the data wit respect to time here 

## [2].  Text Preprocessing:

Now that we have finished deduplication our data requires some preprocessing before we go on further with analysis and making the prediction model.

Hence in the Preprocessing phase we do the following in the order below:-

1. Begin by removing the html tags
2. Remove any punctuations or limited set of special characters like , or . or # etc.
3. Check if the word is made up of english letters and is not alpha-numeric
4. Check to see if the length of the word is greater than 2 (as it was researched that there is no adjective in 2-letters)
5. Convert the word to lowercase
6. Remove Stopwords
7. Finally Snowball Stemming the word (it was obsereved to be better than Porter Stemming)<br>


<h2><font color='red'>[3.2] Preparing the data for input to the model</font></h2>

### We want to input the data in the format of padded vectors which comprises of ranks of words,it is a manual implementation of text tokenizer.So the methodology to be followed is:
   - Counting the number of times a particular word appears in the training corpus.
   - Giving the word with most number of occurence rank 1 and so on 
   - Sorting the list to get all the ranks in the corpus

## # WE will use three different architectures for model implementation
- Model with 2 hidden layers 
- Model with 3 hidden layers
- Model with 5 hidden layers

 __In Each Architecture We will implement using Adam optimizer__:
 
 - 1 LSTM(100) + 2 DROPOUT + 1 BATCHNORMALIZATION + ADAM OPTIMIZER
 
  <img src = https://github.com/yatscool007/Sentimental-Analysis-using-LSTM-/blob/master/lstm_images/mod1.PNG>
  
  
 - lstm(100 cells) + lstm(50 cells)+ Sigmoid + Adam Optimizer + dropout + BatchNormalization
 
 <img src = https://github.com/yatscool007/Sentimental-Analysis-using-LSTM-/blob/master/lstm_images/mod2.PNG>
 
 
 - 2 Convolutional layer + Maxpooling +  LSTM(80) + BatchNormaliztion + Dropout + Adamoptimizer
 
 <img src = https://github.com/yatscool007/Sentimental-Analysis-using-LSTM-/blob/master/lstm_images/mod3.PNG>
 
## Results:

<img src = https://github.com/yatscool007/Sentimental-Analysis-using-LSTM-/blob/master/lstm_images/res.PNG>
