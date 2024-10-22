# Delivery Time Prediction - Porter
# Problem Statement
Porter, India's largest marketplace for intra-city logistics, aims to optimize the delivery experience for customers while supporting its 150,000+ driver-partners. For better customer service, Porter wants to estimate the delivery time for food orders based on various features such as the market, restaurant, and available delivery partners.

The goal of this project is to build a regression model that predicts the estimated delivery time for orders, leveraging the provided dataset.

# Dataset
The dataset contains data on food delivery orders, with each row representing a unique delivery and each column representing a feature.



# Objective
The objective of this project is to predict the delivery time of orders based on features such as market, restaurant category, order details, and delivery partner availability. The prediction model will help Porter provide accurate delivery time estimates to customers.

# Concepts Explored
* Data Preprocessing and Feature Engineering
* Neural Network-based Regression Models
* Handling Categorical Data, Outliers, and Missing Values
* Model Evaluation: MSE, RMSE, and MAE

# Process
1. Data Understanding
* Import Data: Load the dataset into pandas and inspect its structure.
* Exploratory Data Analysis (EDA):
    * Check the characteristics of the dataset, including data types, missing values, and basic statistics.

2. Data Preprocessing
* Target Creation: Calculate the delivery time in minutes as the difference between the created_at and actual_delivery_time timestamps.
* DateTime Feature Engineering:
  * Extract the hour of the day and day of the week from the order timestamp (created_at).
  * Leverage pandas' datetime functions for easier manipulation.
* Null Value Handling: Handle missing values by either imputing or removing rows with null values.
* Encoding Categorical Features: Convert categorical variables like store_primary_category and order_protocol using label encoding or one-hot encoding.

3. Data Visualization
* Countplots and Scatterplots: Visualize relationships between features such as order protocol, restaurant category, and delivery time.
* Outlier Detection and Removal: Identify outliers using boxplots and statistical methods, then remove or transform them.
* Post-Cleaning Visualization: Plot the data again to confirm improvements after outlier removal.

4. Model Training
* Train-Test Split: Split the data into training and testing sets (e.g., 80-20 or 70-30).
* Data Scaling: Scale features to normalize input for the neural network.
* Neural Network Architecture:
  * Create a simple feedforward neural network using TensorFlow/Keras.
  * Experiment with different layers, activation functions, optimizers (e.g., Adam), and learning rates.
* Model Training: Train the model over a required number of epochs.
* Plot Training Metrics: Visualize training/validation loss and accuracy over epochs.

5. Evaluation
* Metrics: Evaluate the model using metrics such as:
  1. MSE (Mean Squared Error)
  2. RMSE (Root Mean Squared Error)
  3. MAE (Mean Absolute Error)

# Key Techniques Used
1. Feature Engineering
* Extracted useful features such as:
  * Delivery time (in minutes)
  * Hour of the day and day of the week from the order timestamp
    
2. Neural Networks for Regression
* Built a neural network model for regression using TensorFlow/Keras.
* Tried different activation functions and optimizers for optimal results.

3. Data Scaling & Outlier Handling
* Applied standard scaling to numerical data before feeding it into the neural network.
* Handled outliers in features like total_items_subtotal and min_item_price to improve model generalization.

# Conclusion
This project demonstrated the power of neural networks in predicting delivery times based on various features from Porter’s logistics data. Feature engineering, especially time-based features, played a crucial role in enhancing model performance. Future improvements could focus on adding more advanced models and further tuning to improve accuracy.

