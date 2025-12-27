# ZomatoAnalytics-Rating-Analysis-Prediction

![Python](https://img.shields.io/badge/Python-3.8%2B-3776AB?style=flat&logo=python&logoColor=white)
![Machine Learning](https://img.shields.io/badge/Machine%20Learning-Regression-FF9800)
![Clustering](https://img.shields.io/badge/Unsupervised-KMeans-009688)
![Explainability](https://img.shields.io/badge/XAI-SHAP-673AB7)
![Domain](https://img.shields.io/badge/Domain-Restaurant%20Analytics-607D8B)
![Status](https://img.shields.io/badge/Status-Completed-2E7D32)

>End-to-end data analytics and machine learning project focused on understanding and predicting restaurant ratings using Zomato restaurant data. The project analyzes how factors such as pricing, location, cuisines, services, and customer engagement influence restaurant ratings and overall performance.
>
##  Project Overview
This project analyzes restaurant data from **Zomato** to understand the key factors influencing restaurant ratings and customer engagement.  
The goal is to build an end-to-end **data analytics and machine learning solution** that predicts restaurant ratings, segments restaurants into meaningful groups, and delivers **actionable business insights** using explainable AI techniques.

---

##  Objectives
- Analyze restaurant characteristics such as **cost, location, cuisines, services, and popularity**
- Predict restaurant ratings using **machine learning models**
- Segment restaurants using **unsupervised learning**
- Interpret model predictions using **Explainable AI (SHAP)**
- Ensure **data quality and consistency** through statistical and NLP-based validation

---

##  Dataset Description
The dataset contains information about restaurants listed on Zomato, including:

- **Restaurant metadata:** city, location, establishment type  
- **Pricing details:** average cost for two, price range  
- **Customer engagement:** votes  
- **Services & facilities:** delivery, seating, payment options  
- **Ratings:** numeric ratings and textual rating labels  

**Target Variable:**  
- `aggregate_rating` (numeric restaurant rating)

---

##  Data Cleaning & Preprocessing
Key preprocessing steps performed:
- Removed duplicate and irrelevant identifier columns  
- Handled missing values appropriately  
- Normalized skewed features (e.g., log transformation on votes)  
- Converted multi-valued text fields into numerical features  
- Encoded categorical variables using **One-Hot Encoding**  
- Scaled numerical features where required  

---

##  Feature Engineering
- Created binary service features from restaurant highlights  
- Extracted cuisine counts and cuisine indicators  
- Performed location clustering using latitude and longitude  
- Created cost bins for better interpretability  
- Normalized multilingual `rating_text` values into unified sentiment categories  

---

##  Exploratory Data Analysis (EDA)
- Univariate and bivariate analysis on **ratings, cost, votes, cuisines, and services**
- City-wise, cuisine-wise, and establishment-wise trend analysis  
- Identified outliers and skewed distributions  
- Derived **business-focused insights** from visual patterns  

---

## Machine Learning Models
Models implemented and compared:
- Linear Regression (baseline)
- Random Forest Regressor
- XGBoost
- LightGBM

**Evaluation Metrics:**
- R² Score  
- RMSE  

**Best Performing Models:**
- **XGBoost** and **LightGBM** showed the highest performance  
- Random Forest performed strongly as a non-linear baseline  

---

##  Model Explainability (SHAP)
- Used **SHAP** to interpret global and local feature importance  
- Identified `log_votes` as the strongest predictor of restaurant ratings  
- Analyzed the impact of **cost, location, cuisines, and services**  
- Improved **model transparency and trust**  

---

##  Clustering Analysis
Unsupervised learning was used to segment restaurants:
- Applied **KMeans clustering**
- Selected optimal clusters using the **Elbow Method**

**Identified segments:**
- Budget local eateries  
- Popular delivery-focused restaurants  
- Premium and high-end dining restaurants  

These clusters help understand **restaurant positioning and customer behavior**.

---

## NLP-Based Analysis
- Normalized multilingual `rating_text` values into unified sentiment categories  
- Validated consistency between **textual ratings and numeric ratings**  
- NLP used only for **analysis and validation** (to avoid data leakage)  

---

##  Key Insights
- **Popularity (votes)** is the strongest driver of restaurant ratings  
- Delivery availability significantly impacts customer engagement  
- Premium restaurants tend to have higher ratings but fewer in number  
- Budget restaurants dominate in volume but vary widely in popularity  
- Clustering reveals actionable restaurant segments for business strategy  

---

## Future Scope
- Incorporate customer review text for advanced sentiment analysis  
- Use word embeddings (Word2Vec, GloVe, BERT)  
- Build hybrid neural networks using structured + text data  
- Develop a **restaurant recommendation system**  
- Perform advanced customer segmentation using clustering + NLP  

---

##  Tech Stack
- **Python**
- Pandas, NumPy
- Matplotlib, Seaborn
- Scikit-learn
- XGBoost, LightGBM
- SHAP

---
