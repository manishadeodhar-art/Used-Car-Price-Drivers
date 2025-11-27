# 📑 Used Car Price Prediction Report
**Prepared for:** Dealer Network Partners  
**Objective:** Fine-tune inventory decisions using data-driven insights from Ridge and Lasso regression models.

---

## 1. Executive Summary
We analyzed historical used car listings to identify the key drivers of vehicle resale value. Two predictive models were tested: **Ridge Regression** and **Lasso Regression**.  

- **Lasso Regression emerged as the stronger model**, offering both higher accuracy and clearer insights into which vehicle attributes most influence price.  
- These findings can help dealers **prioritize inventory acquisition, pricing strategies, and marketing focus**.

---

## 2. Model Performance

| Metric              | Ridge Regression | Lasso Regression |
|---------------------|-----------------|-----------------|
| **Best α (alpha)** | 0.01            | 0.0001          |
| **Test MAE**       | $5,293.14       | $4,211.06       |
| **Test R²**        | 0.64            | 0.76            |

**Interpretation:**  
- Lasso predictions are **closer to actual prices** (lower MAE).  
- Lasso explains **more of the price variation** (higher R²).  
- Ridge is acceptable but less effective for actionable insights.

---

## 3. Key Drivers of Price (from Lasso Model)

### 🚗 Positive Influences (increase resale value)
- **Vehicle Age²** → Older vehicles with certain nonlinear effects can command higher prices in niche markets.  
- **Body Types:** Offroad, convertible, truck, pickup, coupe.  
- **Mileage² (odometer²):** Certain mileage patterns can positively influence perceived value.  

### ⚠️ Negative Influences (decrease resale value)
- **Title Issues:** Salvage, rebuilt, lien, missing, or “parts only” titles sharply reduce resale value.  
- **Fuel Types:** Gas, electric, hybrid, and “other” categories showed lower resale values compared to baseline.  
- **Paint Colors:** Purple, brown, blue, green, silver, and red tend to reduce resale value.  
- **Drive Types:** FWD and RWD vehicles are less valuable compared to AWD.  
- **Body Styles:** Sedans and hatchbacks underperform compared to trucks, SUVs, and specialty vehicles.  

---

## 4. Recommendations for Dealers

- **Inventory Acquisition:**  
  - Prioritize **trucks, pickups, convertibles, and offroad vehicles**.  
  - Avoid vehicles with **title issues** or less desirable paint colors.  

- **Pricing Strategy:**  
  - Adjust pricing downward for vehicles with negative attributes (e.g., salvage titles, unpopular colors).  
  - Highlight positive attributes in marketing (e.g., specialty body types).  

- **Marketing Focus:**  
  - Promote vehicles with **high-demand body styles** and emphasize clean titles.  
  - Consider offering incentives for less desirable inventory (e.g., sedans with salvage titles).  

---

## 5. Visualizations

To make these findings more actionable, the following charts are included:

- **Model Performance Comparison:**  
  - Bar charts comparing Ridge vs. Lasso on **MAE** and **R²**.  

- **Feature Importance (Lasso):**  
  - Horizontal bar chart of the **Top 10 Positive Coefficients** (features that increase resale value).  
  - Horizontal bar chart of the **Top 10 Negative Coefficients** (features that decrease resale value).  
  - Optional: Highlight **Top 3 Positive and Negative Drivers** for a concise view.  

These visualizations provide a clear, stakeholder-ready narrative of which attributes add value and which reduce it.

---

## 6. Interactive Notebook

For full analysis, code, and reproducible workflows, see the Jupyter notebook:  
👉 [Used Car Price Drivers – Analysis Notebook](https://github.com/manishadeodhar-art/Used-Car-Price-Drivers/blob/main/prompt_II.ipynb)

---

## 7. Conclusion
The **Lasso Regression model** provides a reliable, interpretable framework for predicting used car prices. Dealers can use these insights to **fine-tune inventory selection, optimize pricing, and improve profitability**.  

By focusing on the attributes that most strongly influence resale value, your dealership network can make **smarter, data-driven decisions** in a competitive market.
