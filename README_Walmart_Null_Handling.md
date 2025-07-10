# 🛒 Walmart Null Value Handling Project

## 📌 Project Objective
This project focuses on identifying and handling missing values in a simulated real-world Walmart sales dataset. The goal was to apply thoughtful, column-specific strategies to clean the data and make it ready for further analysis.

---

## 📂 Folder Structure

```
Walmart_Null_Handling_Project/
│
├── 01_Dataset/
│   ├── walmart_sales_with_nulls.csv
│   └── walmart_cleaned.xlsx
│
├── 02_Notebook/
│   └── walmart_null_handling.ipynb
│
├── 03_Documentation/
│   └── Walmart_Null_Handling_Documentation.pdf
│
├── 04_Images/
│   ├── before_null_plot.png
│   └── after_null_plot.png
│
└── README.md
```

---

## 🧠 Null Value Handling Strategy

| Column         | Type        | Missing Values | Handling Strategy                                                  |
|----------------|-------------|----------------|--------------------------------------------------------------------|
| Order ID       | Identifier  | 7              | Filled with `'Unknown'`                                            |
| Customer ID    | Identifier  | 6              | Filled with `'Unknown'`                                            |
| Customer Name  | Identifier  | 3              | Filled with `'Unknown'`                                            |
| Order Date     | Date        | 15             | Imputed manually using year/month distribution and region logic    |
| City           | Categorical | 12             | Filled with `'Unknown'`                                            |
| Region         | Categorical | 4              | Inferred using City; dropped row if unmatched                      |
| Category       | Categorical | 7              | Filled using frequency + region-category relationships             |
| Quantity       | Numeric     | 7              | Inferred using similar records (category, region, date)            |
| Sales          | Numeric     | 11             | Filled using average sales by category/region                      |
| Profit         | Numeric     | 12             | Filled with `0.0` (assumed no profit or unknown)                   |

---

## 📈 Visual Summary

| Before Cleaning                         | After Cleaning                          |
|----------------------------------------|-----------------------------------------|
| ![Before](./04_Images/before_null_plot.png) | ![After](./04_Images/after_null_plot.png) |

---

## 🛠️ Tools Used
- **Python 3.x**
- **Jupyter Notebook**
- **Pandas, NumPy**
- **Matplotlib, Seaborn**
- **Excel (for output dataset)**

---

## 📌 Key Learnings

- Handling missing data requires **context-aware decisions**.
- Not all columns should be treated the same — identifiers, dates, categories, and numbers each need different approaches.
- Visualizing before and after null handling helps verify the effectiveness of your strategy.
- Clean data is critical for valid future analysis like sales trends, customer segmentation, or forecasting.

---

## 👨‍💻 Author

**Siddes**  
Aspiring Data Analyst  
📫 [siddesanalyst@gmail.com]  
