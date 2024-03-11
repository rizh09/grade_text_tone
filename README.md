

# Tone Grading Script User Guide

## Overview
The Tone Grading script is a Python program that analyzes the tone of an email text and categorizes it into one of three tones: Formal, Friendly, or Assertive. It utilizes machine learning and natural language processing techniques to perform text classification based on predefined criteria words.

## Prerequisites
- Python installed on your machine
- Required Python packages: `nltk` and `scikit-learn`
- NLTK stop words dataset downloaded (explained in the guide)

## Usage
1. Clone or download the script from the repository to your local machine.
2. Install the required Python packages by running the following command in your terminal or command prompt:
   ```
   pip install nltk scikit-learn
   ```
3. Download the NLTK stop words dataset by running the following Python code once in your Python environment:
   ```
   import nltk
   nltk.download('stopwords')
   ```
4. Open a terminal or command prompt and navigate to the directory where you saved the Tone Grading script.
5. Run the script using the following command:
   ```
   python tone_grader_ml.py
   ```
6. The script will prompt you to enter the email text. Type or paste the email text and press Enter.
7. The script will analyze the tone of the email text and display the predicted tone category as the output.

## Understanding the Script
The Tone Grading script performs the following steps:
1. It defines criteria words for each tone category, such as formal, friendly, and assertive words.
2. The script prepares the training data by combining the criteria words into categories.
3. A TF-IDF vectorizer is created with stop word removal using the NLTK stop words dataset.
4. The training vectors are created by transforming the training data using the TF-IDF vectorizer.
5. A linear SVM classifier is trained on the training vectors and corresponding category labels.
6. The input email text is transformed into a vector using the same vectorizer.
7. The trained classifier predicts the tone category based on the vectorized input.
8. The predicted tone category is displayed as the output.

## Customization
If you wish to customize the criteria words or add more tones, you can modify the script as follows:
1. Update the criteria words for each tone category in the `formal_words`, `friendly_words`, and `assertive_words` lists.
2. Add or modify the categories in the `categories` dictionary, mapping each category to its corresponding criteria words.
3. Re-run the script to incorporate the changes in the tone grading process.

Please note that creating a large and representative dataset for each tone category is crucial for accurate tone grading. You may need to collect and label a diverse set of emails or texts to achieve better results.

