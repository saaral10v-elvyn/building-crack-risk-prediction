# Building Crack Severity Prediction Using Machine Learning

## Project Overview

This project explores machine learning techniques to classify building-crack records into two categories using structural and environmental information.

The project demonstrates data preparation, feature engineering, model training, classification evaluation, and saving a trained machine learning pipeline.

**Important:** The target is an exploratory crack-severity proxy derived from crack measurements. It is not a verified structural-risk label and must not be used to determine whether a real building is safe.

## Objectives

- Explore and prepare a structural-crack dataset.
- Create an exploratory severity proxy.
- Train a Random Forest classifier.
- Evaluate predictions using classification metrics.
- Save the trained model and evaluation results.

## Dataset

The dataset contains 291 records with features including:

- Structure type and crack type
- Crack length, width, and depth
- Material type and structure age
- Humidity, moisture, and temperature
- Crack location, load-bearing information, and environment

The available dataset has no verified structural-risk target. Therefore, the project creates a proxy label for experimentation.

## Methodology

1. Load and inspect the dataset.
2. Split the data into training and testing sets.
3. Standardize crack measurements and construct the exploratory severity proxy.
4. Exclude the measurements used to construct the proxy from the classifier's input features.
5. Encode categorical features and scale numerical features.
6. Train a Random Forest classifier.
7. Evaluate the model and save its outputs.

## Model

**Algorithm:** Random Forest Classifier

**Input features:** Structure type, crack type, material, structure age, humidity, moisture, temperature, crack location, load-bearing information, and environment.

**Training records:** 232

**Testing records:** 59

## Evaluation Results

The experimental model uses a classification threshold of 0.30 for the higher-severity proxy class.

| Metric | Result |
|---|---:|
| Accuracy | 54.2% |
| Precision (higher-severity proxy) | 33.3% |
| Recall (higher-severity proxy) | 68.8% |
| F1 score (higher-severity proxy) | 0.449 |

These results are preliminary and are based on a small test set. They measure prediction of the constructed proxy, not real-world structural safety.

## Repository Files

- `building_crack_risk_prediction.ipynb` — data preparation, training, and evaluation notebook (use the actual uploaded notebook filename if different).
- `crack_severity_model.pkl` — saved trained model pipeline.
- `model_predictions.csv` — test-set predictions and probabilities.
- `model_evaluation.csv` — saved classification metrics.
- `README.md` — project documentation.

## Technologies Used

- Python
- Pandas and NumPy
- Scikit-learn
- Jupyter Notebook / Google Colab
- GitHub

## Limitations

- The dataset does not contain verified structural-risk labels.
- The severity target is a constructed proxy, not a ground-truth engineering assessment.
- The dataset and test set are small.
- Performance may change with different data splits.
- The model is not validated for practical building inspections or safety decisions.

## Future Improvements

- Obtain a larger dataset with expert-verified severity labels.
- Validate measurements and investigate unusual records.
- Use more robust validation and model comparison.
- Improve class detection using appropriate evaluation and threshold selection.
- Develop a demonstration interface after validating the model on suitable data.

## Disclaimer

This project is for educational and portfolio demonstration purposes only. It is not a substitute for inspection or assessment by a qualified structural engineer.
