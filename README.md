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

3. Personal_proj3: 
Financial Complaint Router & Dispute-Risk Predictor | Python, Scikit-learn, LightGBM, SHAP, KeyBERT, spaCy, Sentence-Transformers

- Built an end-to-end complaint triage system on 4,888 real CFPB consumer complaints, comparing TF-IDF, KeyBERT, and NER extraction methods to structure unstructured narratives, and trained a routing classifier achieving 89% accuracy across 3 team categories
- Engineered a dispute-risk model combining structured features with sentence embeddings via LightGBM, improving accuracy from 69% to 80% and minority-class precision from 38% to 53% by incorporating complaint text signal
- Applied SHAP (TreeExplainer) to surface company identity as the dominant dispute-risk driver, validating model behavior against independently calculated company-level risk rates from raw data
- Designed a rule-based regulatory compliance flag covering 31.5% of complaints with a compliance-priority routing override, and assembled all components into a single decision engine returning structured JSON output per complaint
