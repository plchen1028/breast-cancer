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

<img width="326" alt="Model Coefficients" src="https://user-images.githubusercontent.com/89415428/221886211-4e21f440-752d-4cc4-8a9a-6cf043809c06.png">



<img width="434" alt="Prediction_Plot" src="https://user-images.githubusercontent.com/89415428/221869889-878eadca-d2f0-4019-b141-1e4352c2aff6.png">

Here is the prediction model that predicts the probablity of death given only face factors. 

<img width="434" alt="Probability of Death by Race" src="https://user-images.githubusercontent.com/89415428/221879495-d0f01442-b11d-47f5-8cf1-0d32f2b36e04.png">

# Code

Here is the setup of the dataset as well as importing the libraries needed for data processing. 
setwd("C:/Users/Patrick/Desktop/CDS492/Breast Cancer Dataset")
breast_cancer <- read.csv("Breast_Cancer.csv")
library(tidyverse)
library(dplyr)
library(reader)

The first question to ask is the proportion of cancer patients who have survived vs the number being dead. This should give an overall estimate of the general survivalbility of cancer rates. A bar graph is depicted showing the number of patients who are alive or dead. 
glimpse(breast_cancer)
ggplot(data = breast_cancer) +
  geom_bar(mapping = aes(x = Status))

This is the overall histogram of all patients with their survival months being included. 
ggplot(data = breast_cancer) +
  geom_histogram(mapping = aes(x = Survival.Months))

This is the overall histogram of all dead patients with their survival months being included. 

deaths <- filter(breast_cancer, Status == "Dead")
ggplot(data = deaths) +
  geom_histogram(mapping = aes(x = Survival.Months))


This is the overall histogram of all alive patients with their survival months being included. 

alive <- filter(breast_cancer, Status == "Alive")
ggplot(data = alive) +
  geom_histogram(mapping = aes(x = Survival.Months))

Here is the histogram of tumor sizes based on dead patients. 
deaths <- filter(breast_cancer, Status == "Dead")
ggplot(data = deaths) +
  geom_histogram(mapping = aes(x = Tumor.Size))

Here is the distribution of survival months for dead patients. 
ggplot(data = deaths) +
  geom_point(mapping = aes(x = Age, y = Survival.Months))

Here is the distribution of survival months for alive patients. 
ggplot(data = alive) +
  geom_point(mapping = aes(x = Age, y = Survival.Months))


Here is the code for calculating the average rate from dead and alive patients. 

patients <- c(rep(0, 3408), rep(1, 616))


n_samples <- 500
sample_size <- 50

create an empty vector to store the sample means

sample_means <- vector("numeric", n_samples)

take samples and calculate the mean of each sample
for (i in 1:n_samples) {
  sample <- sample(patients, sample_size, replace = TRUE)
  sample_means[i] <- mean(sample)
}

plot the sampling distribution
hist(sample_means, main = "Sampling Distribution of Dead and Alive Patients",
     xlab = "Sample Mean", ylab = "Frequency")


ggplot(data = alive) +
  geom_bar(mapping = aes(x = Race))
  
This is the code for converting the alive or death status of patients to binary values for prediction. 

breast_cancer$status <- ifelse(breast_cancer$Status == "Alive", 1, 0)

The model is created based on age, tumor size, stages of cancer, and is based on binomial prediction. 

model <- glm(status ~ Age + Tumor.Size + T.Stage + N.Stage, data = breast_cancer, family = binomial)
summary(model)

breast_cancer$predicted_status <- predict(model, type = "response")

Here is the overall plot of the prediction model. 

library(ggplot2)
ggplot(breast_cancer, aes(x = predicted_status, y = status)) +
  geom_point() +
  geom_smooth(method = "glm", method.args = list(family = "binomial"), se = FALSE) +
  xlab("Predicted probability of death") +
  ylab("Observed status (0 = alive, 1 = dead)") +
  ggtitle("Logistic regression model predictions")

The summary of the model shows which variables have a higher influence of predicting the likelihood of patients dying from cancer. 

summary(model)

Here is rhe prediction model used to determine if race actually is a significant variable in patient deaths. 

logistic_model <- glm(Status ~ Race, data = breast_cancer, family = "binomial")
summary(logistic_model)

probs <- predict(logistic_model, type = "response")
race_probs <- tapply(probs, breast_cancer$Race, mean)

Create a bar plot of the probabilities
barplot(race_probs, xlab = "Race", ylab = "Probability of Death",
        ylim = c(0,1), col = "blue", main = "Probability of Death by Race")



