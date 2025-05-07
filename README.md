# Yelp Sentiment Analysis

This project performs sentiment analysis on Yelp restaurant reviews using text mining techniques and various machine learning models. It aims to classify review sentiment (positive or negative) and assess the effectiveness of different sentiment lexicons and predictive algorithms.

## 📊 Project Overview

Using a sample of restaurant reviews from Yelp, this project:
- Conducts exploratory data analysis to understand review distributions and inconsistencies
- Identifies sentiment-bearing words using star ratings and average word scores
- Compares three sentiment dictionaries: Bing Liu, NRC, and AFINN
- Applies dictionary-based sentiment scoring for binary classification
- Builds and evaluates predictive models using:
  - Naive Bayes
  - Lasso Logistic Regression
  - Random Forest
  - XGBoost
- Compares model performance when using only dictionary terms vs. a broader vocabulary
- Explores the application of ChatGPT API for sentiment extraction and star rating prediction

## 🧰 Tools & Libraries

- **R Programming Language**
- Key Libraries:
  - `tidytext`, `tm`, `textdata`, `tidyverse`
  - `glmnet`, `randomForest`, `xgboost`, `caret`
  - `ggplot2`, `dplyr`, `tibble`

## 🧪 Methodology

1. **Data Exploration**: Analyzed distributions of reviews across businesses and star ratings.
2. **Sentiment Labeling**: Converted star ratings to binary sentiment classes for modeling.
3. **Word-Level Sentiment**: Computed average ratings for words to identify top positive and negative terms.
4. **Dictionary Matching**: Evaluated overlap of dataset vocabulary with Bing, NRC, and AFINN lexicons.
5. **Dictionary-Based Scoring**: Aggregated sentiment scores from each dictionary and used them for naive sentiment classification.
6. **Model Building**:
   - Split data into training and testing sets
   - Constructed Document-Term Matrices (DTM) using tf-idf and term frequency
   - Built models using both lexicon-based and full-term DTMs
   - Compared model performances using accuracy, precision, recall, F1-score, and AUC
7. **Large Language Models**:
   - Used ChatGPT API to classify sentiment and extract aspects
   - Compared ChatGPT performance with traditional models

## 📁 Project Structure

- `SentimentAnalysisRestaurantReviews.Rmd`: Main R Markdown file with all code, visualizations, and analysis
- `data/`: Preprocessed Yelp reviews and business metadata
- `output/`: Plots, model evaluation results, and ChatGPT responses (assumed)

## 📈 Key Findings

- **AFINN** lexicon outperformed Bing and NRC in naive classification.
- **Random Forest** and **XGBoost** models using broader token sets showed the best classification performance.
- Combining all three dictionaries improved model results marginally.
- **ChatGPT** produced sentiment classifications comparable to models and provided granular insights into sentiment aspects.

## ✅ Conclusion

The project demonstrates that while sentiment lexicons provide a useful baseline, machine learning models—especially those trained on broad vocabularies—offer superior performance. Incorporating LLMs like ChatGPT adds qualitative depth, enabling richer interpretation of review sentiment.

### 📂 Dataset
The sample dataset used in this project contains 42,000+ raw Yelp restaurant reviews with star ratings, review text, and business-related metadata.  
🔗 [Download from Google Drive] **https://drive.google.com/file/d/1Eh5Xk2GaCTUkeG-kv2oPIcDuDa9bPFFZ/view?usp=drive_link**

## 🙌 Credits

This project was completed by Rameen Shakeel as part of the IDS 572: Data Mining for Business Analytics course at the University of Illinois Chicago in Spring 2025.
