# 🚇 San Francisco BART Ridership Analysis and Demand Prediction

This project analyzes **2016–2017 San Francisco Bay Area Rapid Transit (BART)** ridership data to identify passenger flow patterns between stations and to build predictive models for estimating commuter demand between any two stations.

The study focuses on data cleaning, integration, feature engineering, and generating real-world insights to support transportation and urban mobility decision-making.

---

## 🎯 Project Objectives

- Identify the busiest and least-used stations and routes  
- Analyze ridership patterns across time (hourly, daily, weekly)  
- Predict the number of passengers commuting between two BART stations  
- Compare **Machine Learning (ML)** and **Deep Learning (DL)** approaches for demand prediction  

---

## ❓ Question B

**Build a model that can predict the number of people commuting to work by BART between any two stations.**

A supervised regression framework was used to estimate passenger throughput based on station pairs and temporal features.

---

## 📂 Dataset Description

- **Years:** 2016 – 2017  
- **System:** Bay Area Rapid Transit (BART)  
- **Target Variable:** `throughput` (number of passengers)

### Data Preparation & Preprocessing
- Combined 2016 and 2017 ridership datasets  
- Extracted temporal features from timestamps:
  - Hour of day
  - Day of week
  - Day  
- Merged station geographic coordinates (latitude & longitude)  
- Used a **representative sample of 30,000 rows** for model training and evaluation  

---

## 🔍 Exploratory Data Analysis (EDA)

- Identified peak-demand stations and routes  
- Analyzed ridership variations by time of day and weekday  
- Determined time windows with **higher seat availability** based on low passenger density  

---

## ⚙️ Modeling Approach

### Machine Learning Models
- Linear Regression  
- Ridge & Lasso Regression  
- Decision Tree Regressor  
- Extra Trees Regressor  
- Gradient Boosting Regressor  
- **XGBoost Regressor**

### Deep Learning Model
- Fully connected neural network (Dense layers)

---

## 📊 Model Performance

### 🧠 Machine Learning Results

| Model | R² Score |
|------|----------|
| **XGBoost Regressor** | **0.69** |
| Decision Tree | 0.60 |
| Extra Trees | 0.55 |
| Gradient Boosting | 0.41 |
| Linear / Ridge / Lasso | ~0.14 |

**Insights:**
- Tree-based and boosting models significantly outperformed linear models.
- The relationship between features and ridership is highly **non-linear**.
- XGBoost achieved the highest explanatory power by capturing complex interactions.

---

### 🤖 Deep Learning Results

- Training samples: **30,000**
- Training environment: CPU
- Performance:
  - **R² = 0.437**

**Insights:**
- The neural network outperformed linear models.
- However, it underperformed compared to tree-based boosting methods.
- This highlights that deep learning is not always optimal for **tabular data**.

---

## ⚖️ Machine Learning vs Deep Learning

| Approach | Strengths | Outcome |
|--------|-----------|---------|
| Machine Learning | Faster, interpretable | **Best performance** |
| Deep Learning | Learns complex patterns | Moderate performance |

---

## 📈 Potential Data Enhancements

This study relies solely on historical BART ridership data. Model performance could be significantly improved by incorporating external data sources such as:

- Public holidays and special dates  
- Weather conditions (rain, heatwaves, storms)  
- Major events (concerts, sports games, festivals)  
- Employment density around stations  
- Service disruptions and maintenance schedules  
- Train frequency and seating capacity  

Including these variables would allow the model to better capture real-world commuter behavior.

---

## 🏙️ How City Planners & BART Authorities Can Use This Analysis

- Optimize train schedules during peak demand periods  
- Improve passenger comfort by allocating additional trains or cars  
- Plan future capacity and infrastructure investments  
- Reduce operational costs during low-demand periods  
- Support sustainability goals by encouraging public transit usage  
- Enable proactive, data-driven transportation management  

---

## 🧾 Conclusion

- Ridership demand is influenced by multiple external factors not present in the dataset.
- Despite this limitation, tree-based models generated meaningful and reliable predictions.
- This project successfully demonstrates:
  - Exploratory data analysis  
  - Feature engineering  
  - ML vs DL model comparison  

Overall, this work highlights how **data-driven approaches can support smarter and more efficient urban transportation planning**.

---

## 🛠️ Technologies Used

- Python  
- Pandas, NumPy  
- Matplotlib, Seaborn  
- Scikit-learn  
- XGBoost  
- TensorFlow / Keras  

---

