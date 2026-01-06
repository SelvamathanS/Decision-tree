# Diabetes Prediction using Decision Tree Classifier

This project demonstrates how to use a **Decision Tree Classifier** to predict whether a person has diabetes based on medical attributes. The model is trained, evaluated, and visualized using Python and scikit-learn.

---

## 📌 Project Overview

The objective of this project is to:

* Load and explore a diabetes dataset
* Train a Decision Tree classification model
* Evaluate model performance using accuracy and classification metrics
* Visualize the trained decision tree

---

## 📂 Dataset

* **File name:** `diabetes.csv`
* **Target column:** `Outcome`

  * `0` → No Diabetes
  * `1` → Diabetes
* **Features:** All remaining medical attributes (e.g., glucose, BMI, age, etc.)

> ⚠️ Ensure the dataset path is correct before running the code.

---

## 🧰 Libraries Used

* `pandas`
* `scikit-learn`
* `matplotlib`
* `graphviz`

Install dependencies if needed:

```bash
pip install pandas scikit-learn matplotlib graphviz
```

---

## 🔄 Workflow

### 1. Data Loading

The dataset is loaded using pandas and stored in a DataFrame.

### 2. Feature & Target Separation

* **X:** All columns except `Outcome`
* **y:** `Outcome`

### 3. Train-Test Split

* 80% training data
* 20% testing data

```python
train_test_split(x, y, test_size=0.2)
```

---

### 4. Model Creation

A **Decision Tree Classifier** is used with:

* **Criterion:** `entropy` (Information Gain)

```python
DecisionTreeClassifier(criterion='entropy')
```

> Other options include:
>
> * `gini` (default)
> * `log_loss`

---

### 5. Model Training

The model is trained using the training dataset.

---

### 6. Prediction

Predictions are made on the test dataset.

---

### 7. Model Evaluation

The following metrics are used:

* **Accuracy Score**
* **Classification Report**

  * Precision
  * Recall
  * F1-score
  * Support

Example output:

```
Accuracy: 0.75
```

---

## 🌳 Decision Tree Visualization

### 1. Tree Plot (Matplotlib)

The decision tree structure is visualized using `plot_tree()` with:

* Feature names
* Class names
* Colored nodes for better interpretation

### 2. Graphviz Visualization

A more detailed and interactive tree is generated using `export_graphviz`.

> ⚠️ Graphviz must be installed on your system for this to work properly.

---
