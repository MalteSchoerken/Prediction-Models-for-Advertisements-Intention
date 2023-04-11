# Prediction-Models-for-Advertisements-Intention
816 advertisements were used to classify three specific marketing strategies, namely price leadership, quality leadership and time leadership. Each of the advertisements was assigned manually to exactly one of these categories. In this code, a total of eight machine learning models are used along with various feature extraction methods to extract features from the advertising texts. Grid Search is used in all cases to optimize the models. The results are comparatively analyzed.

## Machine Learning Models
The Machine Learning Models are classification models from Scikit-Learn, namely:
* k-Nearest-Neighbors
* Support Vector Classification
* Gaussian Process
* Decision Tree
* Random Forest
* Neural Network
* ADA Boost
* Gradient Boosting

## Feature Extraction Methods
The used Feature Extraction methods are:
* Named Entity Recognition using Spacy
* Sentiment Analysis using Textblob
* Manual Keyword Extraction
* Unsupervised Keyword Extraction using the YAKE! implementation from PyPi

## Results
It became evident that both manual and unsupervised Keyword Extraction were significant factors in accurately classifying the companies’ strategies. Both techniques produced features that were ranked the highest in terms of importance score whereas the features produced by Named Entity Recognition and Sentiment Analysis were significantly less relevant. When trained on all of the extracted features, the eight machine learning models achieved accuracies in the range of 78% to 87%. The best predictions were obtained when Gaussian Process and Neural Network were employed both resulting in a micro, macro and weighted F1 score of 0.87. When comparing both models in detail Gaussian Process outperformed Neural Network in two out of three experiments.
