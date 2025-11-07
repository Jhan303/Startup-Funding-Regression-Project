# 🚀 Startup Investment Regression Project

### 📊 Predicting Startup Investment Amounts from Complex Categorical Data

This project aimed to **predict startup investment amounts** using a highly **unstructured, categorical dataset** containing details such as investor names, verticals, sub-verticals, investment types, and city information.
The challenge lay in **extracting signal** from data that was largely **non-numeric**, inconsistent, and extremely noisy — a true test of end-to-end data cleaning, feature engineering, and model optimization.

---

## 🧠 Project Objectives

* Transform raw, messy startup funding data into a machine learning–ready dataset.
* Engineer meaningful features from categorical data (e.g., investors, verticals, sub-verticals).
* Build and tune regression models capable of approximating real-world investment patterns.
* Evaluate predictive power and interpret model behavior despite data limitations.

---

## ⚙️ Data Overview

| Feature                 | Description                                                        |
| ----------------------- | ------------------------------------------------------------------ |
| **Year**                | Year of the investment (extracted from inconsistent date formats). |
| **Vertical**            | Business sector (e.g., FinTech, HealthTech, EdTech).               |
| **Subvertical**         | Specific industry subdomain.                                       |
| **Investors**           | List of investors (cleaned, standardized, and counted).            |
| **Rare Investor Count** | Feature indicating uncommon investors.                             |
| **Type of Investment**  | Investment type (Seed, Series A, etc.).                            |
| **City**                | Headquarters of the startup.                                       |
| **Amount**              | Target variable — investment amount (in INR).                      |

---

## 🧹 Data Cleaning & Feature Engineering Highlights

* Cleaned **severely inconsistent date fields**, extracting accurate years.
* Reconstructed the **“Investors Name”** column using tokenization, splitting, and fuzzy standardization.
* Identified and merged **duplicate investors** caused by inconsistent naming.
* Created **dummy variables** for key categorical fields and frequency encodings for high-cardinality ones.
* Introduced a **“rare investor” feature** to help capture outlier investor behavior.

---

## 🤖 Modeling Approach

Multiple models were tested, including:

* **Linear Regression**
* **Random Forest Regressor**
* **Gradient Boosting Regressor**

After extensive tuning, the **Random Forest model (max_depth=25)** achieved the best results.

---

## 🧾 Best Model Performance

| Dataset   | RMSE            | MAE            | R²       |
| --------- | --------------- | -------------- | -------- |
| **Train** | ₹124,600,163.49 | ₹14,737,272.18 | **0.79** |
| **Test**  | ₹61,911,191.15  | ₹11,271,369.65 | **0.63** |

---

## 📈 Error Distribution

The model’s percentage error showed a **median of ~65%** and a **mean of ~60.8%** — reasonable given the unpredictability and categorical nature of the data.

| Error Band | Frequency (%) |
| ---------- | ------------- |
| 0–10%      | 9.6           |
| 60–70%     | 8.8           |
| 70–80%     | 8.8           |
| >200%      | 13.7          |

*(Visual chart available in project notebook.)*

---

## 🧩 Key Learnings

* Even **highly categorical datasets** can yield learnable patterns with careful feature engineering.
* **Verticals and investor patterns** contain predictive signal — but over-processing can erase it.
* Handling **rare entities and noise** is crucial for real-world business data.
* This project reinforced the importance of **balanced encoding, leakage prevention,** and **interpretability.**

---

## 📷 Visuals & Outputs

The repository includes:

* A **performance summary table** (`model_results.csv`)
* A **chart of prediction error distribution**
* A **sample of top model predictions**

---

## 🧰 Tech Stack

* **Python** (Pandas, NumPy, Scikit-learn)
* **FuzzyWuzzy / RapidFuzz** for investor standardization
* **Jupyter Notebook** for iterative development

---

**📎 Author:** [Jhan Apodaca](https://profiles.datawars.io/jhan.apodaca)
**🔗 Portfolio:** [DataWars Projects](https://profiles.datawars.io/jhan.apodaca)
**💼 LinkedIn:** [linkedin.com/in/jhan-apodaca](https://linkedin.com/in/jhan-apodaca)
