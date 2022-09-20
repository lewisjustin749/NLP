# NLP
Perform a set of preprocessing on the data set and then build a high-performance machine learning model that can be used to predict whether a given news is fake or true.

**Dataset**

news.csv

This data set contains a list of articles. Some of them are fake news and some of them are true news. 

The data set contains the title, text, subject, and date of the article. The target column has binary values 1 or 0, where 1 presents true news and 0 represents fake news.

**1.Load Data and perform basic EDA**
  * import libraries necessary libraries and perform necessariy nltk download operations
  * As part of understanding how the columns are separated, read the file using the open function and create a list and show the first 10 items in the list
  * Based on your observation on how the data are separated, load the data set into pandas data frame and show the first 5 and last 5 rows
  * See whether there are any null values and remove all the rows with any null values, and then show again that there are no more null values
  * Generate a counterplot to show the number of news in each subject
  * Generate a counterplot to show the number of news in each category (fake/ True)
  * Generate two word clouds, one for fake news and one for true news, and observe the most frequent words in each category and just write your observation on them.
  * Create a column "AllText" that has the concatenated subject, title, and text [For example, for each news we have the subject, title, and text. We want a column that has all of this together as a large string]  [See the example answer with the majority vote in this link: https://stackoverflow.com/questions/39291499/how-to-concatenate-multiple-column-values-into-a-single-column-in-pandas-datafra (Links to an external site.) )
  * Using the dataframe's copy function, save the data frame into another dataframe so that you can use it later
  * Drop the title, text, subject, and date columns from the data frame as we will not use them separately. We have all the text in a single column that you have generated above
  * Calculate the length of each text (I mean AllText column) and put them in a length column
  * Plot two histograms to see the distribution of the lengths. One for fake news and one for true news. Write in words about the plots
  * Write in Words: What is TFIDF? How to create bag of words using sklearn? And how to generate TFIDF for the bag of words?

**2.Train Test Split**
  * Import related libraries and perform train test split. Keep 20% data in the test set
  * Using a count plot show how many real and fake news do we have in the training set and how many in the test set

**3.Training and Testing Fake news classifier using MultinomialNB**
  * Create a pipeline that will use countVectorizer with the function you have created earlier for data preprocessing, then use Tftransformer and then use the NaiveBayes classifier
  * Fit the pipeline and then perform prediction
  * Generate classification report and confusion matrix (you have to achieve at least 96% accuracy for the test set to receive full credit)
  * Discuss the performance like how good the model is overall, how good is it in predicting fake news, and how good is it in predicting true news.
  * Copy a part of any news of your choice from a news website and then use the model to predict whether is it true or not. 

**4.Training and Testing a Deep Neural Network**
  * Import related library for using MLPClassifier from sklearn neural netowrk.
  * Create a pipeline like 3i, for MLPClassfier you should use at least two layers and also should verbose = 2 (you can use other parameters as you wish or use the one you see from the uploaded google colab)
  * Fit the pipeline and then perform prediction
  * Generate classification report and confusion matrix (You have to achieve at least 99% accuracy to receive full credit for this model)
  * Discuss the performance like how good the model is overall, how good is it in predicting fake news, and how good is it in predicting true news.
  * Use the same news you have used above and then use the model to predict whether is it true or not. 
  * Discuss any difference in performance between this model and NB model
