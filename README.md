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

##### Linear Regression to Predict MPG of MechaCar

![Image_1](https://github.com/walzfran/MechaCar_Statistical_Analysis-/blob/main/Images/MechaLM_Image.png)

##### Image Analysis
* When looking at our linear regression the variables that provide a non-random amount of variance to the MPG would be the 'Vehicle Legnth' and the 'Ground Clearance'. The linear regression model that was run on these variables agains the MPG result in p-values of 2.60e-12 for 'Vehicle Legnth' and 5.21e-08 for 'Ground Clearance'. The intercept for these variables was also significant which indicates that there are probably other factors we are not looking at in this specific dataset that also have impact on the MPG of the MechaCar.
* The slope of the linear model is not considered zero as the p-value of 5.35e-11 is lower than an extreme level of significance which means the null hypothesis must be rejected. When rejecting the null hypothesis, we are determining that the relationship between our variables in the dataset and the MPG of the MechaCar are not just subject to random chance. 
* This linear model does predict the MPG of the MechaCar as the R-Squared is 0.7149 meaning that the model is 71% accurate in determining the MPG. While this is not a completely accurate model it will predict the MPG more than coincidence.

#### Summary Statistics on Suspension Coils

![Image_2](https://github.com/walzfran/MechaCar_Statistical_Analysis-/blob/main/Images/Total_Summary_Image.png)
![Image_3](https://github.com/walzfran/MechaCar_Statistical_Analysis-/blob/main/Images/Lots_Summary_Image.png)
