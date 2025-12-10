# 🧶 Crochet Procurement Classification Project  

## 📌 Overview  
This project explores **crochet spending analysis** using **MySQL 8.0** and **Python**, with a focus on yarn suppliers **Alize Burkum** and **YarnArt**.  
It demonstrates expertise in:  
- Relational database design  
- SQL-based procurement classification and spend analysis  
- Python-driven data visualization  

---

## ✨ Features  
- **Database schema** for suppliers, categories, items, purchase orders, and order lines  
- **Sample dataset** of crochet yarn purchases  
- **SQL queries** for procurement classification and supplier/category spend analysis  
- **Python integration** with `pandas`, `seaborn`, and `matplotlib`  
- **Visual insights** into supplier spend distribution and category-level trends  

---

## 📂 Project Structure  
```
crochet-procurement/
│
├── sql/                  # SQL scripts for schema & queries
│   ├── schema.sql
│   ├── sample_data.sql
│   └── analysis_queries.sql
│
├── python/               # Python scripts for visualization
│   ├── data_import.py
│   ├── spend_analysis.py
│   └── visualization.py
│
├── docs/                 # Documentation & diagrams
│   ├── ER_diagram.png
│   └── README.md
│
└── requirements.txt      # Python dependencies
```

---

## 🛠️ Database Setup  
1. Create the database:  
   ```sql
   CREATE DATABASE crochet_procurement;
   USE crochet_procurement;
   ```
2. Import schema and sample data:  
   ```sql
   SOURCE sql/schema.sql;
   SOURCE sql/sample_data.sql;
   ```

---

## 📊 Example Analyses  
- **Supplier Spend Breakdown**  
  ```sql
  SELECT supplier_name, SUM(order_line_total) AS total_spend
  FROM suppliers
  JOIN purchase_orders USING(supplier_id)
  JOIN order_lines USING(order_id)
  GROUP BY supplier_name;
  ```
- **Category Spend Visualization (Python)**  
  ```python
  import pandas as pd
  import seaborn as sns
  import matplotlib.pyplot as plt

  df = pd.read_csv("procurement_data.csv")
  sns.barplot(x="category", y="spend", data=df)
  plt.title("Category Spend Analysis")
  plt.show()
  ```

---

## 📈 Visual Insights  
- Supplier spend comparison (Alize Burkum vs YarnArt)  
- Category-level procurement trends  
- Time-series analysis of purchase orders  

---

## 🚀 How to Run  
1. Install dependencies:  
   ```bash
   pip install -r requirements.txt
   ```
2. Run SQL scripts in MySQL 8.0.  
3. Execute Python scripts for analysis and visualization:  
   ```bash
   python python/spend_analysis.py
   ```

---

## 🎯 Skills Demonstrated  
- **Database Design**: Normalized schema with relational integrity  
- **SQL Analytics**: Procurement classification, supplier/category spend queries  
- **Python Visualization**: Clear, insightful charts using `seaborn` and `matplotlib`  
- **Integration**: End-to-end workflow combining SQL and Python  

---

## 📌 Future Improvements  
- Add more suppliers and categories for broader analysis  
- Automate ETL pipeline for real-time procurement data  
- Deploy interactive dashboards with **Plotly** or **Streamlit**  

---

This version makes your README more professional, structured, and portfolio-ready. It highlights your technical and creative strengths while guiding readers through setup and usage.  

👉 Do you want me to also design a **visual ER diagram** and include it in your README so it looks even more polished?
