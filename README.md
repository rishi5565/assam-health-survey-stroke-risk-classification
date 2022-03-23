# **Project Overview**

* Built a classifier model and detected residents from 23 districts of Assam who might be at a higher risk of stroke.

* Downloaded over 140,000+ observations of Assam Health Survey Data with 53 unique features from https://data.gov.in/ to perform classification on.

* Cleaned, explored and manipulated the entire dataset extensively on Python to make everything usable in our project.

* Engineered new features and performed deep exploration and statistical testing on the data.
* Used 2 different datasets from separate sources to train the stroke risk classifier model.

* Applied Synthetic Minority Over-sampling Technique (SMOTE) and various other methods to overcome extreme imbalance ( 1.8% Minority Proportion ) in the stroke risk dataset before modelling the classifier.

* Built a model that was able to detect the minority class with 75% accuracy.

## Potential Users

* People classified in stroke risk category can be reached out to spread awareness, provide diagnostic tools, medical help, etc. to help them take care of their health.

* The information can be used by insurance companies, health diagnostic companies, pharma companies, hospitals, etc. to directly reach out and find potential clients who might buy products and services in the future.

## Resources Used
* **Assam Health Survey Data:** [Source](https://data.gov.in)
* **Heart Risk Data:** [Source](https://archive.ics.uci.edu/ml/machine-learning-databases/heart-disease/)
* **Stroke Risk Data:** [Source](https://data.mendeley.com/datasets/x8ygrw87jw/1)


## Data Processing
Extensive processing of all our datasets were made to make everything usable for our project. Some of the important ones are mentioned below: 

- Detected a discrepancy with the feature "RestingBP" in our Heart Risk Dataset. Further verified it by checking its measures of central tendency and distribution. Proceeded to make necessary changes.
![enter image description here](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/1.png)

- Classified observations as hypertensive or not hypertensive and plotted the information on a bar graph to visually explore if it had any effect on the occurrence of Heart Disease.
![enter image description here](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/2.png)

- Created bins from age feature and plotted the information on bar graph to visually explore if it had any effect on the occurrence of Heart Disease.
![enter image description here](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/3.png)

- Plotted the Pearson Correlation data among all features of Heart Risk dataset on a heatmap to visually interpret the data before modelling the Classifier.
![enter image description here](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/4.png)

- Engineered new features such as high blood sugar classification in stroke risk dataset in accordance with project.
- Applied SMOTE ( Synthetic Minority Over-Sampling Technique ) on stroke risk dataset to balance the training set before modelling the classifier.
- Took the average of multiple readings if available in Assam health survey dataset to create new features for classification.

##  Modelling and Classification
* Used k-nearest neighbors (KNN) classifier to build our Heart Risk Classifier Model as the dataset was small and simple and the classifier is easy to implement and intuitive to understand. Also, since our data had been cleaned of outliers which could cause issues in KNN Classifier, thus it made it even more suitable to use KNN to produce reliable results.
* Wrote a program and found the optimal Number of Neighbors for the KNN Classifier which produced the best detection ( Recall ) results.![enter image description here](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/5.png)

- After applying SMOTE and balancing the classes in our training set, we used Logistic Regression to build our Stroke Risk Classifier Model as the dataset had simple features and Logistic Regression is easier to implement, interpret, and very efficient to train. Also, since it is very fast at classifying unknown records, it was preferable for classifying our Assam Health Survey Dataset which has a high number of observations.

- Was able to achieve a detection rate ( Recall ) of 75% for the Minority Class in the extremely imbalanced stroke risk dataset.
- Classified everyone with a stroke probability of 60% or above as a high risk of stroke resident in Assam health survey dataset in accordance.


## Data Exploration & Statistical Testing
We explored the data from various angles to find all the interesting points of interest. Some of them are provided below:
* **Rural-Urban Relationship with Stroke Risk**
![Top 15 Most Popular Skills](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/6.png)
We saw that the ratio of observations from rural areas was higher than urban in our dataset. To understand if being from Rural or Urban had any statistical significance on stroke risk, we performed a hypothesis test and concluded that it was indeed statistically significant.
![enter image description here](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/7.png)


* **Districts Relationship with Stroke Risk**
To understand if being from different districts had any statistical significance on stroke risk, we performed a hypothesis test and concluded that it was indeed statistically significant.
![Most Offered Perks](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/8.png)
We also performed a Tukey's HSD (honestly significant difference) test between each pair of districts to find the pairs that were most statistically significant. The top 10 results are as follows.
![enter image description here](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/9.png)




* **Salt Iodine Test Values Relationship with Stroke Risk**
To understand if having different salt iodine test values had any statistical significance on stroke risk, we performed a hypothesis test and concluded that it was not statistically significant as we failed to reject Null Hypothesis
![Top 15 Titles](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/10.png)




* **Record Code Iodine Values Relationship with Stroke Risk**
To understand if having different record code iodine values had any statistical significance on stroke risk, we performed a hypothesis test and concluded that it was not statistically significant as we failed to reject Null Hypothesis
![Top 15 Titles](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/11.png)


* **Sex Feature Relationship with Stroke Risk**
Plotted the Sex feature on a bar graph to visually explore if it had any effect on stroke risk.
![Top 15 Locations offering most In-Office Internships](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/12.png)
We saw that males were more likely to be at a higher risk of stroke than females. To further verify if this was statistically significant, we performed a hypothesis test and concluded that it was indeed statistically significant.
![Top 15 Locations offering most In-Office Internships](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/13.png)



* **Haemoglobin Level Relationship with Stroke Risk**
To understand if having different haemoglobin levels had any statistical significance on stroke risk, we performed a hypothesis test and concluded that it was not statistically significant as we failed to reject Null Hypothesis
![Ratio of In-Office to Work From Home](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/14.png)
* **Diastolic Blood Pressure Relationship with Stroke Risk**
To understand if having difference in diastolic BP levels had any statistical significance on stroke risk, we performed a hypothesis test and concluded that it was indeed statistically significant.
![Duration - Stipend KDE Plot](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/15.png)
* **Pulse Rate Relationship with Stroke Risk**
To understand if having difference in Pulse Rate levels had any statistical significance on stroke risk, we performed a hypothesis test and concluded that it was indeed statistically significant.
![Number of Openings - Stipend KDE Plot](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/16.png)
We also checked the same hypothesis with the 2nd Pulse Reading that was provided in the dataset and came to the same conclusion.
![Number of Openings - Stipend KDE Plot](https://github.com/rishi5565/assam-health-survey-stroke-risk-classification/raw/main/Images/17.png)

## Conclusion
We concluded our project by exporting the dataset of residents who are classified to be in higher risk of stroke category to an excel file named “output_data_stroke.xlsx” with the following features:

* Unique ID
* Sex
* District

### [Note]: ***Please refer to the Detailed Project Report word document for all the in-depth information regarding every decision made and the entire thinking process while working on this project. The above information is just a brief summary of the project.***

Thank You,
Rishiraj Chowdhury
[rishiraj5565@gmail.com](mailto:rishiraj5565@gmail.com)
