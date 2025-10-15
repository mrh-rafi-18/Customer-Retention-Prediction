
## Setup Instructions

## Google Colab Setup
-Open the notebook in colab 

-Execute cell by cell. Or **Just run all in one go** then upload the csv file through third code cell. That's it.



# Customer Retention Prediction Project

## Project Overview
This project focuses on developing machine learning models to predict customer churn using historical customer data. The goal is to identify at-risk customers early and enable proactive retention strategies to reduce customer attrition and improve business profitability.

- **Project Duration**: [Add timeline]  
- **Platform**: Google Colab  
- **Tools**: Python, Scikit-learn, XGBoost, LightGBM, PyTorch  
- **Team**: [Add team details if applicable]  

---

## Dataset Description


### Overview
This dataset contains **1,000 customer records** with 15 attributes related to customer demographics, behavior, and engagement metrics. The dataset is designed for customer churn prediction analysis.

### Columns Description

| Column Name | Data Type | Description |
|-------------|-----------|-------------|
| `Customer_ID` | Integer | Unique identifier for each customer |
| `Age` | Integer | Customer's age |
| `Gender` | Categorical | Customer's gender (Male, Female, Other) |
| `Annual_Income` | Float | Customer's annual income (in thousands) |
| `Total_Spend` | Float | Total amount spent by customer |
| `Years_as_Customer` | Integer | Number of years as a customer |
| `Num_of_Purchases` | Integer | Total number of purchases made |
| `Average_Transaction_Amount` | Float | Average amount per transaction |
| `Num_of_Returns` | Integer | Number of product returns |
| `Num_of_Support_Contacts` | Integer | Number of customer support contacts |
| `Satisfaction_Score` | Integer | Customer satisfaction score (1-5 scale) |
| `Last_Purchase_Days_Ago` | Integer | Days since last purchase |
| `Email_Opt_In` | Boolean | Whether customer opted for email marketing |
| `Promotion_Response` | Categorical | Response to promotions (Responded, Ignored, Unsubscribed) |
| `Target_Churn` | Boolean | Target variable - whether customer churned |

### Key Statistics Summary

- **Total Records**: 1,000 customers
- **Features**: 14 independent variables
- **Target Variable**: `Target_Churn` (binary classification)
- **Data Types**: Mix of numerical, categorical, and boolean variables
- **Missing Values**: None apparent from the sample
- **Duplicate Values**: None
- **Correlation of columns with each other**: Very weak

### Potential Use Cases

1. **Churn Prediction**: Build models to predict customer churn
2. **Customer Segmentation**: Identify high-risk customer groups
3. **Retention Strategy**: Understand factors influencing customer retention
4. **Marketing Optimization**: Improve promotion targeting based on response patterns

### Data Quality Notes

- Contains realistic variation in customer behaviors
- Includes both demographic and transactional features
- Balanced representation of different customer segments
- Clean, structured format suitable for analysis

---


## Model Implementation

The project implemented and compared 6 different algorithms:

- Random Forest
- XGBoost
- LightGBM
- Logistic Regression
- TabNet (Deep Learning)
- TabTransformer (Deep Learning)

---

### Evaluation Framework
- **Train-Test Split**: 80-20  
- **Metrics**: Accuracy, ROC-AUC, Precision, Recall, F1-Score  
- **Cross-validation** for robust evaluation  

---

### Key Results

| Model             | Accuracy | ROC-AUC  | Notes                     |
|------------------|----------|----------|--------------------------|
| TabTransformer    | 56.5%    | 0.5584   | Highest Accuracy         |
| LightGBM          | 54.0%    | 0.5227   | Best Tree-based          |
| XGBoost           | 50.0%    | 0.4750   | Balanced Performance     |
| Random Forest     | 48.5%    | 0.4686   |                          |
| Logistic Regression | 49.5%  | 0.4611   | Poor Performance         |
| TabNet            | 48.5%    | 0.4664   |                          |
| Simple ANN        | 52.5%    | 0.4537   | Failed to learn patterns |

---

### Critical Findings

####  Positive Aspects
- Dataset is well-balanced with no class imbalance  
- Comprehensive evaluation of multiple algorithms  
- TabTransformer showed promising results with 56.5% accuracy  

#### Challenges Identified
- **Limited Predictive Power**: All models performed near random chance (~50%)  
- **Weak Feature Signals**: Features lack strong correlation with churn  
- **Data Limitations**: Missing key behavioral and engagement indicators  

####  Model Insights
- **Best Performer**: TabTransformer (56.5% accuracy)  
- **Most Consistent**: Tree-based models (48.5%-54% accuracy)  
- **Poor Performance**: Linear models confirm non-linear relationships  
- **Training Issues**: Simple ANN failed to learn meaningful patterns  

#### Business Implications
- **Current Limitation**: Existing data insufficient for reliable churn prediction  
- **Strategic Insight**: Need enhanced customer behavior tracking  
- **Immediate Action**: Focus on data quality improvement over model optimization  
- **Future Roadmap**: Collect additional behavioral and engagement metrics  

---

### Recommendations
- **Data Enhancement**: Add product usage frequency, customer feedback, web analytics  
- **Feature Engineering**: Create temporal patterns and composite metrics  
- **Alternative Approach**: Consider customer segmentation over individual prediction  
- **Process Improvement**: Implement systematic churn driver analysis  

---

### Conclusion
While the current models show limited predictive capability, this project establishes a strong foundation for data-driven customer retention and provides clear direction for future improvements in data collection and feature engineering.

