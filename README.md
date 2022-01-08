# NWDataPrep-ManagementAssignment1- EDA
This is the first assignment for my Data Preparations and Management Systems Course for Northwestern. Questions are asked and answered below when appropriate.

## Question 1. Provide appropriate descriptive statistics and visualizations to help understand the marginal distribution of the dependent variable.

The distribution of the independent variable of SalePrice seems to show a heavy skew to the right. This is further reflected in the boxplot which indicates that the median fall around the 
160k mark while there are plenty of outliers outside of the standard deviations to go around. Generally speaking it seems that the vast majority of the houses have the salesprice
around 100k-300k but there are plenty of exceptions to that case. This is further confirmed with the general descriptive statistics of the dependent variable,
the maximum is 755k in the circumstance that the median is 163k and the 75th quartile is 214k which shows there is a wide number of outliers even outside those markers.

## Question 2. Investigate missing data and outliers.
There does not seem to be any data missing from the SalePrice output since there are zero nulls available. However, there are several missing data points in certain outputs that 
warrant investigation. These outputs are listed in the code. In the vast majority of cases, the missing data points have a logical explanation. For the missing PoolQC data,
it can be confirmed using the PoolArea data that any data missing from PoolQC is missing because the pool doesn't exist in the house. Similar logic can be followed with the
missing garage related variables, fireplaces, and the missing basement related variables (with the exception of one data point on BsmtExposure). Unfortunately for the other categories there is no real way to discern whether the missing data is due to lack of existence or if it simply human error. However, it appears that the instance of the Electrical variables is likely accidental.

When looking at the outliers for SaleData, I decided to focus on those over 400k. This was due to approximation of the first dot after the whisker in the boxplot. When comparing the outliers to the other data there are notably a lot less null fields when compared to the original dataframe. What this data immedately tells me is that all of these outlier homes have a basement, garage, and at least one fireplace. This is potentially interesting info for predictive values in the future. This data also makes up about 1.9% of the total data. When looking at the overall quality, these homes tend to hover between 8-10 which is on the far upper end when comparing to other homes (red line indicates the minimum outlier value). A similar pattern emerges with basement square footage, garage square footage, and above ground living square footage. All of the outliers are on the upper end of these values and the minimum outlier of these values are on the upper end of the overall dataframe.

## Question 3. Investigate at least three potential predictors of the dependent variable and provide appropriate graphs/statistics to demonstrate the relationships.
When figuring out the proper predictors, I decided to take the knowledge of the outlier data and see how well these variables correlate with the sale price variable. Looking at the basement square footage it's clear that there is a positive relationship between the square footage and the SalePrice. This is made further clear with the r value being .61 and the p-value indicating that the relationship is statistically significant. An even better relationship is shown with the above ground square footage with a r value around .70. However, the best relationship is the relationship between the deemed overall quality of the house and the SalePrice. This isn't particularly surprising given that the more esteemed a house is perceived the higher the price would likely be. The relationship was given an r value of .79 indicating a high correlation. However, it's worth noting that even with a high relationship there is a ton of variability on the price based on the quality as shown in the scatterplot.

## Question 4. Engage in feature creation by splitting, merging, or otherwise generating a new predictor.
For feature creation I decided to take all of the variables that are related to housing features regarding square feet and add them together to create a new variable called TotalArea. This variable did not include Lot Area mainly because the lot size did not show much predictive value. When adding up all of the variables it shows an extremely high correlation of nearly .81 a higher degree of correlation when compared even to the overall quality. The scatterplot does show an extremely large relationship between the two with the exception of two major outliers in square footage related to price. This could have to do with the quality of the home and features and is likely worth exploring. However, in general this new variable seems highly predictive of SalePrice, even with these outliers included.

## Question 5. Using the dependent variable, perform both min-max and standard scaling in Python.
Results of scaling success shown in code. Standard scaler mean is at 0 while standard deviation is at 1. Min-max scaler have a minimum of 0 and maximum of 1.



