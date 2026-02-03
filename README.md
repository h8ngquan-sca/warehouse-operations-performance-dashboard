## 📊 Project Overview
A comprehensive warehouse operation dashboard in 2025 for ecommerce fulfillment center, demonstrating Total Orders, Average Monthly Orders, Fuflill & Cancel & Return Rate, Orders over Months and Days, Top Sellers and Marketplaces base on simulated dataset from real-world operations.
### Quick Facts

| Metric                 | Value                                       |
| ---------------------- | ------------------------------------------- |
| **Total Orders**       | 570,227                                     |
| **Data Period**        | Full Year 2025                              |
| **Time Span**          | Jan 1 - Dec 31                              |
| **Marketplaces**       | 5 (SHOPEE, TIKTOK, PANCAKE, EXTERNAL, KIOT) |
| **Sellers**            | 50+ unique sellers                          |
| **Logistics Partners** | 10+ carriers                                |
## 🛠️ Tool Used

| Component                     | Technology        | Details                                                       |
| ----------------------------- | ----------------- | ------------------------------------------------------------- |
| **Raw Data**                  | WMS (csv file)    | Download from Warehouse Management System (WMS)               |
| **Data Transformation**       | Excel Power Query | Clean, Transform and Load data                                |
| **Calculations**              | Excel             | Pivot Table and Excel Formulas (SUM, AVG...)                  |
| **Dashboard & Visualization** | Excel             | Pivot Chart (bar chart, line chart, column chart) and Slicers |
| **Documentation**             | Markdown          |                                                               |
### Excel Features Used
- **Power Query**: Removed, Filtered, Add & Transform Column
- **Pivot Table**: Add Slicers and Calculatate Metrics (Total Orders, Average Order by Month, Cancel & Return Orders, Cancel & Return Rate, Monthly and Daily Orders, Top 5 Sellers, Top 5 Marketplaces)
- **Pivot Charts**: Bar Chart, Column Chart, Line Chart
## 📈 Key Results

| Metrics              | Value               |
| -------------------- | ------------------- |
| **Total Orders**         | 570.227 orders      |
| **Average Month Orders** | 47.519 orders/month |
| **Fulfillment Rate**     | 88,29%              |
| **Cancel Rate**          | 9,47%               |
| **Return Rate**          | 1,96%               |
### **Key Performance Insights**
#### **Strength #1: Explosive Growth**
- **Finding**: Orders grew from **5,019 (Jan)** → **110,900 (Dec)**
- **Growth Rate**: **22x increase** over 12 months
- **Consistency**: Steady month-over-month growth
- **Projection**: Highly predictable growth pattern (trendline: y = 9226.24x - 12479)
#### **Challenge #1: High Cancel Rate**
- **Current**: 9.74% ~ 55,500 total cancelled orders
- **Next Step**: Need to prepare a Putback team to move picked items from cancel item back to location ready for next picking wave
#### **Challenge #2: Channel Concentration**
- **SHOPEE**: 246,553 orders (46.7% of volume)
- **TIKTOK**: 237,939 orders (41.7% of volume)
- **Combined**: 87.4% of all orders on 2 platforms
- **Next Step**: These two platforms hold a huge market share; close monitoring of their policies is necessary to maintain and improve customer service. Additionally, finding more sellers outside of the platforms is crucial to sharing order volume.
#### **Challenge #3: Seller Concentration**
- **Top Seller (NOFIV)**: 92,397 orders (16.2% of volume)
- **Top 10 Sellers**: ~70% of total volume
- **Risk Level**: HIGH - Losing top seller loses 92K orders/month
- **Next Step**: Need maintain good service level for NOFIV. While finding more seller to share order volume
## 💼 Business Impact
### #1 Capacity Planning
Current: 570K orders/year → 47.5K/month average
Growth: 22x growth
Recommendation:
- Expand and Ultilize storage space
- Require increase staff headcount
- Invest on infrastructure, such as picking basket, picking cart, pack jack...
### #2: Seller Volume:
Current 16% of order volume rely on NOFIV. Therefore, need to more recruit mid-tier sellers to reduce top seller to <10%

## 📁 Project Structure
```
warehouse-fulfillment-dashboard/
│
├── Warehouse_Performance_Dashboard.xlsx    # Main analysis and visualize file
├── fact_Outbound_data_2025.xlsx              # Dataset
├── Warehouse_Performanced_Dashboard.png  # Visualization dashboard (preview)
└── README.md                       # Project documentation
```
## 📊 Visualizations
The project generate a comprehensive dashboard including:
- Total Orders
- Average Monthly Orders
- Fulfill Rate
- Cancel Rate
- Return Rate
- Orders by Months - Line Chart
- Top 10 Sellers by Orders - Bar Chart
- Orders by Days - Line Chart
- Top 5 Marketplaces by Orders - Bar Chart
- Cancel and Return Rate by Marketplaces - Column Chart
- Slicers: Month, Quarter, Seller, Marketplace, Carrier, Type (Order Type)
<img width="1094" height="673" alt="Warehouse_Performanced_Dashboard" src="https://github.com/user-attachments/assets/f4d70560-db0c-482d-bc19-a17fd1f39a78" />

## 🔬 Calculations
### 1. **Total Orders**
Pivot Table:
- Value: Request_Code (Count)
<img width="349" height="733" alt="Total_Orders" src="https://github.com/user-attachments/assets/4548f072-068f-4684-a324-a4ebed611541" />

### 2. **Average Monthly Orders**
Formula: AVERAGE
```
=AVERAGE(G4:G15)
```
### 3. **Fulfil Rate & Cancel Rate & Return Rate**
Pivot Table:
- Rows: Order_Status
- Value: Request_Code (Show value as % of Grand Total)
<img width="339" height="728" alt="Fulfil_Rate_Cancel_ Rate_ Return_Rate" src="https://github.com/user-attachments/assets/53256cba-edf6-47ee-986b-9ff60739985d" />

### 4. Order by Month
Pivot Table:
- Rows: Created_Date (Month)
- Value: Request_Code (Count)
<img width="338" height="721" alt="Order_by_Month" src="https://github.com/user-attachments/assets/a4be6332-5998-45da-9110-b736c3ca7023" />

### 5. **Orders by Days**
Pivot Table:
- Rows: Created_Date (Days)
- Value: Request_Code (Count)
<img width="347" height="730" alt="Order_by_Days" src="https://github.com/user-attachments/assets/da3855a6-88b9-494f-a56f-6e16b7fbff60" />

### 6. **Top 10 Sellers by Marketplaces**
Pivot Table:
- Rows: Seller
- Value: Request_Code (Count)
- Filter Seller: Top 10 Items by Request_Code
<img width="343" height="728" alt="Top_10_Sellers_by_Marketplaces" src="https://github.com/user-attachments/assets/e6b84bb4-6104-4499-ba05-56ff617ffcbe" />

### 7. **Top 5 Marketplaces by Orders**
Pivot Table:
- Rows: Sale_Channel
- Value: Request_Code (Count)
- Filter Seller: Top 5 Items by Request_Code
<img width="337" height="721" alt="Top_5_Marketplaces_by_Orders" src="https://github.com/user-attachments/assets/5e8f789d-fd97-4665-bc90-b05753e62903" />

### 8. Cancel and Return Rate by Marketplaces
Pivot Table:
- Rows: Order_Status
- Column: Sale_Channel
- Value: Request_Code (Show value as % of Grand Total)
<img width="342" height="719" alt="Cancel and Return Rate by Marketplaces" src="https://github.com/user-attachments/assets/2e0149a6-f582-40f5-9050-acbcd3c5fb3c" />

## 🎓 Skills Demonstrated
### Supply Chain & Operations Knowledge
- **Supply Chain Operations:** Multi-channel ecommerce management, logistics partnership coordination, capacity planning, seller performance tracking
- **Data Analysis:** KPI calculation & tracking, trend identification, benchmarking, large-scale data aggregation
- **Excel & Visualization:** Interactive dashboard design, formulas, dynamic filtering, data visualization using Pivot Chart and Filters
- **Business Intelligence:** Strategic recommendations, risk assessment, insight generation, growth forecasting
## 🚀 Future Enhancements
- **Advanced Demand Forecasting:** Incorporate forecasting models to predict future demand trends.
- **PowerBI Visualization:** Develop an interactive PowerBI dashboard to enhance aesthetic appeal and deliver richer, multi-dimensional data insights compared to basic charts.
- **SKU-Level Granularity:** Expand data depth by including detailed SKU attributes (item name, SKU code, categories...) for more precise inventory optimization.
## 👨‍💼 Author
Hoang Quan
- Linkedin: https://www.linkedin.com/in/nphquan08/
- GitHub: https://github.com/h8ngquan-sca
- Email: nphoangquan8@gmail.com
## 📜 License
This project is open source and available under the [MIT License](https://github.com/h8ngquan-sca/warehouse-operations-performance-dashboard/blob/main/LICENSE)
## 🙏 Acknowledgments
This project utilizes a simulated dataset modeled after real-world operational structures. It draws directly from my hands-on experience managing an outbound team at ecommerce fulfillment center, processing over 4,000 orders per day
