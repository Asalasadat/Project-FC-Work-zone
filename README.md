# 🚗 FC-Work-Zones

**Fuel Consumption & Driver Behavior Prediction using Machine Learning and Neural Networks**

FC-Work-Zones is a data-driven framework that analyzes driver behavior and its impact on fuel consumption using real vehicle trajectory data. The project integrates volatility-based behavioral features with clustering, regression, and deep learning models to provide insights into how different driving styles affect energy efficiency across road infrastructures such as **intersections** and **roundabouts**.

---

## 📘 Overview

The main objective of this project is to identify distinct driver behavior patterns and accurately predict fuel consumption based on trajectory-derived features. The framework extracts ten **Volatility Measures (VM1–VM10)**, clusters drivers using **K-Means**, and applies multiple predictive models—including **Linear Regression**, **Random Forest**, and **Neural Networks (TensorFlow/Keras)**—to estimate fuel consumption at the individual driver level.

---

## 🧩 Framework Architecture

### 1️⃣ Data Preprocessing

* Combined and cleaned multiple vehicle trajectory datasets.
* Filtered car trajectories only.
* Handled missing values and extreme outliers.
* Normalized features using **StandardScaler** and **MinMaxScaler**.

### 2️⃣ Feature Extraction – Volatility Measures

* Computed **10 Volatility Measures (VM1–VM10)** capturing variations in:

  * Speed
  * Acceleration
  * Vehicle position
* Interpretation:

  * **High volatility** → aggressive driving behavior
  * **Low volatility** → smooth and conservative driving

### 3️⃣ Driver Behavior Classification

* Applied **K-Means Clustering** to identify three driver behavior categories:

  * 🟦 **Conservative**: steady speed, cautious maneuvers
  * 🟩 **Normal**: balanced and rule-compliant driving
  * 🟥 **Aggressive**: frequent acceleration/deceleration and risky behavior
* Visualized clusters using:

  * Radar Charts
  * PCA-based 2D Scatter Plots

### 4️⃣ Fuel Consumption Estimation

* Estimated fuel consumption using physics-based equations depending on:

  * Longitudinal velocity
  * Acceleration
  * Distance traveled per frame
* Aggregated fuel consumption per driver and per infrastructure type (intersection / roundabout).

### 5️⃣ Predictive Modeling

The following regression models were developed and evaluated:

| Model                       | Library            | Description                                                            | R²   | MSE   |
| --------------------------- | ------------------ | ---------------------------------------------------------------------- | ---- | ----- |
| Linear Regression           | scikit-learn       | Captures linear relationship between volatility and fuel usage         | 0.93 | 2.73  |
| Random Forest Regressor     | scikit-learn       | Ensemble model for complex non-linear patterns                         | 0.93 | 3.14  |
| Neural Network (Sequential) | TensorFlow / Keras | Deep model with ReLU, dropout, batch normalization, and early stopping | 0.92 | ≈3.00 |

All models achieved strong performance (**R² > 0.92**), demonstrating a clear relationship between driving behavior volatility and fuel consumption.

---

## 🧠 Discussion & Insights

* **Linear Regression** achieved the highest accuracy (R² ≈ 0.93), indicating a near-linear relationship between extracted features and fuel consumption.
* **Random Forest** provided comparable performance while offering interpretability through feature importance analysis. The most influential features were velocity, acceleration, and volatility measures (VM3, VM5, VM8).
* **Neural Networks** showed stable convergence and minimal overfitting, successfully modeling complex non-linear relationships.

Overall, the proposed framework effectively combines behavioral analysis with energy consumption prediction, supporting smarter and more sustainable transportation systems.

---

## 📊 Visualizations

* **Radar Charts**: Comparison of behavioral characteristics across clusters.
* **PCA Plots**: 2D visualization of clustered driver styles.
* **Training Curves**: Neural Network loss convergence.
* **Feature Importance**: Random Forest permutation importance analysis.

---

## 🛠️ Technologies & Tools

| Category         | Tools                                                   |
| ---------------- | ------------------------------------------------------- |
| Programming      | Python (Google Colab / Jupyter Notebook)                |
| Data Analysis    | Pandas, NumPy                                           |
| Visualization    | Matplotlib, Seaborn, Plotly                             |
| Machine Learning | scikit-learn (KMeans, Linear Regression, Random Forest) |
| Deep Learning    | TensorFlow / Keras                                      |
| Version Control  | Git & GitHub                                            |

---

## 📈 Key Results Summary

| Metric | Linear Regression | Random Forest | Neural Network |
| ------ | ----------------- | ------------- | -------------- |
| R²     | 0.929             | 0.926         | 0.921          |
| MSE    | 2.73              | 3.14          | 3.00           |
| MAE    | 1.12              | 1.18          | 1.15           |

The results confirm the robustness and consistency of the framework in predicting fuel consumption based on driver behavior patterns.

---

## 👩‍💻 Authors & Supervision

This research project was developed by:

* **Asala Asdat**
* **Nawras Farhat**

Under the supervision of **Dr. Huthaifa Al-Ashqar**
Arab American University (AAUP)

📄 A research paper based on this work is currently under preparation and will be published in an academic journal.

---

## 🧾 Citation

Nawras Farhat & Asala Asdat (2025).
**FC-Work-Zones: Fuel Consumption and Driver Behavior Prediction using Machine Learning and Neural Networks**.
Under the supervision of Dr. Huthaifa Al-Ashqar, Arab American University.
*(Manuscript under publication process)*
