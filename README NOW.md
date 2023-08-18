

# Grocery Outlet sales Prediction
## Analysing sales behaviour to predict future sales

**Author**: Timothy Lingeveldt

### Business problem:

Forcast pruduct sales accross Outlet stores


### Data Source
Big Mart Sales Prediction https://datahack.analyticsvidhya.com/contest/practice-problem-big-mart-sales-iii/

Data Dictionary

![Sales Prediction Dictionary](https://github.com/othyTim/Prediction-of-Product-Sales/assets/138816378/a674b879-cf55-4cc3-9c9e-7be0773c39dc)



## Methods
- Data Cleanup
- Preprossing for Machine learning
- Fit Machine learning models


## Exploratory Data Analysis

### Average sales per Item type accross all Store types
![Barplot sales per item](https://github.com/othyTim/Prediction-of-Product-Sales/assets/138816378/d759c902-fe4e-4867-b4c6-11e811c5a319)


#### Highest sales according to Max Retail Price
The lmplot below indicates the Items that has a high Max Retail Price has higher sales than item with a low MRP
![Scatterplot](https://github.com/othyTim/Prediction-of-Product-Sales/assets/138816378/ad1e008e-ead2-4f3f-84a1-4ea50f662a3f)

## Maching Learning Models Utilised:
    - Linear Regression Model
    - Random Forest Regressor Model
    - Tuned Random Forest Regressor Model
    
### Models Evaluated & Results

- Linear Regression Model (Testing Set):
  - MAE = 11,611,457,508,149.383
  - MSE = 18,338,875,164,037,499,470,947,024,896.000
  - RMSE = 135,421,103,097,107.797
  - R^2 = -6,646,983,012,541,082,370,048.000

- Random Forest Regressor Model (Testing Set):
  - MAE = 785.516
  - MSE = 1,286,271.178
  - RMSE = 1,134.139
  - R^2 = 0.534

- Tuned Random Forest Regressor Model (Testing Set):
  - MAE = 728.354
  - MSE = 1,096,219.795
  - RMSE = 1,047.005
  - R^2 = 0.603


- The Final Model Chosen was a `Random Forest Regressor Model` with:
  - n_estimators tuned to 150
  - max_depth tuned to 5
  - min_samples_leaf tuned to 2
- For the testing set on the model, `60%` of the variance in y was explained by x. 
- The Mean Absolute Error was off by about `728.354`.
- The Mean Squared Error was `1,096,219.795`.
- The Root Mean Squared Error had a calculation of `1,047.005`.

Using this model to make predictions on future sales, based on the R^2 we can understand now that this model could explain 60% of the variation in the target.

## Recommendations
Based on the Exploratory data analysis there is somewhat a corraltion bewteen Max retail - higher the price the more sales
recommendation is for more items to have the max retail price

We should also note The countplot below indicates that Fruits and Vegetables and Snack foods are frequently sold items amongest the stores.
Recommendation here is to maintian good level of stock for the items to cator for the demand.
![Occurance](https://github.com/othyTim/Prediction-of-Product-Sales/assets/138816378/e6e9c731-2386-42ea-9ed0-980628387b2b)




