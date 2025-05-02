# Predict Podcast Listening Time

This repository contains a solution and experimentation for the [Kaggle Playground Series - Season 5, Episode 4](https://www.kaggle.com/competitions/playground-series-s5e4/overview).  
The goal of the competition is to predict listening time of a podcast episode.

## 📁 Project Structure

```
├── Podcast_Prediction.ipynb # Jupyter notebook for EDA, model building, etc.
├── README.md # This file
├── test.csv # Test dataset for generating submissions
└── train.csv # Training dataset
```

## 📈 Evaluation Metric
The competition uses R² score (coefficient of determination) as the evaluation metric.

## 🧪 Model Summary
The notebook includes:
- Exploratory Data Analysis (EDA)
- Feature engineering and preprocessing
- Model training using machine learning algorithms
- Performance evaluation using R² score

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
pip install pandas numpy scikit-learn matplotlib seaborn
```

### 4. Run the notebook
Launch the notebook with Jupyter:
```bash
jupyter notebook Podcast_Prediction.ipynb
```
Go through each cell to explore data, train models, and generate predictions.