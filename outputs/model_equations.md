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
