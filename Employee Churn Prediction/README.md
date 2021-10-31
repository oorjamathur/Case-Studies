## Employee Churn Prediction -  A Case Study

![ChurnAnalysis](https://cdn.ragan.com/wp-content/uploads/2017/09/Signs_Employees_Might_Quit.jpg)

### Story
For any industry employee attrition can be a big concern. Dissatisfied employees leave the company which can ead to heavy osses in the company.
It is important for a compan to retail it's employees otherwise new workforce might take time to adjust and costs in terms of training etc.
For this reason, employee satisfaction is primal.
In churn analysis we try to find the root causes of churning, so that actions can be taken in those areas to reduce the attrition rates.

### Data
There are 2 datasets available - EmployeeData.csv, employee_satisfaction_data.xlsx.
The datasets need to be merged and then insights have to be developed.
The goal is to find out top 3 reasons that are promoting churning of employees.

### Data Set Highlights
#### EmployeeData.csv (shape: (14999, 9))
1. employee_id - employee id's
2. number_project	- no. of projects the employee has worked for
3. average_montly_hours	- no. of hours spent by an employee in a month in office
4. time_spend_company	- no. of years for which employee has been working in this company
5. Work_accident - any accidents in workspace
6. promotion_last_5years - if he has been promoted in last 5 years
7. department	- department of the employee ('sales', 'accounting', 'hr', 'technical', 'support', 'management', 'IT', 'product_mng', 'marketing', 'RandD') - Categorical
8. salary - salary category of the employee ('low', 'medium', 'high') - Categorical
9. left	- Target column (whether employee has churned or not)

#### employee_satisfaction_data.xlsx (shape: (14999, 3))
1. EMPLOYEE #	- employee id
2. satisfaction_level	- level of satisfaction of the employee (27 missing values)
3. last_evaluation - last performance metric (27 missing values)

### Handling Missing Values
satisfaction_level, last_evaluation had missing values which were handled by mean imputation because that didn't seem to change the distribution of these variables much

### ML Algorithm
1. Logistic Regression (hyperparameter tuning: class_weight)
2. Random Forest

### DL Algorithm
1. Tensorflow Keras

### Best Performing Model based on Recall and F1 score - Random Forest

### Top 3 features that are responsible for attrition
1. satisfaction_level
2. time_spend_company
3. number_project

### Insights and Intel shared
1. work to increase the satisfaction levels of the employees
2. Pay more attention to employees in Product manager, RandD and Marketing departments as they tend to churn more.
3. Salary is not playing a major role, so efforts should be given into increasing the satisfaction levels of employees by giving on the spot awards to dereserving employees.
4. Hawthorne principles must be obeyed. (People shoudn't be trated as machines)
5. Send out appreciation mails, gifts etc to emplyees on festivals to promote positive environment in office. 
