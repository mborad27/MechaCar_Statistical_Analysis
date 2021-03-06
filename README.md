# MechaCar: Statistical Analysis with R
## Project Overview
Jeremy has been selected as the primary analyst for AutosRUs's data analytics team. As an employee of 10 years, he has extensive knowledge of the product. The AutosRUs executive team recognizes that the most successful automobile launches utilize data analytics in every decision making process. A few weeks into his new role, AUtosRUs's newest prototype, the MechaCar, is suffering from production troubles that are blocking the manufacturing team's progress. Jeremy and us have been called to review the production data for insights that may help the manufacturing team. We will perform multiple linear regression analysis to identify which variables predict the mpg of MechaCar, collect summary statistics on the pounds per square inch (PSI) of teh suspension coils from the manufacturing lots, run t-tests to determine if the lots are statistically different from the mean population, and design a statistical study to compare vehicle performance of the MechaCar against vehicles from other manufacturers.

## Linear Regression to Predict MPG
![linear_regression_summary](https://user-images.githubusercontent.com/92230478/151720267-f63fef08-0b6d-4634-815c-8f534e0bcd6b.png)
* Variance of a non-random variable is usually 0. Given this fact, the intercept, vehicle_length, and ground_clearance coefficients can be said to provide a non-random amount of variance to the mpg values.
* At a significance level of 0.05, we are able to reject the null hypothesis because of the extremely small p-value. The null hypothesis of a linear regression states that the slope (β1) is equal to 0. However, if we reject the null hypthesis, we're stating that alternative (β1 ≠ 0) is true. Thus, proving that the slope is not 0.
* Multiple R-squared increases as more variables are passed through the regression. However, adjusted R-squared controls against this increase, and adds penalties for the number of predictors in the model, thus making it a more accurate predictor of how effective the linear model is. An adjusted R-square of 0.6825 concludes that this linear model predicts the mpg of MechaCar prototypes relatively well.

## Summary Statistics on Suspension Coils
![total_summary_table](https://user-images.githubusercontent.com/92230478/151720437-0e59fe52-558e-49f8-8dd1-14a8f52250b5.png)
![lot_summary_table](https://user-images.githubusercontent.com/92230478/151720289-cf3e96bc-0c6c-4fa8-b006-d1af64e56bba.png)
* The overall variance for the entire dataset indicates that the current manufacturing data meets the 100 pounds per square inch variance limitation. However, when separated into three lots, the third lot demonstrates a much higher variance. Because the lots are chosen randomly, there is a possiblity that a third of the lot does not meet the necessary suspension coils requirement.

## T-Test on Suspension Coils
### T-Test on Entire Lot
![t-test](https://user-images.githubusercontent.com/92230478/151720376-10c615d9-de48-4075-a0b6-6ef442034410.png)
* At a significance level of 0.05, we fail to reject the null hypothesis since the p-value equals 0.06. Therefore, we cannot reject the fact that the sample mean may be equivalent to the true population mean. Another feature to note is the narrow confidence interval. Although a narrower confidence interval implies that there is a smaller chance of obtaining an observation within that interval, it provides greater accuracy than a wider interval.
### T-Test on 3 Smaller Lots
![lots_t_test](https://user-images.githubusercontent.com/92230478/151720386-8deb19fc-6af7-4960-960d-06119399d34e.png)
#### Lot 1 
At a significance level of 0.05, we fail to reject the null hypothesis since the p-value equals 1. An interesting correlation between p-value and confidence intervals is that as the p-values get larger, the confidence interval becomes smaller, implying more precision in predicting the true population mean
#### Lot 2
At a significance level of 0.05, we fail to reject the null hypthesis again since the p-value equals 0.6072. In addition, the second lot has a relatively small confidence interval.
#### Lot 3
At a significance level of 0.05, we can reject the null hypothesis since the p-value equals 0.04168. The mean of this sample is also significantly smaller in comparison to the previous two lots. More importantly, unlike the previous two lots, the confidence interval for the third lot does not include the predicted population mean.
## Study Design: MechaCar vs. Competition
Another statistical study that can be performed to determine MechaCar's standing against its competition is a linear regression on city and highway fuel efficiency. Gasoline is expensive nowadays, and it is an important feature that many consumers look at when purchasing a new car. The metrics that can be included in this analysis are:
* City and highway fuel efficiency (dependent variable_)
* Horsepower (independent variable)
* Vehicle weight (independent variable)
* AWD capabilities (independent variable)
* MPG (independent variable)

In addition to the MPG, AWD, and vehicle weight data that we already have, we would have to collect fuel efficiency and horse power data for the sample data set at hand.
