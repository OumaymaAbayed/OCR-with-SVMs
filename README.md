# Optical Character Recognition with Support Vector Machines (SVMs) 🅰️🅱️  

## Overview 📚  
This project focuses on developing an Optical Character Recognition (OCR) system using Support Vector Machines (SVMs). The goal is to classify individual English alphabetic characters (A-Z) based on given features extracted from images.  

## Table of Contents 📑  
1. [Introduction](##introduction)  
2. [Features](#features) 
3. [Model Evaluation](#model-evaluation)  
4. [Improvements](#improvements)  
5. [Technologies Used](#technologies-used)  
6. [Contributing](#contributing)  
7. [Credit](#credit)  

## Introduction 🚀  
Optical Character Recognition is a critical task in computer vision that involves recognizing text from images. This project simplifies the OCR process by focusing on character recognition using SVM, utilizing a cleaned dataset where each character is represented as a feature vector.  

## Features 🌟  
- Trains an SVM classifier to recognize characters A-Z.  
- Utilizes a dataset of 20,000 preprocessed character images.  
- Evaluates model performance and accuracy.  
- Implements kernel functions to improve classification accuracy.  

This project uses R, so make sure you have R and RStudio installed. Use Google Colab for executing the code online.

Install Required Packages:
Install the necessary R packages in your environment:

r
install.packages("kernlab")  
Usage 📈
To run the OCR model, follow these steps:

Load the dataset:

r
letters <- read.csv("letter-recognition.csv")  
Train the SVM model:

r
library(kernlab)  
letter_classifier <- ksvm(letter ~ ., data = letters_train, kernel = "rbfdot")  
Make predictions and evaluate:

r
letter_predictions <- predict(letter_classifier, letters_test)  
table(letter_predictions, letters_test$letter)  

## Model Evaluation 📊
The model accuracy is determined by comparing predicted characters against the actual labels in the testing set. The final performance metrics include the overall accuracy and confusion matrix to understand misclassifications.

## Improvements 📈
To enhance the performance of the OCR system, consider the following:

Explore additional feature engineering techniques.
Implement cross-validation for more reliable evaluation.
Experiment with different SVM kernel functions.
Try alternative machine learning models or deep learning techniques such as CNNs.

## Technologies Used 💻
R: The programming language used for implementing the model.
kernlab: R package for Support Vector Machines.
Google Colab: Online platform used for coding and sharing the project.


## Credit
UCI ML: https://archive.ics.uci.edu/
kaggle: https://www.kaggle.com/datasets/nishan192/letterrecognition-using-svm
