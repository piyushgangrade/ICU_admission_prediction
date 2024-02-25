## ICU Admission Prediction Project Documentation
### Purpose

The Intensive Care Unit (ICU) Admission Prediction project is designed to leverage machine learning models to predict the likelihood of a patient requiring ICU admission based on various clinical and demographic features. This initiative stems from the critical need to optimize ICU resource allocation, especially in times of high demand such as during pandemics or mass casualty events. By accurately predicting ICU admissions, healthcare facilities can better prepare and manage their resources, ensuring that patients in dire need receive timely and appropriate care.
Background

The ICU Admission Prediction project aims to optimize ICU resource allocation and improve patient outcomes by using machine learning models to predict the likelihood of ICU admissions. This predictive capability is crucial for healthcare facilities to manage resources efficiently and ensure timely care for patients in critical need.

### Approach

The provided Jupyter notebook outlines a comprehensive analysis for ICU admission prediction using various machine learning models. The analysis involves feature selection, model fitting, hyperparameter tuning, and model comparison based on AUC (Area Under the ROC Curve) scores. Here are the key points and metrics from the notebook:

- **Feature Selection:** The notebook employs Recursive Feature Elimination (RFE) with a Random Forest Classifier to identify the most important features. This method ranks features based on their importance, enabling the selection of the most relevant features for modeling.</li>

- **Model Fitting and Evaluation:**
  - Multiple models, including K-Nearest Neighbors (KNN) and Random Forest Classifier (RFC), are fitted on the dataset.</li>
  - The Random Forest model is further refined using feature importance scores and RFE-selected features to create reduced datasets for modeling.

- **Hyperparameter Tuning:**
  - A grid search approach is used to tune the hyperparameters of the Random Forest Classifier. The search space includes n_estimators, criterion, max_depth, and max_features.
  - The best hyperparameters are selected based on the ROC AUC score during cross-validation.

- **Model Comparison:**
  - Models are compared based on their AUC scores across different data windows (specified as WINDOW 1, WINDOW 2-3, and WINDOW 4-5 in the visualizations).
  - The AUC scores are visualized in bar charts, showing the performance of each model (KNN, RFC, RFC with feature importance, RFC with reduced features, and tuned RFC) across the different windows.

- **Metrics:**
  - The notebook provides AUC scores for each model and configuration, which serve as the primary metric for comparison.
  - The AUC scores are used to evaluate the models' ability to distinguish between classes (ICU admission vs. no ICU admission).

Unique Implementation: Understanding Data Windows

In our approach to predicting ICU admissions, we introduced the concept of "Data Windows" to capture and analyze patient data at various critical intervals before potential ICU admission. This innovative implementation is structured as follows:

- **WINDOW 1:** Represents patient data collected closest to the time of ICU admission, providing acute insights into the immediate factors influencing the need for intensive care.
- **WINDOW 2-3:** Covers an intermediate period before ICU admission, offering a broader view of the patient's condition and trends that may signal the escalation of care needs.
- **WINDOW 4-5:** Encompasses data from the earliest phases of the patient's hospital stay, giving a long-term perspective on the patient's health trajectory leading up to the ICU admission.

By segmenting the data into these windows, our models can assess the predictive importance of features over varying timeframes, enhancing the accuracy and relevance of ICU admission predictions. This segmentation allows for a nuanced understanding of how patients' conditions evolve and how early or late interventions might influence the need for ICU care.

#### Outcomes:
  - The notebook concludes with visualizations comparing the AUC scores of different models and configurations, highlighting the performance variations across different data windows.
  - This comprehensive analysis aids in identifying the most effective model and feature set for predicting ICU admissions.

#### Conclusion

The ICU Admission Prediction project represents a vital step forward in the application of machine learning in healthcare. By accurately predicting ICU admissions, this project has the potential to revolutionize how healthcare providers allocate resources, prioritize patient care, and prepare for fluctuations in ICU demand. As we continue to refine our models and incorporate more data, we anticipate even greater accuracy and utility from our predictions, further contributing to the advancements in healthcare technology and patient care optimization.

#### Acknowledgments

In the development of this project, we humbly acknowledge the use of advanced language models, including ChatGPT and GitHub Copilot. These tools significantly enhanced our coding efficiency and documentation quality by providing real-time suggestions, coding patterns, and writing assistance. Their integration into our workflow allowed us to focus on innovation and problem-solving, ensuring a higher standard of project outcomes. We are grateful for the support these AI tools have provided in bridging the gap between complex machine learning concepts and practical implementation.
