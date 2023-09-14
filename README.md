# Churn_Prediction

Dataset Overview:
The dataset used for this project is titled "Customer Churn Large Dataset." It is designed to predict customer churn, which is a critical challenge in various industries, including telecommunications, subscription-based services, and e-commerce.



# Key Attributes:
1. Age: This attribute represents the age of each customer, indicating their age at the time of data collection.

2. Subscription_Length_Months: It signifies the duration of a customer's subscription in months, providing insights into their loyalty or commitment to the service.

3. Monthly_Bill: Monthly bill refers to the amount a customer is charged on a monthly basis for utilizing the service. It can serve as an indicator of customer spending behavior.

4. Total_Usage_GB: Total usage in gigabytes (GB) denotes the cumulative data consumption by each customer over a certain period. It's a measure of the customer's engagement with the service.

5. Churn: The target variable, "Churn," is binary and serves as the main focus of prediction. It indicates whether a customer has churned (1) or not (0). Churn typically means that a customer has discontinued their subscription or stopped using the service.

6. Gender: This categorical attribute denotes the gender of each customer. It can provide insights into whether gender has any impact on churn.

7. Location: Location represents the geographic location of each customer, providing a potential basis for regional analysis of churn patterns.

8. CustomerID: This attribute serves as a unique identifier for each customer, ensuring the dataset's individuality.

9. Name: The "Name" attribute typically contains customer names, although it may not directly impact churn prediction.



# Data Preparation and Exploration:
The initial step was to load the dataset, which contains information related to customer churn, into the project environment. The primary objective is to construct a predictive model for customer churn. 


# Data Preprocessing:
To ensure that the dataset is ready for analysis, a series of essential steps were taken. First, a check for missing values in the dataset was conducted, and it was found that the dataset was complete without any missing data points. 

Exploratory Data Analysis (EDA) was undertaken to gain a better understanding of the dataset. This involved examining the dataset's shape, columns, data types, and generating summary statistics to get a sense of its overall structure and characteristics. 


# Feature Engineering:
An exploration of potential relationships between variables, such as gender, location, and churn, was carried out. In the process, it became evident that neither gender nor location significantly influenced the prediction of churn.

To enhance the dataset for modelling, columns that did not appear relevant to the prediction task were removed. These columns included 'Location', 'Gender', 'CustomerID', and 'Name'.

Subsequently, the dataset was divided into two subsets: a training dataset and a testing dataset. 

Feature Scaling and Extraction:
Standardization, using the StandardScaler, was employed to normalize the data and make it suitable for machine learning algorithms. This step was pivotal in ensuring that the features' scales did not unduly influence the modeling process.

Principal Component Analysis (PCA) was employed to carry out feature extraction. By reducing the dimensionality of the dataset, PCA was instrumental in simplifying the dataset while retaining the essential patterns. The number of principal components was determined by examining the explained variance plot, with the goal of retaining 95% of the data's variance. 
selected the number of principal components equal to the knee point on the explained variance plot because it represents a data-driven balance between dimensionality reduction and information retention. At the knee point, the rate of increase in explained variance significantly slows down, indicating that additional components contribute relatively little to capturing the overall variability in the data. This choice optimizes our ability to reduce dimensionality while preserving the most essential patterns and minimizing the risk of overfitting in our analysis or modelling.


# Model Selection:
Three different models were explored for the predictive task: an Artificial Neural Network (ANN), Logistic Regression, and Random Forest Classifier. Each model was considered and evaluated based on its performance.

- The ANN model was created as a sequential neural network with input and hidden layers, all employing ReLU activation functions. The model was subsequently compiled and trained.
- Logistic Regression was implemented by initializing and fitting the model.
- A Random Forest Classifier was created and trained as a third model.


# Model Evaluation:
The performance of each model was assessed through a series of metrics, including accuracy, precision, and recall. These metrics are instrumental in gauging the model's efficiency in making accurate predictions.

Based on these metrics, the Random Forest Classifier was ultimately chosen as the most suitable model. This decision was guided by the model's impressive recall score, which was a crucial factor for the prediction task.

Model Optimization:
In a bid to enhance model performance, cross-validation was employed. This technique improved the accuracy of the Random Forest Classifier and provided more confidence in its predictive capabilities.
