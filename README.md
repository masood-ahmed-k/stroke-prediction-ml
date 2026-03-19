# Stroke Prediction Using Machine Learning Models

A comparative study of five machine learning algorithms for predicting stroke occurrence based on patient demographic and health data.

## Overview

Strokes remain one of the leading causes of death and permanent disability worldwide. Early risk prediction can significantly lower mortality rates and improve patient outcomes. This project evaluates and compares five machine learning models to identify the most accurate and effective approach for stroke prediction.

## Dataset

- **Source:** [Stroke Prediction Dataset – Kaggle](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset)
- **Size:** 5,110 entries across 12 columns
- **Features:** Age, gender, hypertension, heart disease, marital status, work type, residence type, average glucose level, BMI, smoking status

## Models Evaluated

| Model | Accuracy |
|---|---|
| Logistic Regression | ~94% |
| XGBoost | ~94% |
| Random Forest | — |
| Decision Tree | Lower |
| SVM | Lower |

## Key Findings

- **Logistic Regression** and **XGBoost** achieved the highest accuracy at approximately 94%.
- Strokes are most common between the ages of 30 and 80.
- Hypertension is a strong indicator of stroke risk.
- All models struggled with recall for the positive (stroke) class due to significant class imbalance in the dataset.

## Project Structure

```
├── Stroke_Prediction_using_Machine_Learning_Models.ipynb   # Main notebook
├── healthcare-dataset-stroke-data.csv                      # Dataset (download from Kaggle)
├── requirements.txt                                        # Python dependencies
├── LICENSE
└── README.md
```

## Getting Started

### Prerequisites

- Python 3.8+
- Jupyter Notebook or JupyterLab

### Installation

```bash
git clone https://github.com/<your-username>/stroke-prediction-ml.git
cd stroke-prediction-ml
pip install -r requirements.txt
```

### Download the Dataset

Download `healthcare-dataset-stroke-data.csv` from the [Kaggle dataset page](https://www.kaggle.com/datasets/fedesoriano/stroke-prediction-dataset) and place it in the project root.

### Run the Notebook

```bash
jupyter notebook Stroke_Prediction_using_Machine_Learning_Models.ipynb
```

## Methodology

1. **Exploratory Data Analysis** — Distribution analysis, correlation checks, and visualizations of key features (age, BMI, glucose level, smoking status, work type).
2. **Data Preprocessing** — Missing value imputation (BMI column filled with mean), label encoding of categorical variables, and train/test split.
3. **Model Training** — Five classifiers trained on the preprocessed data.
4. **Evaluation** — Accuracy scores, classification reports, and ROC-AUC curves compared across all models.

## Recommendations

- Apply oversampling techniques (e.g., SMOTE) to address class imbalance and improve recall for the stroke class.
- Explore feature engineering and hyperparameter tuning for further performance gains.
- Consider ensemble or stacking methods that combine the strengths of multiple models.

## License

This project is licensed under the MIT License — see the [LICENSE](LICENSE) file for details.
