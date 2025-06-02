
# 🩺 Pima Indians Diabetes Classification

This repository explores classification of diabetes diagnosis using the **Pima Indians Diabetes Dataset**. Two models are implemented and compared:

- 🌳 **Custom Decision Tree Classifier**
- 💠 **Support Vector Machine (SVM)**

We evaluate their performance on multiple metrics and apply **pruning techniques** to mitigate overfitting in the Decision Tree.

---

## 📂 Repository Structure



pima-diabetes-classification/
│
├── data/
│   └── diabetes.csv                 # Dataset (768 samples, 8 features)
│
├── notebooks/
│   └── analysis.ipynb              # Full Jupyter notebook
│
├── src/
│   ├── **init**.py
│   ├── preprocess.py               # Data loading and preprocessing
│   ├── models.py                   # Model definitions (DT and SVM)
│   └── evaluate.py                 # Metric evaluation and utilities
│
├── results/
│   └── evaluation\_metrics.md       # Side-by-side performance comparison
│
├── README.md                       # Project overview and usage
└── requirements.txt                # Python dependencies


---

## 🧬 Dataset Overview

- **Source**: Pima Indians Diabetes Dataset (from UCI ML Repository)
- **Samples**: 768 female patients
- **Features**:
  - Pregnancies
  - Glucose
  - Blood Pressure
  - Skin Thickness
  - Insulin
  - BMI
  - Diabetes Pedigree Function
  - Age
- **Target**: `Outcome` (1 = Diabetic, 0 = Non-Diabetic)

---

## 🛠️ Setup Instructions

bash
# Clone the repository
git clone https://github.com/levi1775/pima-diabetes-classification.git
cd pima-diabetes-classification

# Create a virtual environment (optional but recommended)
python -m venv venv
source venv/bin/activate  # or venv\Scripts\activate on Windows

# Install dependencies
pip install -r requirements.txt

---

## 🔍 Model Training & Evaluation

The following models are implemented:

### 🌳 Decision Tree (Custom Implementation)

* Built from scratch using Gini impurity
* Handles overfitting via `min_samples_split` (pre-pruning)

### 💠 Support Vector Machine (SVM)

* Trained using `scikit-learn`
* Feature scaling applied

---

## 📊 Performance Metrics

| Model         | Accuracy | Precision | Recall | F1-Score |
| ------------- | -------- | --------- | ------ | -------- |
| Decision Tree | 0.78     | 0.74      | 0.70   | 0.72     |
| SVM           | 0.81     | 0.79      | 0.74   | 0.76     |

> 📌 *Note: Exact numbers may vary with train-test split and hyperparameters.*

---

## ✂️ Pruning Strategy

To address **overfitting** in Decision Trees:

* ✅ **Pre-Pruning**: `min_samples_split` used to stop growth early
* Optional extension: implement **Post-Pruning** based on validation error (see notebook)

---

## 📁 Files Breakdown

| File                            | Description                               |
| ------------------------------- | ----------------------------------------- |
| `preprocess.py`                 | Loads, scales, and splits the dataset     |
| `models.py`                     | Custom Decision Tree and SVM training     |
| `evaluate.py`                   | Metrics: Accuracy, Precision, Recall, F1  |
| `notebooks/analysis.ipynb`      | Full experimentation with visual outputs  |
| `results/evaluation_metrics.md` | Markdown output of final model comparison |

---

## 🚀 Future Work

* Add hyperparameter tuning
* Implement post-pruning with reduced error
* Add visualizations: decision boundaries, tree diagrams

---

## 🧠 Author

**Your Name**
BTech in Material Science • Passion for Machine Learning
📧 [vedantpimple1775@gmail.com](mailto:vedantpimple1775@gmail.com)
🔗 [LinkedIn](linkedin.com/in/vedant-pimple-523a65228/) | [GitHub](https://github.com/levi1775)

---

## 📜 License

This project is licensed under the MIT License.

