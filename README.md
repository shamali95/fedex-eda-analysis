# 🚚 FedEx Delivery Operations – Exploratory Data Analysis (EDA)

## 🎯 Project Overview
This project performs **Exploratory Data Analysis (EDA)** on a simulated FedEx logistics dataset to uncover operational inefficiencies, identify delay patterns, and recommend strategies for optimizing delivery performance and cost.

The analysis focuses on:
- Improving **operational efficiency**
- Reducing **shipping costs**
- Enhancing **customer satisfaction**

---

## 🧩 Dataset Description
**File:** `fedex_deliveries.csv`

| Column Name | Description |
|--------------|-------------|
| ShipmentID | Unique identifier for each shipment |
| Origin | Origin city |
| Destination | Destination city |
| Pickup_Date | Date of pickup |
| Delivery_Date | Date of delivery |
| Delivery_Status | Delivered / Delayed / In Transit |
| Distance_KM | Distance between origin and destination (in KM) |
| Shipment_Mode | Air / Ground / Freight |
| Weight_KG | Shipment weight in kilograms |
| Cost_USD | Shipping cost in USD |
| Customer_Segment | Business / Retail / Government |
| Delay_Reason | Weather / Operational / Customs / None |

---

## 🧪 Analysis Steps

### **Part A: Data Understanding & Cleaning**
- Handled missing values using median/mode imputation  
- Detected and capped outliers using IQR  
- Converted date columns to datetime and derived `Delivery_Time_Days`  

### **Part B: Univariate & Bivariate Analysis**
- Distribution of delivery times  
- Shipment volume by mode  
- Average cost per customer segment  
- Delivery status distribution  
- Weight vs cost scatter analysis  

### **Part C: Geographic & Operational Insights**
- Top 5 Origin–Destination city pairs  
- Delay rates by shipment mode  
- Correlation heatmap of numeric features  
- Delay reason impact on delivery time  
- Average delivery time comparison by mode  

### **Part D: Business Recommendations**
1. **Optimize Mode Allocation:**  
   Shift short-distance (<300 km) Air shipments to Ground to reduce costs without major time impact.  
2. **Reduce High-Cost Deliveries:**  
   Investigate the top 5% most expensive shipments for route optimization or contract renegotiation.  
3. **Operational Improvements:**  
   Weather and operational delays dominate — invest in predictive maintenance and dynamic rerouting.  
4. **Customer Satisfaction:**  
   Notify customers proactively of predicted delays and offer priority handling for premium accounts.

---

## 📊 Visualizations
Generated under the `/figures` directory:
- `delivery_time_distribution.png`
- `volume_by_mode.png`
- `avg_cost_by_segment.png`
- `delay_rate_by_mode.png`
- `short_distance_cost_comparison.png`
- `high_cost_shipments_by_mode.png`

---

## 📁 Repository Structure
```
FedEx_EDA_Notebook.py
fedex_deliveries.csv
figures/
├── delivery_time_distribution.png
├── short_distance_cost_comparison.png
├── high_cost_shipments_by_mode.png
top_city_pairs.csv
delays_by_mode.csv
avg_time_by_mode.csv
high_cost_shipments_top5percent.csv
```

---

## 🧠 Key Insights
- Average delivery time ≈ **4–5 days**
- **Ground mode** dominates shipment volume
- **Air mode** is fastest but ~2× more costly
- **Operational delays** are most common
- Potential to cut shipping costs by **20–25%** with optimized mode allocation

---

## 💻 Tools & Libraries
- **Language:** Python  
- **Libraries:** pandas, numpy, matplotlib, seaborn  
- **Environment:** Jupyter / Google Colab  

---

## 🧾 How to Run the Project
```bash
# 1. Clone this repository
git clone https://github.com/shamali95/fedex-eda-analysis.git

# 2. Navigate to project directory
cd fedex-eda-analysis

# 3. Install dependencies
pip install pandas numpy matplotlib seaborn

# 4. Run the notebook/script
python FedEx_EDA_Notebook.py
```

---

## 🏁 Project Highlights
✔️ Automated detection of short-distance Air shipments for cost optimization  
✔️ Identification of top 5% high-cost deliveries for route improvement  
✔️ Actionable data-driven business recommendations  
✔️ Professional visualizations suitable for reports or dashboards  

---

### ⭐ If you found this project insightful, don’t forget to star ⭐ the repo!
