# Second Prototype of Breast Cancer Research Project
Link to Data Science Website: https://sites.google.com/view/pchenportfolio/home

The goal of this project is to showcase the factors involved with a higher risk of breast cancer and dying from it. Predictions and analysis of this 
situation can be applied to the medical field. 

The dataset being included in this project includes more than 4,000 patients with their breast cancer demographics. Categories include different stages of cancer,
race, alive or death status, tumnor size, survival months during treatment, and marital status. The following example visualization shown below is the 
general proportion of patients who have died from breast cancer compared to the ones who have survived from it. It provides a general guideline on
the overal scope of this project. More visualizations on race, survival months, with histograms being provided, are also presented. 

<img width="403" alt="Alive-Dead" src="https://user-images.githubusercontent.com/89415428/217355611-de0c4f6d-b79f-4e78-b209-d3f39390542f.png">


Two methods of analysis are being presented in the project. The first method involves setting up a prediction model based on stages of cancer, the size of tumor, and the age of the patient. This is done to ensure the accuracy of the model and how well it performs under real world usage and conditions. THe second method includes
using a prediction model to calculate the probability of which race has a higher risk of dying from cancer. The first method is in general more preferred because it accounts for a lot of the independent variables which makes it an accurate model for determining which independent variable is likely to play a role in cancer death. 
By generating a summary table, we can see which coefficients or variables have an influence in the patient's mortality. 

<img width="326" alt="Model Coefficients" src="https://user-images.githubusercontent.com/89415428/221886258-7d1f9b17-008f-4217-ac7d-2eec243fc5e2.png">


The results from this analysis show that despite a disproportionate amount of races in the data exploratory analysis, there is no correlation which shows which race has a higher chance of dying from breast cancer (according to the prediction model). According to the summary table, T4 and N3 are the leading factors which will not make a patient alive. 



# Exploratory Data Analysis
The following variables used in this dataset include dead or alive status, survival months, and tumor size as the variables being used for the data analysis. A few statistics and visualizations will be used to portray the number of patients who are alive or dead, the number of survival months while on treatment, and whether or not tumor size affects the patient mortality rate. The data was collected from kaggle and was reported to be from the year 2017.

In the first visualization which is a bar graph, out of the 4,025 patients being surveyed, around 600 patients have died from breast cancer even when receiving treatment. This gives a general consensus on what the death risk could be from having breast cancer. 

<img width="403" alt="Alive-Dead" src="https://user-images.githubusercontent.com/89415428/217355611-de0c4f6d-b79f-4e78-b209-d3f39390542f.png">

The next two images show the patient survival months during treatment. The first image shows the number of patients, who survived breast cancer, with their survival months being recorded in a histogram. What is interesting to note about this data visualization is that the minimum time for treatment starts at around 45 months. For the dead patients, survival months is more Normal with regards to the histogram. This can give an indication that breast cancer treatment, even in its early intended use, can still have patients being dead. 


<img width="403" alt="alive-patient-survival-months" src="https://user-images.githubusercontent.com/89415428/217357617-841a8aee-9b68-4e1a-928f-25c20ec6eb0e.png">
<img width="403" alt="dead-patient-survival months" src="https://user-images.githubusercontent.com/89415428/217357635-69a19bcc-735c-4e2d-95fe-fd5a18463221.png">

The final visualization being used is a slightly skewed Normal histogram which shows tumor size in the demographic of patients who have died from cancer. There is no trend stating that large tumor size leads to an increased chance of death. This could possibly mean that smaller tumors, which can be small and also numerous, could increase the likely hood of death in a patient with cancer. 
<img width="435" alt="Tumor-size-deaths" src="https://user-images.githubusercontent.com/89415428/217358563-c1311e15-91b0-4d7c-9277-f54953a3efd7.png">

What this data exploratory analysis does answer is whether or not treatment in terms of survival months is effective for breast cancer patients. In terms of alive status, survival months matter after a certain minimum time period. For dead patients, the number of survival months is more variable. The analysis also includes the general risk factor for a patient dying from breast cancer. With regards to tumor size, breast cancer deaths do not result from large tumors, but rather smaller ones. 

The following visualization shows the amount of correlation in survival months in patients who were dead. In this case, there is no significant factor which determines a possible correlation between age and survival months for patients who are alive.

![image](https://user-images.githubusercontent.com/89415428/218744082-1545852d-cb58-447f-908a-3588f575172d.png)



The following visualization shows the amount of correlation in survival months in patients who were alive and free from cancer. In this case, there is no significant factor which determines a possible correlation between age and survival months for patients who are alive. In general there is a broad consensus of the cancer treatments taking from around 45 months to 95 months of treatment

![image](https://user-images.githubusercontent.com/89415428/218744120-975feaf2-f237-40a7-89fa-fbbb6ff6e90d.png)



In this analysis, the patients were sampled using a distribution. 1 would represent live patients, and 0 would represent dead patients. 500 samples with each sample being size 50 was used with replacement. In this case, the mean is somewhere between 0.15 and 0.20. The average death rate would be somewhere in this area. 

![image](https://user-images.githubusercontent.com/89415428/218744190-9437f02d-4a9d-4c0e-ad1f-7d1322584148.png)

In general, under certain conditions, we must be very careful about providing the rate or probability that any patient can die. Because the data set is not a time series and was collected only in the year 2017, we cannot make the assumption that this rate is all true for all years. Because we are measuring the rate of death over a period of time, it is recommended to use a Poisson Distribution. Poisson Distributions typically are used for measuring rates in a single unit of time, especially for events which are rare. Depending on the size of risk for breast cancer, Poisson can be used. 

The final image shows the races of people who have died from the cancer. Top image is for dead patients, and lower one is for alive patients. While white people seem to have a much higher risk of deaths, this could be due to a skewed pick from the population. The othe races can include Asian or other unknown race.
![image](https://user-images.githubusercontent.com/89415428/218746475-0428013d-3b4f-44bb-8426-3dcf466c6eee.png)
![image](https://user-images.githubusercontent.com/89415428/218746630-fb45d502-1958-43e4-b954-684148c4c477.png)


# Linear Regression Models

Here is the linear regression model for predicting the survival months of dead patients based on age, tumor size, n stage, and t stage cancer. What the model does 
not account is actually the race. What we can infer from the model is that the line is in general accurate. This model can be used to predict the status of a 
patient based on the stages of cancer, the size of tumor, and the age. The summary table is also generated. 


<img width="446" alt="GLM plot" src="https://user-images.githubusercontent.com/89415428/230967398-e7edc357-865a-4cf8-b47c-aabaad10b2c0.png">

<img width="389" alt="Model Coefficients" src="https://user-images.githubusercontent.com/89415428/230967500-40ee1363-6826-491a-8d2e-6e2468eb95d7.png">




Here is the prediction model that predicts the probablity of death given only race factors. 

<img width="434" alt="Probability of Death by Race" src="https://user-images.githubusercontent.com/89415428/221879495-d0f01442-b11d-47f5-8cf1-0d32f2b36e04.png">
