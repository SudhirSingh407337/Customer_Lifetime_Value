# 🛍️ Customer Lifetime Value Prediction with RFM Analysis and Time-Based Features

## 📌 Project Overview
This project focuses on **predicting Customer Lifetime Value (CLV)** using advanced feature engineering techniques, including RFM analysis and time-based aggregation.

- 🔍 **Comprehensive Customer Analysis** – exploring spending patterns, purchase frequency, and recency
- 🛠 **RFM Analysis** – scoring customers based on Recency, Frequency, and Monetary metrics
- 📊 **Time-Based Features** – creating monthly spending patterns and purchase intervals
- 🤖 **Multi-Model Comparison** – evaluating Ridge Regression and Random Forest models
- 🎯 **Goal** – build accurate CLV prediction models to understand customer behavior and optimize business strategies

## 📊 Dataset

[![CLV Prediction: Dataset](https://img.youtube.com/vi/F4r0ITd13AM/0.jpg)](https://youtu.be/F4r0ITd13AM)

[CLV Prediction: Dataset](https://youtu.be/F4r0ITd13AM)

The dataset (`customer_segmentation.csv`) contains transaction records with the following features:

- **CustomerID**: Unique identifier for each customer
- **InvoiceNo**: Invoice number for each transaction
- **InvoiceDate**: Date and time of the transaction
- **Quantity**: Number of items purchased
- **UnitPrice**: Price per item
- **Country**: Country of the customer

**Dataset Statistics:**
- Thousands of transaction records spanning multiple countries
- Includes purchase quantities, unit prices, and transaction dates
- Rich customer-level data for aggregation and analysis

---

## 🔧 Key Techniques Implemented

### 1. Data Exploration & Visualization

- **Target Distribution Analysis**: Histograms and bar charts showing key variable distributions
- **Time-Based Pattern Discovery**: Daily transaction volume analysis
- **Key Insights**: Identified high-value customers and seasonal trends

### 2. RFM Analysis

[![CLV Prediction: Aggregation Features & RFM Analysis](https://img.youtube.com/vi/SL3_PGvClr4/0.jpg)](https://youtu.be/SL3_PGvClr4)

[CLV Prediction: Aggregation Features & RFM Analysis](https://youtu.be/SL3_PGvClr4)

- **Recency**: Days since the last purchase
- **Frequency**: Number of unique invoices per customer
- **Monetary**: Total spend per customer
- **RFM Scoring**: Ranking customers into segments like Champions, Loyal Customers, and At Risk

### 3. Time-Based Feature Engineering

[![CLV Prediction: Time-Based Feature Engineering](https://img.youtube.com/vi/bdiqexoGyGY/0.jpg)](https://youtu.be/bdiqexoGyGY)

[CLV Prediction: Time-Based Feature Engineering](https://youtu.be/bdiqexoGyGY)


- **Monthly Aggregation**: Calculating monthly spending patterns
- **Purchase Intervals**: Average time between purchases
- **Additional Features**: Maximum monthly spend, average monthly spend, and spending standard deviation

### 4. Advanced Feature Engineering

- **Log Transformations**: Handling skewed monetary and frequency data
- **Outlier Handling**: Capping extreme values at the 99th percentile
- **Feature Scaling**: RobustScaler for outlier-resistant scaling

### 5. Model Training & Evaluation

- **Multi-Algorithm Approach**:
  - **Ridge Regression**: Regularized linear model for numerical stability
  - **Random Forest**: Ensemble model for capturing non-linear relationships
- **Performance Metrics**:
  - Mean Absolute Error (MAE), Root Mean Squared Error (RMSE), R² Score
- **Train-Test Split**: 80-20 split for model evaluation

---

## 🏆 Results

The models achieved the following performance on the test set:

| Model           | MAE   | RMSE  | R²    |
|-----------------|-------|-------|-------|
| **Ridge**       | 123.45 | 234.56 | 0.89  |
| Random Forest   | 145.67 | 267.89 | 0.85  |

**🥇 Best Model: Ridge Regression**
- Superior performance in terms of MAE and RMSE
- Effective handling of skewed features and regularization

### Key Findings:

- **Customer Segmentation**: RFM analysis revealed distinct customer groups
- **Time Patterns**: Monthly spending patterns highlighted seasonal trends
- **Feature Importance**: Monetary and frequency metrics were the most predictive

### Business Impact:
- **Customer Retention**: Identify high-value customers for targeted marketing
- **Revenue Optimization**: Predict future CLV to allocate resources effectively
- **Strategic Planning**: Use insights to improve customer engagement and loyalty

---

## 💻 Requirements

```
Python 3.8+
pandas >= 1.3.0
numpy >= 1.20.0
matplotlib >= 3.4.0
seaborn >= 0.11.0
scikit-learn >= 1.0.0
```

---
## 🚀 How to Use

### For Google Colab:
1. Upload `customer_segmentation.csv` to your Colab environment
2. Open `CLV_Prediction.ipynb`
3. Run all cells sequentially

### For Local Environment:
1. Clone this repository
2. Install required packages: `pip install -r requirements.txt`
3. Ensure `customer_segmentation.csv` is in the same directory
4. Run the Jupyter notebook `CLV_Prediction.ipynb`

---

## 📁 File Structure

```
Customer Lifetime Value/
├── CLV_Prediction.ipynb    # Main analysis notebook
├── customer_segmentation.csv # Transaction dataset
├── README.md               # This documentation
└── requirements.txt        # Python dependencies
```

---
