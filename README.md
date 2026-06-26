# ML_projects

1. Personal_proj1:
Multilingual Language Detection & Translation System | Python, Scikit-learn, NLP

- Built a language detection classifier from scratch supporting 17 languages using character level n-gram features and TF-IDF vectorization
- Trained a Multinomial Naive Bayes model on 10,000+ multilingual text samples with 50,000 TF-IDF character n-gram features achieving 99.18% accuracy
- Evaluated model using confusion matrix, per-class precision, recall and F1-score, identified linguistically meaningful misclassification patterns
- Integrated Google Translate API for end-to-end detection and translation pipeline with confidence-based uncertainty warnings

2. Personal_proj2:
Smart Grid Failure Prevention Model | Python, Scikit-learn, Random Forest, K-Means

- Built an end-to-end predictive maintenance proof of concept on 10,000 industrial sensor readings, performing data cleaning, VIF-based feature selection and one-hot encoding to prepare a 5-feature modeling dataset
- Trained a Random Forest classifier optimized for Recall using GridSearchCV, improving recall from 38.2% (baseline) to 50.0% (tuned), validated with StratifiedKFold cross-validation achieving consistent 57.81% mean recall
- Evaluated model using ROC-AUC (90.22%), confusion matrix and threshold analysis; tuned decision threshold from 0.50 to 0.358 to achieve 73.5% recall at 8.6% false alarm rate, catching 16 additional failures per cycle
- Segmented 9,661 healthy assets into 3 actionable maintenance tiers (Low / Medium / High Risk) using K-Means clustering with optimal K selected via Elbow and Silhouette methods, identifying Process Temperature and Tool Wear as primary risk drivers
