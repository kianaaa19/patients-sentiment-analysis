# Sentiment Analysis of German Reviews

## Overview
This document provides a comprehensive overview of a project that aims to perform sentiment analysis on German texts. The primary focus is on analyzing reviews provided in German, particularly targeting feedback on healthcare services. The goal is to classify the sentiments expressed in these reviews accurately, allowing for better understanding and improvement of services offered.

## Project Understanding
In this project, we dive into the sentiment analysis of texts extracted from reviews available in the Excel file named `Eberswaldeneu.xlsx`. Sentiment analysis helps businesses and organizations gauge customer opinions, which can significantly influence improvements in service delivery. By conducting this analysis, we can classify reviews into positive, negative, and neutral sentiments.

## Data Understanding
The dataset comprises reviews organized by doctor names, with information drawn from multiple sheets of an Excel file. The initial inspection revealed a total of 268 rows with various attributes:
- **Doctor**: The name of the doctor associated with the review.
- **Review**: The text of the patient's review about the doctor.

### Sample Data Summary
- **Number of Reviews**: 245 after preprocessing.
- **Unique Doctors**: 21 different doctors providing services.

## Data Processing
Data processing involves several steps to clean and prepare the data for analysis:
1. **Read Excel File**: All sheets from `Eberswaldeneu.xlsx` are read.
2. **Preprocess Data**: The reviews are cleaned by ensuring that missing values are appropriately filled, and rows without doctor names are removed.
3. **Combine Reviews**: Reviews belonging to a single doctor are organized.
4. **Final Dataset**: The processed data consists of two columns: `Doctor` and `Review`.

## Exploratory Data Analysis (EDA)
During the exploratory data analysis stage, we inspect the processed data to understand distributions and trends within the `Review` and `Doctor` columns. Visualization techniques such as bar charts and histograms were implemented to highlight sentiment distributions and the frequency of reviews across different doctors.

## Modeling
For sentiment analysis, we utilized the Spark NLP from John Snows Lab library along with BERT pre-trained models to build a classification pipeline. Key steps include:
- **Document Assembly**: Prepare the reviews for processing.
- **Feature Extraction**: Use sentence embeddings to understand the context of each review.
- **Sentiment Classification**: Implement a sentiment classifier to assign sentiment labels.

## Evaluation
The performance of the sentiment analysis model was evaluated based on the outputs of the classification stages, with results displayed in a formatted table. The system aims to specifically output positive or negative sentiment labels, which can then be compared with actual review sentiments for validation.

## Conclusion
The sentiment analysis project demonstrates the power of NLP techniques in analyzing and understanding customer feedback in the healthcare sector. By effectively processing and interpreting sentiment from German text reviews, healthcare organizations can gain valuable insights into patient perceptions, ultimately paving the way for service improvements and enhanced patient satisfaction. The project resulted in categorized sentiments for each review, yielding a deeper understanding of the strengths and weaknesses of the healthcare providers involved.
