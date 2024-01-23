# Employee Performance Analysis
## INX Future Inc.

## PROJECT SUMMARY:
## BUISNESSCASE & GOAL OF PROJECT: BASED ON GIVEN FEATURE OF DATASET WE NEED TO PREDICT THE PERFOMANCE RATING OF EMPLOYEE
INX Future Inc Employee Performance - Project
The Data science project which is given here is an analysis of employee performance.

### The Goal and Insights of the project are as follows:

Department wise performances
Top 3 Important Factors effecting employee performance
A trained model which can predict the employee performance based on factors as inputs. This will be used to hire employees
Recommendations to improve the employee performance based on insights from analysis
In this comprehensive project, we thoroughly analyzed a dataset containing information on 1200 employees with 28 features. The dataset was divided into quantitative and qualitative features, where 19 features were quantitative (comprising 11 numeric and 8 ordinal columns), and 8 features were qualitative. The 'EmpNumber' feature, containing alphanumeric data, was identified as irrelevant to performance rating and was excluded from further analysis.

Our analysis journey encompassed Univariate, Bivariate, and Multivariate stages, including correlation analysis and a department-wise breakdown. Correlation, a statistical measure revealing linear relationships between variables, played a crucial role in understanding the association between features and performance ratings.

Given the mixed nature of the dataset, incorporating both categorical and numerical data, we approached the project as a classification problem, with the target variable representing ordinal data. To address this, we employed three machine learning models: Support Vector Classifier, Random Forest Classifier, and Artificial Neural Network (Multilayer Perceptron). Among these models, the Artificial Neural Network demonstrated the highest accuracy at 95.80%.

A key objective of the project was to identify the most influential features impacting performance ratings. To achieve this, we employed feature importance techniques within machine learning models. Notably, we utilized Manual and Frequency Encoding methods during preprocessing to convert string-based categorical data into numerical formats. This transformation was crucial as most machine learning algorithms operate on numerical inputs.

The project successfully met its goals through a combination of machine learning models and visualization techniques. The findings not only provided accurate performance rating predictions but also unearthed valuable insights into the factors driving employee performance. The thorough analysis and strategic use of diverse techniques showcase the depth and effectiveness of our approach in addressing the project objectives.

### 1. Requirement
The data provided for this project was sourced from IABAC, where the collected information originates from IABAC™. The dataset revolves around INX Future Inc (referred to as INX), a prominent provider of data analytics and automation solutions, boasting over 15 years of global business presence. INX has consistently held a position as one of the top 20 best employers for the past five years. It's crucial to note that the data does not stem from an actual organization. The entire project was conducted in a Jupyter notebook using the Python platform.

### 2. Analysis
The analysis involved a description of the data features, which play a significant role in the overall analysis. These features provide insights into the relationship between dependent and independent variables. Pandas was utilized to describe the datasets, addressing key questions early in the project. The data within the dataset were categorized into numerical and categorical data, allowing for a comprehensive understanding of the information at hand.

### Categorical Features
1. EmpNumber
2. Gender
3. EducationBackground
4. MaritalStatus
5. EmpDepartment
6. EmpJobRole
7. BusinessTravelFrequency
8. OverTime
9. Attrition

### Numerical Features
1. Age
2. DistanceFromHome
3. EmpHourlyRate
4. NumCompaniesWorked
5. EmpLastSalaryHikePercent
6. TotalWorkExperienceInYears
7. TrainingTimesLastYear
8. ExperienceYearsAtThisCompany
9. ExperienceYearsInCurrentRole
10. YearsSinceLastPromotion
11. YearsWithCurrManager
12. Ordinal Features
13. EmpEducationLevel
14. EmpEnvironmentSatisfaction
15. EmpJobInvolvement
16. EmpJobLevel
17. EmpJobSatisfaction
18. EmpRelationshipSatisfaction
19. EmpWorkLifeBalance
20. PerformanceRating

### 3.Univariate, Bivariate, & Multivariate Analysis
Library Used: Matplotlib & Seaborn Plots Used: Histplot, Violinplot, CountPlot, Barplot

### 1. Univariate Analysis:
In Univariate analysis, the focus is on obtaining unique labels of categorical features, along with exploring the range and density of numerical values. This process involves utilizing Matplotlib and Seaborn libraries to create informative visualizations, including Histplot for numerical data and CountPlot for categorical data. The insights gathered during Univariate Analysis contribute to a comprehensive understanding of individual features.

### 2. Bivariate Analysis: 
Bivariate Analysis involves examining the relationship between each independent feature and the dependent variable. Utilizing Matplotlib and Seaborn, various plots such as histplot and Barplot are employed to visually assess the interactions between variables. This analysis provides valuable insights into how independent features correlate with the target variable, contributing to a nuanced understanding of feature dynamics.

### 3. Multivariate Analysis:
Multivariate Analysis extends the examination to the relationship between two variables concerning the target variable. Employing advanced visualizations such as Violinplot and barplot using Matplotlib and Seaborn, this analysis delves into the complex interactions and dependencies within the dataset.

### 4.Explotary Data Analysis
Basic Check & Statistical Measures
Their is no constant column is present in Numerical as well as categoriacl data.

### Distribution of Continuous Features:
In the initial stages of data exploration, it is crucial to gain a preliminary understanding of how various features are distributed relative to one another. To achieve this, the distplot function from the Seaborn plotting library is employed. This distribution analysis encompasses both numerical features, offering an overarching view of data density and concentration across different levels.

The age distribution spans from 18 to 60, with the majority of employees falling within the 30 to 40 age range.

Employees have varied experiences across multiple companies, with a notable proportion having worked in up to 8 companies. The prevalent trend indicates that many employees joined the company after employment in 2 prior companies.

Hourly rates exhibit a range of 65 to 95, indicating that the majority of employees fall within this salary bracket.

In general, the tenure of most employees in the company does not exceed 5 years. Furthermore, the majority of employees receive a salary hike ranging from 11% to 15%, reflecting a consistent pattern in the compensation structure of the organization.

### Check Skewness and Kurtosis of Numerical Features
### Checking weather the data is Normally distributed or Not with Skewness and Kurtosis,
The numerical feature "YearsSinceLastPromotion" exhibits skewness, as indicated by a skewness value of 1.9724. This positive skewness suggests that the distribution of the data is skewed to the right, with a longer tail on the positive side.
Additionally, the kurtosis value for"YearsSinceLastPromotion" is 3.5194, indicating that the distribution has heavier tails and a more pronounced peak compared to a normal distribution. Overall, these skewness and kurtosis values imply that the data in the "YearsSinceLastPromotion" column is not normally distributed.
### Distribution of Mean of Data
The distribution of the mean closely resembles a Gaussian distribution with a mean value of 9.5. Approximately 80% of feature means fall within the range of 8.5 to 10.5, indicating a central tendency around the mean value.

### Distribution of Standard Deviation of Data
The distribution of the standard deviation in the data exhibits a Gaussian-like pattern. Approximately 30% of feature standard deviations are concentrated in the range of 3 to 20, while the remaining 70% of feature standard deviations fall within the range of 0 to 2.

### 5.Data Pre-Processing
#### 1.checking for Missing Values:
No instances of missing values were identified in the dataset.
#### 2.Categorical Data Conversion:
To manage categorical data with numerous labels, a dual approach of manual encoding and frequency encoding was employed.
**1. Manual Encoding:**
Utilizing the map function, manual encoding proved to be an effective technique. This method involves mapping labels based on their frequency, providing a structured conversion of categorical features.
**2. Frequency Encoding:**
This technique transforms categorical variables into numerical values by considering the frequency distribution. By incorporating value counts, frequency encoding captures the prevalence of each label within the data, facilitating a numerical representation.

#### 3.Outlier Handling:
As certain features exhibit outliers, the approach to address this involves imputation utilizing the Interquartile Range (IQR) method. Given that the data in these features does not conform to a normal distribution, IQR proves to be a robust technique for identifying and managing outliers within the dataset.
#### 4.Feature Transformation:
Addressing the presence of skewness and kurtosis in the "YearsSinceLastPromotion" feature, a Square Root Transformation technique is applied.
Square Root Transformation: This method involves replacing each data point with its square root, particularly useful for count data or small whole numbers. Negative values are converted to positive by adding a constant before the transformation.

**Q-Q Plot:** Utilizing a Q-Q plot, the transformation's effectiveness is visually evaluated by comparing the quantiles of the transformed data against a theoretical distribution.

#### 5. Scaling the Data:
The data is scaled using the Standard Scalar technique.
**Standard Scaling:** Standardization involves scaling the features, assuming a normal distribution. It transforms the features to have a mean of 0 and a standard deviation of 1, ensuring consistency in scaling across the dataset.

### 6.Future Selection
#### 1. Dropping Unique and Constant Features:
The "Employee Number" column is dropped as it contains constant values.
The "Years Since Last Promotion" column is also dropped since a new feature has been created using square root transformation.
#### 2. Checking Correlation:
Correlation is examined through the use of a heatmap.
The heatmap, a graphical representation using color-coding, reveals that there are no highly correlated features present in the dataset.
#### 3.Checking Duplicates:
Thorough examination confirms the absence of any duplicate entries in the dataset.
#### 4. PCA (Principal Component Analysis):
PCA is employed to reduce the dimensionality of the data, which initially contains 27 features after dropping unique and constant columns.
Through PCA, it is determined that using 25 features results in minimal variance loss, making them the selected set for analysis.
Principal Component Analysis is a statistical technique designed to analyze large datasets with numerous dimensions per observation. It aids in enhancing data interpretability, preserving information, and facilitating the visualization of multidimensional data.
#### 5. Saving Pre-Processed Data:
The pre-processed data, incorporating all the transformations and modifications, is saved into a new file.
The target feature is added to the saved file to ensure completeness and facilitate further analysis.

### 1. What were the most important features selected for analysis and why?
- The most important features selected for analysis were determined through Principal Component Analysis (PCA). After dropping unique and constant columns, the dataset initially comprised 27 features. The PCA analysis revealed that retaining 25 features resulted in minimal variance loss. Therefore, these 25 features were considered the most important for further analysis. PCA is utilized to reduce dimensionality while preserving essential variance, making the chosen features representative of the dataset and suitable for in-depth analysis.
 
### 2. Did you make any important feature transformations?
- Yes, an important feature transformation was applied to address skewness and kurtosis in the "YearsSinceLastPromotion" feature. Specifically, a Square Root Transformation technique was employed. This transformation involves replacing each data point with its square root, and it is particularly useful for handling skewness, especially in count data or small whole numbers. Additionally, to handle negative values, a constant was added before the transformation. The Square Root Transformation aims to improve the distributional properties of the "YearsSinceLastPromotion" feature, making it more suitable for analysis.
  
###  3. Correlation or interactions among the features selected and how it is considered?
- In the context of the feature selection process using Principal Component Analysis (PCA), the technique inherently considers correlations or interactions among the features.
Correlations: PCA looks at how features relate to each other.
Interactions: It identifies patterns or interactions among features.
Reduction: PCA simplifies data by combining features, keeping the most important information.
Minimizing Redundancy: It helps avoid using overly similar features, making the analysis more efficient. In essence, PCA considers how features work together, finds important patterns, and simplifies the data for better analysis.

### 7.Machine learning Model Creation & Evaluation
#### 1. Define Dependent and Independent Features:
#### 2. Balancing the Data:
The dataset is observed to be imbalanced, prompting the need for balancing techniques.
SMOTE (Synthetic Minority Oversampling Technique) is employed to address this imbalance. SMOTE is a widely used oversampling method designed to rectify class distribution by randomly generating synthetic instances within the minority class. It alleviates the imbalance issue by creating new instances between existing minority instances.
#### 3. Splitting Training and Testing Data:
The dataset is split into training and testing sets, with 80% of the data allocated for training purposes.
The remaining 20% of the data is reserved for testing, ensuring a comprehensive evaluation of the model's performance on unseen data.
#### Algorithm:
HERE WE WILL BE EXPERIMENTING WITH FIVE ALGORITHM
1. Support Vector Machine
2. Artificial Neural Network [MLP Classifier]
3. XG Boosting
4. Random forest
5. KNN
Support Vector Machine demonstrates robust performance on the training data, achieving an accuracy of 96.61%, while the testing score is slightly lower at 94.66%.
Artificial Neural Network (Multilayer Perceptron) exhibits commendable performance on the training data, achieving an accuracy of 92.08%, and maintains a high testing score of 93.71%.
XG Boosting consistently performs exceptionally well in both training and testing, attaining a 100% accuracy rate. it raises concerns about overfitting.
Random Forest achieves a perfect accuracy of 100% on the training data but slightly decreases to 94.66% on the testing set.
K-Nearest Neighbors performs well on the training data with an accuracy of 94.51%, but the testing score is comparatively lower at 83.61%.
Considering the overall performance, Support Vector Machine is selected as the preferred model due to its strong accuracy and generalization on both training and testing datasets.
### 8.Saving Model
Save model with the helpof pickle file

### Tools and Library Used:
#### Tools:
Jupyter
#### Library Used:
Pandas
Numpy
Matplotlib
Seaborn
pylab
Scipy
Sklearn
Pickle
### Goal 1: Department Wise Performances
PLOT USED
**Violinplot:** It shows the distribution of quantitative data across several levels of one (or more) categorical variables such that those distributions can be compared.

**CountPlot:** countplot is used to Show the counts of observations in each categorical bin using bars.

**1. SALES:**
Among the various performance levels, employees in the sales department consistently exhibit a higher performance rating at level 3 in contrast to levels 2 and 4.
Moreover, a fascinating gender-based disparity emerges within the sales department's performance ratings. The data reveals that female employees tend to receive slightly higher performance ratings compared to their male counterparts.

**2. HUMAN RESOURCES:**
In the Human Resources department there's a clear seen performance rating trend employees often higher performance rating at level 3 compared to both level 2 and level 4. Interestingly, when we look at gender differences, male employees in HR tend to have higher performance ratings compared to their female colleagues.

**3. DEVELOPMENT:**
In the Development department, most employees are getting better performance ratings at level 3 compared to levels 2 and 4. Surprisingly, there's not much of a difference between male and female employees—they both have almost the same ratings.

**4. DATA SCIENCE:**
In the Data Science department, employees tend to excel with higher performance ratings at level 3 compared to levels 2 and 4. Male employees, in particular, are performing well in this department. However, overall performance ratings in this department are lower compared to other departments.

**5. REASEARCH AND DEVELOPMENT:**
In the Research and Development department, employees receive higher performance ratings at level 3 compared to levels 2 and 4. Interestingly, female employees have slightly higher performance ratings than their male counterparts in this department.

**6. FINANCE:**
In the Finance department, employees tend to have higher performance ratings at level 3 compared to levels 2 and 4. Notably, male employees excel in this department.

### Goal 2: Top 3 Important Factors effecting employee performance
The top three important features affecting the performance rating are ordered with their importance level as follows,
1. Employment Environment Satisfaction
2. Employee Salary Hike Percentage
3. Experience Years In CurrentRole
**1. Employee Environment Satisfaction:**
The predominant performance ratings for employees are found at levels 3 and 4, with 367 and 361 employees, respectively, indicating a high level of satisfaction with their work environment.

**2. Employee Last Salary Hike Percent:**
Employees experiencing a salary hike in the range of 11-19% are more likely to receive performance ratings of 2 and 3. In contrast, those receiving a hike between 20-22% tend to achieve higher performance ratings, especially at level 4.

**3. Employee Work-Life Balance:**
Employees who report a work-life balance at level 3 demonstrate higher performance ratings, suggesting a positive association between work-life balance and overall work performance.

### Goal 3: A Trained model which can predict the employee performance
The trained model is created using the machine learning algorithm as follows with the accuracy score,
Support Vector Machine on the training data, achieving an accuracy of 96.61%, while the testing score is slightly lower at 94.66%.
Artificial Neural Network (Multilayer Perceptron) on the training data, achieving an accuracy of 92.08%, and maintains a high testing score of 93.71%.
XG Boosting well in both training and testing, attaining a 100% accuracy rate.
Random Forest achieves a perfect accuracy of 100% on the training data but slightly decreases to 94.66% on the testing set.
K-Nearest Neighbors on the training data with an accuracy of 94.51%, but the testing score is 83.61%.

### Goal 4: Recommendations to improve the employee performance
**1. Prioritize Employee Environment Satisfaction:**
Conduct regular surveys to gauge employee satisfaction with the work environment. Identify areas of improvement based on feedback and implement necessary changes. Foster a positive and inclusive workplace culture to enhance overall satisfaction.

**2. Implement Salary Hikes:**
Consider regular evaluations of employee performance and provide salary hikes as a reward for outstanding contributions. Ensure a transparent and fair system for determining salary increases. Communicate the connection between performance and rewards to motivate employees.

**3. Regular Employee Promotions:**
Establish a policy to promote employees every 6 months, recognizing and rewarding consistent high performance. Provide clear criteria for promotion to encourage career growth and development.

**4. Enhance Work-Life Balance:**
Introduce flexible work arrangements and policies to support better work-life balance. Encourage employees to take advantage of vacation days and provide resources for managing stress.

**5. Promote Gender Diversity in HR Recruitment:**
Actively consider and promote female candidates during HR recruitment. Recognize the strengths and contributions of female employees in the workplace.

While some of the employees who gives feedback like Low & Medium from Job Satisfaction & Relationship Satisfaction feature, such employees gives Excellent performance more in number. So company should focus on them.

------------------------------------------------------------------------ THANK YOU -----------------------------------------------------------------
