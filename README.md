# ❤️ Heart Disease Prediction using Machine Learning

A beginner-friendly machine learning project that predicts the likelihood of heart disease based on patient health parameters. The project demonstrates the complete workflow of an ML application, including data preprocessing, model training, model serialization, and deployment using Flask. Users can interact with the trained model through a simple web interface to obtain predictions in real time.

**Project Level:** Beginner

---

## 🚀 Features

- Data preprocessing using Pandas and NumPy
- Heart disease prediction using Random Forest Classifier
- Model and scaler serialization using Pickle
- User-friendly web interface built with Flask
- Real-time prediction based on user inputs

---

## 🛠️ Tech Stack

- **Python**
- **Scikit-learn**
- **Pandas**
- **NumPy**
- **Flask**
- **Pickle**
- **Jupyter Notebook**

---

## 📁 Project Structure

```text
Heart_Disease_Prediction/
│
├── Models/
│   ├── rf_classifier.pkl
│   └── scaler.pkl
│
├── templates/
│   └── index.html
│
├── app.py
├── Modeling.ipynb
├── datasets_4123_6408_framingham.csv
├── .gitignore
└── README.md
```

---

## 📌 Running the Project by Cloning the Repository

### 1. Clone the repository

```bash
git clone <repository-url>
cd Heart_Disease_Prediction
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

### 3. Activate the virtual environment

#### Windows (PowerShell)

```powershell
.\venv\Scripts\Activate.ps1
```

#### Linux/macOS

```bash
source venv/bin/activate
```

### 4. Install the required packages

```bash
pip install -r requirements.txt
```

### 5. Run the Flask application

```bash
python app.py
```

### 6. Open the application

Visit:

```text
http://127.0.0.1:5000
```

---

## 🔨 Running the Project from Scratch

### Step 1: Clone the repository

```bash
git clone <repository-url>
cd Heart_Disease_Prediction
```

### Step 2: Create and activate a virtual environment

```bash
python -m venv venv
```

Activate it:

**Windows**

```powershell
.\venv\Scripts\Activate.ps1
```

**Linux/macOS**

```bash
source venv/bin/activate
```

### Step 3: Install dependencies

```bash
pip install flask pandas numpy scikit-learn jupyter
```

### Step 4: Train the model

Launch Jupyter Notebook:

```bash
jupyter notebook
```

Open and run all cells in:

```text
Modeling.ipynb
```

Ensure the trained model and scaler are saved in the `Models` directory.

### Step 5: Run the Flask application

```bash
python app.py
```

### Step 6: Access the application

Open your browser and navigate to:

```text
http://127.0.0.1:5000
```

---

## ⚠️ Challenges Faced and Solutions

| Challenge | Solution |
|-----------|-----------|
| `FileNotFoundError` while loading the model | Verified the project structure and corrected the model path to `Models/rf_classifier.pkl`. |
| `ModuleNotFoundError: No module named 'sklearn'` | Installed the required dependencies inside the project's virtual environment. |
| Multiple virtual environments (`venv` and `.venv`) were created accidentally | Removed the redundant environment and maintained a single `venv` folder. |
| Git tracking unnecessary files | Configured `.gitignore` to exclude `venv/`, `__pycache__/`, and notebook checkpoint files. |
| Compatibility issues with Python 3.14 while installing Scikit-learn | Used a compatible Python version (Python 3.11) and recreated the virtual environment. |

---

## 📚 Key Learnings

- Understanding the end-to-end machine learning workflow
- Training and evaluating a classification model
- Saving and loading machine learning models using Pickle
- Building simple web applications with Flask
- Managing dependencies using virtual environments
- Using Git and GitHub for version control

---

## 🔮 Future Improvements

- Improve the frontend design and user experience
- Deploy the application on cloud platforms such as Render
- Compare multiple machine learning algorithms
- Add input validation and better error handling

---

## 🙌 Acknowledgements

This project was developed as a learning exercise to understand how machine learning models can be integrated into web applications for real-world use cases.