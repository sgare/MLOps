# 🏦 Bank Churn Prediction - MLOps Pipeline  

This project demonstrates an **end-to-end MLOps pipeline** for predicting customer churn in a bank.  
It covers model development, experiment tracking, containerization, CI/CD automation, and deployment.  

---

## 📌 Project Overview
- **Problem:** Predict whether a customer will churn.  
- **Solution:** Machine learning classification pipeline with deployment.  
- **MLOps Stack:**  
  - Model Training & Evaluation → Python, Scikit-learn  
  - Experiment Tracking → MLflow  
  - Model Serialization → Joblib  
  - Containerization → Docker  
  - CI/CD → GitHub Actions  
  - Deployment → Hugging Face Spaces (interactive app)  

---

## 📂 Project Structure
.
├── app.py # Streamlit/FastAPI app for predictions
├── train.py # Model training script
├── predict.py # Script for inference
├── src/ # Helper modules (data prep, utils, etc.)
│ ├── data_preprocessing.py
│ ├── model_utils.py
│ └── init.py
├── config.yaml # Model and pipeline configuration
├── requirements.txt # Python dependencies
├── Dockerfile # Docker image setup
├── docker-compose.yml # Multi-service setup (optional)
├── .github/
│ └── workflows/
│ └── ci-cd.yml # GitHub Actions workflow for CI/CD
├── README.md # Project documentation
├── LICENSE # License file
└── .gitignore # Ignore unnecessary files


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

Improved prediction accuracy with hyperparameter tuning.
Automated experiment logging with MLflow.
Seamless deployment with Docker + GitHub Actions.

## Contributing
Pull requests are welcome. For major changes, please open an issue first to discuss.

## License
This project is licensed under the MIT License.
