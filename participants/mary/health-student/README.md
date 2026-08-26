# 🩺 College Student Health Behavior — Multiclass Classification

## 📌 Project Overview

This project focuses on the analysis and prediction of **college students' health conditions** based on their lifestyle habits, physiological indicators, psychological factors, and physical activity.

The project uses the **College Student Health Behavior Dataset**, a dataset containing approximately **50,000 observations** describing different aspects of students' daily lives and health-related conditions.

The main objective is to develop a **supervised machine learning model** capable of classifying students into one of three health categories:

* 🟢 **Fit** — Healthy and balanced condition
* 🟡 **At-Risk** — Moderate health risks associated with lifestyle or behavioral factors
* 🔴 **Unhealthy** — Higher level of health-related risks

The project combines **data analysis, data preprocessing, exploratory data analysis, machine learning, model comparison, hyperparameter optimization, and model interpretation**.

---

# 🎯 1. Business Understanding

## 1.1 Background

University students face many factors that can affect their physical and psychological well-being.

Academic workload, irregular sleep schedules, sedentary behavior, excessive screen time, unbalanced diets, insufficient physical activity, and psychological stress can all contribute to changes in students' health conditions.

For educational institutions, understanding these factors can help identify students who may require additional support and develop more effective health and prevention strategies.

Machine learning provides an opportunity to analyze multiple behavioral, physiological, psychological, and academic factors simultaneously in order to identify patterns associated with different health conditions.

---

## 1.2 Business Problem

Universities may have access to large amounts of information about students, but identifying students who may be at higher risk of health deterioration can be challenging.

A predictive system could potentially help institutions:

* Identify students with higher health risks;
* Better understand the factors associated with student well-being;
* Support preventive health initiatives;
* Identify behavioral profiles associated with different health conditions;
* Improve student well-being programs;
* Better understand the relationship between academic pressure and psychological well-being;
* Support data-driven decision-making in student health programs.

> ⚠️ **Important:** The model developed in this project should be considered a **decision-support and analytical tool**, not a medical diagnostic system.

---

# 🤖 2. Machine Learning Problem

This project is formulated as a **supervised multiclass classification problem**.

Given a set of explanatory variables describing a student's lifestyle, physiological characteristics, psychological state, and other relevant factors, the model learns a function:

$$
f(X) = y
$$

where:

* **X** represents the explanatory variables;
* **y** represents the student's health condition.

The target variable is:

`health_condition`

with three possible classes:

| Class            | Description                                                                                 |
| ---------------- | ------------------------------------------------------------------------------------------- |
| 🟢 **Fit**       | The student's lifestyle and health indicators correspond to a relatively healthy condition. |
| 🟡 **At-Risk**   | The student's profile presents moderate health-related risks.                               |
| 🔴 **Unhealthy** | The student's profile presents higher levels of health-related risks.                       |

---

# 📊 3. Dataset Description

## 3.1 Dataset Name

**College Student Health Behavior Dataset**

The dataset contains approximately **50,000 observations** and was designed to represent different aspects of college students' lifestyles and health.

According to the dataset description, it was constructed based on trends observed in large-scale student health studies conducted in China and synthesized to reproduce realistic patterns observed in modern university environments.

The dataset combines information from different dimensions of student health, including:

* Lifestyle behaviors;
* Physical activity;
* Sleep;
* Physiological indicators;
* Psychological factors;
* Academic influences;
* Temporal information.

Each observation represents a student's health-related information at a particular point in time.

---

# 🧩 4. Feature Categories

The variables can be organized into several major categories.

## 4.1 Lifestyle Features

These variables describe students' everyday habits and behaviors.

Examples include:

* Sleep duration;
* Water intake;
* Screen time;
* Sitting time;
* Diet type;
* Smoking and alcohol consumption;
* Exercise duration;
* Physical activity level.

These variables help describe how students' daily routines may be associated with their health condition.

---

## 4.2 Physiological Features

The dataset also contains measurable physiological indicators, including:

* Body Mass Index (**BMI**);
* Heart rate;
* Calorie expenditure;
* Step count;
* Physical activity indicators.

These variables provide information about the physical characteristics and activity levels of students.

---

## 4.3 Psychological and Behavioral Features

Psychological and behavioral characteristics are represented through variables such as:

* Stress level;
* Sleep quality;
* Mental health status;
* Academic pressure;
* Social relationships;
* Chronic fatigue;
* Anxiety-related indicators.

These variables are particularly relevant because student health is influenced not only by physical behavior but also by psychological and social factors.

---

## 4.4 Temporal Information

The original dataset also includes temporal information associated with observations.

This makes it possible to investigate how certain behaviors or health-related indicators may change over time, such as:

* Sleep patterns;
* Stress levels;
* Physical activity;
* Other lifestyle behaviors.

---

# 📋 5. Dataset Metadata

| Property                   | Value                                      |
| -------------------------- | ------------------------------------------ |
| **Dataset Name**           | College Student Health Behavior Dataset    |
| **Author**                 | Ziya                                       |
| **Platform**               | Kaggle                                     |
| **Original Dataset**       | `enhanced_student_health_dataset_50k.xlsx` |
| **Number of observations** | ~50,000                                    |
| **Problem Type**           | Multiclass Classification                  |
| **Target Variable**        | `health_condition`                         |
| **Number of Classes**      | 3                                          |
| **License**                | CC0: Public Domain                         |
| **Usability Score**        | 8.82 / 10                                  |
| **Tags**                   | Data Analytics, Data Cleaning              |

---

# 🎯 6. Target Variable

The target variable is:

```text
health_condition
```

It contains three classes:

### 🟢 Fit

Represents students whose health-related indicators and lifestyle patterns correspond to a relatively balanced condition.

### 🟡 At-Risk

Represents students whose lifestyle or health indicators suggest the presence of moderate health-related risks.

### 🔴 Unhealthy

Represents students whose profile is associated with a higher level of health-related risks.

The objective of the machine learning model is therefore to learn the relationship between the explanatory variables and these three health categories.

---

# 💼 7. Project Objectives

## 7.1 Business Objectives

The main business objectives are to:

1. Understand the main factors associated with student health conditions;
2. Identify profiles associated with higher health risks;
3. Explore relationships between lifestyle, psychological factors, academic pressure, and health;
4. Provide data-driven insights that could support student well-being initiatives.

## 7.2 Machine Learning Objectives

From a machine learning perspective, the project aims to:

1. Perform exploratory data analysis;
2. Identify and handle missing values and data quality issues;
3. Prepare the dataset for machine learning;
4. Build several multiclass classification models;
5. Compare model performances using appropriate evaluation metrics;
6. Optimize the best-performing model's hyperparameters;
7. Interpret the model's predictions and identify important features.

---

# 🔬 8. Data Science Workflow

The project follows a typical end-to-end machine learning workflow:

```text
Raw Dataset
     │
     ▼
Data Understanding
     │
     ▼
Data Quality Assessment
     │
     ▼
Exploratory Data Analysis
     │
     ▼
Data Preprocessing
     │
     ▼
Feature Engineering
     │
     ▼
Train / Validation Split
     │
     ▼
Baseline Models
     │
     ▼
Model Comparison
     │
     ▼
Hyperparameter Optimization
     │
     ▼
Model Interpretation
     │
     ▼
Final Predictions
```

---

# ⚠️ 9. Important Considerations

Although the dataset represents realistic patterns of student health behavior, it should not be interpreted as a clinical dataset.

The `health_condition` variable represents the classification provided by the dataset and should not be interpreted as a medical diagnosis.

Furthermore, predictive performance does not necessarily imply causality. For example, if a variable is strongly associated with the target, this does not automatically mean that the variable directly causes the observed health condition.

Therefore, the project focuses on **prediction and pattern discovery rather than medical diagnosis or causal inference**.

---

# 📚 10. Dataset Source

The original dataset is the **College Student Health Behavior Dataset**, published on Kaggle by **Ziya**.

Original file:

```text
enhanced_student_health_dataset_50k.xlsx
```

The competition dataset is a derived version of the original dataset provided for the machine learning prediction task.

The dataset is released under the **CC0: Public Domain** license according to its Kaggle description.

---

# 🚀 11. Project Scope

This project covers the following stages:

* 📊 Exploratory Data Analysis
* 🧹 Data Cleaning
* 🔎 Missing Value Analysis
* 📈 Statistical Analysis
* 🧬 Feature Engineering
* 🤖 Machine Learning
* ⚙️ Hyperparameter Optimization
* 📏 Model Evaluation
* 🔍 Model Interpretation
* 🏆 Final Prediction

The ultimate goal is to build a robust classification pipeline capable of predicting the health condition of college students while providing interpretable insights into the factors associated with each class.

---

## 👩‍💻 Project

**College Student Health Behavior — Machine Learning Classification**

*Data Science / Machine Learning Project*
