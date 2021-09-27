# HOUSE-PRICE-PREDICTION
Predicting the price of a house based on their features (no of bedrooms, no of bathrooms, square footage etc.) using a deep learning model.
The data was explored by using visualization techniques and statistical analysis such as:
•	Checking for null values
•	Using the describe method to view the data’s statistical analysis
•	Used seaborn’s distribution plot to visualize the price feature (since it’s a continuous label) which showed that the house prices mostly fall between 0-1.5 million dollars and some outliers for the extremely expensive houses.
•	used a count plot to visualize the most common number of rooms most houses in the data usually has (between 2-5)
•	used the correlation method to check for correlations between the data features.
•	Explored more on the data’s highly correlated features using a scatterplot for e.g. house price and living space, and this showed the more the living space, the more the house price.
•	Temporarily dropped some outliers in the data by removing the top 1 percent of the most expensive houses I.e they are the house prices with 1 or 2 frequency in the data, In order to Use a scatter plot to show the relation between the house price and the latitude and longitudes of the house. This helped reveal the locations with the most expensive house prices.
•	A box plot was used to show the price difference between houses located at the waterfront and houses not located at the waterfront.
FEATURE ENGINEERING
•	Feature engineering was carried out on the data to get rid of labels that aren’t useful to us for e.g. Feeding the ID and zip code columns as it is to the model will cause errors since the model would assume they are continuous features
•	Initially the date was a string object, it was converted to a date time object.
•	Extra columns (year and month of house sold) were created for better analysis.
•	Used a group by method to see average price variations for each month and year.
•	Dropped the initial date column after extracting month and year from it.
DATA PREPROCESSING AND CREATING A MODEL
•	Separated the input label (X) from the output label (y)
•	Performed a train test split on both the X and y variables
•	Feature scaling was carried out on the independent variables to prevent data leakage.
•	Used a sequential model with dense layer for our Artificial Neural Network, and gave the number of neurons the same number of columns in our feature data.
•	We assign rectified linear unit (RELU) as our activation function.
•	Assigned a single dense layer as our final output
•	Compiled the model by using adam as the optimizer and mse as loss function.
•	Performed a train fit on our X and y labels, and I also passed in validation data inorder to keep track of performance of our training and test data.
•	Used batch size to feed in the training data in small batches which might take a while but will prevent overfitting.
•	Used 400 epochs on the training data.


