# Sexist-Tweet-Detector


This project aims to classify tweets as sexist or non-sexist using both traditional machine learning models and transformer-based models like RoBERTa. The repository includes scripts for data preprocessing, training, evaluation, and prediction.

---

## **Project Structure**

- **`eda_ml.ipynb`**  
  This notebook contains:
  - Exploratory Data Analysis (EDA)
  - Text preprocessing and encoding using Bag of Words (BoW) and TF-IDF
  - Comparison of machine learning models: SVM, Naive Bayes, and Random Forest
  - Hyperparameter tuning for SVM (with TF-IDF) and Random Forest models

- **`Roberta_training.ipynb`**  
  This notebook focuses on transformer-based models:
  - Fine-tuning the RoBERTa model for the sexist/non-sexist classification task
  - Encoding, training, and evaluation steps
  - **The final RoBERTa model can be downloaded during the execution of this notebook** and saved locally.

- **`robertatweet_final.ipynb`**  
  The final script for:
  - Preprocessing new data
  - Text encoding
  - Predictions using the pre-trained RoBERTa model downloaded and saved during the execution of `Roberta_training.ipynb`.

- **`data_hate_no_hate.csv`**  
  The dataset used to train and evaluate the models. It includes tweets with sexist and non-sexist labels, along with annotator demographics.

---

## **Dataset Description**

The dataset, `data_hate_no_hate.csv`, has the following columns:

| Column                  | Description                                                                                              |
|-------------------------|----------------------------------------------------------------------------------------------------------|
| **tweet**               | The tweet text to be analyzed.                                                                          |
| **number_annotators**   | The total number of annotators who labeled the tweet.                                                   |
| **annotators**          | A list of IDs representing the annotators.                                                              |
| **gender_annotators**   | The genders of the annotators (e.g., 'M' for male, 'F' for female).                                      |
| **age_annotators**      | The age ranges of the annotators (e.g., '18-22', '23-45', '46+').                                       |
| **ethnicities_annotators** | The self-reported ethnicities of the annotators.                                                     |
| **study_levels_annotators** | The educational levels of the annotators (e.g., Bachelor's degree, Master's degree).                |
| **countries_annotators** | The countries of origin for the annotators.                                                            |
| **labels**              | The annotations for the tweet, indicating whether it is sexist (**YES**) or non-sexist (**NO**).        |
