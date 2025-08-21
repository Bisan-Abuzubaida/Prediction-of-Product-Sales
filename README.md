# Prediction-of-Product-Sales

## Project Overview

This project focuses on predicting product sales across different outlets using a structured retail dataset. It combines **comprehensive data preprocessing, exploratory data analysis (EDA), and machine learning modeling** to generate actionable insights. The primary objective is to forecast sales at the item level, which is highly valuable for inventory management, pricing optimization, and retail strategy planning. This repository showcases end-to-end data science skills: from raw data handling to building predictive models and extracting business insights.

## Dataset

The dataset provides detailed information on products and outlets, including:

* **Item attributes**: Identifier, Weight, Visibility, Type, Fat Content, and Maximum Retail Price (MRP)
* **Outlet attributes**: Identifier, Size, Location Type, Outlet Type, and Outlet Establishment Year.
* **Target variable**: `Item_Outlet_Sales`

The task is to predict sales (`Item_Outlet_Sales`) using the above features.

## Workflow & Steps Taken

A structured workflow was followed to ensure reliable insights and accurate modeling:

1. **Data Cleaning**

   * Treated missing values in `Item_Weight` and `Outlet_Size`.
   * Standardized categorical values for consistency.

2. **Data Transformation**

   * Applied **multi-indexing** for better hierarchical analysis of sales trends across outlets and item categories.
  
3. **Exploratory Data Analysis (EDA)**

   * Distribution analysis of continuous features like MRP, Sales, and Visibility.
   * Boxplots, scatter plots, and heatmaps to understand relationships.
   * Correlation analysis to identify key predictors.

4. **Feature Engineering**


5. **Modeling**


6. **Results**


## Key Insights & Visuals

### 1. Regression: Item MRP vs. Item Outlet Sales

<img width="589" height="455" alt="reg plot sales with MPR" src="https://github.com/user-attachments/assets/7bd6b9d5-d051-4fee-a92b-1f86f764c747" /> <br> 

* A moderate positive trend exists: higher MRP generally aligns with higher sales.
* Items priced under 50 usually record sales below 2,000.
* Sales density increases in the 120–150 range, where many items achieve 4,000–6,000 units.
* Items priced above 200 show the strongest performance, with some exceeding 12,000 units.
* At each price point, sales vary widely: for instance, items at 150 range from under 1,000 to over 10,000 units.
* Noticeable price clusters emerge around 120, 150, and 200+, suggesting common pricing strategies or popular product categories.

**Insight:** Price influences sales, but the wide spread at each price level highlights that other factors—such as outlet type or visibility—also play a crucial role. Certain price points clearly attract more buyers.

---

### 2. Regression: Item Visibility vs. Item Outlet Sales

<img width="589" height="455" alt="download" src="https://github.com/user-attachments/assets/9382b742-eb10-4dbe-ad68-2f052903809d" /> <br>

* Surprisingly, products with 0% recorded visibility are still sold, and in some cases, achieve high sales.
* This indicates that `visibility = 0` may not mean the product wasn’t displayed. It likely reflects missing values, placeholders, or recording issues.
* Beyond zero, there is no strong positive correlation: high visibility does not guarantee strong sales.

**Insight:** Visibility data should be interpreted with caution. While visibility could influence customer behavior, its measurement inconsistencies suggest other factors dominate sales performance.

---

### 3. Sales by Item Type and Outlet Type

<img width="589" height="590" alt="boxplot - sales by item type and outlet type" src="https://github.com/user-attachments/assets/90f8e396-9300-45d0-8708-3f7f697eec8e" /> <br>

* **Supermarket Type 3** consistently achieves higher median sales across most item types, especially for Household, Dairy, and Snack Foods.
* **Grocery Stores** exhibit low and narrow sales ranges across nearly all item types, indicating limited performance.
* Certain categories like Breakfast and Seafood have low sales across all outlet types, highlighting niche or low-demand products.
* Wide variability in categories like Snack Foods and Dairy suggests their performance is highly outlet-dependent.

**Insight:** Sales depend heavily on both **item type and outlet type**, with Supermarket Type 3 leading in performance and Grocery Stores consistently underperforming. This highlights the importance of outlet format in retail strategy.

## Results Summary

* **Item MRP** is the single strongest driver of sales, with clear thresholds influencing performance.
* **Item Visibility** reveals inefficiencies: products can be prominent but still underperform.
* **Outlet Type and Location** amplify sales differences, making them critical for strategy.
* 


## Author

This project was developed as part of a data science portfolio to demonstrate advanced skills in **data wrangling, EDA, feature engineering, and predictive modeling**, with a focus on deriving **business-driven insights**.
