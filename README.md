### Report on Classification Models for Social Network Ads Dataset

*** Introduction:
This report documents the application of various classification models to predict whether a user purchased an item based on demographic data and social network 
advertising statistics. The dataset used is "Social_Network_Ads.csv".

*** Dataset Overview:

**Attributes:**
 - The dataset contains demographic information and social network advertising statistics:
 - `Age`, `EstimatedSalary`, `Purchased` (target variable indicating purchase outcome).

*** Exploratory Data Analysis:
  - Initial exploration included loading the dataset (`pd.read_csv()`), examining data types and missing values (`df.info()`), and statistical summaries (`df.describe()`).
  - Checked for class distribution in the target variable (`Purchased`) and visualized it using a bar plot to understand the balance between purchased and not
    purchased instances.

*** Data Preprocessing:

*** Feature Selection:
  - Selected features `Age` and `EstimatedSalary` (`x`) as predictors for modeling.

 *** Feature Scaling:
  - Applied Standard Scaling using `StandardScaler` from `sklearn.preprocessing` to standardize the numerical features (`x`) to have zero mean and unit variance.

  *** Data Splitting:**
  - Split the dataset into training and testing sets using `train_test_split` from `sklearn.model_selection`, with a test size of 20% and a random state of 0.

*** Model Construction and Evaluation:

*** Model 1: Logistic Regression
  *** Description:
    - Implemented Logistic Regression (`LogisticRegression`) with parameters `C=1`, `solver="liblinear"`, and `multi_class="ovr"` to predict purchase outcomes.
    - Evaluated model performance using accuracy score (`accuracy_score`) and visualized the confusion matrix (`confusion_matrix`) using a heatmap (`sns.heatmap()`).

  *** Performance Metrics:
   - Calculated precision (`precision_score`) and recall (`recall_score`) to assess the model's ability to correctly classify positive (purchased) instances.

**Model 2: Decision Tree Classifier
 *** Description:
  - Developed a Decision Tree classifier (`DecisionTreeClassifier`) with parameters `criterion="entropy"` and `splitter="best"` to build a decision tree
    based on the training data.
  - Evaluated model accuracy and visualized the confusion matrix to analyze classification performance.

 *** Performance Metrics:
  - Computed precision and recall scores to evaluate the precision of positive predictions and the model's sensitivity to detect positive instances.

*** Model 3: Random Forest Classifier
 ***Description:
  - Constructed a Random Forest classifier (`RandomForestClassifier`) with `n_estimators=15`, `criterion="entropy"`, and `max_depth=3` to ensemble decision trees.
  - Assessed model accuracy, visualized the confusion matrix, and examined precision and recall scores.

 *** Performance Metrics:
  - Calculated precision and recall to measure the effectiveness of the Random Forest model in correctly identifying positive instances.

*** Conclusion:
 **Model Comparison:
  - Each model (Logistic Regression, Decision Tree, Random Forest) exhibited different strengths in predicting purchase outcomes based on demographic and
    advertising data.
  - **Logistic Regression** provided a straightforward linear approach with interpretable coefficients.
  - **Decision Tree** offered a non-linear decision boundary and could capture complex interactions between features.
  - **Random Forest** further enhanced predictive accuracy through ensemble learning, aggregating multiple decision trees.
  
In conclusion, this report demonstrates the application of classification models to predict purchasing behavior based on demographic and advertising data, 
highlighting their performance and utility in real-world applications such as targeted marketing strategies. Each model's strengths and limitations provide 
insights into choosing the appropriate approach based on specific business needs and data characteristics.
