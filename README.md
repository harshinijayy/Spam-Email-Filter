# Spam-Email-Filter
This project focuses on building a spam filter to classify emails as spam or not spam using a logistic regression model. The objective was to achieve at least 85% accuracy on both training and test datasets while applying robust feature engineering and data preprocessing techniques. 
Tools and Libraries: Python, Scikit-learn, Pandas, NumPy

Overview

The spam filter is built using Python, with specific emphasis on:
- Preprocessing email data.
- Creating meaningful features for classification.
- Implementing and fine-tuning a logistic regression model.
- Evaluating performance through accuracy metrics on training, validation, and test sets.

Data Preprocessing Process

The dataset contained email text and corresponding labels (spam or not spam). 
Preprocessing steps included:
- Text Conversion: All email text was converted to lowercase for consistency.
- Handling Missing Values: Missing or NaN values in the dataset were filled with empty strings to avoid disruptions in feature extraction.
- Data Splitting: The dataset was split into training (90%) and validation (10%) sets to train and validate the model effectively.

Feature Engineering

To improve the model's predictive accuracy, several features were extracted:

Keyword-Based Features:
- Selected words likely to indicate spam were identified (e.g., drug, bank, prescription, memo, private).
- A binary feature matrix was created where each column represented the presence (1) or absence (0) of a keyword in the email text.
- The words_in_texts utility was used for efficient feature extraction.

Additional Features:
- Number of words/characters in the subject/body.
- Use of punctuation (e.g., !, %).
- Percentage of capital letters in the email.

Model Implementation
A logistic regression model was chosen for its simplicity and interpretability:
- The model was trained using the binary feature matrix (X_train) and corresponding labels (Y_train).
- Regularization and hyperparameter tuning were explored using tools such as GridSearchCV to prevent overfitting and optimize model performance.

Results and Analysis

Accuracy Metrics
- Training Set Accuracy: Achieved approximately 85%.
- Validation Set Accuracy: Consistently around 85%.
- Test Set Accuracy: Met or exceeded the 85% threshold after iterative improvements.

Insights 
- The presence of certain keywords (e.g., drug, bank) had a significant impact on spam classification, as reflected in the model coefficients.
- Cross-validation and regularization were crucial in avoiding overfitting, ensuring the model generalizes well to unseen data.

Recommendations for Further Improvement

- Experiment with additional features like email length, punctuation counts, or HTML-specific tags.
- Explore advanced preprocessing techniques, such as stemming or lemmatization, to improve keyword matching.
- Consider other metrics like precision, recall, or F1-score for a more comprehensive evaluation.

