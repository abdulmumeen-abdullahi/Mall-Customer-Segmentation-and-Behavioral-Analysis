# Mall Customer Segmentation and Behavioral Analysis

## 1. Introduction
## 1.1 Project Overview
This project analyzes customer data from a shopping mall to uncover actionable insights that can enhance business strategies. Specifically, the analysis segments customers based on their spending behavior and demographic attributes, providing a foundation for targeted marketing and improved customer experiences. The dataset was sourced from Kaggle and contains variables such as Customer ID, Age, Gender, Annual Income, and Spending Score.

## 1.2 Business Context
Understanding customer behavior is critical to the success of a shopping mall. By identifying distinct customer segments, the mall can tailor its offerings and marketing strategies to better meet the needs of its clientele. This analysis supports data-driven decision-making, ensuring resources are allocated effectively to maximize customer satisfaction and revenue.

# 2. Data Exploration and Preparation
## 2.1 Data Overview
The dataset includes the following key variables:
- Customer ID: Unique identifier for each customer (removed for analysis).
- Age: Customer age in years.
- Gender: Gender of the customer.
- Annual Income: Annual income of the customer in dollars.
- Spending Score: A score assigned based on customer spending patterns and behavior.
The dataset was checked for missing values, outliers, and overall data integrity. The data types were appropriate for analysis, and no significant missing values were observed.

## 2.2 Data Cleaning and Transformation
- Unnecessary columns, such as Customer ID, were removed to streamline the analysis.
- Outliers were assessed using boxplot which revealed that there is no outlier across the features in the data set.

![download](https://github.com/user-attachments/assets/93fdb9c0-214f-422d-982d-1d74e354e642)

- Min-Max Scaling was applied to standardize variables like Annual Income and Spending Score for clustering to ensure that clustering algorithms performed optimally.

# 3. Customer Segmentation
## 3.1 Segmentation Approach
K-means clustering was selected as the primary segmentation method, with a silhouette score of 0.47 and an inertia error of 584.67. This method outperformed Gaussian Mixture (silhouette score: 0.41), DBSCAN (-1.0), and Agglomerative Clustering (0.34).

![download](https://github.com/user-attachments/assets/e27f1a9a-cfbd-4d5e-84bf-d4f0d1612796)

The elbow method was used to determine the optimal number of clusters. The accurate n_clusters in K-Means is typically selected as the point on the elbow chart where the rate of decrease in within-cluster sum of squares (WCSS) significantly slows down, indicating a diminishing return in clustering improvement. 

![download](https://github.com/user-attachments/assets/4bbd9833-2f2b-4b04-8fae-949847294f7e)

Segmentation was based on Annual Income and Spending Score, as these variables are most indicative of customer behavior.

![download](https://github.com/user-attachments/assets/a67e27f4-35ff-499b-a82b-911696c2fb5b)

## 3.2 Customer Profiles
Each segment/cluster represent unique characteristics:
1. High Spenders: This segment is characterized by customers with high annual income and high spending scores. These are likely to be affluent customers who have the means and inclination to spend generously.
2. Saver Customers: This segment comprises customers with high annual income but low spending scores. They are likely financially conscious individuals who prioritize saving over spending.
3. Target Customers: This segment consists of customers with low annual income and low spending scores. They are likely to be value-conscious customers who are looking for affordable options.

# 4. Customer Behavior Analysis
## 4.1 Spending Behavior
- A scatter plot of Age vs. Spending Score and Annual Income vs. Spending Score revealed that:
1.	Age vs Spending Score: There are many people who have similar ages and spending scores. It's hard to see any clear patterns or trends.
2.	Annual Income vs Spending Score: There are many people who have similar annual income and spending scores. It's difficult to identify a strong relationship between annual income and spending score.

![download](https://github.com/user-attachments/assets/0cb32b30-28f5-4617-a900-69fdf48a57c7)

## 4.2 Demographic Analysis
- Gender analysis indicated no significant difference in spending scores and annual income between males and females.

![download](https://github.com/user-attachments/assets/f24d8239-5416-414b-b425-362cceb72997)

- Age analysis showed younger customers, under 35 years old and 75 years old or older tend to have higher spending scores, suggesting they are a lucrative target demographic for marketing efforts.

![download](https://github.com/user-attachments/assets/a6e78865-4616-47c1-ac7b-8d87376a053d)

# 5. Data Visualization
The following visualizations were created to craft a compelling narrative, highlighting key insights such as the diversity within high-income groups and the spending potential across demographics. These stories were designed to engage stakeholders and emphasize actionable opportunities.

### -> Histograms: 
Distribution of Age, Annual Income, and Spending Score.

![download](https://github.com/user-attachments/assets/f0cdfb4d-8ed6-4ba4-b198-8b2cf4ff8262)

### -> Pie Charts:
- Gender Distribution: The bar chart shows that 50.4% (i.e., 7595) of the customers are male while 49.6% (7484) are female.

![download](https://github.com/user-attachments/assets/10a50d93-886b-4b4d-9b5e-f64971afcacd)

- Comparison of Spending Scores and Annual Income across gender shows that 50.3% of the total annual income of the customers came from male while 49.7% came from female. Also, 50.6% of the total spending score is for the male while 49.4% is for the female.

![download](https://github.com/user-attachments/assets/926eccae-0c17-4f34-ada2-64a4012cd758)

### -> Bar Charts:
- Comparison of Average Annual Income across age groups shows that the 65-74 age group has the highest average annual income of $110928 followed by the 75 or older age group of $110173.

![download](https://github.com/user-attachments/assets/839ebffc-e7ea-4877-82fb-38a503bc5e83)

# 6. Key Findings and Insights
## 6.1 Summarize Key Findings
- High-income customers exhibit diverse spending behaviors, requiring nuanced marketing strategies.
- Younger customers have higher spending scores, making them a priority for targeted campaigns.
- Three distinct customer segments were identified, each with unique characteristics and preferences.

## 6.2 Business Implications
- Implement targeted marketing campaigns for younger, high-spending customers.
- Develop exclusive offers for high-income, low-spending individuals to increase their engagement.
- Allocate resources to retain low-income, high-spending customers, ensuring their loyalty.

# 7. Conclusion
## 7.1 Recap of Key Findings
This analysis identified three distinct customer segments and highlighted significant trends in spending behavior and demographics. The findings provide a solid foundation for enhancing customer engagement and revenue.

## 7.2 Limitations and Future Work
Limitations include the absence of variables like purchase history and psychographic data, which could provide deeper insights. Future research could incorporate additional data sources and explore longitudinal customer behavior trends.

# 8. Appendix
## 8.1 Data Dictionary
- Age: Numeric, customer’s age.
- Gender: Categorical, customer’s gender.
- Annual Income: Numeric, customer’s annual income in thousands of dollars.
- Spending Score: Numeric, score indicating spending behavior.

## 8.2 Technical Details
- Tools Used: Python, Pandas, Seaborn, Matplotlib, Scikit-learn.
- Clustering Method: K-means with Min-Max Scaling applied to relevant variables.
- Evaluation Metrics: Silhouette score and inertia error.
