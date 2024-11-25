## CHD Prediction Project
### Aim
* The aim of this project is to find the optimal combination non-invasive diagnostic tests (in addition to certain patient attributes) to develop a model that can accurately diagnose if a patient is at risk of coronary heart disease.

### Project background
* Coronary heart disease involves the reduction of blood flow to the heart muscle due to build up of plaque of in the arteries of the heart. Presently, invasive coronary angiography represents the gold standard for establishing the presence, location, and severity of CHD.  However, this method is costly and is associated with mortality in patients. Hence, it could be useful to develop a non-invasive diagnostic test for the presence of CHD. 
* It should be noted that several non-invasive diagnostic tests have been proposed by scientific literature. These include tests such as exercise electrocardiogram, thallium scintigraphy and fluoroscopy of coronary calcification. However the diagnostic accuracy of these tests only ranges between 35%-75%. This brings us to the need for a computer aided diagnostic tool. 
* This tool would combine the results of these non-invasive tests with other patient attributes to boost the diagnostic power of these non-invasive methods. This project aims to find that optimal combination and build a model to provide accurate diagnosis. 

### Data structure
* 303 observations and 14 columns (one column is the target column)

### Column description:
	• age: Age of the patient in years
	• sex: Male: 1; Female: 0
	• cp (chest pain type):
		○ 0: typical angina
		○ 1: atypical angina
		○ 2: non-anginal
		○ 3: asymptomatic
	• trestbps: patient's level of blood pressure at resting mode in mm/HG
	• chol (serum cholesterol in mg/dl)
	• fbs: Blood sugar levels on fasting > 120 mg/dl represents as 1 in case of true and 0 as false 
	• restecg: Result of electrocardiogram while at rest:
		○ 0 : Normal 
		○ 1: having ST-T wave abnormality (T wave inversions and/or ST elevation or depression of > 0.05 mV) 
		○ 2: showing probable or definite left ventricular hypertrophyby Estes' criteria
	• thalach: maximum heart rate achieved
	• exang: exercise-induced angina (True/ False)
	• oldpeak: ST depression induced by exercise relative to rest
	• slope: ST segment measured in terms of slope during peak exercise
		○ 0: up sloping
		○ 1: flat 
		○ 2: down sloping
	• ca: number of major vessels (0-3) colored by fluoroscopy
	• thal (blood disorder called thalassemia): 
		○ 0: NULL 
		○ 1: normal blood flow 
		○ 2: fixed defect (no blood flow in some part of the heart) 
		○ 3: reversible defect (a blood flow is observed but it is not normal)
	• target: 
		○ 1 means patient is diagnosed with heart disease
		○ 0 means patient is normal
  
  ### Report structure
	1. Data set overview
		a. Exploring # of cols and rows, column names
		b. Identifying and removing NA values
	2. Exploratory data analysis (EDA)
		a. Univariate analysis
			i. Descriptive statistical analysis for numerical columns
			ii. Univariate bar graphs and stacked bar graphs for categorical columns
		b. Bivariate analysis
			i. Heatmap for correlation analysis
			ii. Difference in means hypothesis testing to test generalize patterns identified in data
			iii. Correlation graphs + line of best fit
	3. Model building
		a. Creating train and test datasets
		b. Using backwards elimination with BIC to determine best model
	4. Evaluation
		a. AUC-ROC evaluation
		b. Determining best predictive threshold
