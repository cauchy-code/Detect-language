# Detect-language
Detect the language from the written sentence:
1)Importing Libraries: You start by importing the necessary libraries. This includes pandas for data manipulation, numpy for numerical computations, and scikit-learn (sklearn) for machine learning functionalities.
2)Loading Data: You load the dataset from a CSV file hosted on GitHub using pd.read_csv() function from pandas. The dataset contains text samples and their corresponding languages.
3)Data Exploration: You print the first few rows of the dataset using data.head() to get a sense of its structure. Then, you check for any missing values in the dataset using data.isnull().sum() and examine the distribution of languages using data["language"].value_counts().
4)Preparing Data: You separate the features (x) and the target variable (y) from the dataset. The features (x) are the text samples, while the target variable (y) is the language label.
5)Feature Extraction: You use CountVectorizer() from scikit-learn to convert the text data into a numerical format suitable for machine learning algorithms. This step transforms the text data into a matrix of token counts.
6)Splitting Data: You split the dataset into training and testing sets using train_test_split() function. This allows you to train the model on a portion of the data and evaluate its performance on unseen data.
7)Training the Model: You initialize a Multinomial Naive Bayes classifier using MultinomialNB() and train it on the training data using model.fit().
8)Model Evaluation: You evaluate the performance of the trained model on the testing data using model.score().
9)Prediction: You prompt the user to input a text, then convert it into the numerical format using the same CountVectorizer instance used earlier (cv.transform([user]).toarray()). Finally, you use the trained model to predict the language of the input text and print the output.
