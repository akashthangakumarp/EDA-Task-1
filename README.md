# 🛒 E-Commerce Order Analysis Using Python & Pandas

## 📌 Project Overview

This project focuses on **cleaning, analyzing, and understanding an E-Commerce Order Dataset** using **Python and Pandas**.

The dataset contains information about customers, products, orders, payment modes, quantities, prices, discounts, and ratings.

---

## 🛠️ Technologies Used

* **Python**
* **Pandas**
* **Google Colab / Jupyter Notebook**
* **CSV**

---

## 📂 Dataset

**File:** `Ecommerce_Order_Test_Dataset.csv`

* **Rows:** 101
* **Columns:** 13

### Dataset Columns

| Column          | Description       |
| --------------- | ----------------- |
| `Order_ID`      | Unique order ID   |
| `Order_Date`    | Date of order     |
| `Delivery_Date` | Delivery date     |
| `Customer_Name` | Customer name     |
| `Gender`        | Customer gender   |
| `City`          | Customer city     |
| `Category`      | Product category  |
| `Product`       | Product name      |
| `Payment_Mode`  | Payment method    |
| `Quantity`      | Quantity ordered  |
| `Unit_Price`    | Price of one unit |
| `Discount`      | Discount value    |
| `Rating`        | Customer rating   |

---

## 🔍 Tasks Performed

### Q1. Load and Inspect

* Loaded the CSV file into a DataFrame named `df`.
* Displayed the first 5 rows.
* Displayed the number of rows and columns.
* Displayed all column names.

### Q2. Understand the Dataset

Used the following Pandas functions:

* `info()` — to display basic information about the dataset.
* `describe()` — to display the statistical summary of numerical columns.

### Q3. Handle Missing Values

First, the missing values in each column were identified.

The following methods were used to handle missing values:

* Filled missing `City` values with `"Unknown"`.
* Filled missing `Customer_Name` values with `"Unknown"`.
* Filled missing `Rating` values with the **mean rating**.
* Filled missing `Payment_Mode` values with `"Unknown"`.

### Q4. Remove Duplicates

* Found the number of duplicate rows.
* Removed duplicate rows using `drop_duplicates()`.
* Displayed the new shape of the DataFrame.

### Q5. Clean Text Data

The following columns were cleaned:

* `Gender`
* `City`
* `Payment_Mode`

Used:

* `strip()` — to remove unnecessary spaces.
* `title()` — to make text formatting consistent.

Displayed the unique values after cleaning.

### Q6. Create New Columns

Three new columns were created.

#### Total Price

```text
Total Price = Quantity × Unit Price
```

#### Discount Amount

```text
Discount Amount = Total Price × Discount
```

#### Final Amount

```text
Final Amount = Total Price - Discount Amount
```

Displayed the following columns:

* `Order_ID`
* `Product`
* `Quantity`
* `Total Price`
* `Discount Amount`
* `Final Amount`

---

## 📊 Numerical Analysis

The following calculations were performed:

* **Total Quantity Ordered**
* **Average Unit Price**
* **Maximum Unit Price**
* **Minimum Unit Price**
* **Average Rating**

---

## 🔎 Filtering

The following filtering operations were performed:

### 1. Orders where Quantity > 3

Filtered orders where the quantity ordered was greater than 3.

### 2. Orders where Rating ≥ 4.5

Filtered orders with a customer rating of 4.5 or higher.

### 3. Orders where Final Amount > 5000

Filtered orders where the final amount was greater than 5000.

### 4. Orders from Chennai

Filtered orders where the city was **Chennai**.

Only the required feature/value was displayed for each filtering condition.

---

## 🔽 Sorting

The dataset was sorted by **Final Amount** from highest to lowest.

The **top 5 orders** were displayed with the following columns:

| Column         |
| -------------- |
| `Order_ID`     |
| `Product`      |
| `Category`     |
| `Quantity`     |
| `Final Amount` |

---

## 📊 Key Pandas Operations Used

Some important Pandas functions used in this project are:

```python
pd.read_csv()
df.head()
df.shape
df.columns
df.info()
df.describe()
df.isnull().sum()
df.fillna()
df.duplicated()
df.drop_duplicates()
df.sort_values()
df.loc[]
df.unique()
```

---

## 🎯 Objective

The main objective of this project is to understand the basic steps involved in **data preprocessing and analysis using Pandas**.

The project covers:

* Data loading
* Data inspection
* Missing value handling
* Duplicate removal
* Text cleaning
* Feature creation
* Numerical analysis
* Data filtering
* Data sorting

---

## 📁 Project Structure

```text
E-Commerce-Order-Analysis/
│
├── Ecommerce_Order_Test_Dataset.csv
├── ecommerce_order_analysis.ipynb
└── README.md
```

---

## ✅ Conclusion

This project demonstrates how **Python and Pandas** can be used to clean and analyze an E-Commerce dataset.

The dataset was successfully **inspected, cleaned, processed, filtered, and sorted** to obtain useful information about customer orders, quantities, prices, discounts, final amounts, and ratings.

Overall, this project provides practical experience with **data preprocessing and basic data analysis using Pandas**.
