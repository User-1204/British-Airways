# Predicting Airline Booking Completion: A Machine Learning Approach

**COMPANY**: British Airways (via Forage Virtual Experience)  

**NAME**: Sakshi Makwana   

**DOMAIN**: Machine Learning / Customer Behavior Modeling   

**PLATFORM**: Hosted on Forage



## Project Overview

This project was developed as part of the **British Airways Virtual Data Science Experience** hosted on **Forage**. The objective was to analyze airline customer booking data to predict whether a customer would complete a booking. This involved cleaning and engineering features from the dataset, training a machine learning model, evaluating its performance, and communicating insights in a business-oriented format.

---

## Objectives

- Build a machine learning model to predict booking completion.
- Understand which variables most influence booking behavior.
- Communicate key insights through visualizations and a business summary slide.

---

## Dataset Overview

- **Source**: Provided by Forage as part of the British Airways simulation.
- **Size**: ~100,000 rows (est.)
- **Target Variable**: `booking_complete` (1 = Booking completed, 0 = Not completed)
- **Key Feature Types**:
  - **Temporal**: `flight_hour`, `flight_day`
  - **Behavioral**: `sales_channel`, `trip_type`, `booking_origin`, `route`
  - **Derived Features**: `is_weekend_flight`, `morning_flight`
  - **Engineered**: One-hot encoded categorical variables

---

## Tools & Technologies Used

- Python 3.8+
- Pandas, NumPy – data manipulation
- Matplotlib, Seaborn – visualization
- Scikit-learn – modeling and evaluation

---

## Methodology

1. **Data Exploration & Cleaning**:
   - Removed nulls, inspected distributions.
2. **Feature Engineering**: 
   - Converted `flight_day` to integers.
   - Engineered `is_weekend_flight` and `morning_flight`.
   - One-hot encoded categorical features.
3. **Model Training**: 
   - RandomForestClassifier
   - 80/20 train-test split
   - 5-fold cross-validation
4. **Evaluation**: 
   - Classification report
   - Confusion matrix
   - Visual feature importance and time-based analysis

---

## Model Performance

- **Cross-Validation Accuracy**: ~73%
- **Precision**: ~0.70  
- **Recall**: ~0.003  
- **Confusion Matrix**: High precision, low recall due to class imbalance

---

## Key Insights

- **Purchase lead time** is the strongest predictor of booking.
- **Flight hour and duration** also affect completion likelihood.
- **Booking origin** had minimal influence.
- Bookings were more likely in **early morning hours**.
- Overall booking completion rate was approximately **42%**.

---

## Visual Highlights

Below are some visualizations that illustrate the key insights from the project:

### Top 20 Most Important Features
![Top Features](https://github.com/user-attachments/assets/b8d729ff-fc9e-43ad-93f5-5d560e4e092a)

### Booking Completion Rate by Flight Hour
![Booking by Hour](https://github.com/user-attachments/assets/63e07f9a-d876-4954-8866-f2541128b487)

### Overall Conversion Rate (KPI Visual)
![Conversion KPI](https://github.com/user-attachments/assets/c93376b6-1136-4535-b6d6-40ace6b03f34)

---

## Business Communication

A professional summary slide was created to present the model and insights to stakeholders.

> View it in: `PowerPoint summary.pptx`

---

## Limitations & Future Work

- **Recall** is very low – use SMOTE or weighted metrics
- **Model Tuning**: Try GridSearchCV, XGBoost
- **Deployment**: Streamlit dashboard or Flask app
- **Explainability**: Use SHAP or permutation importance

---

## Note

This project is a portfolio piece from the British Airways x Forage Virtual Experience. Not affiliated with actual British Airways operations.
