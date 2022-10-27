# churnprediction1
​
# Phase_3_Project
![image](https://user-images.githubusercontent.com/110459255/198085450-30798243-59b7-406a-91a3-0bd8b39fce56.png)
​
### Table of contents 
- [Business Understanding](#business-understanding)
- [Overview](#overview)
- [Business Objective](#business-objective)
- [Project Goal](#projrct-goal)
- [Data Understanding](#data-understanding)
- [Data Preparation](#data-preparation)
- [Exploratory Data Analysis](#exploratory-data-analysis)
- [Preprocessing](#preprocessing)
- [Conclusion](#conclusion)
- [Recommendation](#recommendation)
- [Limitations](#limitations)
​
---
### Business Underastanding
####  Overview
Influenza, commonly known as "the flu", is an infectious disease caused by influenza viruses. Symptoms range from mild to severe and often include fever, runny nose, sore throat, muscle pain, headache, coughing, and fatigue. These symptoms begin from one to four days after exposure to the virus (typically two days) and last for about 2–8 days. Diarrhea and vomiting can occur, particularly in children. Influenza may progress to pneumonia, which can be caused by the virus or by a subsequent bacterial infection. Other complications of infection include acute respiratory distress syndrome, meningitis, encephalitis, and worsening of pre-existing health problems such as asthma and cardiovascular disease.
There are four types of influenza viruses: A, B, C and D. Human influenza A and B viruses cause seasonal epidemics of disease (known as flu season) almost every winter in the United States. Influenza A viruses are the only influenza viruses known to cause flu pandemics, i.e., global epidemics of flu disease.
​
---
### Target Variables
`h1n1_vaccine` - Whether respondent received H1N1 flu vaccine.
​
`seasonal_vaccine` - Whether respondent received seasonal flu vaccine.
​
---
 ###  Business objectives
 Listed below are ways in which the public can help curb the spread of the flu:
​
1.Take time to get a flu vaccine.
 * CDC recommends a yearly flu vaccine as the first and most important step in protecting against flu viruses.Flu vaccines help to reduce the burden of flu illnesses, hospitalizations and deaths on the health care system each year.
 
2.Take everyday preventive actions to stop the spread of germs.
 * Avoid close contact with people who are sick.
 * If you are sick, limit contact with others as much as possible to keep from infecting them.
 * Cover coughs and sneezes.
 * Cover your nose and mouth with a tissue and throw it away after use when you cough or sneeze.
 
3.Take flu antiviral drugs if your doctor prescribes them.
 * If you are sick with flu, antiviral drugs can be used to treat your illness.
 * Antiviral drugs are different from antibiotics. They are prescription medicines (pills, liquid or an inhaled powder) and are not available over-the-counter.
 ---
 
 ### Project goal
 Our main goal for the project is to determine how the following factors affect people's decisions to get the H1N1 and seasonal flu vaccine;
 * To determine how People's Backgrounds(age,education,race,sex,marital status,employment status) affect their decision to get the vaccinated.
 
 * To determine how people's opinions on H1N1 vaccine and seasonal flu vaccine affect  people's decision to get the vaccine.
 
 *To determine how health behaviours(washing hands,buying face masks,avoiding close contact with others,taking antiviral medication,avoiding touching your face) affect people's decision to get the vaccine.
 
 ---
 
 ### 2.Data Understanding
 
`respondent_id` - Unique and random identifier
​
`h1n1_concern` - level of concern about the H1N1 flu.(0 = Not at all concerned; 1 = Not very concerned; 2 = Somewhat concerned; 3 = Very concerned.)
​
`h1n1_knowledge` - Level of knowledge about H1N1 flu.(0 = No knowledge; 1 = A little knowledge; 2 = A lot of knowledge.)
​
`behvioural_antiviral_meds` - Has taken antiviral medications. (binary)
​
`bevioral_avoidance` - as avoided close contact with others with flu-like symptoms. (binary)
​
`behavioral_face_mask` - Has bought a face mask. (binary)
​
`behavioral_wash_hands` - Has frequently washed hands or used hand sanitizer. (binary)
​
`behavioral_large_gatherings` - Has reduced time at large gatherings. (binary)
​
​
`behavioral_touch_face` - Has avoided touching eyes, nose, or mouth. (binary)
​
`doctor_recc_h1n1` - H1N1 flu vaccine was recommended by doctor. (binary)
​
`doctor_recc_seasonal` - Seasonal flu vaccine was recommended by doctor. (binary)
​
`chronic_med_condition` - Has any of the following chronic medical conditions: asthma or an other lung condition, diabetes, a heart condition, a kidney condition, sickle cell anemia or other anemia, a neurological or neuromuscular condition, a liver condition, or a weakened immune system caused by a chronic illness or by medicines taken for a chronic illness. (binary)
​
`child_under_6_months` - Has regular close contact with a child under the age of six months. (binary)
​
`health_worker` - Is a healthcare worker. (binary)
​
`health_insurance` - Has health insurance. (binary)
​
`opinion_h1n1_vacc_effective` - Respondent's opinion about H1N1 vaccine effectiveness.(1 = Not at all effective; 2 = Not very effective; 3 = Don't know; 4 = Somewhat effective; 5 = Very effective.)
​
`opinion_h1n1_risk` - Respondent's opinion about risk of getting sick with H1N1 flu without vaccine.(1 = Very Low; 2 = Somewhat low; 3 = Don't know; 4 = Somewhat high; 5 = Very high.)
​
`opinion_h1n1_sick_from_vacc` - Respondent's worry of getting sick from taking H1N1 vaccine.(1 = Not at all worried; 2 = Not very worried; 3 = Don't know; 4 = Somewhat worried; 5 = Very worried.)
​
`opinion_seas_vacc_effective` - Respondent's opinion about seasonal flu vaccine effectiveness.(1 = Not at all effective; 2 = Not very effective; 3 = Don't know; 4 = Somewhat effective; 5 = Very effective.)
​
`opinion_seas_risk` - Respondent's opinion about risk of getting sick with seasonal flu without vaccine.(1 = Very Low; 2 = Somewhat low; 3 = Don't know; 4 = Somewhat high; 5 = Very high.)
​
`opinion_seas_sick_from_vacc` - Respondent's worry of getting sick from taking seasonal flu vaccine.(1 = Not at all worried; 2 = Not very worried; 3 = Don't know; 4 = Somewhat worried; 5 = Very worried.)
​
`age_group` - Age group of respondent.
​
---
​
### Data Preparation
Within our data preparation phase, we performed the following tasks:
 - Clean Data
    - Removed Duplicates
    - Filled Missing Values
​
---
### Eploratory Data Analysis
Here is a an overview on some of the features and how they affect people's opinion on getting the vaccine
Represenation of the age group dataset
![image](https://user-images.githubusercontent.com/110459255/198104650-de7efbbf-9e9b-43e9-b9b7-64c70a6bc198.png)
The elderly mainly obtain vaccination compared to the rest of the age groups. This could be attributed to the low immune of the elderly people hence the high risk of flu transmission. The rest of the age groups comprising of young adults have a relatively stronger immune making them less prone to contracting the flu illness.
​
To check for the relationship of various factors with H1N1 and Seasonal vaccine; education, gender, employment status and age group were plotted against the two vaccines.
![image](https://user-images.githubusercontent.com/110459255/198158069-74518df4-dd16-4359-9049-f238b59ca7f4.png)
​
​
---
​
### Modeling
We build a couple of models using different featuers in our dataset to try  predicting whether an individual will go for H1N1 vaccine or Seasonal Flu Vaccines.The models have different levels of  accuracy.   
            - Random forest
            - multiple output classifier 
            - Binary relevance (Logistic Regression)
            - Binary relevannce (Gaussian)
            - XGBoost
            
 ### Training the model
 
The model is trained with the training features (X_train) and training labels (y_train) and is given some
new   data   it   hasn't   seen   before   (X_test)   to   evaluate   how   well   it   classifies   the   new   data.
The training or test split percentages do not however affect our workflow. 70% of the data was set for
training purposes while 30% was set for testing purposes.
​
MinMaxScaler
This is a technique used to transform features by scaling each feature to a given range. It is an 
estimator that scales and translates each feature individually such that it is in the given range on 
the training se
 
 ---
 
 ### Reccommendations
 
Since vaccination is the main preventive strategy for influenza, optimizing formations and
identifying factors that interfere with the administration of the vaccine is vital. Identifying factors
that produce a priming effect and enhance response is important in understanding how to
improve efficiency of influenza vaccine. Prospective safety monitoring followed by rigorous
signal refinement is critical to inform decision making by regulatory and public health agencies
​
---
### Conclusion
Our study demonstrates that college graduates, females, those not in the labor force and the 
elderly have the highest turn out in obtaining both the h1n1 vaccine and the seasonal vaccine. 
Evidently, the probability of an individual to get vaccinated against flu is often dictated by; 
demographic factors, what people perceive and day to day behaviors towards preventing 
infection.
​
---
​
 
### Limitations
​
Vaccination data was obtained from electronic records hence subject to errors and misclassification
​
---
​
​
​
 
 
