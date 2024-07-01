# Customer Segmentation By K-Means Clustering

## 1. Objective
The objective of this project is to perform customer segmentation using K-Means clustering. By grouping customers based on their demographic and purchasing behavior, we can gain insights into distinct customer segments and tailor marketing strategies accordingly.

## 2. Data Description
The dataset comprises demographic and purchasing information of customers. Below are the attributes used in this analysis:

| No | Field Name            | Description                                  | Data Type |
|----|-----------------------|----------------------------------------------|-----------|
| 1  | ID                    | Customer's unique identifier                 | Integer   |
| 2  | Year_Of_Birth         | Customer's birth year                        | Float     |
| 3  | Academic_Level        | Customer's academic level                    | String    |
| 4  | Income                | Customer's yearly household income           | Float     |
| 5  | Registration_Time     | Date when the customer enrolled with the company | String    |
| 6  | Recency               | Number of days since the customer's last purchase | Float     |
| 7  | Liquor                | Amount spent on liquor in the last 2 years   | Float     |
| 8  | Vegetables            | Amount spent on vegetables in the last 2 years | Float     |
| 9  | Pork                  | Amount spent on pork in the last 2 years     | Float     |
| 10 | Seafood               | Amount spent on seafood in the last 2 years  | Float     |
| 11 | Candy                 | Amount spent on candy in the last 2 years    | Float     |
| 12 | Jewellery             | Amount spent on jewellery in the last 2 years | Float     |
| 13 | Num_Deals_Purchases   | Number of purchases made with a discount     | Float     |
| 14 | Num_Web_Purchases     | Number of purchases made through the company’s website | Float     |
| 15 | Num_Catalog_Purchases | Number of purchases made using a catalogue   | Float     |
| 16 | Num_Store_Purchases   | Number of purchases made directly in stores  | Float     |
| 17 | Num_Web_Visits_Month  | Number of visits to the company’s website in the last month | Float     |
| 18 | Promo_10              | 1 if the customer accepted the offer in the 1st campaign, 0 otherwise | Float     |
| 19 | Promo_20              | 1 if the customer accepted the offer in the 2nd campaign, 0 otherwise | Float     |
| 20 | Promo_30              | 1 if the customer accepted the offer in the 3rd campaign, 0 otherwise | Float     |
| 21 | Promo_40              | 1 if the customer accepted the offer in the 4th campaign, 0 otherwise | Float     |
| 22 | Promo_50              | 1 if the customer accepted the offer in the 5th campaign, 0 otherwise | Float     |
| 23 | Complain              | 1 if the customer complained in the last 2 years, 0 otherwise | Float     |
| 24 | Gender                | Customer's gender                            | String    |
| 25 | Phone                 | Customer's phone                             | String    |
| 26 | Phone_Number          | Customer's phone number                      | String    |
| 27 | Year_Register         | Year when the customer enrolled              | Float     |
| 28 | Month_Register        | Month when the customer enrolled             | Float     |
| 29 | Total_Purchase        | Total purchases of the customer              | Float     |
| 30 | Living_With           | Marital status and number of children        | Float     |
| 31 | Payment_Method        | Customer's payment method                    | String    |

## 3. Tools and Techniques
For this project, Python was used along with the following libraries:
- **pandas**: For data manipulation and analysis.
- **numpy**: For numerical computations and array operations.
- **matplotlib**: For data visualization.
- **seaborn**: For enhanced data visualization and statistical plots.
- **sklearn (scikit-learn)**: For machine learning algorithms, including K-Means clustering and PCA.

Additionally, the following techniques were applied:
- **Data Visualization**: To visualize data insights and clustering results.
- **Linear Regression**: To understand relationships between variables.
- **Principal Component Analysis(PCA)**: To reduce dimensionality and enhance clustering performance.
- **K-Means Clustering**: To segment customers into distinct groups.

## 4. Implementation
The project implementation involved the following steps:
1. **Data Cleaning**: Preparing the data by handling missing values, outliers, and incorrect data entries.
2. **Data Transformation**: Transforming the data into suitable formats for analysis.
3. **Exploratory Data Analysis (EDA)**: Analyzing and visualizing the data to uncover patterns and insights.
4. **PCA**: Applying Principal Component Analysis to reduce dimensionality and enhance clustering.
5. **Clustering**: Using K-Means clustering to segment the customers.
6. **Segment Exploration**: Analyzing the characteristics of each customer segment.

## 5. Summary of Outcome

### EDA Summary:
1. **Customer Relationships**: Most customers have partners.
2. **Education Levels**: Many customers are highly educated, with only a small portion having basic education.
3. **Spending Patterns**: Liquor shows the highest spending levels, significantly ahead of other categories, possibly due to its high cost or the store's specialization in liquor. Pork follows as the second highest, with other categories considerably lower.
4. **Promotions**: Promo_30 is the most effective promotion for retaining customers or encouraging repeat purchases.
5. **Income and Education**: Customers with basic education generally have lower incomes, distributed at lower levels compared to other education groups.
6. **Income and Spending**: A $100 increase in annual income predicts a 7.25% increase in monthly spending.
7. **Income and Liquor Spending**: Every $100 rise in monthly income is expected to increase the percentage spent on liquor by approximately 1%.
8. **Marital Status and Children**: All marital status groups tend to spend less and tend to accept more discounts with more children.
9. **Purchase Channels**: The majority of purchases are made directly from the store.
10. **Education and Purchases**: Customers with basic education appear to make fewer purchases, likely due to their lower incomes.
11. **Purchase Intervals**: On average, customers have a 37-day interval between purchases, with some infrequent buyers—over 25% have intervals exceeding 50 days, and some even surpass 100 days.
12. **Customer Activity**: Some customers have a Recency-Average Interval Rate exceeding 5, suggesting they may no longer be active buyers.

### Segments Summary:

**Segment 1: Frugal Family Shoppers**
- **Income**: Lower income group, spend low.
- **Children**: Typically have 1-2 children, with some having 3.
- **Shopping Behavior**: Not very prone to discounts, prefer in-store and online transactions over catalog.
- **Web Visits**: Despite infrequent purchases, they visit the website regularly.
- **Gender**: Only male and female, no other types.
- **Payment Method**: Mostly pay with Card or Cash.

**Segment 2: Wealthy Scholars**
- **Income**: Higher income group, spend high.
- **Children**: Majority have no or only 1 child.
- **Days Since Registration**: Many are long-time customers.
- **Shopping Behavior**: Majority once use 1-2 discounts. Purchases channels spread evenly.
- **Number of Deals Purchases**: Almost all made at least 1 or 2 deals.
- **Web Visits**: Despite frequent purchases, they visit the website not so often.
- **Academic Level**: High levels of education with advanced degrees.
- **Gender**: No female.

**Segment 3: Tech-Savvy Online Shoppers**
- **Income**: Lower income group, spend low.
- **Children**: Typically have 1-2 children, with some having 3.
- **Shopping Behavior**: Prone to discounts, mostly making transactions in-store and on web, not on catalog.
- **Web Visits**: Despite infrequent purchases, they visit the website regularly.
- **Gender**: Only male and female, no other types.
- **Payment Method**: Mostly pay online, some pay with mobile.

**Segment 4: High-Earning Women**
- **Income**: Higher income group with diverse spending patterns.
- **Children**: Majority have no or only 1 child.
- **Shopping Behavior**: Majority once use 1-2 discounts. Purchases channels spread evenly.
- **Web Visits**: Despite frequent purchases, they visit the website not so often.
- **Gender**: Significant female representation, minimal other types.

**Segment 5: Diverse Shoppers**
- **Income**: Lower income group, spend low.
- **Children**: Typically have 1-2 children, with some having 3.
- **Shopping Behavior**: Prone to discounts, mostly making transactions in-store and on web, not on catalog.
- **Web Visits**: Despite infrequent purchases, they visit the website regularly.
- **Gender**: No male or female, only other types.
