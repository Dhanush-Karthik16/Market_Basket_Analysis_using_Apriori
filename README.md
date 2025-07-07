# 🛒 Market Basket Analysis using Apriori Algorithm

This project performs **Association Rule Mining** on transactional retail data using the **Apriori algorithm**. The aim is to discover patterns and relationships between frequently purchased items — a process known as **Market Basket Analysis**.

---

## 📁 Dataset

- **Name:** Market_Basket_Optimisation.csv  
- **Format:** 7501 transactions (rows), each with up to 20 items (columns)
- **Source:** Commonly used synthetic dataset for Apriori demonstrations

---

## 🧠 Objectives

- Transform transactional data into a list of itemsets
- Apply the **Apriori algorithm** to extract frequent itemsets and association rules
- Filter rules based on:
  - **Minimum Support** = 0.003
  - **Minimum Confidence** = 0.2
  - **Minimum Lift** = 3
- Identify the top 10 strongest rules using **lift**

---

## 🔧 Technologies Used

- Python
- Pandas & NumPy
- `apyori` (Apriori implementation)
- Jupyter Notebook / Google Colab

---

## 📊 Key Steps

1. **Data Preprocessing:**
   - Load CSV file
   - Convert transaction rows into a list of itemsets (removing empty/nulls)
   
2. **Apriori Algorithm:**
   - Define support, confidence, lift, and rule length
   - Generate frequent itemsets and association rules

3. **Rule Extraction & Filtering:**
   - Use custom `inspect()` function to extract LHS, RHS, Support, Confidence, and Lift
   - Convert to Pandas DataFrame for further analysis
   - Display top rules by Lift

---

## 📈 Output Example (Top Rules)

| LHS         | RHS         | Support | Confidence | Lift  |
|-------------|-------------|---------|------------|-------|
| Mineral water | Whole wheat bread | 0.005       | 0.24       | 3.1   |
| Eggs         | Frozen vegetables  | 0.004       | 0.22       | 3.3   |
| ...         | ...         | ...     | ...        | ...   |

> These rules indicate items that are often purchased together, which can inform product bundling, promotions, or store layout decisions.

---

## ▶️ How to Run

1. Install dependencies (in Jupyter/Colab):
   ```python
   !pip install apyori
