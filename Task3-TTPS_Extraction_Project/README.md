# Project Report: TTPs Prediction

## Group Members:
- Manthan Gopal Dhole
- Aniket Umare
- Jeevak Moon

## Introduction
The TTPs Prediction project aims to classify and predict Tactics, Techniques, and Procedures (TTPs) used in cyber attacks based on given paragraphs or text. The project utilizes machine learning and natural language processing techniques to identify the most similar TTP for a given paragraph and provide a summarization of the paragraph's content. This report provides an overview of the project, its implementation details, and the functions involved.

## 1. Project Overview
The TTPs Prediction project focuses on the following key components:

### a. Data
The project utilizes a dataset of TTPs stored in a CSV file named "Complete_Data.csv." This dataset contains information about various TTPs, including tactics, techniques, and procedures.

### b. Universal Sentence Encoder
The project uses the Universal Sentence Encoder from TensorFlow Hub to encode and represent paragraphs or sentences as fixed-length vectors. This encoder converts textual data into numerical representations suitable for machine learning models.

### c. Machine Learning Models
Two machine learning models are employed in this project. The first model, named "AttackOrNot.joblib," is used to classify whether a given paragraph represents an attack or not. The second model uses cosine similarity to identify the most similar TTP for a given paragraph.

### d. Text Preprocessing
Before encoding and modeling, the project applies preprocessing techniques to the text data. This includes removing special characters, email addresses, IP addresses, and HTML tags, as well as reducing whitespace and converting all text to lowercase.

### e. Summarization
The project includes a text summarization function that uses the spaCy library to extract the most relevant sentences from a paragraph based on word frequencies and scores. This function provides a concise summary of the paragraph's content.

## 2. Implementation Details
The implementation details of the TTPs Prediction project are as follows:

a. Loading Data:
The project starts by reading the TTP dataset from the "Complete_Data.csv" file. This dataset contains information about various TTPs, including tactics, techniques, and procedures. The dataset is loaded into a pandas DataFrame for further processing.

b. Sentence Encoding:
The Universal Sentence Encoder model is loaded using TensorFlow Hub. This model is responsible for encoding paragraphs or sentences into fixed-length vectors, enabling comparison and similarity calculations.

c. Text Preprocessing:
The project includes a preprocessing function that applies several steps to clean the text data. This function removes URLs, email addresses, IP addresses, HTML tags, special characters, and extra whitespace. The preprocessed text is then ready for vectorization and embedding.

d. Text Summarization:
To provide a summary of the paragraph's content, the project utilizes the spaCy library. The summarization function calculates word frequencies, sentence scores, and selects the most relevant sentences based on a specified percentage. These selected sentences are combined to form the summary.

e. Similarity Calculation:
The project uses cosine similarity to find the most similar TTP for a given paragraph. The TTPs are represented as vectors using the Universal Sentence Encoder, and the similarity is computed between the paragraph's vector and all TTP vectors. The TTP with the highest cosine similarity score is considered the most similar.

## Conclusion
The TTPs Prediction project utilizes machine learning, natural language processing, and text summarization techniques to predict TTPs for given paragraphs or text. By leveraging the Universal Sentence Encoder and cosine similarity, the project identifies the most similar TTP and provides relevant information and summarizations. The user-friendly interface enables users to interact with the project easily and obtain insights into the TTPs present in their textual data.

**Reference:**
1. TIM: threat context-enhanced TTP intelligence mining on unstructured threat data
2. Construction of TTPS from APT reports using BERT
