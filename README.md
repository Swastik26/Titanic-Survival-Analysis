# **Titanic Survival Analysis**

## **Table of Contents**
1. [Project Overview](#project-overview)  
2. [Dataset Description](#dataset-description)  
3. [Data Analysis & Preprocessing](#data-analysis-and-preprocessing)  
4. [Modeling Approach](#modeling-approach)  
5. [Results & Insights](#results-and-insights)  
6. [Installation & Usage](#installation-and-usage)  
7. [Future Work & Contributions](#future-work-and-contributions)  
8. [Contact Information](#contact-information)  

---

## **1. Project Overview**
This project aims to analyze and predict passenger survival on the RMS Titanic using machine learning models. The tragic sinking of the Titanic in **1912** resulted in the loss of over **1,500 lives**, making it one of the deadliest maritime disasters. By analyzing passenger data, we aim to uncover survival patterns and build predictive models to determine survival likelihood based on key features.

### **Objectives:**
- Perform in-depth exploratory data analysis (EDA) to identify survival factors.
- Preprocess the data for machine learning model development.
- Apply and evaluate various models to predict survival.
- Derive meaningful insights from model outcomes.

---

## **2. Dataset Description**
The Titanic dataset contains **891 records** and **12 features**, each providing information about passengers onboard the ship.

| Feature        | Description                        | Example       |
|----------------|-------------------------------------|---------------|
| PassengerId    | Unique identifier                  | 1             |
| Pclass         | Passenger class (1 = First)        | 3             |
| Name           | Passenger name                     | "John Doe"    |
| Sex            | Gender of the passenger            | Male          |
| Age            | Age of the passenger               | 29            |
| SibSp          | Number of siblings/spouses aboard  | 1             |
| Parch          | Number of parents/children aboard  | 0             |
| Ticket         | Ticket number                      | 347082        |
| Fare ($)       | Ticket price                       | 8.05          |
| Cabin          | Cabin number                       | B57           |
| Embarked       | Port of embarkation (C/Q/S)        | S             |
| Survived       | Survival status (1 = Survived)     | 0             |

### **Statistical Summary:**
- Survival rate: **38.4%** (342 passengers out of 891 survived)  
- Gender breakdown: **577 males** (16% survival rate), **314 females** (74% survival rate)  
- Passenger Class Distribution: **216 in First Class**, **184 in Second Class**, **491 in Third Class**  
- Average age: **29.7 years**, with the youngest passenger being **0.42 years** and the oldest **80 years**.

---

## **3. Data Analysis & Preprocessing**
### **Key Steps:**
1. **Handling Missing Values:**
   - Imputed missing values for `Age` using median values per class and gender.
   - Filled missing `Embarked` values with the mode (`S`).

2. **Outlier Detection:**
   - Detected fare outliers using IQR; fares above **$500** were capped.

3. **Feature Engineering:**
   - Created binary features for `FamilyOnBoard` (`SibSp + Parch`).
   - Binned ages into categories: Child (0-12), Teen (13-18), Adult (19-60), Senior (60+).

4. **Data Visualization:**
   - **Survival by Gender:** Females had a survival rate of **74%**, while males had only **16%**.
   - **Survival by Class:** First-class passengers had a **63% survival rate**, compared to only **24%** in Third Class.

---

## **4. Modeling Approach**
### **Models Evaluated:**
1. **Logistic Regression:** A simple baseline model to predict binary outcomes.
2. **Random Forest Classifier:** Improved model capturing non-linear relationships.
3. **Gradient Boosting Classifier:** Best-performing model after hyperparameter tuning.

### **Model Performance Summary:**
| Model                     | Accuracy (%) | Precision | Recall |
|---------------------------|--------------|-----------|--------|
| Logistic Regression       | 79.6         | 0.78      | 0.72   |
| Random Forest Classifier  | 83.2         | 0.81      | 0.76   |
| Gradient Boosting         | 85.7         | 0.83      | 0.80   |

---

## **5. Results & Insights**
### **Key Findings:**
- **Gender Impact:** Females were significantly more likely to survive, as evidenced by a **74% survival rate**.
- **Passenger Class:** First-class passengers had the highest survival rate of **63%**, highlighting the disparity in lifeboat access.
- **Age Factor:** Children under **12 years** had a survival rate of **59%**, compared to **38%** for adults.
- **Family Influence:** Passengers traveling with families had a **20% higher** survival rate.

### **Visualization Summary:**
- Bar plot: Survival rates by passenger class.
- Heatmap: Feature correlations with survival.

---

## **6. Installation & Usage**  

### **Prerequisites:**
- Python 3.8+  
- Required Libraries: `pandas`, `numpy`, `matplotlib`, `scikit-learn`, `seaborn`

### **Installation:**
```bash
git clone https://github.com/your-username/titanic-survival-analysis.git
cd titanic-survival-analysis
pip install -r requirements.txt
```

### **Usage:**
```bash
python main.py
```

---

## **7. Future Work & Contributions**  
### **Planned Enhancements:**
- Integration with additional data sources (weather data on the day of sinking).  
- Experimentation with deep learning models for further accuracy improvement.  
- Deployment as a web application using `Flask` or `Streamlit`.  

### **Contributions:**
Contributions are welcome! Please fork the repository and submit a pull request.

---

## **8. Contact Information**  
Feel free to reach out for collaboration or questions:

- **Email:** [Gmail-ID-Swastik](swastikchattopadhyay.2004@gmail.com)   
- **LinkedIn:** [LinkedIn-Url-Swastik](https://www.linkedin.com/in/swastik-chattopadhyay-398551251/)  

Let's connect and collaborate on data-driven solutions!

