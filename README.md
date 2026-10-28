# Developing an NLP Model to Classify Disaster Tweets

This repository contains the code and research for the natural language processing (NLP) project detailed in the "CAIS++ Fall 2025 Project.jpg" poster presentation[cite: 1]. The goal of this project is to create a machine learning model capable of accurately predicting whether a given tweet is referring to a real natural disaster or simply using disaster-related keywords metaphorically[cite: 1]. 

This project was developed under the USC Viterbi School of Engineering and CAIS++ (Center for AI in Society's Student Branch)[cite: 1].

## Project Overview
Many disaster relief organizations and news agencies are interested in programmatically monitoring Twitter for emergency events[cite: 1]. However, human language is nuanced; it is not always clear if a person's words are announcing a legitimate disaster (e.g., "Forest fire near La Ronge") or using slang (e.g., "I love this song, it's fire")[cite: 1]. 

This project aims to solve this binary classification problem to assist agencies in monitoring social media data[cite: 1].

## Dataset
The primary data source used for this project is the "Natural Language Processing with Disaster Tweets" dataset hosted on Kaggle[cite: 1]. 
* **Total Size:** 10,000+ hand-classified tweets[cite: 1].
* **Training Set:** 7,613 samples used to teach the model[cite: 1].
* **Test Set:** 3,263 samples used to evaluate final performance[cite: 1].
* **Target Variables:** 
  * `1`: A real disaster[cite: 1].
  * `0`: Not a disaster[cite: 1].

## Methodology

### Data Preprocessing
* Cleaned tweets by converting text to lowercase, removing URLs and punctuation, and filling missing fields[cite: 1].
* Utilized the resulting cleaned text column for all modeling[cite: 1].

### Baseline Models
* Generated TF-IDF features to convert the textual tweets into numerical vectors[cite: 1].
* Trained **Logistic Regression** and **Naive Bayes** models to serve as baseline classifiers[cite: 1].

### Deep Learning Model (BERT)
* Fine-tuned a `bert-base-uncased` deep learning model for binary classification[cite: 1].
* BERT was selected because its transformer architecture understands context and captures the semantic relationships between words[cite: 1].

### Training and Evaluation
* Split the data into training and validation sets[cite: 1].
* Trained models for several epochs[cite: 1].
* Evaluated performance using accuracy, precision, recall, F1-score, and confusion matrices[cite: 1].

## Results
By fine-tuning the pre-trained BERT model, we achieved the best classification performance, outperforming the traditional statistical methods (Naive Bayes and Logistic Regression)[cite: 1]. The results demonstrated that the sequence and context of words are crucial for distinguishing between the literal and metaphorical uses of disaster-related keywords[cite: 1].

## Social Implications
Deploying accurate NLP classification for disaster tweets has several real-world benefits:
* **Efficient Emergency Response:** Enables shorter response times, more targeted aid, and better resource allocation[cite: 1].
* **Early Warning System:** Acts as an effective real-time alerting mechanism[cite: 1].
* **Combatting Misinformation:** Provides news agencies with a platform to verify information, generate direct communication channels, and improve public awareness[cite: 1].

## Future Work
* Combine predictions from multiple transformer models (such as RoBERTa and DistilBERT) through an ensemble approach[cite: 1].
* Use synonyms to artificially create more training samples for the "disaster" class[cite: 1].
* Analyze specific keywords (e.g., "crash", "deluge") that yield the highest error rates in order to create highly specific preprocessing rules[cite: 1].

## Team
* **Authors:** Maymoona Khan, Tina Abraham, Jacques Vlok[cite: 1]
* **Curriculum Leads:** Angela Zhuang & Shreeya Chand[cite: 1]
