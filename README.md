
# **Titanic Survival Prediction – MLOps Pipeline**

This project implements an end-to-end **MLOps pipeline** for predicting Titanic passenger survival using machine learning. It includes data preprocessing, model training, testing, and deployment using FastAPI and GitHub Actions.

---

## 🚀 **Project Structure**
```
titanic_pipeline/
├── .github/workflows/       # GitHub Actions for CI/CD
├── requirements/           # Dependency files
├── tests/                  # Unit tests
├── titanic_model/          # Model definition and training logic
├── MANIFEST.in             # Package metadata
├── Makefile                # Automation commands
├── mypy.ini                # Type checking configuration
├── pyproject.toml          # Build system configuration
├── script.py               # Script for manual testing
└── setup.py                # Package setup
```

---

## 📦 **Setup - When run Locally**
### 1. **Clone the Repository**
```bash
git clone git@github.com:snehapriya-bs/MlOps-Fundamentals.git
cd MlOps-Fundamentals
```

### 2. **Install Dependencies**
```bash
python -m venv fastapi
fastapi\Scripts\activatet
```

### 3. **Install Dependencies**
```bash
pip install -r requirements/test_requirements.txt
```

## 🏋️‍♀️ **Training the Model**
Train the model using:
```bash
python titanic_model/train_pipeline.py
```

## 🧪 **Run Tests**
Run unit tests:
```bash
pytest tests/
```

## ✅ **## 📦 **Setup - with GitHub Actions**
- CI/CD is automated using GitHub Actions (`.github/workflows/main.yml`)  
- Runs tests and checks automatically on push/pull requests  


## 🏆 **Future Improvements**
- Add monitoring and logging
- Adding API 
- Automate model retraining  
- Extend to other datasets  


