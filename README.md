# **Customer Churn Prediction**

## **Project Overview**
Customer churn is a critical business problem, particularly in subscription-based industries. This project aims to predict whether a customer will churn (leave the service) using supervised machine learning models. The insights generated can help businesses take proactive measures to retain customers and improve overall profitability.

## **Dataset**
The dataset consists of customer demographic and financial information. The target variable is `Exited`, which indicates whether a customer has churned (`1`) or remained (`0`).

### **Features**
| Feature            | Description                                              |
|-------------------|----------------------------------------------------------|
| RowNumber        | Index of the row (irrelevant for prediction)              |
| CustomerId       | Unique identifier for each customer (irrelevant)          |
| Surname          | Customer's surname (not used for prediction)              |
| CreditScore      | Customer's credit score                                   |
| Geography        | Customer’s country (France, Germany, Spain)               |
| Gender           | Customer’s gender (Male/Female)                           |
| Age              | Customer’s age                                           |
| Tenure           | Number of years with the bank                            |
| Balance          | Customer's account balance                               |
| NumOfProducts    | Number of bank products the customer has                 |
| HasCrCard        | Whether the customer has a credit card (0 or 1)          |
| IsActiveMember   | Whether the customer is active (0 or 1)                  |
| EstimatedSalary  | Estimated annual salary                                  |
| **Exited**       | **Target variable: 1 = Churn, 0 = Retained**             |

## **Project Workflow**

### **1. Data Preprocessing**
- Remove irrelevant features (`RowNumber`, `CustomerId`, `Surname`).
- Encode categorical variables (`Gender`, `Geography`).
- Handle missing values (if any).
- Standardize numerical features for better model performance.

### **2. Model Development**
- Split data into training (80%) and testing (20%) sets.
- Train multiple models including:
  - Logistic Regression (baseline)
  - Random Forest
  - Gradient Boosting (XGBoost, LightGBM, CatBoost)
- Evaluate models using precision, recall, F1-score, and ROC-AUC.

### **3. Hyperparameter Tuning**
- Optimize model parameters using GridSearchCV or RandomizedSearchCV.

### **4. Model Deployment**
- Save the best-performing model.
- Deploy using Flask or FastAPI.
- Integrate with a front-end dashboard for real-time predictions.

## **Installation & Setup**

### **1. Clone the Repository**
```bash
 git clone https://github.com/yourusername/customer-churn-prediction.git
 cd customer-churn-prediction
```

### **2. Install Dependencies**
```bash
 pip install -r requirements.txt
```

### **3. Run the Model Training**
```bash
 python train.py
```

### **4. Run the API Server (for deployment)**
```bash
 python app.py
```

## **Results & Insights**
- The best model achieved an **ROC-AUC score of X.XX**.
- **Feature Importance Analysis:**
  - **Age** and **Balance** were the strongest predictors of churn.
  - **Active customers** were less likely to churn.
- **Business Recommendation:**
  - Provide incentives for customers with high churn risk.
  - Target inactive members with personalized engagement strategies.

## **Contributors**
- **Okon Prince** – Data Scientist
- **Obi Cajetan** _ Data Scientist
- **Lovina Ehimen-Ugbede (Vina)** - NLP Specialist

## **License**
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## **Acknowledgments**
- Inspired by real-world customer churn prediction use cases.
- Special thanks to the open-source machine learning community.

---

**Follow this repository for future updates and improvements!**
