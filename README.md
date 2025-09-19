# 🏦 Bank Churn Prediction - MLOps Pipeline  

This project demonstrates an **end-to-end MLOps pipeline** for predicting customer churn in a bank.  
It covers model development, experiment tracking, containerization, CI/CD automation, and deployment.  

---

## 📌 Project Overview
- **Problem:** Predict whether a customer will churn.  
- **Solution:** Machine Learning classification pipeline.  
- **MLOps Stack:**  
  - Preprocessing → `data_preprocessing.py`  
  - Model Training & Evaluation → `model_utils.py`  
  - Experiment Tracking → MLflow  
  - Model Serialization → Joblib  
  - Containerization → Docker  
  - CI/CD → GitHub Actions  
  - Deployment → Streamlit app / Hugging Face Spaces  

---

## 📂 Project Structure
.
├── app.py # Streamlit/FastAPI app for predictions
├── train.py # End-to-end training pipeline
├── predict.py # Script for inference
├── data_preprocessing.py # Data loading & preprocessing functions
├── model_utils.py # Model training, evaluation, save/load utils
├── init.py # Makes imports cleaner
├── config.yaml # Configurations (hyperparameters, paths)
├── requirements.txt # Python dependencies
├── Dockerfile # Docker container setup
├── .github/
│ └── workflows/
│ └── ci-cd.yml # GitHub Actions workflow for CI/CD
├── .gitignore # Ignore unnecessary files
└── README.md # Project documentation


---

## ⚙️ Setup & Installation

### 1️⃣ Clone the repository
'''bash
git clone https://github.com/sgare/MLOps.git
cd MLOps
'''

### 2️⃣ Create virtual environment & install dependencies
python -m venv venv
source venv/bin/activate   # On Windows: venv\Scripts\activate
pip install -r requirements.txt

### 3️⃣ Run training
python train.py

### 4️⃣ Run app locally
streamlit run app.py

## MLOps Workflow

Data Preprocessing → clean & prepare data.
Model Training → train ML model with hyperparameters.
Experiment Tracking → log runs, metrics, models in MLflow.
Model Serialization → save best model with Joblib.
Containerization → package app & model into Docker image.
CI/CD Automation → auto-build & deploy via GitHub Actions.
Deployment → serve predictions via Hugging Face Spaces.

## Tech Stack
Language: Python
Libraries: Scikit-learn, Pandas, NumPy, MLflow, Joblib
Deployment: Streamlit, Docker, Hugging Face
CI/CD: GitHub Actions

## Results
Automated data preprocessing & training.
Improved prediction accuracy with hyperparameter tuning.
Reproducible experiments with MLflow.
Seamless deployment with Docker + GitHub Actions.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss.

## License
This project is licensed under the MIT License.
