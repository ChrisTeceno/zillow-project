# zillow-project

# PROJECT OVERVIEW

The goal of this project is to create a predictive model that can predict the tax assessed values of single family properties based on the features of the home. The model is trained on data from zillow found on kaggle and looks specifically at transactions for the year 2017.

## Project Description

Zillow attempted with varying degrees of success to predict housing values based of off several data points. We will use a smaller subset of that data to train and test our models and eventually present the best performing model.

## Goals

1. Find the drivers of property value. 
2. Make a model that performs better than baseline. 
3. Refine or create a better model. 
4. Give recommendations for new data to create better models.

## Initial questions
### Question 1:
    
    Is there a correlation between calculated square feet and the value of the property?

## Question 2:
    
    Is there a correlation between bathrooms and the value of the property?

## Question 3:

    Is there a correlation between the number of bedrooms and the value of the property?

## Question 4:

    Is there a correlation between the buildings age and the value of the property?

### Data Dictionary

| Variable           | Meaning                                                                   | values          |
| -----------        | -----------                                                               | -----------     |
| tax_value          | The total tax assessed value of the parcel (target variable)              | 1,000 - 4.9e+07 |
| bedrooms           | Number of bedrooms in home                                                | 0 - 14          |
| bathrooms          | Number of bathrooms in home including fractional bathrooms                | 0 - 18          |
| sqft               | Calculated total finished living area of the home (in square feet)        | 128 - 21929     |
| age                | Age of the structure (in years) at the time the data was collected (2017) | 1 - 139         |
| fips_la_county     | Is property in LA County                                                  | 0,1             |
| fips_orange_county | Is property in Orange County                                              | 0,1             |
| fips_Ventura_county| Is property in Venture County                                             | 0,1             |

### Steps to Reproduce
1. Download the data from CodeUp SQL database using query in acquire.py
2. Clone all modules from my github repo
3. Ensure all libraries are installed, sklearn, pandas, numpy, matplotlib, seaborn, and scikit-learn

## Plan
1. Get the data
2. clean and prepare the data, remove outliers, scale, dummy variables
3. split the data into training, validate and testing sets
4. explore the training data. Look for features to use in modeling, make visuals
5. build a baseline model
6. build own models and compare
7. test best model against test set
8. give recomedations to move forward

## CONCLUSION
### Drivers of churn
All the features seem important in predicting the value of the property but the number of bathrooms appears the most important.
Sqft was not as important as expected and I would like to delve into that more given more time.

### Model improvement
Our models almost all perform better than the baseline model. With one having a RMSE of $100k better than the baseline. I would like to try different ways to scale the data and remove outliers.

### Recommendations
More features I would add in would be lot size, long/lat (or other available location info), and potentially pull data to determine proximity to schools, hospitals, and determine crime rate.