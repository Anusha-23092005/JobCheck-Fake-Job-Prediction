# JobCheck – Fake Job Prediction System

## Overview
JobCheck is a Machine Learning-based web application designed to help users identify potentially fraudulent job postings. It analyzes job posting information and predicts whether a job advertisement is likely to be genuine or fake.

The application provides an interactive interface for job analysis, model performance evaluation, prediction history, and downloadable reports.

## Features
- **Fake Job Prediction:** Analyze job postings using trained machine learning classifiers.
- **Model Performance:** View model evaluation metrics and compare classifier performance.
- **Dataset Analysis:** Explore the datasets used by the application.
- **Prediction History:** Review previously stored prediction records.
- **Evaluation Reports:** Access model metrics and before-and-after comparisons.
- **Web Interface:** User-friendly interface built using Flask, HTML, and CSS.

## Technologies Used
- Python
- Flask
- Scikit-learn
- Pandas
- NumPy
- HTML5
- CSS3
- SQLite
- Joblib
- Matplotlib

## Project Structure

```text
JobCheck-Fake-Job-Prediction/
├── app.py
├── train_models.py
├── requirements.txt
├── README.md
├── templates/
│   ├── base.html
│   ├── dataset.html
│   ├── history.html
│   ├── index.html
│   ├── performance.html
│   └── report.html
├── static/
│   └── style.css
├── uploads/
│   ├── data.xlsx
│   └── jobcheck_synthetic_fake_job_dataset_300.csv
└── results/
    ├── baseline_model_metrics.csv
    ├── before_after_comparison.csv
    ├── model_metrics.csv
    ├── oversampled_model_metrics.csv
    └── oversampling_recall_comparison.png
```

The trained model file, if included, is named `models.joblib`. The application may also create a SQLite database for prediction history.

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/Anusha-23092005/JobCheck-Fake-Job-Prediction.git
cd JobCheck-Fake-Job-Prediction
```

### 2. Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows:

```bash
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

## Running the Application

Start the Flask application:

```bash
python app.py
```

Open the local URL displayed in the terminal, usually:

http://127.0.0.1:5000

## Model Training

If the trained model file is not included or you want to retrain the classifiers, run:

```bash
python train_models.py
```

Ensure that the required dataset is available at the location expected by the training script.

## Evaluation

The `results/` directory contains evaluation reports for comparing model performance, including baseline metrics, model metrics, oversampled model metrics, and recall comparisons.

Common classification metrics include:
- Accuracy
- Precision
- Recall
- F1-score

These metrics help evaluate how well the models distinguish potentially fraudulent job advertisements from genuine postings.

## Intended Use

JobCheck is an academic machine learning project intended to support preliminary job-posting risk assessment. Its predictions should not be treated as definitive proof that a job posting is fraudulent or genuine. Users should independently verify employers and job offers before sharing personal information or accepting employment.

## Future Enhancements
- Integration with verified employer information.
- Explainable prediction results.
- Enhanced downloadable safety reports.
- Improved detection using larger and more diverse datasets.
- Deployment to a secure cloud platform.

## Author
Anusha

## License
This project is intended for academic and educational purposes. A formal open-source license can be added if required.
