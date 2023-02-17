# Real Estate Investment Problem Statement

J.P. Morgan Chase is facing the challenge of identifying undervalued properties in the real estate market in order to increase their profit margins. With the use of a statistical model, the company aims to make informed decisions on purchasing these underpriced properties. This project presents a solution to this real-world problem and offers practical applications in the field of real estate investment.

# Data Used
This project utilizes the following datasets:
- House data
- School grade data
- Crime data

# Distance Calculation
In order to identify areas with higher prices, the following steps were taken:
1. Identification of high-priced areas through analysis of the data
2. Creation of a new column to calculate the shortest distance between each house and the high-priced areas

![Price Map](https://github.com/SpaceMonkey0453/PNWHousingModel/blob/main/Visualizations/Lat-LongWithPrice.png)

Note: Data cleaning was performed to remove outliers outside of King's County, as well as any inconsistencies in latitude and longitude data.

# School District Dataframe Creation
The GPS location of the center of each school district in King's County was obtained through Google Maps and used to create a dataframe of school districts.

# Addition of School Scores to Data
A dataframe of school districts was created, including the average grade of the students. The closest district was then identified for each house in the data, and the average grade was added to the house data.

# Analysis of Price Distribution
The distribution of price was analyzed, and the relationship between various columns and price was examined. This was followed by a review of the map for any notable patterns in price.

Before
![Price Distribution](https://github.com/SpaceMonkey0453/PNWHousingModel/blob/main/Visualizations/PriceFreq.png)

After
![Price Distribution](https://github.com/SpaceMonkey0453/PNWHousingModel/blob/main/Visualizations/PriceFreqNoOutliers.png)

# Conversion of Ordinal Categories to Integers
Ordinal categories were converted to integers in order to be used in the modeling process. Additionally, inflation was adjusted based on the year sold for any price prior to 2022 to ensure consistent dollar values across records.

# Replacing Date, Year Build, and Year Renovated
In order to improve the model's performance, the columns for date, year build, and year renovated were replaced with a new column, "Years Since Build or Renovated". This new column provides a numerical representation of the data that is better suited for use in a statistical model.

# Final Model Results
The final model achieved the following results:
- Root Mean Squared Error (RMSE): 270,246.79
- Mean Absolute Error (MAE): 189,430.83
- R-squared score: 70.66

![Q-Q Plot](https://github.com/SpaceMonkey0453/PNWHousingModel/blob/main/Visualizations/QQPlot.png)

![Price vs Prediction](https://github.com/SpaceMonkey0453/PNWHousingModel/blob/main/Visualizations/ActualVsPredictedPrices.png)