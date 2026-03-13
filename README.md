# Phishing URL Detection: ML & Transformer-Based Text Embeddings

## Overview

This project explores the problem of detecting phishing websites using machine learning techniques. The goal is to build models capable of distinguishing between **benign** and **phishing URLs** by leveraging a feature-engineered dataset containing structural and lexical characteristics extracted from URLs.

The work is based on a replication of the research study _“A Feature-Engineered Dataset of Benign and Phishing URLs for Machine Learning and Large Language Models Evaluation.”_ The objective is to reproduce the experimental setup described in the paper and evaluate whether similar model performance can be achieved using the provided dataset.

---

## More Details

The project currently includes two primary notebooks:

### 1. Replication Study

The notebook `phishing_url_detection.ipynb` reproduces the experimental methodology described in the original research paper. It trains and evaluates two approaches:

- **Random Forest classifier** trained on engineered URL features
- **MiniLM embeddings + Logistic Regression** trained on raw URL text

This notebook contains detailed explanations of the dataset, the experimental setup, model training, and comparisons with the results reported in the original paper.

### 2. External Model Evaluation

The notebook `phishing_url_model_external_evaluation.ipynb` evaluates the **generalization ability** of the trained MiniLM + Logistic Regression model on a separate dataset containing only raw URL strings. Goal: To help assess how well the transformer-based approach performs on unseen URL distributions.

---

Additional resources:

- Replication Study Notebook [Kaggle](https://www.kaggle.com/code/sahandnamvar/phishing-url-detection-using-rf-minilm-lr)
- Original Dataset [Kaggle](https://www.kaggle.com/datasets/sahandnamvar/phishing-url-detection-111k-urls-22-features)
- Original Dataset [Mendeley](https://data.mendeley.com/datasets/65z9twcx3r/1)
- Original Paper [A Feature-Engineered Dataset of Benign and Phishing URLs...](https://www.sciencedirect.com/science/article/pii/S2352340925008832?via%3Dihub)

## How to Run

1. Clone the repository.
2. Ensure the dataset file is available in the working directory (download link above).
   - You may need to adjust the file path in the notebook accordingly.
3. Open terminal/cmd and navigate to the project directory.
4. Install the required dependencies using pip or Conda.
5. Run the Jupyter notebook to execute the code and reproduce the results.

```bash
git clone https://github.com/SahandNamvar/phishing-url-detection.git
cd phishing-url-detection
pip install -r requirements.txt # Or Conda environment setup
jupyter notebook phishing_url_detection.ipynb
```
