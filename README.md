# Fedex-Logistics-Performance-Analysis

## 📌 Project Overview

This project performs **Exploratory Data Analysis (EDA)** on FedEx logistics and delivery data to understand shipment patterns, delivery performance, logistics costs, product groups, fulfillment methods, and factors associated with delivery delays.

The analysis uses Python-based data cleaning, transformation, statistical analysis, and visualization techniques to generate meaningful business insights and recommendations.

---

## 🎯 Business Objective

The primary objective of this project is to analyze logistics and delivery data and identify:

* Delivery performance and delay patterns
* Shipment volume across different categories
* Shipment mode performance
* Product-group distribution
* Country-level delivery patterns
* Fulfillment-method performance
* Relationship between shipment weight and insurance value
* Relationship between freight cost and delivery delay
* Correlations among important numerical variables

The findings can help the business identify areas that require operational attention and support data-driven logistics decisions.

---

## 📊 Dataset

The project uses the **SCMS Delivery History Dataset**.

The dataset contains shipment and logistics-related information such as:

* Shipment information
* Country
* Product Group
* Shipment Mode
* Fulfillment Method
* Vendor information
* Shipment dates
* Delivery dates
* Weight
* Freight Cost
* Insurance Value
* Product and pricing information

### Dataset Size

* **Rows:** 10,324
* **Columns:** 33

---

## 🛠️ Technologies Used

* **Python**
* **Pandas** – Data manipulation and analysis
* **NumPy** – Numerical operations
* **Matplotlib** – Data visualization
* **Seaborn** – Statistical visualization
* **Plotly** – Interactive visualizations
* **Jupyter Notebook / Google Colab**

---

## 🔎 Project Workflow

The analysis follows these major steps:

### 1. Data Loading

The dataset is loaded into a Pandas DataFrame for analysis.

### 2. Data Understanding

Initial analysis includes:

* Shape of the dataset
* Column names
* Data types
* Statistical summary
* Unique values
* Duplicate records
* Missing values

### 3. Data Cleaning

The dataset is prepared for analysis by:

* Handling missing values
* Checking duplicate records
* Converting date columns
* Cleaning numerical fields
* Handling inconsistent values
* Creating derived variables

### 4. Feature Engineering

Two important variables were created:

* `Delivery_Delay`
* `Delivery_Status`

These variables help evaluate whether shipments were delivered earlier, on time, or later than the scheduled delivery date.

---

## 📈 Exploratory Data Analysis

The project analyzes multiple business questions using different visualization techniques.

### Shipment and Delivery Performance

The analysis examines overall delivery performance and identifies the proportion of shipments that were delivered on time versus delayed.

### Shipment Mode Analysis

Different shipment modes are compared to understand their delivery-delay patterns.

The analysis indicates that **Ocean shipments show a greater tendency toward positive delivery delays**, while Truck and Air Charter generally show negative delivery delays.

### Product Group Analysis

The dataset is highly concentrated in the **ARV** product group.

Product-group counts include:

| Product Group | Count |
| ------------- | ----: |
| ARV           | 8,550 |
| HRDT          | 1,728 |
| ANTM          |    22 |
| ACT           |    16 |
| MRDT          |     8 |

Because some product groups contain very few observations, conclusions about their delivery performance should be interpreted carefully.

### Weight vs Insurance

A scatter plot and correlation analysis were used to examine the relationship between shipment weight and insurance value.

The correlation is approximately:

**0.53**

This indicates a moderate positive relationship.

In general, heavier shipments tend to be associated with higher insurance values.

However, correlation does not prove that shipment weight directly causes higher insurance costs.

### Freight Cost vs Delivery Delay

The relationship between freight cost and delivery delay was also examined.

The correlation is approximately:

**-0.025**

This is very close to zero, suggesting little linear relationship between freight cost and delivery delay in this dataset.

Therefore, simply increasing freight expenditure may not necessarily reduce delivery delays.

### Fulfillment Method

Delivery performance was compared across fulfillment methods.

The analysis found average delivery delays of approximately:

| Fulfillment Method | Average Delay |
| ------------------ | ------------: |
| Direct Drop        |    -3.54 days |
| From RDC           |    -8.28 days |

Both averages are negative, meaning shipments were delivered earlier than their scheduled dates on average.

### Correlation Analysis

A correlation heatmap was created to examine relationships among important numerical variables.

Important observations include:

* Weight and insurance have a moderate positive relationship.
* Freight cost and delivery delay have almost no linear relationship.
* The heatmap helps identify variables that may be useful for further analysis or predictive modeling.

---

## 📊 Visualizations

The project uses several visualization techniques, including:

* Bar charts
* Scatter plots
* Box plots
* Correlation heatmaps
* Pair plots
* Interactive Plotly charts

These visualizations are used to identify patterns, relationships, distributions, and potential operational issues.

---

## 💡 Key Insights

Some of the important findings from the analysis are:

1. **ARV represents the majority of shipments**, making it the most important product group in terms of shipment volume.

2. **Ocean shipments show greater delivery-delay concerns** compared with some other shipment modes.

3. **Weight and insurance value have a moderate positive relationship**, with a correlation of approximately 0.53.

4. **Freight cost has almost no linear relationship with delivery delay**, with a correlation of approximately -0.025.

5. **Both fulfillment methods analyzed have negative average delivery delays**, indicating that shipments were delivered earlier than their scheduled dates on average.

6. Product groups with very small numbers of observations should not be used to make strong general conclusions.

---

## 💼 Business Recommendations

Based on the EDA findings, the following actions can be considered:

### 1. Investigate Ocean Shipment Delays

Ocean shipments show greater delivery-delay concerns. The logistics team should investigate factors such as:

* Route
* Country
* Transit time
* Scheduling
* Port-related factors
* Shipment volume

### 2. Focus on High-Volume Product Groups

Since ARV represents the majority of records, operational improvements involving this product group could have a larger overall impact.

### 3. Do Not Assume Higher Freight Cost Reduces Delays

The near-zero correlation between freight cost and delivery delay suggests that increasing freight expenditure alone may not solve delivery-delay problems.

The company should investigate operational factors that have a stronger relationship with delays.

### 4. Consider Shipment Weight When Evaluating Insurance

Since shipment weight has a moderate positive relationship with insurance value, heavier shipments may require greater attention when evaluating insurance requirements and costs.

### 5. Perform Further Analysis

The EDA can be extended using predictive analytics or machine learning to identify the factors that most strongly influence delivery delays.

---

## 📁 Project Structure

```text
Fedex-Logistics-Performance-Analysis/
│
├── README.md
│
├── Fedex_Logistics_Performance_Analysis.ipynb
│
├── data/
│   └── SCMS_Delivery_History_Dataset.csv
│
├── images/
│   └── project_visualizations/
│
├── requirements.txt
│
└── .gitignore
```

> **Note:** If the original dataset cannot be publicly shared, it should not be uploaded to GitHub. In that case, keep the dataset locally and provide instructions for obtaining it separately.

---

## ▶️ How to Run the Project

### 1. Clone the repository

```bash
git clone YOUR_GITHUB_REPOSITORY_URL
```

### 2. Navigate to the project directory

```bash
cd Fedex-Logistics-Performance-Analysis
```

### 3. Install the required libraries

```bash
pip install -r requirements.txt
```

### 4. Open the Jupyter Notebook

```bash
jupyter notebook
```

Then open:

```text
Fedex_Logistics_Performance_Analysis.ipynb
```

---

## 📦 Requirements

The main Python libraries used in this project are:

```text
pandas
numpy
matplotlib
seaborn
plotly
jupyter
```

---

## 🚀 Future Scope

This project can be extended beyond exploratory analysis by:

* Building a **delivery-delay prediction model**
* Identifying the most important factors influencing delays
* Developing a logistics performance dashboard
* Performing country-level risk analysis
* Comparing shipment modes using statistical testing
* Creating automated logistics performance reports
* Applying machine learning for delivery-delay prediction

---

## 👩‍💻 Author

**Pragati Vidhate**

Python Developer | Data Analyst | Data Science Enthusiast

### Skills Demonstrated

`Python` · `Pandas` · `NumPy` · `EDA` · `Data Visualization` · `Statistics` · `SQL` · `Machine Learning`

---

## ⭐ Project Summary

This project demonstrates an end-to-end **Exploratory Data Analysis workflow**, from data cleaning and feature engineering to visualization, statistical analysis, business insights, and recommendations.

The analysis shows how logistics data can be transformed into actionable insights for improving delivery performance and supporting data-driven business decisions.
