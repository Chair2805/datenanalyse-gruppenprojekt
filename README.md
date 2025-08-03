# datenanalyse-gruppenprojekt
LETS GOOO
# Task 1
## 1.1 Data Leakage and biases (10 marks)
### 1.1.1- 
In the summary above, you’ll notice that they perform a regression of their engineered
features against UPDRS score. They then predict UPDRS score to define a measure called
NQI. They then use NQI as a feature to classify Parkinson’s vs Healthy. Something seems
fishy here. Discuss this for no more than a paragraph (hint: this might be a form of data
leakage).
### 1.1.2- 
Think carefully about the tapping dataset. Can you imagine any biases that might
creep into our dataset? For example, if a patient has Parkinson’s disease, they might use a
computer less (because the disease prevents them), and as such the differences in typing
might be a training effect rather than a disease effect. Discuss this for no more than two
paragraphs (you can use bullet points).

## 1.2. Exploratory Data Analysis (20 marks)
### 1.2.1- 
Using a boxplot, visualise the difference in UPDRS scores for the Healthy and
Parkinson’s patients.
### 1.2.2- 
Test for significant differences of the UPDRS scores between the Healthy participants
and Parkinson’s patients. (Hint: you could use the implementations of scipy.stats or pingouin
to compute the statistics. Remember to test for any assumptions your test of choice might rely
on, like normal distribution etc.)
### 1.2.3- 
Visualise the correlations of all feature variables (for example using seaborn pairplot)
and discuss anything you notice (no more than two paragraphs).

# Task 2: Regression vs UPDRS score (30 marks)
Dataset: Your second task again uses the data in MIT
USERS
_
_
FEATURES.csv
Can we find any predictive information in the typing features that tell us about UPDRS? We will perform a
regression of our features against UPDRS score (a continuous variable).
Questions:
## 2.1 Linear regression of features against UPDRS score (15 marks)
### 2.1.1- 
Perform a linear regression of the feature variables against UPDRS score.Don’t forget
to split your data into training and testing appropriately!
### 2.1.2- 
Which features display the strongest relationship? What are their coefficients? Use an
appropriate measure to define the goodness of fit.

## 2.2 Non-linear regression of features against UPDRS score (15 marks)
### 2.2.1- 
Perform a non-linear regression of the feature variables against UPDRS score, using a
support vector machine. Don’t forget to split your data into training and testing appropriately!
### 2.2.2- 
Compare and contrast your results with the linear regression.

# Task 3: Classification of healthy vs Parkinson's disease (40 marks)
Dataset: Your third task continues with the same file MIT
USERS
_
_
FEATURES.csv.
Can our features classify parkinson’s vs healthy patients? Remember that UPDRS score does not count
as a feature so do not include it in your feature set - we don’t want any data leakage.
Questions:
## 3.1 Logistic regression classification (25 marks)
### 3.1.1- 
Use a logistic regression to classify parkinson’s vs healthy. Report the accuracy on a
test set, or use cross validation and report the mean accuracy. Create a visualisation of the
classification results.
Note: you will need to convert the string values to binary numbers for classification.
### 3.1.2- 
Use a Support Vector Classifier to classify parkinson’s vs healthy. Report the accuracy
appropriately and any accompanying visualisations.

## 3.2 Dimensionality reduction and Classification (15 marks)
### 3.2.1- 
Repeat 3.1.1 and 3.1.2 but on dimensionality reduced features, instead of the original
features. How does the performance compare?
