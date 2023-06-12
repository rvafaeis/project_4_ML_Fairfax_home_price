## ML Fairfax County VA Home Prices
![image](https://github.com/rvafaeis/project_4_ML_Fairfax_home_price/assets/120426753/6b52a0f1-8ba1-4726-8bb6-0d023d43a1bc)
The aim of this project was to gather and analyze data from local single family home sold prices in Fairfax County, VA and use that data to construct machine learning model to accurately predict home prices.

### ETL
First, the data was obtained from the MLS website. The data from 2019-2023 was downloaded as .csv files and used the Python library Pandas to edit and clean the data. The interquartile range (IQR) was also obtained and used to remove outliers. Utilizing the IQR to remove outliers greatly improved our Neural Network. These box plots visualize our dataset range before and after using the IQR.
![image](https://github.com/rvafaeis/project_4_ML_Fairfax_home_price/assets/120426753/05a5fe0b-9893-493c-b741-49a2bd57ecf8)

A geoapify API was utilized to add latitude and longitude to our data. Lastly, the get_dummies function from Pandas was implemented to indicate our categorical data using numbers to prepare our dataset for our machine learning model.

### Neural Network
The aim of our neural network is to accurately predict house prices in Fairfax County. To do that, a regression neural network model was constructed. Identifying the target variable as the home sold price and the rest of the variables as features. A StandardScaler was used to reduce the overall likelihood that outliers, variables of different units, or skewed distributions will have a negative impact on a model’s performance.
The data was split into test and train variables using sklearn to begin our prediction model. 

Before constructing and testing our model, a correlation function was used to identify which variables are mostly correlated to the home sold price. The image below shows the correlation heat map.
![image](https://github.com/rvafaeis/project_4_ML_Fairfax_home_price/assets/120426753/999610c7-53b9-4306-8f71-dffce88c4c02)

Multiple models, activation functions, and optimizers were teseted and after trial and error, the sequential model was the best performing model. The activation function was determined to be best as rectified linear unit (Relu) for each of the three layers in our model. Our outer layer used a linear activation function and the best optimizer was determined to be rmsprop. The table shows how each of the models performed using accuracy metrics including r-squared values.
![image](https://github.com/rvafaeis/project_4_ML_Fairfax_home_price/assets/120426753/37f7888b-f9f2-4c34-a637-c790b5582565)


https://public.tableau.com/app/profile/raheleh.vafaei.saadi/viz/FairfaxVASFHomePrice/Sheet7?publish=yes
