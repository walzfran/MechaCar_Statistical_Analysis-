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


