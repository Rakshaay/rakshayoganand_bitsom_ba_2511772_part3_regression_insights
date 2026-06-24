# Model Equations

## Dummy Variable Creation

Regression analysis requires numerical inputs, so categorical variables were converted into dummy variables.

### Variable Used: Store Type

The original store_type variable contained four categories:

- Residential
- High Street
- Airport
- Mall

Three dummy variables were created:

| Original Category | Store_Residential | Store_HighStreet | Store_Airport |
|-------------------|------------------|------------------|----------------|
| Residential | 1 | 0 | 0 |
| High Street | 0 | 1 | 0 |
| Airport | 0 | 0 | 1 |
| Mall (Reference Category) | 0 | 0 | 0 |

### Reference Category

**Mall** was selected as the reference category and was not included as a separate dummy variable.

Using all four categories together would create perfect multicollinearity (dummy variable trap), making the regression model unable to estimate coefficients correctly. Therefore, one category must be omitted, and all other categories are interpreted relative to the reference category.

---

# Simple Regression Model

Dependent Variable:
- Monthly Sales

Independent Variable:
- Marketing Spend

Equation:

Monthly Sales = β₀ + β₁(Marketing Spend) + ε

From the regression output:

Monthly Sales = 560777.35 + 2.1296 × Marketing Spend

where:

- β₀ = 560777.35 (Intercept)
- β₁ = 2.1296 (Marketing Spend coefficient)
- ε = Error term

---

# Multiple Regression Model

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

Equation:

Monthly Sales =
β₀
+ β₁(Marketing Spend)
+ β₂(Footfall)
+ β₃(Average Discount %)
+ β₄(Staff Count)
+ β₅(Inventory Availability %)
+ β₆(Competitor Distance)
+ β₇(Holiday Flag)
+ β₈(Customer Rating)
+ ε

Using the regression coefficients:

Monthly Sales =
95006.4
+ 1.1856(Marketing Spend)
+ 27.858(Footfall)
- 72102(Average Discount %)
+ 3084.08(Staff Count)
+ 2989.33(Inventory Availability %)
- 2890.20(Competitor Distance)
+ 12984.10(Holiday Flag)
+ 10433.90(Customer Rating)
+ ε

---

## Interpretation

- A one-unit increase in Marketing Spend is associated with an increase of approximately **1.19 units** in Monthly Sales, holding other variables constant.
- Higher Footfall, Staff Count, Inventory Availability, Holiday Flag, and Customer Rating are positively associated with Monthly Sales.
- Higher Average Discount Percentage and Competitor Distance are negatively associated with Monthly Sales.
- The reference category for Store Type is **Mall**, and the coefficients of other store types are interpreted relative to Mall stores.


# Model Equations

# 1. Simple Regression Equation

## Business Objective

The simple regression model estimates Monthly Sales based only on Marketing Spend.

### Equation

Monthly Sales = 560777.35 + (2.1296 × Marketing Spend)

### Business Interpretation

- **Intercept (560777.35):**
  If no money is spent on marketing, the model estimates baseline monthly sales of approximately **560,777**.

- **Marketing Spend Coefficient (2.1296):**
  For every one-unit increase in marketing spend, monthly sales are expected to increase by approximately **2.13 units**, assuming all other factors remain unchanged.

This indicates that marketing investment has a positive impact on store sales.

---

# 2. Multiple Regression Equation

## Business Objective

The multiple regression model estimates Monthly Sales by considering several business factors simultaneously.

### Equation

Monthly Sales =

95006.40

+ (1.18561 × Marketing Spend)

+ (27.85800 × Footfall)

− (72102.00 × Average Discount Percentage)

+ (3084.08 × Staff Count)

+ (2989.33 × Inventory Availability Percentage)

− (2890.20 × Competitor Distance)

+ (12984.10 × Holiday Flag)

+ (10433.90 × Customer Rating)

+ Error

---

# 3. Explanation of Each Coefficient

| Variable | Business Explanation |
|--------------------------------|------------------------------------------------|
| Intercept | Base monthly sales when all predictor values are zero. |
| Marketing Spend | Higher marketing investment is associated with higher monthly sales. |
| Footfall | More customer visits increase expected monthly sales. |
| Average Discount Percentage | Larger discounts reduce expected monthly sales value, possibly due to lower selling prices. |
| Staff Count | Additional staff members improve customer service and increase sales. |
| Inventory Availability Percentage | Better stock availability leads to higher sales by reducing lost opportunities. |
| Competitor Distance | Stores farther from competitors tend to have slightly lower predicted sales in this dataset. |
| Holiday Flag | Holiday periods increase expected monthly sales compared to non-holiday periods. |
| Customer Rating | Higher customer satisfaction is associated with higher monthly sales. |

---

# 4. Dummy Variables

The categorical variable **Store Type** was converted into dummy variables so that it could be used in regression analysis.

Three dummy variables were created:

- Store_Residential
- Store_HighStreet
- Store_Airport

Each dummy variable takes:

- **1** = Store belongs to that category
- **0** = Store does not belong to that category

---

# 5. Reference Category

**Mall** was selected as the reference category.

No separate dummy variable was created for Mall stores.

This avoids the dummy variable trap (perfect multicollinearity) and allows the other store types to be compared against Mall stores.

---

# 6. Final Model Selected

**Multiple Linear Regression Model**

---

# 7. Reason for Selecting the Final Model

The multiple regression model was selected because it provides a much better explanation of monthly sales performance than the simple regression model.

## Performance Comparison

| Metric | Simple Regression | Multiple Regression |
|----------------------|----------------|----------------|
| R-Squared | 0.1672 | 0.8285 |
| Adjusted R-Squared | 0.1646 | 0.8241 |
| Standard Error | 94846.03 | 43526.80 |

The multiple regression model explains approximately **82.85%** of the variation in monthly sales, while the simple regression model explains only **16.72%**.

From a business perspective, the multiple regression model provides better insights because it considers multiple operational factors including marketing investment, customer footfall, staffing levels, inventory availability, discounts, competition, holidays, and customer ratings.

These insights enable management to make better decisions regarding marketing budgets, staffing, inventory planning, pricing strategies, and overall store performance improvement.

---

# Conclusion

The multiple regression model is the preferred model because it delivers significantly higher predictive accuracy and provides actionable business insights for improving monthly sales across retail stores.
