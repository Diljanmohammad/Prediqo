# Prediqo
### Predict Smarter. Prepare Better.

Prediqo is a machine learning-powered career readiness platform that estimates a student's placement readiness score and generates personalized recommendations to help identify areas for improvement.

The project demonstrates an end-to-end machine learning workflow, including data preprocessing, model training, prediction, feature-importance analysis, and web application deployment.

## ✨ Features

- **Placement Readiness Score:** Estimates readiness on a scale of 0–100.
- **Readiness Classification:** Categorizes students into four readiness bands.
- **Personalized Recommendations:** Generates prioritized actions to improve career preparation.
- **Feature Importance:** Visualizes the features influencing model predictions.
- **Responsive Interface:** Provides an interactive web experience.
- **REST API:** Supports health checks and readiness predictions.
- **Reproducible Pipeline:** Includes a training script and documented synthetic dataset.

## 🛠️ Tech Stack

| Category | Technologies |
|---|---|
| Programming Language | Python |
| Backend | Flask |
| Machine Learning | Scikit-learn |
| Data Processing | Pandas, NumPy (where used) |
| Frontend | HTML, CSS, JavaScript |
| Deployment | Vercel |

## 📁 Project Structure

```text
prediqo/
├── app.py
├── train_model.py
├── requirements.txt
├── vercel.json
├── README.md
├── LICENSE
├── .gitignore
├── data/
│   └── career_readiness_synthetic.csv
├── model/
│   └── careerlens_model.pkl
├── static/
│   ├── app.js
│   └── style.css
└── templates/
    └── index.html
```

## 🚀 Getting Started

### Prerequisites

- Python 3.12 (recommended)
- Git
- pip

### 1. Clone the repository

```bash
git clone https://github.com/Diljanmohammad/prediqo.git
cd prediqo
```

### 2. Create a virtual environment

**Windows CMD:**

```bat
python -m venv .venv
.venv\Scripts\activate
```

### 3. Install dependencies

```bash
python -m pip install --upgrade pip
pip install -r requirements.txt
```

### 4. Run the application

```bash
python app.py
```

Open your browser and visit:

**http://127.0.0.1:5000**

The repository includes a trained model. Run `python train_model.py` only if you want to reproduce the dataset and model.

## 🔌 API Endpoints

### Health Check

```http
GET /api/health
```

Checks the application's health status.

### Placement Readiness Prediction

```http
POST /api/predict
Content-Type: application/json
```

Send a JSON request containing the input fields defined by `FEATURES` in `app.py`. Refer to the implementation for the exact request schema and response format.

## ⚙️ Machine Learning Workflow

1. **Data Preparation:** Load and prepare the synthetic dataset.
2. **Feature Engineering:** Process the features required by the model.
3. **Model Training:** Train the machine learning model using the training script.
4. **Prediction:** Generate a readiness score and classification.
5. **Recommendations:** Produce prioritized suggestions based on student inputs.
6. **Visualization:** Present prediction results and feature importance.

## ☁️ Deployment

Prediqo can be deployed on Vercel using its Flask application and deployment configuration.

1. Push the project to GitHub.
2. Import the repository into Vercel.
3. Set the root directory to `./`.
4. Verify the Python runtime and deployment configuration.
5. Deploy and test the application.

Check `vercel.json` and the current Vercel runtime requirements before deploying. Renaming the GitHub repository does not automatically change the deployed website's URL or visible branding.

## 📊 Dataset and Limitations

Prediqo uses a synthetic dataset generated through the documented process in `train_model.py`. It is intended for demonstrating machine learning concepts and creating a reproducible application.

The generated readiness score is **not a validated probability of getting placed** and should not be treated as a definitive assessment of a student's abilities.

Real-world use would require representative, appropriately collected data, rigorous model validation, and fairness evaluation.

## 🔮 Future Improvements

- Improve model validation and evaluation.
- Enhance personalized recommendations.
- Add user accounts and progress tracking.
- Introduce model explainability and fairness analysis.
- Evaluate performance using appropriately collected real-world data.

## 📜 License

This project is distributed under the MIT License. See the `LICENSE` file for details.

---

**Prediqo — Predict Smarter. Prepare Better.**
