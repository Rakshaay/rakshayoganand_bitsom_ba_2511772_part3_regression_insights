# Retail Store Monthly Sales Regression Analysis

# 1. Business Problem Summary

The objective of this project is to identify the key business factors associated with monthly sales performance across retail stores.

The analysis supports leadership in making data-driven decisions regarding marketing investment, inventory management, staffing, discount strategy, and overall store operations. Regression analysis is used to determine which variables are most strongly associated with monthly sales and to provide actionable business recommendations.

---

# 2. Dataset Description

The dataset contains monthly performance information for multiple retail stores.

### Variables Included

- Store ID
- Month
- Region
- Store Type
- Marketing Spend
- Footfall
- Average Discount Percentage
- Staff Count
- Inventory Availability Percentage
- Competitor Distance (km)
- Holiday Flag
- Customer Rating
- Monthly Sales
- Monthly Profit

Total observations: **320**

---

# 3. Dependent and Independent Variables

## Dependent Variable

- Monthly Sales

## Independent Variables

- Marketing Spend
- Footfall
- Average Discount Percentage
- Staff Count
- Inventory Availability Percentage
- Competitor Distance
- Holiday Flag
- Customer Rating

Categorical Variable:

- Store Type (converted into dummy variables)

---

# 4. Regression Approach

Two regression models were developed.

## Simple Regression

Dependent Variable:
- Monthly Sales

Independent Variable:
- Marketing Spend

Purpose:
To understand the relationship between marketing investment and monthly sales.

### Results

- R² = **0.1672**
- Marketing Spend has a positive and statistically significant relationship with Monthly Sales.

---

## Multiple Regression

Dependent Variable:
- Monthly Sales

Independent Variables:

- Marketing Spend
- Footfall
- Average Discount Percentage
- Staff Count
- Inventory Availability Percentage
- Competitor Distance
- Holiday Flag
- Customer Rating

### Results

- R² = **0.8285**
- Adjusted R² = **0.8241**
- Standard Error = **43526.8**

The multiple regression model explains approximately 82.85% of the variation in monthly sales.

---

# 5. Dummy Variable Approach

The categorical variable **Store Type** was converted into dummy variables.

Created dummy variables:

- Store_Residential
- Store_HighStreet
- Store_Airport

Reference category:

- **Mall**

The reference category was excluded to avoid the dummy variable trap (perfect multicollinearity).

---

# 6. Model Comparison Summary

| Metric | Simple Regression | Multiple Regression |
|---------------------|----------------|----------------|
| R Square | 0.1672 | 0.8285 |
| Adjusted R Square | 0.1646 | 0.8241 |
| Standard Error | 94846.03 | 43526.80 |
| Observations | 320 | 320 |

### Summary

The multiple regression model provides significantly better explanatory power and prediction accuracy than the simple regression model.

---

# 7. Final Model Selected

**Multiple Linear Regression**

Reasons:

- Higher R² value (0.8285)
- Lower prediction error
- Includes multiple business drivers instead of only marketing spend
- Provides better support for business decision-making

---

# 8. Business Recommendation

Leadership should focus on:

- Increasing customer footfall
- Investing in effective marketing campaigns
- Maintaining high inventory availability
- Optimizing staffing levels
- Improving customer satisfaction

Discount strategies should be carefully evaluated, and competitor distance should not be interpreted as a direct business lever.

The multiple regression model should be used as the primary analytical model for future sales planning and forecasting.

---

# 9. Assumptions and Limitations

### Assumptions

- Linear relationship between variables
- Independent observations
- Accurate and complete dataset
- Consistent business conditions across observations

### Limitations

- External factors such as local events and economic conditions are not included.
- Regression identifies association but does not prove causation.
- Some stores have large residuals, suggesting additional business variables may improve prediction accuracy.
- Results depend on the quality of the available data.

---

# 10. Screenshots Included

The project includes the following screenshots:

- cleaning_preview.png
- dummy_variables_preview.png
- simple_regression_output.png
- multiple_regression_output.png
- model_comparison_preview.png
- residuals_preview.png

These screenshots provide evidence of data preparation, regression outputs, model comparison, and residual analysis.

Simple regression
<img width="874" height="281" alt="simple_regression_output" src="https://github.com/user-attachments/assets/d8319fd2-034b-46aa-9d2f-e4e680a03fc8" />

Multiple regression
<img width="668" height="305" alt="multiple_regression_output" src="https://github.com/user-attachments/assets/0dcc177c-946a-4873-a505-23e6a7ecc871" />

Model comparsion
<img width="320" height="285" alt="model_comparison_preview" src="https://github.com/user-attachments/assets/8e9a0d46-60bf-47ec-a4c3-cd66a54cfb22" />

Residuals
<img width="632" height="301" alt="residuals_preview" src="https://github.com/user-attachments/assets/ee3e6680-cb77-4b40-ad15-3a5e01e81d8a" />



