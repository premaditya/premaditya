<h1 align="center">Prem Aditya Dhulipala</h1>

<p align="center">
  <b>Data Science &amp; Machine Learning &nbsp;·&nbsp; Python &nbsp;·&nbsp; NLP &nbsp;·&nbsp; Computer Vision</b>
</p>

<p align="center">
  B.Tech CSE graduate who builds end-to-end ML projects: data cleaning, model comparison, evaluation, and a working Streamlit app on top.
</p>

<p align="center">
  <a href="https://www.linkedin.com/in/prem-aditya-dhulipala-627a43268"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Prem_Aditya_Dhulipala-0A66C2?style=flat-square"></a>
  <a href="https://github.com/premaditya?tab=repositories"><img alt="Repositories" src="https://img.shields.io/badge/GitHub-All_repositories-181717?style=flat-square&logo=github&logoColor=white"></a>
</p>

<p align="center">
  <a href="#featured-projects">Projects</a> &nbsp;·&nbsp;
  <a href="#technical-skills">Skills</a> &nbsp;·&nbsp;
  <a href="#next-on-my-list">Next</a> &nbsp;·&nbsp;
  <a href="#connect">Connect</a>
</p>

---

## About

I am a computer science graduate focused on becoming a data scientist. I learn by building: each project below starts from a public dataset, compares several models, and ends in an app you can run and try.

I enjoy problems where the data needs real work before modelling (class imbalance, text preprocessing, image features), and I try to document the limitations of my models honestly. I am looking for entry-level Data Science and Machine Learning opportunities.

## Projects at a glance

| Project | Area | Approach | Result |
|---|---|---|---|
| [Diabetes Risk Prediction](https://github.com/premaditya/Diabetes-Detection) | Tabular ML | Random Forest, compared against 4 other models | F1 75.96% · ROC-AUC 96.55% |
| [Air Writing Recognition](https://github.com/premaditya/Air-Writing) | Computer vision | MediaPipe hand tracking + HOG features + KNN | Real-time A–Z recognition from a webcam |
| [Toxic Comment Detection](https://github.com/premaditya/Toxic-Comment-Detection) | NLP | TF-IDF + Multinomial Naive Bayes | Macro ROC-AUC 95.5% · Macro F1 49.6% |
| [Laptop Price Prediction](https://github.com/premaditya/laptop-price-prediction) | Regression | KNN regression behind a Streamlit form | Interactive price estimator |

## Featured Projects

### [Diabetes Risk Prediction](https://github.com/premaditya/Diabetes-Detection)

Binary classifier that estimates diabetes risk from patient health and lifestyle data, served through a Streamlit app that shows a risk label and probability.

- **Data:** Kaggle Diabetes Prediction Dataset, 100,000 records, only 8.5% positive.
- **Workflow:** cleaning → EDA → encoding and scaling → feature selection → SMOTE → training → hyperparameter tuning → evaluation → deployment as an app.
- **Models compared:** Logistic Regression, Decision Tree, KNN, Naive Bayes, Random Forest (best).
- **Finding:** HbA1c level and blood glucose level were the strongest predictors.
- **Result:** Random Forest reached 95.77% accuracy, 75.96% F1 and 96.55% ROC-AUC. F1 is the number to watch here because the classes are imbalanced.
- **Note:** educational project, not a medical tool.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![imbalanced-learn](https://img.shields.io/badge/imbalanced--learn-SMOTE-555555?style=flat-square)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

<!-- TODO: add "Live demo" link here once the app is deployed -->

### [Air Writing Recognition](https://github.com/premaditya/Air-Writing)

Write English letters in the air with your index finger; a webcam tracks your hand and a trained model recognises the letter. No keyboard, mouse or touchscreen needed.

- **Interaction:** gesture controls (one finger draws, three fingers predict, open palm clears the canvas).
- **Pipeline:** MediaPipe Hand Landmarker for tracking, 34×34 canvas image, HOG feature extraction, KNN classifier over 26 classes (A–Z).
- **Model selection:** KNN was chosen after comparing Logistic Regression, Decision Tree, Random Forest and Gaussian Naive Bayes, with GridSearchCV tuning on accuracy, precision, recall and F1.
- **Delivery:** real-time Streamlit app using streamlit-webrtc, plus a standalone OpenCV desktop version. Code is split into modules for canvas, hand tracking, preprocessing and prediction.
- **Limitations (documented in the repo):** one hand at a time, sensitive to lighting and fast movement.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

<!-- TODO: add a short demo GIF or a "Live demo" link here -->

### [Toxic Comment Detection](https://github.com/premaditya/Toxic-Comment-Detection)

Multi-label NLP classifier that flags a comment as toxic, severe toxic, obscene, threat, insult and/or identity hate, with confidence scores in a Streamlit app.

- **Data:** Jigsaw Toxic Comment Classification Challenge (Kaggle), about 159,000 comments.
- **Approach:** text preprocessing with NLTK, TF-IDF vectorisation, Multinomial Naive Bayes.
- **Results:** macro ROC-AUC 95.5%, macro F1 49.6%. The gap shows the model ranks comments well but struggles on rare classes.
- **Honest limitations:** English only, weak on Threat and Identity Hate (few training samples), no understanding of sarcasm or context.
- **Planned next steps (from the repo):** balanced data, word embeddings, BERT/RoBERTa, LSTM/GRU.
- A written project report is included in the repository.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![NLTK](https://img.shields.io/badge/NLTK-NLP-555555?style=flat-square)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

<!-- TODO: add "Live demo" link here once the app is deployed -->

### [Laptop Price Prediction](https://github.com/premaditya/laptop-price-prediction)

Streamlit app that estimates a laptop's price in euros from its specifications, using a saved K-Nearest Neighbors regression model.

- **Inputs:** brand, type, OS, CPU and GPU brand, RAM, screen size and resolution, weight, touchscreen/IPS, and SSD/HDD/flash/hybrid storage.
- **Feature engineering:** pixels per inch (PPI) is computed from resolution and screen size.
- **App:** validated inputs, a specifications summary, and a custom dark UI.

![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)

## Technical Skills

Everything listed here is used in the projects above.

**Languages and data analysis**
&nbsp;![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Pandas](https://img.shields.io/badge/Pandas-150458?style=flat-square&logo=pandas&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?style=flat-square&logo=numpy&logoColor=white)
![Matplotlib](https://img.shields.io/badge/Matplotlib-11557C?style=flat-square)
![Seaborn](https://img.shields.io/badge/Seaborn-4C72B0?style=flat-square)

**Machine learning**
&nbsp;![scikit-learn](https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white)
![imbalanced-learn](https://img.shields.io/badge/imbalanced--learn-SMOTE-555555?style=flat-square)
&nbsp;Classification · regression · model comparison · GridSearchCV · handling class imbalance · evaluation (F1, ROC-AUC, confusion matrix)

**NLP**
&nbsp;![NLTK](https://img.shields.io/badge/NLTK-NLP-555555?style=flat-square)
&nbsp;Text preprocessing · TF-IDF · multi-label classification

**Computer vision**
&nbsp;![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?style=flat-square&logo=opencv&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square)
&nbsp;Hand tracking · HOG features (scikit-image)

**Apps and tools**
&nbsp;![Streamlit](https://img.shields.io/badge/Streamlit-FF4B4B?style=flat-square&logo=streamlit&logoColor=white)
![Jupyter](https://img.shields.io/badge/Jupyter-F37626?style=flat-square&logo=jupyter&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?style=flat-square&logo=git&logoColor=white)
![GitHub](https://img.shields.io/badge/GitHub-181717?style=flat-square&logo=github&logoColor=white)
&nbsp;Joblib model persistence · streamlit-webrtc

## Next on my list

Directions I have already noted as next steps in my own repositories. These are plans, not completed work:

- Transformer models (BERT, RoBERTa) for toxic comment detection
- Word embeddings (Word2Vec, GloVe) and sequence models (LSTM, GRU) for NLP
- Deploying my Streamlit apps so each project has a live demo

## Connect

I am happy to talk about my projects or about entry-level Data Science and ML roles.

<!-- TODO: add an email line here if you want recruiters to be able to contact you directly -->

<p>
  <a href="https://www.linkedin.com/in/prem-aditya-dhulipala-627a43268"><img alt="LinkedIn" src="https://img.shields.io/badge/LinkedIn-Connect-0A66C2?style=flat-square"></a>
  <a href="https://github.com/premaditya?tab=repositories"><img alt="GitHub" src="https://img.shields.io/badge/GitHub-Browse_my_repositories-181717?style=flat-square&logo=github&logoColor=white"></a>
</p>
