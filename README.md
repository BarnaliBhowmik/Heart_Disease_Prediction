# Heart Disease Prediction

A machine learning web application that predicts the **10-year risk of coronary heart disease (CHD)** based on clinical and lifestyle inputs, built on the Framingham Heart Study dataset.

🎥 **[Watch Demo](https://drive.google.com/file/d/1YQ-G7gmMIsGlcP55gAYt8kTwqInjTgLX/view?usp=sharing)**
<img width="1001" height="521" alt="Screenshot 2026-10-31 070956" src="https://github.com/user-attachments/assets/609bc011-3550-49c6-b3f1-3310072c0306" />
<img width="1007" height="517" alt="Screenshot 2026-10-31 071012" src="https://github.com/user-attachments/assets/479e1a69-fcc1-45a9-b55c-4888423d32f9" />

---

## Overview

This project uses a **Random Forest Classifier** trained on the Framingham Heart Study dataset to assess a patient's 10-year CHD risk. Users fill in a 3-step interactive form, and the model returns an instant prediction.

---

## Features

- 3-step guided form — Personal, Lifestyle, and Cardiovascular inputs
- Real-time interactive sliders for numerical values
- Toggle buttons for categorical fields (Yes / No, Male / Female)
- Background image with 50% opacity for clean visual presentation
- Color-coded result — green for low risk, red for high risk
- Fully integrated Flask backend with pre-trained model and scaler

---

## Tech Stack

| Layer | Technology |
|---|---|
| Frontend | HTML, CSS, JavaScript |
| Backend | Python, Flask |
| ML Model | Random Forest Classifier (scikit-learn) |
| Preprocessing | StandardScaler (scikit-learn) |
| Model Storage | Pickle (`.pkl`) |

---

## Project Structure

```
heart-disease-prediction/
│
├── Models/
│   ├── rf_classifier.pkl       # Trained Random Forest model
│   └── scaler.pkl              # Fitted StandardScaler
│
├── templates/
│   └── index.html              # Frontend UI
│
├── static/
│   └── Heart_Disease.jpeg      # Background image
│
├── app.py                      # Flask application
├── requirements.txt
└── README.md
```

---

## Input Features

The model uses the following 14 clinical features:

| Feature | Type | Description |
|---|---|---|
| Gender | Categorical | Male / Female |
| Age | Numeric | Age in years |
| Current Smoker | Categorical | Yes / No |
| Cigarettes Per Day | Numeric | Average daily cigarette count |
| BP Medications | Categorical | On BP medication or not |
| Prevalent Stroke | Categorical | History of stroke |
| Prevalent Hypertension | Categorical | Diagnosed hypertension |
| Diabetes | Categorical | Diagnosed diabetes |
| Total Cholesterol | Numeric | mg/dL |
| Systolic BP | Numeric | mmHg |
| Diastolic BP | Numeric | mmHg |
| BMI | Numeric | kg/m² |
| Heart Rate | Numeric | Beats per minute |
| Glucose Level | Numeric | mg/dL |

---

## Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/your-username/heart-disease-prediction.git
cd heart-disease-prediction
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run the app

```bash
python app.py
```

### 4. Open in browser

```
http://127.0.0.1:5000
```

---

## Requirements

```
flask
numpy
scikit-learn
```

---

## Sample Test Cases

### High Risk Patient (expected: Heart Disease)

| Field | Value |
|---|---|
| Gender | Male |
| Age | 63 |
| Current Smoker | Yes |
| Cigarettes/Day | 30 |
| BP Medications | Yes |
| Prevalent Stroke | Yes |
| Prevalent Hypertension | Yes |
| Diabetes | Yes |
| Total Cholesterol | 310 |
| Systolic BP | 175 |
| Diastolic BP | 105 |
| BMI | 34.2 |
| Heart Rate | 95 |
| Glucose | 220 |

### Low Risk Patient (expected: No Heart Disease)

| Field | Value |
|---|---|
| Gender | Female |
| Age | 32 |
| Current Smoker | No |
| Cigarettes/Day | 0 |
| BP Medications | No |
| Prevalent Stroke | No |
| Prevalent Hypertension | No |
| Diabetes | No |
| Total Cholesterol | 185 |
| Systolic BP | 112 |
| Diastolic BP | 74 |
| BMI | 22.5 |
| Heart Rate | 68 |
| Glucose | 78 |

---

## Dataset

**Framingham Heart Study** — a longitudinal cardiovascular cohort study.  
Source: [Kaggle — Framingham Heart Study Dataset](https://www.kaggle.com/datasets/aasheesh200/framingham-heart-study-dataset)

---

## License

This project is for educational purposes only and is not intended for clinical use.
