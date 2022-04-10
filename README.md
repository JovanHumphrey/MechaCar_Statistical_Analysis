# MechaCar_Statistical_Analysis

## Project Overview

Working with AutosRUs to troubleshoot issues with their new prototype: the MechaCar. The project required statistical analysis. For the purpose of this analysis, I utilized the R programing language to manipulate the data, run the analysis, and create plots. I’ve provided summary statistics for different variables, visualizations for different datasets, and an interpretation of the test results. Lastly, given the scope of the project I've also proposed additional study designs with hypothesis and analysis.

# Deliverable 1

## Linear Regression to Predict MPG

The MechCar_mpg.csv dataset contains mpg test results for 50 MechaCar prototypes. These prototypes were produced using multiple design specs such as vehicle length and ground clearance to identify vehicle performance. I performed a linear regression model to predict the mpg of MechaCar prototypes using the variables from the provided dataset.

### MPG Linear Regression Results
![linear_regression_summary](https://github.com/JovanHumphrey/MechaCar_Statistical_Analysis/blob/main/Images/linear_regression_summary.JPG)

### Questions and Answers About Linear Regression

<b>Which variables/coefficients provided a non-random amount of variance to the mpg values in the dataset?</b>

<b>Variable P-Values</b>
Vehicle Length: 2.608e-08
Vehicle Weight: 0.0776
Spoiler Angle: 0.3069
Ground Clearance: 5.21e-08
All Wheel Drive (AWD): 0.1852

Null hypothesis can be explained by random chance. Alternative hypothesis cannot be explained by random chance. In this model our null hypothesis would be that the variables play no part in the mpg fuel-efficiency of the prototypes. Our alternative hypothesis would be that the variables play some role in fuel-efficiency. We use the p-value to provide evidence as to which hypothesis is true, by measuring the p-value against a significance level. Generally speaking, a significance level of 5% is sufficient to make that determination. If the p-value is smaller than our significance level, we can state that there is sufficient evidence to reject the null hypothesis. Alternatively, if the p-value is larger than the significance level we would state that we don't have sufficient evidence to reject the null hypothesis.

By comparing the p-value of each variable against the p-value of the regression model (5.35e-11), using the significant level as a measurement we can reject the null hypothesis for the vehicle length, spoiler angle, and AWD. In other words, these variables influence fuel-efficiency.

<b>Is the slope of the linear model considered to be zero? Why or why not?</b>

The p-value for the model is 5.35e-11 which is smaller than 5%, therefore the slope of the model is not zero.

<b>Does this linear model predict mpg of MechaCar prototypes effectively? Why or why not?</b>

The r-squared value of this model is .7149 which indicates that we have 71% prediction accuracy. This suggests a positive correlation between fuel-efficiency and the measured variables. 


# Deliverable 2

## Summary Statistics on Suspension Coils

The MechaCar Suspension_Coil.csv dataset contains the results from multiple production lots. The weight capacities of multiple suspension coils were tested to determine if the manufacturing process was consistent across lots. The design specifications for the MechaCar suspension coils dictate that the variance of the suspension coils must not exceed 100 pounds per square inch. I created a table to show the total summary and the lot summary. The total summary looks at PSI information across all three lots, while the lot summary shows the PSI statistics for each lot.

### Trip Analysis Visualization

### Statistics Results
![total_summary](https://github.com/JovanHumphrey/MechaCar_Statistical_Analysis/blob/main/Images/total_summary.JPG)
![total_summary](https://github.com/JovanHumphrey/MechaCar_Statistical_Analysis/blob/main/Images/PSI_t_test.JPG)

### Questions and Answers About Trip Analysis

<b> Does the current manufacturing data meet the PSI requirements for all manufacturing lots in total and each lot individually? Why or why not?</b>
<p>The total summary shows the variance for all three lots is 62.29356 which is within the 100 PSI limit. That said lot 3 has a much higher variance, skewing the results upward in the total summary.</p>

# Deliverable 3

## T-Tests on Suspension Coils

I performed t-tests to determine if all manufacturing lots are statistically different from the population mean on 1500 pounds per square inch. I then performed t-tests to determine if each lot individually is statistically different.

### T-Test Results
![lot1_t_test](https://github.com/JovanHumphrey/MechaCar_Statistical_Analysis/blob/main/Images/lot1_t_test.JPG)
![lot2_t_test](https://github.com/JovanHumphrey/MechaCar_Statistical_Analysis/blob/main/Images/lot2_t_test.JPG)
![lot3_t_test](https://github.com/JovanHumphrey/MechaCar_Statistical_Analysis/blob/main/Images/lot3_t_test.JPG)

<b>Lot P-Values</b>
Lot 1: 1 
Lot 2: 0.6072
Lot 3: 0.04168

Lots 1 and 2 didn't show any statistical variation. Lot 3 is under the significance level. Combined with a lower PSI and lower mean, this indicates that lot 3 suspension coils aren't performing up to standard.

# Deliverable 4

## Study Design: MechaCar vs Competition

The above tests are invaluable for helping AutosRUs with its next product launch although additional studies should be done to compare the performance of MechaCar vehicles with those of its competition. I recommend that the company consider testing the variance of highway and city fuel-efficiency of other vehicles. The null hypothesis would be that MechaCars has the same fuel-efficiency as its competitors. The alternative hypothesis would be that the fuel-efficiency of MechaCar vehicles isn't equal to its competitors. This test could be done with additional linear regressions using the data of other vehicle manufacturers. Like the linear regression above the results of these tests would confirm if the p-values of other vehicles are statistically significant.
