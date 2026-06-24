# Residual Analysis

## Predicted Sales and Residuals

Residual = Actual Sales − Predicted Sales

A positive residual indicates that actual sales were higher than predicted, while a negative residual indicates that actual sales were lower than predicted.

---

## Five Largest Positive Residuals

| Marketing Spend | Footfall | Avg Discount | Staff Count | Inventory Availability | Competitor Distance | Holiday Flag | Customer Rating | Actual Sales | Predicted Sales | Residual |
|----------------|-----------|--------------|-------------|------------------------|---------------------|---------------|-----------------|--------------|-----------------|------------|
| 63582.11 | 6856 | 0.074 | 17 | 89.5 | 5.48 | 0 | 3.2 | 799046.94 | 693573.46 | 105473.48 |
| 52758.01 | 4063 | 0.057 | 12 | 91.7 | 0.92 | 0 | 3.5 | 713611.16 | 611624.25 | 101986.91 |
| 78111.97 | 6389 | 0.150 | 13 | 83.9 | 3.05 | 0 | 4.8 | 787715.51 | 686951.63 | 100763.88 |
| 78839.39 | 5150 | 0.171 | 13 | 85.8 | 7.57 | 0 | 4.3 | 735509.40 | 639182.94 | 96326.46 |
| 113736.00 | 8961 | 0.202 | 24 | 86.2 | 21.63 | 0 | 4.0 | 870937.40 | 775842.61 | 95094.79 |

### Business Interpretation

These stores performed significantly better than predicted by the regression model. The model under-predicted sales by approximately 95,000–105,000 units. Possible reasons include successful local promotions, strong customer loyalty, favorable market conditions, or other business factors that were not included in the model.

---

## Five Largest Negative Residuals

| Marketing Spend | Footfall | Avg Discount | Staff Count | Inventory Availability | Competitor Distance | Holiday Flag | Customer Rating | Actual Sales | Predicted Sales | Residual |
|----------------|-----------|--------------|-------------|------------------------|---------------------|---------------|-----------------|--------------|-----------------|------------|
| 141540.29 | 5400 | 0.013 | 12 | 87.0 | 4.26 | 0 | 4.5 | 627171.90 | 744034.83 | -116862.93 |
| 79346.10 | 9628 | 0.102 | 20 | 99.0 | 19.01 | 1 | 3.2 | 685379.08 | 798997.50 | -113618.42 |
| 56856.63 | 9431 | 0.142 | 23 | 86.9 | 4.97 | 0 | 3.4 | 658920.30 | 766724.09 | -107803.79 |
| 68600.62 | 3988 | 0.124 | 11 | 85.0 | 0.48 | 0 | 3.6 | 511844.41 | 602689.71 | -90845.30 |
| 54597.83 | 9429 | 0.188 | 21 | 83.3 | 11.71 | 0 | 4.2 | 641865.03 | 732611.05 | -90746.02 |

### Business Interpretation

These stores performed significantly worse than predicted by the model. The model over-predicted sales by approximately 90,000–117,000 units. Possible reasons include inventory shortages, operational issues, stronger local competition, lower customer demand, or temporary business disruptions that were not captured by the regression variables.

---

## Under-Prediction and Over-Prediction

Positive residuals indicate that the model under-predicted sales, meaning the stores achieved better performance than expected.

Negative residuals indicate that the model over-predicted sales, meaning the actual sales were lower than expected.

Based on the residual analysis, the prediction errors appear to be associated with individual store performance rather than a consistent pattern for a particular store type. This suggests that external factors such as local promotions, economic conditions, or management practices may influence sales but are not included in the regression model.

---

## Conclusion

The multiple regression model explains a large proportion of the variation in monthly sales (R² = 0.8285) and performs well overall. However, the residual analysis shows that some stores experience substantial prediction errors, indicating opportunities to improve the model by incorporating additional business variables such as local events, competitor promotions, and seasonal effects.
