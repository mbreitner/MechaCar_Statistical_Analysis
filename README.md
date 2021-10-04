# MechaCar_Statistical_Analysis

## Project Ovierview ## 
The goal of this project was to use statistical analysis in R to analyze production metrics across different manufacturing lots. I wanted to identify which variables in my dataset can predict the mpg of the MechaCar prototypes, collect summary statistics on the PSI of the suspension coils from each lot, and run t-tests to determine if each manufacturing lot are statistically different from the mean population. 


## Linear Regression to Predict MPG
![Linear_Regression_Summary](https://user-images.githubusercontent.com/84791455/135931567-dd2d2ad4-5bbe-487c-8c98-f81e91022fce.PNG)

- Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?
    The intercept, vehicle_length, and ground clearance are variables/coefficents that provide a non-random amount of variance to the mpg values. 

- Is the slope of the linear model considered to be zero? Why or why not?
    The slope of the linear model is not considered to be 0 so we can reject the null hypothesis. The p-value is lower than what is considered statistically relevant which is why we can reject the null hypothesis and assume the slope is not 0. 
    
- Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?
    Based on our analysis, this linear model does effectively predict the mpg of the MechaCar prototypes. The Multiple R-squared increases as more variables are passed through the regression model. Although, the adjusted R-sqaured is able to control against the increase in variables and is a more accurate predictor of the success rate of this model. The adjusted R-squared sitting at .6825 suggests that this linear regression model will accurately predict the mpg of the MechaCar Prototypes the majority of the time. 
    

## Summary Statistics on Suspension Coils
![Total_Summary](https://user-images.githubusercontent.com/84791455/135932646-4f6f1758-0cb8-4803-9465-ae69926d2890.PNG)

![Lot_Summary](https://user-images.githubusercontent.com/84791455/135932652-2d7a28b4-1e66-495a-b186-62ee0ef0ba4e.PNG)

- The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. Does the current manufacturing data meet this design specification for all manufacturing lots in total and each lot individually? Why or why not?
    
    Analyzing the variance for each lot, we can conclude that lots 1 & 2 meet the required variance of less than 100. Lot 3 does not meet these requirements because it has a variance that is significantly higher than 100 (170+) and is also significantly higher than the other two lots. The company may want to reconsider how they are measuring the suspension coils or make some serious adjustments to the production methods on lot 3. 
    

## T-Tests on Suspension Coils 
![Entire_lot_T_Test](https://user-images.githubusercontent.com/84791455/135933034-59725199-aae4-46e4-a1ee-56e8d5aa8616.PNG)

When looking at the t-test for all lots, we can fail to reject the null hypothesis because the p-value is greater than 0.05. We cannot reject the fact that the sample mean may be equivalent to the true poplualtion mean. The narrow confidence interval also provides greater accuracy when analyzing our sample. 

![Lot1_T_Test](https://user-images.githubusercontent.com/84791455/135933196-f1996aa1-344d-46c0-adc4-22edbab693cf.PNG)

Lot1 has a p-value of 1 which means we can fail to reject the null hypothesis.

![Lot2_T_Test](https://user-images.githubusercontent.com/84791455/135933245-3f068190-1879-4e85-b05f-32f20f1ce27f.PNG)

Lot 2 also has a p-value greater than 0.05 so we can fail to reject the null hypothesis here as well. 

![Lot3_T_Test](https://user-images.githubusercontent.com/84791455/135933292-5ffc2b69-a5ef-4036-b3b7-a53cb208ef34.PNG)

Lot 3 has a p-value less than 0.05 so we can reject the null hypothesis. 


## Study Design: MechaCar vs. Competition
An additional statistical study that can be performed to analyze MechaCar's ability to beat their competition is a linear regression on city and highway fuel efficiency. As gas prices continue to rise and electric vehicles beginning to take over, this is an important data point that most consumers will consider when looking to purchase a car. 

The metrics that should be included are the following:
  - dependent variable:
    - city and highway fuel efficiency
  - independent variables: 
    - horse power
    - vehicle weight
    - awd capabilities
    - MPG
    
 The null hypothesis would be that city and highway fuel efficieny for MechaCar is more efficient than the competition. 
 


