# 🛒 Customer Lifetime Value (CLTV) Analysis

This project aims to identify and segment high-value customers based on their predicted lifetime value using historical transaction data. By analyzing customer behavior patterns, we enable targeted marketing, retention strategies, and better revenue forecasting.

---

## 📌 Objective

Estimate **Customer Lifetime Value (CLTV)** to:
- Identify high-value customers
- Enable targeted loyalty and retention campaigns
- Optimize marketing spend and maximize long-term revenue

---

## 📂 Dataset

- **Source**: [UCI Online Retail Dataset](https://archive.ics.uci.edu/ml/datasets/online+retail)
- **Records**: 541,909 transactions
- **Fields**: `InvoiceNo`, `StockCode`, `Description`, `Quantity`, `InvoiceDate`, `UnitPrice`, `CustomerID`, `Country`

---

## 🔧 Tools & Libraries Used

- Python
- Pandas, NumPy
- Matplotlib, Seaborn
- `lifetimes` (BG/NBD & Gamma-Gamma modeling)

---

## 🧹 Data Cleaning & Preparation

- Converted `InvoiceDate` to datetime format
- Dropped rows with missing `CustomerID`
- Removed cancelled orders (invoices starting with 'C')
- Filtered out negative/zero `Quantity` and `UnitPrice`
- Created new `Revenue` feature (`Quantity * UnitPrice`)

---

## 📊 Exploratory Data Analysis (EDA)

### ✅ Top Insights:
- **Top Revenue-Generating Countries**:  
  🇬🇧 United Kingdom dominates, followed by 🇳🇱 Netherlands, 🇮🇪 Ireland, 🇩🇪 Germany, 🇫🇷 France  
- **Monthly Revenue Trend**:  
  Peak in **November**, dip in **December**  
- **Top Products**:  
  High revenue driven by select products (e.g., gift items)

---

## 🧠 RFM Analysis

Calculated key metrics per customer:
- **Recency**: Days since last purchase
- **Frequency**: Number of unique purchases
- **Monetary**: Total spend

RFM scores were assigned using quartiles and summed to get a composite score (`RFM_score`).  
**High-value customers** identified with scores ≥ 9.

---

## 📈 CLTV Modeling

Used `lifetimes` package with:
- **BG/NBD Model** to predict future purchase frequency
- **Gamma-Gamma Model** to estimate average profit per purchase

### 🔢 CLTV Calculation:
- Computed 30-day CLTV
- Segmented customers into `High`, `Medium`, and `Low` based on CLTV percentiles

---

## 📌 Key Results

| Segment | Avg. CLTV | Predicted Purchases | Avg. Profit |
|---------|-----------|----------------------|--------------|
| High    | 739       | 0.96                 | 890          |
| Medium  | 146       | 0.44                 | 362          |
| Low     | 56        | 0.21                 | 298          |

### 📊 Visualizations:
- Revenue trends by country and month
- CLTV distribution across segments
- Customer count per segment

---

## 💡 Business Recommendations

### 1. **Targeted Campaigns**
- High CLTV: Personalized offers, loyalty programs
- Medium CLTV: Upselling & cross-selling
- Low CLTV: Targeted discounts or minimal spend

### 2. **Geographic Focus**
- Prioritize UK, but explore emerging markets like Germany and France

### 3. **Peak Season Strategy**
- Prepare for November surge
- Plan inventory and promotions in advance

---

## 📁 Project Structure
├── 📄 online_retail.csv  
├── 📊 Customer Lifetime Value Analysis-checkpoint.ipynb  
└── 📝 README.md


**Bhavesh Kalihari**  
📧 [Email](mailto:bhaveshkalihari70@gmail.com)  
🔗 [LinkedIn](https://www.linkedin.com/in/bhavesh-kalihari)  
📁 [GitHub](https://github.com/STAAR13)
