# DIGITAL SKILLUP ACADEMY (DSA) CAPSTONE DATA ANALYSIS PROJECT 

#  Amazon Product Review Analysis

##  Overview

This project is a case study completed as part of my Data Analysis learning journey. The analysis was conducted using **Microsoft Excel**, focusing on extracting actionable insights from **Amazon product review data**. 

---

##  Dataset Description

The dataset contains information scraped from Amazon product pages. It includes:

- **Product Details**: name, category, price, discount, and ratings  
- **Customer Engagement**: user reviews, titles, and content  
- **Data Size**:  
  - `1,465 rows`  
  - `16 columns`

Each row represents a **unique product**, and aggregated reviewer data is stored in **comma-separated values**.

## Steps Taken
First, i started cleaning the data by removing the duplicates on product id using **remove duplicate** under the data tool group
Secondly, i counted the blanks on the dataset by using the **countblank function** to kow the number of blank cells in the dataset.
Due to the length of the data in product category, i used text to **columns function** and then delimeter to split the column into four separate columns apart from the major category in the dataset. 
---

##  Analysis Tasks & Key Insights

Using **Excel Pivot Tables, Calculated Columns, and Filters**, I performed the following analysis:

### 1.  Average Discount by Category  
- Identified average discount percentages across different product categories.

### 2.  Product Count per Category  
- Counted how many products were listed under each product category.

### 3.  Total Reviews per Category  
- Summed up the number of customer reviews per category.

### 4.  Highest Average Ratings  
- Filtered products with the highest average ratings.

### 5.  Actual Price vs Discounted Price  
- Calculated average actual prices and compared them with discounted prices by category.

### 6.  Most Reviewed Products  
- Identified top products with the highest number of reviews.

### 7.  50%+ Discounted Products  
- Filtered how many products offer 50% or more discount.

### 8.  Rating Distribution  
- Analyzed the spread of product ratings (e.g., how many products are rated 3.0, 4.0, etc.).

### 9.  Total Potential Revenue  
- Computed estimated revenue using:  
  `Potential Revenue = Actual Price × Rating Count`

### 10.  Price Bucket Distribution  
- Segmented unique products by price range:  
  - Below ₹200  
  - ₹200–₹500  
  - Above ₹500  

---

## Excel Functions Used
Average Discount
=([@[Actual Price]]-[@[discounted_price]])*100

Price Range Bucket
=IF(I2<200,"<₹200",IF(OR(I2=200,I2<=500),"₹200 - ₹500",">₹500"))

=IF([@[discount_percentage]>=50%,"YES","NO")

Discount Range
=IF([@[discount_percentage]]<=10%,"0-10%",IF([@[discount_percentage]]<=20%,"11-20%",IF([@[discount_percentage]]<=30%,"21-30%",IF([@[discount_percentage]]<=40%,"31-40%",IF([@[discount_percentage]]<=50%,"41-50%",IF([@[discount_percentage]]<=60%,"51-60%",IF([@[discount_percentage]]<=70%,"61-70%",IF([@[discount_percentage]]<=80%,"71-80%",IF([@[discount_percentage]]<=90%,"81-90%","91-100%")))))))))

Products With Highest Rating and Review
=AVERAGE([@rating]+[@[rating_count]]/1000), then sorted using top ten

##  Files Included

- `Amazon_Review_Analysis.xlsx`: Excel file with cleaned data, pivot tables, and analysis
- `Charts.png`: Key visualizations used to support findings
- `README.md`: Project overview (this file)

---

##  Tools Used

- Microsoft Excel  
  - Pivot Tables  
  - Calculated Columns  
  - Conditional Formatting  
  - Filters & Sorting  
  - Charts & Graphs
