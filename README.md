# Module 13 Challenge - Student Loan Recommendation System with Deep Learning


## Project Overview

This project uses deep learning to predict the probability that a student will successfully repay their loans, providing insights that financial institutions can use to tailor loan offers. Furthermore, a recommendation system is proposed to offer loan options that match each student's unique academic and financial profile.

### Steps in Data Preparation

1. **Feature and Target Selection**: The features (X) dataset includes all columns except `credit_ranking`, which serves as the target (y) dataset.
2. **Data Splitting**: Both datasets are split into training and testing sets.
3. **Data Scaling**: Features are standardized using Scikit-learn’s `StandardScaler` to optimize neural network training.

## Modeling Approach

### Neural Network Architecture
The model was designed as a sequential deep learning neural network with the following configuration:
- **Layers**: Multiple dense layers with ReLU activation functions.
- **Output Layer**: A binary output layer to predict the likelihood of loan repayment.

### Compilation and Training
The model was compiled with:
- **Loss Function**: `binary_crossentropy` for binary classification.
- **Optimizer**: `adam` for adaptive learning.
- **Evaluation Metric**: `accuracy`.
- **Epochs**: The model was trained over 50 epochs to achieve optimal performance.

### Model Export
The trained model was saved in Keras format as `student_loans.keras` for future predictions and evaluations.

## Model Evaluation

The model was evaluated on the testing data using:
- **Loss and Accuracy**: These metrics provided insights into the model’s predictive performance.
- **Classification Report**: Included precision, recall, f1-score, and support for each class, highlighting the model’s accuracy and reliability.

## Prediction and Recommendation System

### Prediction
The saved model was reloaded, and predictions were made on the test data, followed by generating a classification report.

### Recommendation System Design
The project also proposes a content-based recommendation system for student loans, leveraging student-specific data:

1. **Data Requirements**: Financial history, academic performance, career potential, and geographic information.
2. **Filtering Method**: Content-based filtering, as it aligns well with personalized student profiles, offering loan options tailored to unique student attributes.
3. **Real-World Challenges**:
   - **Data Privacy**: Protecting sensitive financial and academic information is crucial.
   - **Bias and Fairness**: Ensuring the system doesn’t introduce unfair loan options based on demographics or financial background.
