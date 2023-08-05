# Sentiment-Analysis-on-Movie-Reviews-using-Python
Sentiment Analysis on Movie Reviews using Python

We train many different ML models with different Parameters on the rotten tomatoes dataset to classify reviews into 5 classes: negative, somewhat negative, neutral, somewhat positive, positive.

About the Dataset:

The dataset is comprised of tab-separated files with phrases from the Rotten Tomatoes dataset. The train/test split has been preserved for the purposes of benchmarking, but the sentences have been shuffled from their original order. Each Sentence has been parsed into many phrases by the Stanford parser. Each phrase has a PhraseId. Each sentence has a SentenceId. Phrases that are repeated (such as short/common words) are only included once in the data.

train.tsv contains the phrases and their associated sentiment labels. We have additionally provided a SentenceId so that you can track which phrases belong to a single sentence.
test.tsv contains just phrases. You must assign a sentiment label to each phrase.
The sentiment labels are:

0 - negative
1 - somewhat negative
2 - neutral
3 - somewhat positive
4 - positive

 

Preprocessing:

Split the data into train, validation and test data. Further, we split the sentences into words and we also remove unwanted words (called stopwords) as well as we remove the punctuations. After this, we then split the train, validation and test sets into their respective X and Y values so that we can use it for training the model.

 

Models:

We try many different models and each of them with different parameters so that we can know which model is the best for us.

 

Firstly we use Logistic Regression along with count vectorizer and we get the following accuracy and precision:

0.7304348754752445 0.7281238636213457

We also create a plot of the different metrics

 

Next, we use the LinearSVC support vector machine along with the count vectorizer and we get the following accuracy and precision:

0.7492097056687599 0.7459823196224461

We also create a plot of the different metrics

 

Next, we try the Multinomial Naive Bayes along with the count vectorizer and we get the following accuracy and precision:

0.6806249733008672 0.6718214289545724

We also create a plot of the different metrics

 

Next, we try Logistic regression with tfidf vectorizer and we get the following accuracy and precision:

0.7083066342005212 0.7102583566141313

We also create a plot of the different metrics

 

Next, we try LinearSVC support vector machine with tfidf vectorizer and we get the following accuracy and precision:

0.7713806655559827 0.7676422371873227

We also create a plot of the different metrics

 

Finally comparing all the accuracies and precisions along with the graphs that we created, we choose Linear Regression with count vectorizer as the best model and we also use grid search to find the best parameters.

We create the model again with these best parameters and run the code and make the predictions on the test data set and then we save it to another csv file.
