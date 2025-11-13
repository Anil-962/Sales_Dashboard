# 📊 Sales Performance Dashboard (Power BI)

A complete end-to-end **Sales Analytics Dashboard** designed in Power BI, focused on transforming raw sales data into clear business insights.  
This project reflects my ability to work with data modeling, DAX, visualization design, and dashboard storytelling — exactly how analytics is done in the real world.

---

## 🧩 Project Story

I started this project with one goal:

### **"Build a clean, executive-friendly dashboard that answers the real questions a business cares about."**

Most dashboards online are messy, overloaded, or visually inconsistent.  
So I challenged myself to design something that looks:

✔ Corporate  
✔ Minimal  
✔ Insight-focused  
✔ Client-ready  

This required not just building charts, but understanding **why each chart matters**, and how it contributes to decision-making.

As I refined the design, I focused on:

- Clean color themes  
- Consistent spacing  
- Intuitive layout  
- Professional KPI cards  
- A balanced mix of visuals  
- Smooth user interaction  

The final dashboard is something I’d proudly deliver to a client or add to my analytics portfolio.

---

## 🚀 What This Dashboard Shows

### **1. Executive Summary KPIs**
These top-level metrics help management understand the business instantly:

- **Total Sales**
- **Total Profit**
- **Total Orders**
- **Average Order Value (AOV)**
- **MoM Growth %**

### **2. Trend Analysis**
A monthly line chart reveals:

- seasonality  
- performance drops  
- peak sales months  
- stability vs volatility  

### **3. Regional Performance**
Which regions are performing well and where growth is slowing down.

### **4. Product Insights**
Shows the **Top 10 products** by revenue with clear ranking.

### **5. Profit vs Sales Comparison**
Helps identify:

- high-revenue but low-profit products  
- low-revenue but high-profit opportunities  
- product-level strategy decisions  

---


### **Relationships**
- `Orders[OrderDate]` → `Calendar[Date]`
- `Orders[CustomerID]` → `Customers[CustomerID]`
- `Orders[ProductID]` → `Products[ProductID]`

This structure ensures time intelligence functions (DATEADD, MoM growth) work correctly.

---

## 🧮 Key DAX Measures

```DAX
Total Sales = SUM(Orders[Sales])

Total Profit = SUM(Orders[Profit])

Total Orders = COUNT(Orders[OrderID])

AOV = DIVIDE([Total Sales], [Total Orders])

MoM Growth % =
VAR CurrentMonth = [Total Sales]
VAR PreviousMonth =
    CALCULATE([Total Sales], DATEADD('Calendar'[Date], -1, MONTH))
RETURN
DIVIDE(CurrentMonth - PreviousMonth, PreviousMonth)
```
--
## 🛠 Tools & Technologies

- **Power BI Desktop**
- **DAX (Data Analysis Expressions)**
- **Power Query (ETL)**
- **Data Modeling (Star Schema)**
- **Visualization & UX Design**

---

## 🎯 What I Learned

### 1. The importance of good layout
A dashboard isn’t just charts — it’s a visual story.  
Spacing, alignment, and consistency matter more than people think.

### 2. Data modeling matters
Once the dataset was structured properly, DAX became easier and visuals behaved correctly.

### 3. Clean design wins
Removing clutter (borders, too many colors, inconsistent backgrounds) dramatically improved clarity.

### 4. DAX time intelligence
Understanding `DATEADD`, `SAMEPERIODLASTYEAR`, MoM calculations, and other time-intelligence functions strengthened the insights.

### 5. User-centric thinking
I built this dashboard not for myself, but for a business user:
- simple  
- intuitive  
- actionable  

---

## 📸 Dashboard Preview

(Add your screenshot here)

![Dashboard Preview]("./Screenshots/Sales_Dashboard.png")

---

---

## 👨‍💻 About Me

**Ani**  
Power BI Developer | Data Analyst  
Passionate about dashboards, clean design, and business storytelling.

🔗 **LinkedIn:** ([add your link here](https://www.linkedin.com/in/anil-kumar-g-r))




