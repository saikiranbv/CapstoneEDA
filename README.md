# Retailrocket recommender system

## Overview

The objective of this project is to Understanding user behavior through implicit signals like clicks and views is crucial for building effective recommender systems in real-world e-commerce platforms. Being able to predict preferences from limited interaction data helps personalize user experience, boosting engagement and conversions. Simultaneously, detecting and removing abnormal traffic is essential to ensure the recommendations are based on genuine customer behavior and do not suffer from noise or bias�leading to better decision-making and higher ROI for businesses.

Here is a link to the Jupyter Notebook https://github.com/saikiranbv/CapstoneEDA/blob/main/capstoneEDA.ipynb

## Table of Contents

1. [Business Understanding](#business-understanding)
2. [Data Analysis](#data-analysis)
3. [Visualization](#vizualization)
4. [Modeling](#modeling)

## Business Understanding

The primary objective is to accurately predict item properties associated with �addtocart� events based on a visitor�s prior �view� behavior, and cdetect and filter out abnormal user activity to improve the performance of recommender systems

## Data Analysis

The data will be sourced from the publicly available RetailRocket Recommender System Dataset https://www.kaggle.com/datasets/retailrocket/ecommerce-dataset which includes:

	events.csv � records user interactions (view, add to cart, transaction)
	item_properties_part1.csv and item_properties_part2.csv � describe time-stamped item properties
	category_tree.csv � describes the hierarchical relationships between product categories

Here are the number of records in each file
Events data: 2,756,101
Category data: 1669
Item data: 20,275,902

Number of unique visitors = 1,407,580
Number of unique items = 235,061
Number of unique transactions = 17,673

## Visualization

As the Item data is hashed and category data is only a parent child relationship, most of the analysis is from Events data. 

### The Top 10 users are 
![image](https://github.com/saikiranbv/CapstoneEDA/blob/main/images/Top_ten_Users.png)

### The distribution by event type
![image](https://github.com/saikiranbv/CapstoneEDA/blob/main/images/Event_type_count.png)

### The distribution by event type in a Pie chart
![image](https://github.com/saikiranbv/CapstoneEDA/blob/main/images/Event_tupe_pie.png)

### The Ten items that are viewed are 
![image](https://github.com/saikiranbv/CapstoneEDA/blob/main/images/Top_ten_Viewed_Items.png)

### The Ten items that are added to cart are 
![image](https://github.com/saikiranbv/CapstoneEDA/blob/main/images/Top_ten_Items_AddedtoCart.png)

### The Ten items that are purchased are 
![image](https://github.com/saikiranbv/CapstoneEDA/blob/main/images/Top_ten_sold_items.png)

### The distribution of Customers returning vs New
![image](https://github.com/saikiranbv/CapstoneEDA/blob/main/images/ReturningUsersvsNew.png)


## Modeling

Linear Regression: Used as a baseline model for comparison.
Random Forest: Employed to capture non-linear relationships and improve predictive performance.
Here are the results:

 Model                 | Test Accuracy | Precision | Recall  | F1 Score |
|----------------------|---------------|-----------|---------|----------|
| Logistic Regression  | 0.9916        | 0.8125    | 0.0055  | 0.0109   |
| Random Forest        | 0.9870        | 0.1235    | 0.0897  | 0.1040   |

### Linear Regression:
![image](https://github.com/saikiranbv/CapstoneEDA/blob/main/images/Linear_Regression.png)

### Random Forest:
![image](https://github.com/saikiranbv/CapstoneEDA/blob/main/images/Random_Forest.png)

