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
missing garage related variables, and the missing basement related variables (with the exception of one data point on BsmtExposure).
