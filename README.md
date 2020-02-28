# Determining-Strength-of-Various-Indicators-in-Predicting-Social-Mobility-in-Los-Angeles

## Background
The aim of this mini project was to see what factors across Los Angeles predict social mobility. Traditionally, education level, income, and employment rates are used as primary indicators of social mobility. I was interested in seeing the correlation of other possible social indicators such as the number of people married in a tract, incarceration rate, and the number of children present in a tract. To do this, social mobility was calculated as the normalized product of individual income and employment rate in the same tracts. The results are presented below. 

## Results
![alt text](https://github.com/PaarthSharma98/Determining-Strength-of-Various-Indicators-in-Predicting-Social-Mobility-in-Los-Angeles/blob/master/Manipulated%20Data%20and%20Figures/FractionMarried.png)
When looking at the relationship between the fraction of married individuals in a tract and that tract's opportunity for social mobility, there was a strong positive correlation. The R squared value of 0.9757 is a fairly strong indicator of this. It can partially be explained by research which demonstrates that a stable home (married parents) provides a stronger base for children to grow up and succeed as adults.  

![alt text](https://github.com/PaarthSharma98/Determining-Strength-of-Various-Indicators-in-Predicting-Social-Mobility-in-Los-Angeles/blob/master/Manipulated%20Data%20and%20Figures/IncarcerationRate.png)
When looking at the relationship between the incarceration in a tract and that tract's opportunity for social mobility, there was a weaker positive correlation. The R squared value of 0.8931, although strong, is definitely prone to confounding variables. One would expect this relationship to have a negative correlation - lower incarceration rates should ideally result in higher social mobility. 

![alt text](https://github.com/PaarthSharma98/Determining-Strength-of-Various-Indicators-in-Predicting-Social-Mobility-in-Los-Angeles/blob/master/Manipulated%20Data%20and%20Figures/NumberChildren.png)
When looking at the relationship between the number of children in a tract and that tract's opportunity for social mobility, there was a fairly strong positive correlation. The R squared value of 0.9359 is a strong indicator of this. Logically, it makes sense that tracts with more children have a higher density of families. Here, one would expect a safer environment and parents who have higher income and employment rate to support a family. 

## Data Analysis Steps
1. Data was collected from [The Opportunity Atlas](https://www.opportunityatlas.org/) for Los Angeles. All datasheets had the following column values: [Tract Name Metric]
2. Data was extracted from each excel into a common spreadsheet for Los Angeles
3. In a new column, I used the IFERROR and INDEX commands to add the tract id of each metric into one column
4. The "Remove Dublicates" excel feature was used to ensure only unique values remained in the column
5. Next, I used VLOOKUP to find and add data pertaining to each tract into a new table. Thus, I had a new table witht he following column values: [Tract Name Metric1 Metric2 Metric3...]
6. I then added new columns next to each metric and normalized all the values by dividing by the max value (found with MAX function)
7. Various scatter plots were then created and fitted with a linear trendline
8. The regression feature from excel data analysis was also used to provide more statistical information for the data
