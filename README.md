# Developing an NLP Model to Classify Disaster Tweets

This repository contains the code and research for the natural language processing (NLP) project detailed in the "CAIS++ Fall 2025 Project.jpg" poster presentation. The goal of this project is to create a machine learning model capable of accurately predicting whether a given tweet is referring to a real natural disaster or simply using disaster-related keywords metaphorically. 

This project was developed under the USC Viterbi School of Engineering and CAIS++ (Center for AI in Society's Student Branch).

## Project Overview
Many disaster relief organizations and news agencies are interested in programmatically monitoring Twitter for emergency events. However, human language is nuanced; it is not always clear if a person's words are announcing a legitimate disaster (e.g., "Forest fire near La Ronge") or using slang (e.g., "I love this song, it's fire"). 

This project aims to solve this binary classification problem to assist agencies in monitoring social media data.

## Dataset
The primary data source used for this project is the "Natural Language Processing with Disaster Tweets" dataset hosted on Kaggle. 
* **Total Size:** 10,000+ hand-classified tweets.
* **Training Set:** 7,613 samples used to teach the model.
* **Test Set:** 3,263 samples used to evaluate final performance.
* **Target Variables:** 
  * `1`: A real disaster.
  * `0`: Not a disaster.

## Methodology

### Data Preprocessing
* Cleaned tweets by converting text to lowercase, removing URLs and punctuation, and filling missing fields.
* Utilized the resulting cleaned text column for all modeling.

### Baseline Models
* Generated TF-IDF features to convert the textual tweets into numerical vectors.
* Trained **Logistic Regression** and **Naive Bayes** models to serve as baseline classifiers.

### Deep Learning Model (BERT)
* Fine-tuned a `bert-base-uncased` deep learning model for binary classification.
* BERT was selected because its transformer architecture understands context and captures the semantic relationships between words.

### Training and Evaluation
* Split the data into training and validation sets.
* Trained models for several epochs.
* Evaluated performance using accuracy, precision, recall, F1-score, and confusion matrices.

## Results
By fine-tuning the pre-trained BERT model, we achieved the best classification performance, outperforming the traditional statistical methods (Naive Bayes and Logistic Regression). The results demonstrated that the sequence and context of words are crucial for distinguishing between the literal and metaphorical uses of disaster-related keywords.

## Social Implications
Deploying accurate NLP classification for disaster tweets has several real-world benefits:
* **Efficient Emergency Response:** Enables shorter response times, more targeted aid, and better resource allocation.
* **Early Warning System:** Acts as an effective real-time alerting mechanism.
* **Combatting Misinformation:** Provides news agencies with a platform to verify information, generate direct communication channels, and improve public awareness.

## Future Work
* Combine predictions from multiple transformer models (such as RoBERTa and DistilBERT) through an ensemble approach.
* Use synonyms to artificially create more training samples for the "disaster" class.
* Analyze specific keywords (e.g., "crash", "deluge") that yield the highest error rates in order to create highly specific preprocessing rules.

## Team
* **Project Members:** Maymoona Khan, Tina Abraham, Jacques Vlok
* **Curriculum Leads:** Angela Zhuang & Shreeya Chand
