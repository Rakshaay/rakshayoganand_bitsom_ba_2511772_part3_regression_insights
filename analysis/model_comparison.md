# Model Comparison

## 1. Model Names

### Model 1: Simple Linear Regression
Predicts Monthly Sales using Marketing Spend.

### Model 2: Multiple Linear Regression
Predicts Monthly Sales using multiple business factors.

---

## 2. Variables Used

### Simple Regression

**Dependent Variable**
- Monthly Sales

**Independent Variable**
- Marketing Spend

### Multiple Regression

**Dependent Variable**
- Monthly Sales

**Independent Variables**
- Marketing Spend
- Footfall
- Average Discount Percentage
- Staff Count
- Inventory Availability Percentage
- Competitor Distance
- Holiday Flag
- Customer Rating

---

## 3. R-Squared Comparison

| Model | R-Squared |
|----------|-----------|
| Simple Regression | 0.1672 |
| Multiple Regression | 0.8285 |

### Interpretation

The simple regression model explains approximately **16.72%** of the variation in monthly sales.

The multiple regression model explains approximately **82.85%** of the variation in monthly sales, making it a much stronger model.

---

## 4. Significant Variables

Variables with p-value less than 0.05 are considered statistically significant.

### Simple Regression

| Variable | P-value |
|------------|-------------|
| Marketing Spend | 2.48E-14 |

Marketing Spend is statistically significant.

### Multiple Regression

| Variable | P-value |
|-------------------------------|-------------|
| Marketing Spend | 1.67E-18 |
| Footfall | 1.12E-24 |
| Average Discount Percentage | 0.0465 |
| Staff Count | 0.0144 |
| Inventory Availability Percentage | 2.94E-10 |
| Competitor Distance | 7.56E-07 |
| Customer Rating | 0.0286 |

Holiday Flag has a p-value of approximately 0.0503, which is slightly above the 0.05 threshold and is considered marginally significant.

---

## 5. Business Usefulness

### Simple Regression

The model shows that increasing marketing spend is associated with higher monthly sales.

However, it ignores many important operational factors and therefore provides limited business insight.

### Multiple Regression

The model provides a much better understanding of the drivers of monthly sales.

It helps management evaluate the impact of:

- Marketing investment
- Customer footfall
- Discounts
- Staffing levels
- Inventory availability
- Competitor proximity
- Customer ratings

This model is more useful for business decision-making and sales forecasting.

---

## 6. Limitations

### Simple Regression

- Uses only one predictor.
- Low explanatory power.
- Ignores operational and customer-related factors.

### Multiple Regression

- Does not capture external factors such as economic conditions or seasonal events.
- Assumes a linear relationship between variables.
- Results depend on the quality and completeness of the available data.

---

# Conclusion

The multiple regression model outperforms the simple regression model.

It has a much higher R-squared value (0.8285 vs 0.1672), identifies several statistically significant business drivers, and provides stronger support for business decision-making.
