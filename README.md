# MechaCar_Statistical_Analysis

### Analysis of MechaCar performance with R 

### Overview 

##### AutoRUs is suffering from production troubles on thier new MechaCar and the company is hoping that the data analytics team will be ale to review the production data for a bit of insight that will help the manufaturing team moving forward with production. 

##### The goal of this analysis is to: 
* Identify which variables in the dataset predict the MPG of the MechaCar prototypes
* Collect summary statistics on the pounds per square inch (PSI) of the suspension coils from the manufacturing lots 
* Determine if the manufacturing lots are statistically different from the mean population
* Design a study to compare vehicle performace for the MechaCar vehicles against other vehicles from competing manufacturers

### Results

#### Linear Regression to Predict MPG of MechaCar

![Image_1](https://github.com/walzfran/MechaCar_Statistical_Analysis-/blob/main/Images/MechaLM_Image.png)

##### Analysis
* When looking at our linear regression the variables that provide a non-random amount of variance to the MPG would be the 'Vehicle Legnth' and the 'Ground Clearance'. The linear regression model that was run on these variables agains the MPG result in p-values of 2.60e-12 for 'Vehicle Legnth' and 5.21e-08 for 'Ground Clearance'. The intercept for these variables was also significant which indicates that there are probably other factors we are not looking at in this specific dataset that also have impact on the MPG of the MechaCar.
* The slope of the linear model is not considered zero as the p-value of 5.35e-11 is lower than an extreme level of significance which means the null hypothesis must be rejected. When rejecting the null hypothesis, we are determining that the relationship between our variables in the dataset and the MPG of the MechaCar are not just subject to random chance. 
* This linear model does predict the MPG of the MechaCar as the R-Squared is 0.7149 meaning that the model is 71% accurate in determining the MPG. While this is not a completely accurate model it will predict the MPG more than coincidence.

#### Summary Statistics on Suspension Coils

![Image_2](https://github.com/walzfran/MechaCar_Statistical_Analysis-/blob/main/Images/Total_Summary_Image.png)
![Image_3](https://github.com/walzfran/MechaCar_Statistical_Analysis-/blob/main/Images/Lots_Summary_Image.png)

##### Analysis
* When looking at the Suspension Coil Statistics the dictated variance of the coils must not exceed 100 PSI. The Total Summary Data in the first image is under the 100 PSI and does meet the specifications outlined by AutoRUs. 
* When looking at the second image where the data is broken down by individual lots we see that there is an issue with the products coming from lot 3 as the variance is well above the specifications set by AutoRUs as it is 170.28. With this information gathered on the dataset it would be who of the manufacturers to delve a bit deeper into what is happening at lot 3 as they are not meeting the needs of AutoRUs. 

#### T-Tests on Suspension Coils

![Image_4](https://github.com/walzfran/MechaCar_Statistical_Analysis-/blob/main/Images/Total_PSI_Image.png)

##### Analysis 
* When looking at the results of the T-Test performed on the suspension coils across all of the manufacturing lots it shows that they are not statistically different from the population mean as the the p-value is not low enough at .0603 to reject the null hypothesis. 
* Below I will break down each lot in different T-Tests to see if an where the results skew to either reject or agree with the null hypothesis. 

![Image_5](https://github.com/walzfran/MechaCar_Statistical_Analysis-/blob/main/Images/Lot1_PSI_Image.png)
#####
* When reviewing the T-Test results for Lot 1 it shows that the results are not statistically different from the population mean, the p-value is 1 which means we cannot reject the null hypothesis. 

![Image_6](https://github.com/walzfran/MechaCar_Statistical_Analysis-/blob/main/Images/Lot2_PSI_Image.png)
#####
* When reviewing the T-Test results for Lot 2 it shows that the results are not statistically different from the population mean, the p-value is .6072 which means we cannot reject the null hypothesis. 

![Image_7](https://github.com/walzfran/MechaCar_Statistical_Analysis-/blob/main/Images/Lot3_PSI_Image.png)
#####
* When reviewing the T-Test results for Lot 3 it shows that the results are statistically different from the population mean, the p-value is low enough at .04168 for us to reject the null hypothesis. This means that AutoRUs may want to reject the parts from Lot 3 or perform a deeper inspection to see what is happening at the Lot to create such discrepancies in their products. 

#### Study Design: MechaCar vs. Competition

##### The goal of this analysis is to have the MechaCar perform better than their competitors in the marketplace. When thinking about what drives consumers to purchase a new car there are many factors that come into play: cost, fuel efficiency, horse power, maintenance costs, saftey ratings and also the reliability. I know that when I am looking to purchase such a high ticket item I want to make sure it is going to take me to all of the places I need to go in an efficient and reliable way. In addition to the variables we looked at in the analysis I think that we should perform more tests to look at improving the fuel efficiency to the MechaCar and ensuring that the car performs well in different weather conditions - this is especially important to me as I am located in Michigan so seeing all 4 seasons and having a car that can perform well in each one is very important. 

#### Metrics to Test 
#### For us to analyze the MechaCar against the competition we should measure the following metrics:
* Cost
* Fuel Efficiency
* Performance Rating

#### Null Hypothesis or Alternative Hypothesis 

##### Cost
##### Null Hypothesis: The mean of cost of all vehicles in the sample set are equal
##### Alternative Hypothesis: At least one of the vehilves in the sample set has a different mean of cost than the other vehicles 

##### Fuel Efficiency
##### Null Hypothesis: The mean of fuel efficiency of all vehicles in the sample set are equal
##### Alternative Hypothesis: At least one of the vehilves in the sample set has a different mean of fuel efficiency than the other vehicles 

##### Performance Rating
##### Null Hypothesis: The mean of performance rating of all vehicles in the sample set are equal
##### Alternative Hypothesis: At least one of the vehilves in the sample set has a different mean of performance rating than the other vehicles 

#### Statistical Test 
##### For cost I would use a one-way ANOVA test, this will test the mean for MechaCar against competitors.For fuel efficiency I would use a two-way ANOVA test using city and highway as the variables for MPG on the MechaCar and other competitors cars. And for the performance rating I would use another one-way ANOVA test to test the mean against the MechaCar and the competitors. 

#### Data Needed 
##### For all three of the metrics you would want to have data collected on cost, fuel efficiency and performance ratings. Ideally you would have data collected from at least 50 vehicles for the MechaCar and 4 other competitors in the same car class. This would lead to needing data on at least 250 cars so that you have a wide enough range of information to complete these tests with accuracy and not just coincidence. 

