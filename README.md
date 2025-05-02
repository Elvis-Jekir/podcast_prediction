# Predict Podcast Listening Time

This repository contains a complete solution and experimentation for the [Kaggle Playground Series - Season 5, Episode 4](https://www.kaggle.com/competitions/playground-series-s5e4/overview).  
The goal of the competition is to predict the listening time of podcast episodes based on features such as episode metadata, popularity scores, publication info, and more.

## 📁 Project Structure
```
├── Podcast_Prediction.ipynb       # Jupyter notebook for EDA, feature engineering, model building, and evaluation
├── README.md                      # Project documentation
├── test.csv                       # Test dataset for generating submissions
└── train.csv                      # Training dataset
```

## 📈 Evaluation Metric
The competition uses the **R² score** (coefficient of determination) as the evaluation metric.

## 🔍 Project Overview
We explored the dataset from multiple angles to understand key drivers of listening behavior. After handling missing data, correcting outliers, and engineering relevant features, we trained and compared several regression models.

## 📊 Key Insights
- `Episode_Length_minutes` had a 92% correlation with the target and was the strongest predictor.
- Genre, sentiment, and publication timing had minimal influence on listening time.
- Engineered features like `Ad_Density` and a `No_Guest` flag added value to the model.

## 🤖 Models Used
We trained and evaluated multiple regression models:
- **Linear Regression** – Baseline model
- **Gradient Boosting** – Tuned with RandomizedSearchCV
- **XGBoost** – Stable but did not outperform others
- **Random Forest** – Best overall performance with R² ≈ 0.7784 after improved preprocessing

## ⚠️ Challenges
- Handling missing values for key features required context-aware strategies
- Memory limitations forced dataset splitting for some models (e.g., Gradient Boosting)
- Long training times (especially with Random Forest) limited the scope of tuning

## 🧪 Notebook Summary
The notebook includes:
- Exploratory Data Analysis (EDA)
- Feature engineering and preprocessing
- Handling of missing data and outliers
- Model training and evaluation
- Comparison of results using R² and RMSE

## 🚀 Setup Instructions

### 1. Clone this repository
```bash
git clone https://github.com/Elvis-Jekir/podcast_prediction.git
cd podcast_prediction
```

### 2. Create and activate a virtual environment (optional)
```bash
python3 -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

### 3. Install dependencies
```bash
pip install pandas numpy scikit-learn matplotlib seaborn xgboost
```

### 4. Run the notebook
Launch the notebook with Jupyter:
```bash
jupyter notebook Podcast_Prediction.ipynb
```
Explore the code to analyze the dataset, train models, and generate predictions.

## ✅ Final Notes
This project highlights the importance of combining data understanding with model experimentation. By iteratively improving our preprocessing and feature selection, we achieved strong predictive performance and valuable insights into podcast engagement behavior.
