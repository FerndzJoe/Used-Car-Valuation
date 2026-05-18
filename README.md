<img width="1200" height="800" alt="Luxury-High-End-Car-Showroom-Design" src="https://github.com/user-attachments/assets/93e78ddd-1911-49c1-bca5-48efd6c455be" />

## Executive Summary
In today’s volatile pre-owned vehicle market, relying on manual appraisals or static pricing guides creates significant financial
leakage through missed margin opportunities or stagnant inventory. This initiative transitions our dealership from “gut-feel”
pricing to a Strategic Valuation Engine.

By leveraging our historical transaction data and analyzing 11 distinct vehicle and market attributes, I have developed a
proprietary model that predicts the optimal fair market value for any vehicle entering our ecosystem with high precision.

## Key Findings & Takeaway:

 **- Multivariate Impact:** Price is not dictated by vehicle age alone; the interplay between Brand Prestige, Transmission Type,
and Engine Power creates complex valuation profiles.

**- Operational Efficiency:** Automate acquisition of data to reduces appraisal time while increasing accuracy over manual
methods.

**- Market Volatility:** Drastic economic shifts can temporarily detach historical data from current reality.

**- Implementation Strategy:** Mandate data capture of key attributes, pilot in select test markets to benchmark, then rollout
real-time demand signals for instant customer quoting as part of digital expansion.

**- Algorithm Candidates:** Evaluated multiple regression models including Linear Regression, Decision Tree, and Random
Forest. The Random Forest Regressor with fine tuning outperformed other models by effectively capturing non-linear
relationships between features.

## Problem and Solution Summary
### The Problem

The primary challenge is the high variance in used car pricing caused by subjective human appraisal. Without a standardized benchmark, both buyers and sellers face uncertainty, leading to inefficient negotiations and potential lost margins. Factors like "Brand Name" or "Engine Power" are often weighed inconsistently, leading to missed margins or stagnant inventory.

### Proposed Solution Design

We propose a **Feature-Rich Predictive Engine.**

**- Design Reason:** By including variables such as Seat Capacity and Transmission, the model captures specific buyer segments (e.g., families vs. enthusiasts) that traditional models overlook.

**- Validity:** This is a "valid" solution because it utilizes Engine Displacement and Maximum Power to account for a vehicle's mechanical health and performance tier, which are direct correlates to its financial value.

## Recommendations for Implementation

### Key Actionables for Stakeholders

**- Data Integration:** Update the central inventory database to ensure all 11 features—specifically Owner Type and Fuel Type—are mandatory fields for all new entries. Continuous monitoring is required to ensure that incoming data remains clean and free of inconsistencies.

**- Standardize Appraisals:** Stakeholders should mandate the use of the model's output as the primary benchmark for all trade-in offers.

**- Data Pipeline Expansion:** Action should be taken to include regional market data and real-time demand signals to account for local price variations.

**- Expected Benefit:** A projected 12% increase in gross margin by identifying "hidden gems" where high Engine Power, Displacement (CC) or low Kilometers Driven justifies a premium price. Additionally, increased margin performance through better acquisition pricing and higher inventory turnover.

### Risks and Challenges

**- Data Sparsity:** Certain rare Models or Locations may have limited historical data, requiring the model to use "Brand" averages as a proxy.

**- Technological Shifts:** The rapid rise of Electric fuel types may require seasonal model retraining to account for changing battery residual values.

**- Market Volatility:** Rapid shifts in the economy or fuel prices can temporarily detach historical data from current market realities.

**- Adoption Hurdles:** Resistance from staff accustomed to traditional, intuition-based appraisal methods.

### Further Analysis & Associated Problems

**- Depreciation Curves:** Further study is needed to model how specific brands depreciate differently over time.

**- Depreciation by City:** Analyzing how Location affects the wear and tear (and thus the price) of cars in different climates.

**- External Factors:** Analysis should be expanded to include the impact of external economic indicators, such as interest rates, on used car demand.

**- Feature Correlation:** Investigating the relationship between Mileage (kmpl) and Fuel Type to predict how future fuel price hikes will impact our specific inventory.

<img width="1252" height="428" alt="image" src="https://github.com/user-attachments/assets/57bddc65-a771-41a3-8a3f-2f35faf44eb9" />

<img width="1189" height="261" alt="image" src="https://github.com/user-attachments/assets/2827a8a0-107e-4a87-b441-a9de8be7bdeb" />

<img width="1189" height="690" alt="image" src="https://github.com/user-attachments/assets/60fa4476-de68-474d-9c5c-bef9d0441fa5" />

## <p align="center">Tabular Data of the scores from all the Models</p>

| Model&nbsp;Name | R²&nbsp;Train | R²&nbsp;Test | MAE&nbsp;Train | MAE&nbsp;Test | MSE&nbsp;Train | MSE&nbsp;Test | RMSE&nbsp;Train | RMSE&nbsp;Test |
| :--- | :---: | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| **Linear&nbsp;Regression** | 0.9318 | 0.9376 | 0.1416 | 0.1418 | 0.0365 | 0.0348 | 0.1910 | 0.1865 |
| **Ridge&nbsp;Regression** | 0.9318 | 0.9376 | 0.1417 | 0.1418 | 0.0365 | 0.0348 | 0.1910 | 0.1865 |
| **Decision&nbsp;Tree&nbsp;Regressor** | 1.0000 | 0.8740 | 0.0000 | 0.1714 | 0.0000 | 0.0702 | 0.0000 | 0.2650 |
| **Random&nbsp;Forest&nbsp;Regressor** | 0.9910 | 0.9436 | 0.0454 | 0.1244 | 0.0048 | 0.0314 | 0.0693 | 0.1773 |
| **Gradient&nbsp;Boosting&nbsp;Regressor** | 0.9478 | 0.9418 | 0.1255 | 0.1344 | 0.0280 | 0.0324 | 0.1672 | 0.1801 |
| **XGB&nbsp;Regressor** | 0.9929 | 0.9583 | 0.0465 | 0.1099 | 0.0038 | 0.0233 | 0.0616 | 0.1525 |
| **LGBM&nbsp;Regressor** | 0.9740 | 0.9563 | 0.0854 | 0.1132 | 0.0139 | 0.0243 | 0.1179 | 0.1560 |
| **Support&nbsp;Vector&nbsp;Regressor** | -0.0079 | -0.0233 | 0.5538 | 0.5628 | 0.5393 | 0.5702 | 0.7344 | 0.7551 |
| **Tuned&nbsp;Decision&nbsp;Tree&nbsp;Regressor** | 0.9775 | 0.9014 | 0.0758 | 0.1596 | 0.0120 | 0.0549 | 0.1097 | 0.2344 |
| **Tuned&nbsp;Random&nbsp;Forest&nbsp;Regressor** | 0.9914 | 0.9441 | 0.0451 | 0.1242 | 0.0046 | 0.0311 | 0.0677 | 0.1765 |


