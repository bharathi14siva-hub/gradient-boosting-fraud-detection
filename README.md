# Gradient Boosting for Credit Card Fraud Detection

## Project Overview
This project uses a **HistGradientBoostingClassifier** from Scikit-learn to identify potentially fraudulent credit card transactions. The model is trained on transaction data and evaluated using classification metrics and a confusion matrix.

## Objectives
- Detect fraudulent transactions.
- Evaluate model performance using precision, recall, F1-score, and accuracy.
- Analyze feature importance using permutation importance.
- Save and reload the trained model for predictions.

## Technologies Used
- Python
- Pandas
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

## Model
**Algorithm:** Histogram-based Gradient Boosting Classifier (`HistGradientBoostingClassifier`)

## Results

| Metric | Result |
|---|---:|
| Test Accuracy | 99.9066% |
| Fraud Precision | 71% |
| Fraud Recall | 74.74% |
| Fraud F1-score | 0.73 |

### Confusion Matrix

| | Predicted Legitimate | Predicted Fraud |
|---|---:|---:|
| Actual Legitimate | 56,622 | 29 |
| Actual Fraud | 24 | 71 |

The model correctly identified 71 fraud transactions out of 95 in the test set. It missed 24 fraud transactions, so improving fraud recall is a potential area for future work.

## Feature Importance
Permutation importance was used to estimate how much model performance decreases when individual features are shuffled. Features such as V12 and V14 showed high importance in the analysis.

## Model Persistence
The trained model was saved as:

`gradient_boosting_fraud_model.pkl`

The saved model was successfully reloaded and tested on sample transactions.

## How to Run
1. Clone or download this repository.
2. Install the required Python libraries.
3. Place the dataset in the expected location.
4. Open the Jupyter Notebook.
5. Run the cells in order to train, evaluate, and test the model.

Install the dependencies with:

```bash
pip install pandas matplotlib seaborn scikit-learn joblib jupyter
```

## Future Improvements
- Improve fraud detection recall.
- Evaluate precision-recall trade-offs.
- Tune hyperparameters and compare models.
- Test performance on additional unseen transactions.

## Disclaimer
This project is intended for educational purposes and is not a production-ready fraud detection system.
