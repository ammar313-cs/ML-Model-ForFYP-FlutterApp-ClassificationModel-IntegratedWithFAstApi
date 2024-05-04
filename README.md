# Edible Items Analysis and Classification with FastAPI Endpoint for Testing in Flutter App

This repository contains code for preprocessing, analyzing, and classifying items from JioMart datasets. The code is designed to perform various tasks including data preprocessing, machine learning model training, API implementation using FastAPI, and exposing the API publicly using ngrok.

## Overview

The provided code snippet performs the following tasks:

### Data Preprocessing and Exploration:
- Imports the Pandas library to read and explore the dataset stored in the CSV file "jio_mart_items.csv".
- Identifies unique categories and subcategories present in the dataset.
- Assigns labels to subcategories based on whether they are edible or not.

### Model Training and Evaluation:
- Loads additional dataset "products_data.csv" and merges it with the main dataset.
- Splits the merged dataset into train, validation, and test sets.
- Utilizes TF-IDF vectorization to convert text data into numerical features for model training.
- Trains a logistic regression model with cross-validation and evaluates its performance on validation and test sets.

### API Implementation with FastAPI:
- Implements an API endpoint `/classify` to classify multiple items using the trained logistic regression model.
- Implements an API endpoint `/clean_strings` to clean strings in JSON data.

### ngrok Setup:
- Authenticates and sets up ngrok to create a public URL for the FastAPI server.

## Usage

To use this code, follow these steps:

1. Clone this repository to your local machine.
2. Ensure you have Python installed along with necessary dependencies specified in `requirements.txt`.
3. Execute the provided code in your preferred environment (e.g., Jupyter Notebook, Google Colab).
4. Explore the processed data, model training, and evaluation results.
5. Optionally, deploy the FastAPI server using ngrok for public access.

## Directory Structure

README.md # This file providing an overview and usage guide
jio_mart_items.csv # Dataset containing JioMart items
products_data.csv # Additional dataset for merging
code.ipynb # Jupyter Notebook containing the code snippet
requirements.txt # List of required Python dependencies

## Dependencies

Ensure you have the following dependencies installed:

- pandas
- scikit-learn
- fastapi
- uvicorn
- ngrok

You can install them using the following command:
pip install -r requirements.txt


