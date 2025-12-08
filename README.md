Consumer-Lending-Risk-Insights

This repository contains a complete Exploratory Data Analysis (EDA) workflow performed on the Credit Risk Previous Loans dataset.
The CaseStudyCODE.ipynb includes data cleaning, missing value treatment, outlier removal, feature engineering, visualization, and statistical hypothesis testing.

Project Files:
📁 credit-risk-analysis/
 ┣ 📓 CaseStudyCODE.ipynb                            → Main notebook with all analysis
 ┣ 📓 REPORT OF THE CASE STUDY.pdf    → Report covering statistical analysis 
 ┣ 📓 requirement.txt                                         → Report covering statistical analysis
 ┣ 📁 data                                                           → Place your dataset here
 ┗ 📜 README.md                                          → Project documentation

1. Project overview
The goal of this analysis is to
•	Clean and prepare the data
•	Analyze relationships between variables
•	Validate insights using statistical testing
•	Prepare the dataset for predictive modelling.

2. Data loading
The dataset is loaded using:
 Initial inspection was performed using:
•	df.head()
•	df.shape
•	df.info()
•	df.describe()

4. Data cleaning
a)	Missing Values
•	Calculated missing percentages.
 
•	Dropped columns with >40% missing values.
•	 
•	Fill null values:
o	Numeric columns → median
o	Categorical columns → mode
b)	Incorrect Values
•	Converted negative day values to absolute using .abs().
•	Added YEARS_DECISION column for better interpretation.
After cleaning, 100% of missing values were handled.

4. Outlier detection & removal
Used IQR (Inter Quartile Range) Method:
 
cols_outliers is a list of column names where remove outliers.
Q1 calculates the 25th percentile (column value).
Q3 calculates the 75th percentile (column value).
lower is lower bound of that column
upper is upper bound of that column
df takes only that rows where the value is between lower and upper bound.

5. Feature Engineering
New features added:
Feature	Description
CREDIT_ANNUITY_RATIO	Ratio of approved credit to annuity
APPLICATION_CREDIT_RATIO	How close application amount is to approved credit
IS_REFUSED	Binary flag for refused loans
IS_APPROVED	Binary flag for approved loans

6. Exploratory Data Analysis (EDA)
In EDA visualization is done and visualization include:
•	Histograms + KDE
•	Boxplots
•	Countplots
•	Scatterplots
•	Correlation heatmap

7. Statistical Hypothesis Testing
Performed to validate findings:
a)	Chi-Square Tests : Categorical relationships.
b)	Two-sample T-Test : Mean comparison between customer groups.








•	
•	
•	
•	

