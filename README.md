# AI-Based Customer Churn Prediction & Retention Strategy

Machine learning project for predicting customer churn in the telecommunications industry and using the model results to support customer-retention strategies.

## Project Overview

Customer churn directly affects recurring revenue and customer lifetime value. This project uses customer profile and usage data to build a machine-learning classification model that predicts whether a customer is likely to churn.

The project was developed as part of the **GCI World 2026 Final Assignment**.

### Main workflow

1. Load customer and usage datasets.
2. Merge the datasets using `Customer_ID`.
3. Remove columns with more than 50% missing values.
4. Fill remaining missing values using mode/median.
5. Encode categorical variables with `LabelEncoder`.
6. Split the data into training and testing sets.
7. Train a `RandomForestClassifier`.
8. Evaluate the model using accuracy, precision, recall, F1-score, and a confusion matrix.

## Model

**Algorithm:** Random Forest Classifier

The report describes the model as suitable for the dataset because it can handle large datasets, mixed feature types, reduce overfitting through an ensemble of decision trees, and provide feature-importance information.

## Reported Results

According to the project report:

| Metric | Score |
|---|---:|
| Accuracy | 85% |
| Precision | 83% |
| Recall | 80% |
| F1 Score | 81% |

The report highlights customer care calls, dropped voice calls, mean revenue, months in service, and average monthly minutes as important predictive features.

## Project Structure

```text
customer-churn-prediction/
│
├── data/
│   └── README.md
│
├── notebooks/
│   └── customer_churn_prediction.ipynb
│
├── report/
│   └── customer_churn_report.pdf
│
├── .gitignore
├── README.md
└── requirements.txt
```

## Dataset

The notebook expects these two CSV files:

```text
Client.csv
Record.csv
```

The notebook loads them using:

```python
record = pd.read_csv('Record.csv')
client = pd.read_csv('Client.csv')
```

and merges them on `Customer_ID` when that column is available in both files.

The dataset files are intentionally not included in this repository package. See `data/README.md`.

## Installation

Clone the repository:

```bash
git clone https://github.com/YOUR_USERNAME/customer-churn-prediction.git
cd customer-churn-prediction
```

Create a virtual environment:

### Windows

```bash
python -m venv venv
venv\Scripts\activate
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Install and launch Jupyter:

```bash
jupyter notebook
```

Open:

```text
notebooks/customer_churn_prediction.ipynb
```

Before running the notebook, place `Client.csv` and `Record.csv` in the same working directory expected by the notebook, or update the CSV paths in the notebook.

## Technologies

- Python
- Pandas
- NumPy
- Scikit-learn
- Matplotlib
- Seaborn
- Jupyter Notebook
- Machine Learning
- Random Forest

## Business Strategy

The project proposes an AI-powered retention workflow:

**Predict → Trigger → Offer → Support → Monitor**

Possible retention actions described in the project report include:

- Discount plans
- Loyalty rewards
- Priority customer support
- Network improvements
- Personalised AI recommendations

## Future Improvements

The project report proposes:

- Real-time churn prediction
- Live customer risk-scoring dashboard
- Advanced feature engineering
- LSTM/Transformer-based models
- Personalised recommendation engine
- CRM integration
- Automated multi-channel retention campaigns

## Author

**Deepak M**

BTech Computer Science & Engineering  
PES University

## Disclaimer

This repository contains the project notebook and report. Dataset availability and redistribution rights depend on the original dataset source and its license.
