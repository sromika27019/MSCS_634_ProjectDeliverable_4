# MSCS_634_ProjectDeliverable_4

## Project Overview  
I developed an IoT-driven system to help small-scale farmers optimize irrigation and fertilizer use by predicting crop yield and uncovering actionable patterns from field sensor data.

## Dataset  
- **Source:** `fieldsensor.csv`  
- **Contents:** Hourly readings of soil moisture, ambient temperature, soil pH, plot identifiers, timestamps, and measured crop yield.  
- **Why I chose it:** It provides the temporal and environmental variables needed to model and explain variations in yield.

## Project Steps  
1. **Data Loading & Cleaning**  
   - Removed invalid soil moisture readings (≤ 0)  
   - Forward-filled missing sensor values  
2. **Feature Engineering**  
   - Computed a 24-hour rolling average of soil moisture per plot  
3. **Exploratory Data Analysis**  
   - Correlation heatmap to identify relationships among soil moisture, temperature, pH, and yield  
4. **Modeling**  
   - **Regression (Random Forest):** Predicted continuous crop yield  
   - **Classification (Logistic Regression):** Separated high- vs. low-yield conditions  
   - **Clustering (K-Means):** Grouped field observations into three condition clusters  
   - **Association Rules (Apriori):** Extracted “high temperature” ↔ “low moisture” patterns  
5. **Interpretation & Visualization**  
   - Plotted feature importances, ROC/accuracy metrics, cluster scatter plots, and rule tables  
6. **Recommendations & Ethics**  
   - Proposed real-time alerts, automated irrigation triggers, and temperature-mitigation strategies  
   - Discussed data privacy, sampling bias, and reproducibility safeguards

## Major Findings  
- **Top Predictor:** 24-hour rolling soil moisture explained ≈ 45 % of yield variance (R² ≈ 0.72, MAE = 3.5).  
- **Classification Accuracy:** 81 % accuracy distinguishing high vs. low yield conditions.  
- **Clusters Identified:**  
  1. Moderate moisture/temperature (“baseline”)  
  2. High moisture/low-moderate temperature (“optimal”)  
  3. Low moisture/high temperature (“stress”)  
- **Key Rule:** High temperatures often coincide with adequate moisture (support = 0.12, confidence = 0.75), reflecting controlled irrigation.

---


