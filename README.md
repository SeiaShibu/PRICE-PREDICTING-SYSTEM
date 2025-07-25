﻿# PRICE-PREDICTING-SYSTEM
🏷️ Prices Predictor System
This project is a production-grade ML pipeline built with ZenML, MLflow, and scikit-learn to predict prices using a modular, reproducible machine learning workflow.

🚀 Project Features
Modular ZenML Pipelines (training & deployment)

MLflow Tracking for experiment management

Reproducible experiments with steps for preprocessing, training, and evaluation

Model deployment and live predictions with sample_predict.py

Local storage of MLflow runs

Configurable through config.yaml

📁 Project Structure
graphql
Copy
Edit
├── data/                 # Raw datasets
├── pipelines/            # Training and deployment pipelines
├── steps/                # Data preprocessing, model training steps
├── src/                  # Source code for utilities
├── explanations/         # (Optional) Model explanations
├── analysis/             # EDA and notebook analysis
├── mlruns/               # MLflow run artifacts
├── requirements.txt      # Required Python packages
├── config.yaml           # Configurations for model/pipeline
├── run_pipeline.py       # Script to run training pipeline
├── run_deployment.py     # Script to deploy pipeline
├── sample_predict.py     # API-like script to run predictions
└── tests/                # Unit tests
🛠️ Setup Instructions
1. Clone the Repository
bash
Copy
Edit
git clone <repo-link>
cd prices-predictor-system/prices-predictor-system
2. Create Virtual Environment
bash
Copy
Edit
python -m venv venv
venv\Scripts\activate  # Windows
# source venv/bin/activate  # Mac/Linux
3. Install Requirements
bash
Copy
Edit
pip install --upgrade pip
pip install -r requirements.txt
4. Initialize ZenML
bash
Copy
Edit
zenml init
zenml integration install mlflow sklearn
zenml experiment-tracker register mlflow_tracker --flavor=mlflow --tracking_uri=http://127.0.0.1:5000
zenml experiment-tracker set mlflow_tracker
5. Run MLflow Tracking Server (optional for tracking)
bash
Copy
Edit
mlflow ui
6. Run Training Pipeline
bash
Copy
Edit
python run_pipeline.py
7. Run Deployment Pipeline
bash
Copy
Edit
python run_deployment.py
8. Predict from Model
bash
Copy
Edit
python sample_predict.py
🟣 Tech Stack
Python

ZenML

MLflow

scikit-learn

Pandas

