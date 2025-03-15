
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

## 📦 **Setup**
### 1. **Clone the Repository**
```bash
git clone git@github.com:snehapriya-bs/MlOps-Fundamentals.git
cd MlOps-Fundamentals
```

### 2. **Install Dependencies**
```bash
pip install -r requirements/test_requirements.txt
```

---

## 🏋️‍♀️ **Training the Model**
Train the model using:
```bash
python titanic_model/train_pipeline.py
```

---

## 🌐 **Running the API**
Start FastAPI server:
```bash
uvicorn titanic_model.routes:app --host 0.0.0.0 --port 8000
```

---

## 🚀 **Testing the API**
Test prediction with `curl`:
```bash
curl -X POST "http://localhost:8000/predict" -H "Content-Type: application/json" -d '{"Pclass": 3, "Sex": "male", "Age": 22, "SibSp": 1, "Parch": 0, "Fare": 7.25}'
```

---

## 🧪 **Run Tests**
Run unit tests:
```bash
pytest tests/
```

---

## 🐳 **Docker Deployment**
1. **Build the Docker image**  
```bash
docker build -t titanic-pipeline .
```
2. **Run the container**  
```bash
docker run -p 8000:8000 titanic-pipeline
```

---

## ✅ **GitHub Actions**
- CI/CD is automated using GitHub Actions (`.github/workflows/main.yml`)  
- Runs tests and checks automatically on push/pull requests  

---

## ✅ **Endpoints**
| Method | Endpoint | Description |
|--------|----------|-------------|
| POST   | `/predict` | Predict survival outcome |
| GET    | `/health`  | Check API health status |

---

## 🎯 **Model Details**
- Dataset: Titanic dataset  
- Vectorizer: Stored in `vectorizer.pkl`  
- Model: Trained using Logistic Regression, stored in `model.pkl`  

---

## 🏆 **Future Improvements**
- Add monitoring and logging  
- Automate model retraining  
- Extend to other datasets  

---

Let me know if you’d like to modify or refine anything! 😎
