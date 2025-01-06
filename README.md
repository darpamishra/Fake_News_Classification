# Fake_News_Classification

## About the Dataset

The WELFake dataset is a curated collection of 72,134 news articles, meticulously balanced between 35,028 real and 37,106 fake news entries. By merging data from Kaggle, McIntire, Reuters, and BuzzFeed Political datasets, it offers a diverse and robust platform for fake news detection tasks. This combined dataset addresses overfitting challenges and enhances the effectiveness of machine learning models by providing richer textual data.

## Dataset Structure

Serial Number: Unique index for each entry.

Title: The headline of the news article.

Text: The main content of the news article.

Label: Binary classification of the article:

0: Fake

1: Real

This dataset is published in the IEEE Transactions on Computational Social Systems (DOI: 10.1109/TCSS.2021.3068519).

## Prerequisites

Ensure the following Python libraries are installed before using the dataset:

numpy

pandas

nltk

scikit-learn

seaborn

matplotlib

To suppress unnecessary warnings, use the warnings library.

## Workflow for Data Analysis

### Step 1: Load and Clean the Data

Read the dataset into a Pandas DataFrame.

Drop irrelevant columns such as Unnamed: 0.

Handle missing values by replacing them with blank spaces.

### Step 2: Visualize Data Distribution

Plot a count chart using Seaborn to visualize the proportion of fake versus real news articles.

### Step 3: Preprocess Text Data

Apply the Porter Stemmer to preprocess the text in the title column. The process includes:

Lowercasing all text.

Removing non-alphabetic characters.

Tokenizing the text into words.

Removing stopwords.

Stemming the words to their root forms.

After preprocessing, drop the text column to focus solely on the title for analysis.

### Step 4: Convert Text to Features

Use TfidfVectorizer to transform the title column into numerical vectors, enabling machine learning compatibility.

### Step 5: Train-Test Split

Split the dataset into training and testing sets (80% training, 20% testing).

Stratify the split to maintain label distribution consistency.

### Step 6: Train a Logistic Regression Model

Train a Logistic Regression model on the training dataset.

### Step 7: Evaluate Model Performance

Evaluate the model using the following metrics:

Accuracy Score: Measures the overall correctness of predictions.

Confusion Matrix: Visualizes the count of true positives, true negatives, false positives, and false negatives.

Classification Report: Provides precision, recall, F1-score, and support for each class.

### Step 8: Make Predictions

Test the model with individual samples to predict whether a news article is fake or real, and compare predictions with actual labels.


# Results and Outputs

## Key Metrics

Accuracy: The accuracy of the model on the test data is displayed.

Confusion Matrix: A heatmap visualizes the prediction breakdown.

Classification Report: Comprehensive metrics for each class are presented.

## Sample Prediction

Example predictions demonstrate the functionality and reliability of the model.
