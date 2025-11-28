# DSA210-Term-Project

## 1. Project Overview

This project aims to analyze how various factors such as education, experience, and personal skills influence individuals’ career satisfaction.
Career satisfaction (measured on a 1–10 scale) represents how fulfilled and content people feel with their professional lives, considering aspects such as salary, work-life balance, and growth opportunities.

The project will use machine learning models — mainly regression-based approaches — to predict Current Satisfaction and identify which factors have the most significant impact.
The analysis will also include feature engineering and hypothesis testing to ensure interpretability and meaningful insights.

## 2. Motivation

As a senior student who will graduate this year and start working soon, I wanted to explore the factors that influence **career satisfaction** — something that I will personally experience in the near future.  
Choosing this topic was both a professional and personal decision: I wanted to understand which aspects of education, experience, and personal skills truly impact how fulfilled people feel in their careers.

While many students focus on grades or technical experience, career satisfaction often depends on a combination of factors — such as **academic background, internships, soft skills, networking, and work-life balance**.  
Through this project, I aim to identify which of these have the strongest correlation with overall career happiness and to build a data-driven model that predicts satisfaction levels based on realistic graduate profiles.

This topic also aligns closely with my upcoming transition from university to professional life, allowing me to interpret the data not only from a statistical perspective but also from a **real-world, personal perspective**.  
Ultimately, the goal is to understand what truly drives success and happiness at work, beyond traditional metrics like salary or GPA.

## 3. Data Collection:
I obtained the dataset from Kaggle as a csv file. This dataset contains ~400 individuals with details about education, experience, and job outcomes.
Dataset: 
| Category | Example Columns | Description |
|-----------|------------------|--------------|
| Demographics | `Age`, `Gender`, `Field_of_Study` | Personal & field info |
| Education | `High_School_GPA`, `University_GPA`, `SAT_Score` | Academic performance |
| Experience | `Internships_Completed`, `Projects_Completed`, `Certifications` | Practical experience |
| Skills | `Soft_Skills_Score`, `Networking_Score` | Communication & interpersonal ability |
| Career Outcomes | `Starting_Salary`, `Work_Life_Balance`, `Current_Satisfaction` | Job success & satisfaction indicators |

**Target variable (Y):** `Current_Satisfaction` (1–10 scale).

Apart from these, there will also be data that I will produce with the data I have.(Feature engineering)

## 4.Plan
### Exploratory Data Analysis (EDA)

- **Data Cleaning & Preprocessing:** Perform data cleaning and preprocessing on the Education and Career Success dataset by handling missing values, normalizing numeric features.

- **Descriptive Statistics:** Perform descriptive statistics to summarize the Education and Career Success dataset by calculating measures such as mean, median, and standard deviation to understand the overall distribution and trends of key variables.
  
- **Visualization:** Histograms, bar charts, scatter plots, and correlation heatmaps.
### Machine Learning Methods
- **Regression Models:** Multiple Linear Regression, Random Forest Regressor to predict continuous satisfaction scores on a 1–10 scale.
- **Classification Models:** Categorize individuals into “Low”, “Medium”, and “High” satisfaction levels for comparative analysis.
## 5. Exploratory Data Analysis (EDA)
### 1. Data Preprocessing

Before performing statistical analysis and modeling, several preprocessing steps were applied to ensure data quality and consistency:

Handling Missing Values:
Continuous variables such as GPA, SAT scores, Work-Life Balance, and Starting Salary were checked for missing values. No missing values ​​and outliers were found.

Normalization of Numeric Features:
Columns with different scales — such as High_School_GPA, University_GPA, Internships_Completed, and Starting_Salary — were standardized using z-score normalization to prepare them for regression models.

### 2. Feature Engineering
## Overall Academic GPA
Academic_Life = (`High_School_GPA` + `University_GPA`)/2
Purpose : To create a single, composite score that represents a student's overall academic level, rather than individual GPA values.

##  Experience Score

Experience_Score = `Internships_Completed` + `Projects_Completed` + `Certifications`

Purpose: To combine all components of practical experience into a single numerical score.
This score better summarizes an individual's level of preparedness for the business world.

## Stress Level
Stress_Level = 10- `Work_Life_Balance`
I reversed the scale so that a higher value means more stress.
In this way, the relationship between stress level and career satisfaction can be examined more easily.

