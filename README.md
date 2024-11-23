# On-Time Order Preparation Prediction

In industries like food delivery, e-commerce, and manufacturing, timely order preparation is critical. Being able to predict how long it will take to prepare an order can help businesses manage resources, avoid delays, and keep customers happy. This project uses machine learning to predict order preparation times and classify whether orders will be ready on time or not.

---

## Project Overview

The goal of this project was to build and compare machine learning models to address two key problems:  
1. **Predicting Preparation Time**: Using regression models to estimate how long an order will take to prepare.  
2. **On-Time Classification**: Determining whether an order will be ready on time based on specific criteria.  

By analyzing data, engineering features, and experimenting with different models, this project aimed to provide actionable insights and improve operational efficiency.

---

## How It Works

### **Data Extraction and Preprocessing**
The data was stored in a MySQL database. We started by querying the relevant tables and preparing the dataset. This involved:  
- Cleaning the data to handle missing values and inconsistencies.  
- Engineering new features from timestamps, like order creation times and preparation intervals.  
- Removing outliers using techniques like Z-score and IQR.  
- Balancing the dataset to handle imbalanced labels for the classification task.

### **Task 1: Predicting Preparation Time**
We trained regression models to predict how long it would take to prepare an order, based on features like:  
- Store and product details  
- Planned preparation times  
- Other contextual information  

**Models used**:  
- Linear Regression with regularization (Lasso)  
- Support Vector Regression (SVR)  
- Neural Networks  

**Evaluation metrics**:  
- Mean Absolute Error (MAE)  
- Mean Squared Error (MSE)  
- R-squared  

### **Task 2: On-Time or Late Classification**
This task focused on predicting whether an order would be completed on time. An order was considered late if the actual preparation time exceeded the planned time by more than 5 minutes.  

**Models used**:  
- Logistic Regression  
- Support Vector Machines (SVM)  
- Neural Networks  

**Evaluation metrics**:  
- Accuracy  
- Precision, Recall, and F1-score  
- AUC-ROC  

To improve the classification model's performance, we balanced the dataset using techniques like SMOTE and undersampling.

---

## Tools and Technologies

- **Languages**: Python (pandas, numpy, scikit-learn, imbalanced-learn)  
- **Database**: MySQL for data querying and extraction  
- **Visualization**: Matplotlib and Seaborn for exploratory data analysis  

---

## Results

- **Regression Models**: Achieved accurate preparation time predictions with minimal error (low MAE and MSE).  
- **Classification Models**: Developed a reliable system to classify orders as on-time or late, with strong precision and recall.  
- Identified the most important factors affecting preparation time and on-time delivery, providing actionable recommendations for improvement.

---

## Future Improvements

- Add real-time prediction capabilities by integrating streaming data.  
- Incorporate external factors like weather or traffic to refine predictions further.  
- Test advanced models like XGBoost and ensemble techniques to enhance performance.

---

This project showcases how machine learning can solve practical problems in industries where timing is everything. By improving prediction accuracy, businesses can optimize their workflows and provide a better customer experience.
