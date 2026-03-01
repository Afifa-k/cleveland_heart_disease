# 25-02-2026
- currently studying and planning the project
- read the data mining review section and understood the difference between supervised and unsupervised learning.
- Data Mining has two objectives : classification or predcition
- Classification models predict categorical labels (unordered, discrete). Decision tree and neural networks are used in classification models
- Prediction models predict continuous-valued functions. Regression, Association and clustering are used in prediction models.

# 26-02-2026
## Methodology
- 6 main steps :
  1. Business understanding: understanding the objectives and requirements from a business perspective
     converting this knowledge into a data mining problem definition, and designing a plan to achieve the objectives.
  2. Data understanding: understand the raw data, identify its quality, gain insights,  detect interesting subset to form hypotheses for hidden information.
  3. Data preparation: constructs the final dataset that will be fed into the models, attribute selection, cleaning and transforming.
  4. Data modelling: applying various techniques to get optimal values
  5. Data evaluation: evaluates the model to ensure that it achieves the business objectives. 
  6. Deployment phase: specifies the tasks that are needed to use the models.

# 27-02-2026
## Data Scource 
- 909 records, 15 attributes were obtained from the Cleveland Heart Disease database
- training and testing data was split equally 455 and 454 respectively.
- all the attributes are converted into categorical data.
- there will be 3 models
- Predictable attribute - "Diagnosis" 0 - no disease, 1 - has disease
-  It is assumed that problems such as missing data, inconsistent data, and duplicate data have all been resolved.
## categorical data ->feature engineerinng 
- Descritization/ binning
- ex. age
- if age<35 -> young
- else if age >35 & age<55 -> middle-aged
- else -> old
- Now, convert these categories ["young","middle-aged","old"] to labels [1,2,3] respectively.
- df["Age_category"] = pd.cut(df["Age"],
                              bins = [0,35,55,100],
                              labels = [1,2,3])
- after this you can drop original numerical columns if the model only needs categorical data.
  df = df.drop(["Age",...,], axis = 1) #axis = 1 for cols; 0 for rows
- summary: since we want the data in categorical format, all the numeric values were converted into categories/labels 
although this is different from label encoding as label encoding is just naming and discretization makes the model understand categories like age less than 35 is young.

#01-03-2026
## Mining Models
This section explains that the mining models were built and managed using the DMX query language for training, prediction, and accessing model details. Default settings were used, except for tuning Minimum Support (1) in Decision Tree and Minimum Dependency Probability (0.005) in Naïve Bayes. The models were tested on separate test data and evaluated using accuracy, Lift Chart, and Classification Matrix before deployment.

## read next
Mining Models
