# Prediction-Models-for-Advertisements-Intention
816 advertisements were used to classify three specific marketing strategies, namely price leadership, quality leadership and time leadership. Each of the advertisements was assigned manually to exactly one of these categories. In this code, a total of 8 machine learning models are used along with various feature extraction methods to extract features from the advertising texts. Grid Search is used in all cases to optimize the models. The 8 machine learning models and 3 different feature selections (experiment 1-3) are comparatively analyzed. This Repository includes the corresponding Code to the Bachelor Thesis: "What do advertisers want? Predicting the intention of online banner ads." in the Jupiter Notebook as well as the used data set (GT_intention.csv) and the Grid Search tables.

## Run the Code
It is possible to run all cells in the Jupiter Notebook. The data set that is used (GT_intention.csv) is included in this repository. Grid Search is included in the Code, which takes about 4 hours and automatically runs on all cores. However, it can be skipped since the Grid Search results already exist in the tables. For skipping Grid Search run everything until the Chapter "Optimizing parameters" and from the beginning of the Chapter "Comparism of the Experiments".

## Machine Learning Models
The machine learning models are classification models from Scikit-Learn, namely:
* k-Nearest-Neighbors
* Support Vector Classification
* Gaussian Process
* Decision Tree
* Random Forest
* Neural Network
* ADA Boost
* Gradient Boosting

## Feature Extraction Methods
The used feature extraction methods are:
* Named Entity Recognition (NER) using Spacy
* Sentiment Analysis (SA) using Textblob
* Manual Keyword Extraction (MKE)
* Unsupervised Keyword Extraction (UKE) using the YAKE! implementation from PyPi

## Experiments
The three compared experiments are:
* Experiment 1: Using NER, SA and MKE features
* Experiment 2: Using NER, SA and UKE features
* Experiment 3: Using all features

## Results
It became evident that both manual and unsupervised Keyword Extraction were significant factors in accurately classifying the companies’ strategies. Both techniques produced features that were ranked the highest in terms of importance score whereas the features produced by Named Entity Recognition and Sentiment Analysis were significantly less relevant. When trained on all of the extracted features, the eight machine learning models achieved accuracies in the range of 78% to 87%. The best predictions were obtained when Gaussian Process and Neural Network were employed both resulting in a micro, macro and weighted F1 score of 0.87. When comparing both models in detail Gaussian Process outperformed Neural Network in two out of three experiments.
