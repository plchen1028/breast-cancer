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



