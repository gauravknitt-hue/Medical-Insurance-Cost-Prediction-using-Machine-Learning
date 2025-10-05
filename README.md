# 🏥 Medical Insurance Cost Prediction 

## Project Overview

This is **Project 11** from the Machine Learning Project Series by Siddhardhan. The goal of this project is to build and evaluate a Machine Learning model to **predict an individual's medical insurance charges** based on personal and demographic features.

---

## 🎯 Key Goal

To develop a **Linear Regression** model capable of accurately estimating the `charges` (insurance cost) using patient data.

---

## 💻 Technologies and Libraries

| Category | Technology/Library | Purpose |
| :--- | :--- | :--- |
| **Language** | **Python** | Primary development language. |
| **Environment** | **Google Colab** | Used for execution and code demonstration. |
| **Data Handling** | **Pandas** (`pd`) | Data loading, manipulation, and DataFrame management. |
| **Numerical Ops** | **NumPy** (`np`) | Handling numerical arrays and reshaping data for the model. |
| **Visualization** | **Matplotlib** (`plt`), **Seaborn** (`sns`) | Exploratory Data Analysis (EDA) and plotting data distributions. |
| **Machine Learning** | **Scikit-learn** (`sklearn`) | Model training (`LinearRegression`), data splitting (`train_test_split`), and evaluation (`metrics`). |

---

## 📂 Dataset

The project uses the **Medical Cost Personal Datasets** (`insurance.csv`).

| Feature | Description | Type/Action |
| :--- | :--- | :--- |
| `age` | Age of the primary beneficiary. | Numerical |
| `sex` | Gender (male/female). | Categorical (requires encoding) |
| `bmi` | Body Mass Index (ideally 18.5 to 24.9). | Numerical |
| `children` | Number of children covered by the insurance. | Numerical |
| `smoker` | Smoking status (yes/no). | Categorical (requires encoding) |
| `region` | Residential area in the U.S. (northeast, southeast, etc.). | Categorical (requires encoding) |
| **`charges`** | **Individual medical costs billed by health insurance.** | **Target Variable** (Numerical) |

---

## ⚙️ ML Workflow

The entire process is broken down into the following stages:

### 1. Data Analysis and Preprocessing

* **Data Loading:** The `insurance.csv` file is loaded into a Pandas DataFrame.
* **Initial Checks:** Identifying the number of rows/columns and confirming the absence of **missing values** (`null` data) in the dataset.
* **Exploratory Data Analysis (EDA):** Visualizing the distribution of key features (e.g., `age`, `bmi`, `charges`) and counts for categorical features (`sex`, `smoker`, `region`).
* **Categorical Encoding:** Converting all text-based categorical features (`sex`, `smoker`, `region`) into numerical labels that the Linear Regression model can understand (e.g., Male $\rightarrow 0$, Female $\rightarrow 1$).

### 2. Splitting Data

* **Features (X) and Target (Y):** Separating the input features (all columns except `charges`) from the target variable (`charges`).
* **Train-Test Split:** Splitting the data into **80% training data** and **20% testing data** using `train_test_split`.

### 3. Model Training and Evaluation

* **Model Initialization:** An instance of the `LinearRegression` model is created.
* **Training:** The model is trained using the **training data (`X_train`, `Y_train`)**.
* **Evaluation:** Model performance is assessed using the **R-squared Score ($\text{R}^2$ Score)** on both the training and testing data. This helps check for issues like **overfitting** (where the model performs well on training data but poorly on test data).

### 4. Predictive System

* A final function is created that takes a new set of input data (with required categorical encoding) and provides the final predicted medical insurance cost. The predictive result is shown to be very close to the actual charges in the source data.

---

## 🚀 How to Run the Code

1.  **Clone the Repository:** Download the project files (assuming the code notebook/script is included).
2.  **Get the Dataset:** Obtain the `insurance.csv` file.
3.  **Use Colab/Jupyter:** Open the notebook/script in a Python environment.
4.  **Execute Cells:** Run the cells sequentially to install dependencies, load the data, train the model, and test the predictive system.

---

## 🎥 Source and Reference

This project is implemented following the tutorial by **Siddhardhan**:

* **Video:** [Project 11. Medical Insurance Cost Prediction using Machine Learning with Python | ML Projects](https://www.youtube.com/watch?v=ntBa7YKc9XM)
* **Channel:** Siddhardhan
