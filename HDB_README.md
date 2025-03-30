** INTRODUCTION **

Hello, thank you for viewing. This project surrounds the idea of HDB resale flats and the prices. The main model used here is Ridge Regression. This project is done completely by me. 

** OBJECTIVES **

In this project, we aim to predict the resale prices of HDB flats based on a variety of variables. This gives insight into the pricing for resale HDB flats for consumers to determine whether the prices are within acceptable range. 

** Exploratory Data Analysis **

For this dataset that was used, it consisted a total of 78 columns. I.e, 78 variables. We will dive deeper into the variables we will be using. 

Looking at the variables, I noticed several variables that are similar in nature but not exactly what I am looking for. An important factor affecting the resale price of HDB flats would be the remaining lease of the flat. For example, a flat with 50 years remaining lease and a flat with 80 years remaining lease would result in value difference. Therefore, I had created a new variable titled 'remaining_lease'. 

Upon further research, I had decided to drop some variables that are irrelevant. Next, we will check for missing or and duplicated values for the variables we want. 

There is 1 variable (Mall nearest distance) with missing value. Hence, we will need to fix that. In order to tackle missing values, we can patch it with the mean of the column. However, in this case it would affect our output greatly. This is because the nearest distance to the mall from Pioneer and Kallang will differ. Hence, it is inaccurate to patch the missing value with the mean of the entire column. 

In order to tackle the missing values, we will do K-Nearest Neighbour.

Next, we want to further improvise on the variable for 'town' as there are too many different types if we are using it for modelling. It will affect the one hot encoding subsequently. We simplify it into 5 regions for modelling later.

Looking through the variables again, more variables were dropped. 

** One hot encoding ** 

There are 2 categorical variables, we will need to proceed with one hot encoding to prepare for modelling. 

** MODELLING **

We are done with the data preparation. Hence we can proceed with modelling. 

Split it into X & Y test train, and we will use standard scaler. 

Multiple models were looked at for the best results, we will settle on Ridge regression as it has better accuracy.

We check against the test and train set to ensure that overfitting did not occur. 

** RESULTS ** 

R-squared on the test data: 0.7619817633111378
Mean Squared Error (MSE): 4853330077.428648
Mean Absolute Error (MAE): 52547.41408180377
Root Mean Squared Error (RMSE): 69665.84584592831

Our accuracy is about 76%

** Outro ** 

Thank you for taking some time to read whether you're just viewing or a hiring manager. If you think there are any way I can improve my model, feel free to email me at sohyann13@gmail.com :) 