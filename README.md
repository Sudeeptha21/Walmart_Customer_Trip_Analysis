# 🛒 Walmart Customer Trip Analysis  
Clustering & Association Rule Mining

## 📌 Objectives
The goal of this project is to **find similar customer shopping visits** using clustering and to **mine association rules** in Walmart shopping baskets. These techniques help uncover hidden shopping patterns, customer profiles, and cross-selling opportunities.  

## Input Files
- **Walmart_visits_7trips.csv** → Used for **K-Means clustering**  
- **Walmart_baskets_1week.csv** → Used for **Association Rule Mining**  

**Data Source:** Walmart & Kaggle  
- Original Kaggle competition: [Walmart Trip Type Classification (2015)](https://www.kaggle.com/c/walmart-recruiting-trip-type-classification)  

## 📊 Data Description
The raw data is in **long market basket format**, capturing items purchased during each visit, along with trip-related details.  
- `TripType`: Categorical id for shopping trip type (e.g., grocery trip, holiday shopping, etc.).  
- `DOW`: Day of Week of the trip.  
- `UniqueItems`: Number of unique items purchased.  
- `TotalQty`: Total quantity of items purchased.  
- `TotalRtrnQty`: Quantity of returned items.  
- `NetQty`: Net purchased items (purchases - returns).  
- `UniqueDepts`: Number of unique departments visited.  
- `OneItemDepts`: Departments with single product purchases.  
- `RtrnDepts`: Departments with returns.  

For **association rule mining**, transactions are represented at the department level (`DepartmentDescription`).

## ⚙️ Methods
1. **Clustering (K-Means, K-Means++, PAM):**  
   - Groups similar shopping trips based on features like Net Quantity, Total Items, and Departments.  
   - Reveals customer segments such as quick errand trips vs. bulk shopping trips.  

2. **Decision Tree (C5.0):**  
   - Identifies key predictors of shopping behavior and returns.  
   - Provides interpretable classification rules.  

3. **Association Rule Mining (Apriori):**  
   - Discovers relationships between departments.  
   - Example: *Frozen Foods + Produce → Dry Goods (Lift = 3.06)*.  

## 📈 Key Insights
- **Net Quantity** is the strongest indicator of whether a trip involves returns.  
- Clustering reveals **distinct shopper types**, from single-item trips to large, multi-department visits.  
- Association rules identify **cross-selling opportunities**, e.g., customers buying Frozen Foods and Produce are three times more likely to buy Dry Goods.  

## 🚀 Applications
- **Marketing & Promotions:** Bundle or recommend products based on strong associations.  
- **Customer Segmentation:** Personalize offers for quick errand shoppers vs. bulk family shoppers.  
- **Operations:** Use Net Quantity insights to improve return management and reduce losses.  

## 📜 License
This project is for educational purposes. Data sourced from Kaggle/Walmart competition.  
