# Clustering Analysis of VSPP Power Plants (PEA Internship Project)

##  Overview
This project analyzes **Very Small Power Producer (VSPP)** power plants that Provincial Electricity Authority (PEA) purchases electricity from.  
The goal is to use **unsupervised learning (K-Means clustering)** to group power plants by **efficiency, stability, and reliability**, and support **data-driven contract renewal decisions**.

---

##  Data Description
- **Fuel Types:** Solar, Biomass, Biogas (Biological), Trash-to-Energy  
- **Historical Data:** 36 months of monthly electricity generation (kWh)  
- **Capacity:** Contracted installed capacity (MW)  
- **Features created (per plant):**
  - `Efficiency (%)` → Actual vs. maximum potential generation  
  - `CV (%)` → Production stability (Coefficient of Variation)  
  - `Missing Rate (%)` → Percentage of months with no generation  

---

##  Methodology
1. **Data Preparation**
   - Cleaned and standardized monthly generation data
   - Handled missing values and anomalies  

2. **Feature Engineering**
   - Created 3 indicators: Efficiency, CV, Missing Rate  

3. **Standardization**
   - Scaled features for fair clustering  

4. **Clustering Analysis**
   - Applied **K-Means**  
   - Determined optimal clusters using **Elbow Method** and **Silhouette Score**  

5. **Visualization**
   - **Elbow & Silhouette Plots** → cluster validation  
   - **PCA 2D plots** → visual interpretation of clusters  

6. **Interpretation**
   - Profiled each cluster into **High-Performance, Medium, Low/Unstable** groups  
   - Provided actionable insights for contract renewal  

---

##  Results
- **Optimal clusters = 3** for all fuel types  
- **Cluster Profiles** (common pattern across all fuels):
  - **Cluster A:** High efficiency, stable →  Recommend contract renewal  
  - **Cluster B:** Medium efficiency, some fluctuation →  Conditional renewal / improvement required  
  - **Cluster C:** Low efficiency, unstable / frequent missing →  Not recommended for renewal  

---

##  Impact
- Provided PEA with a **transparent, data-driven framework** for VSPP contract renewal decisions  
- Reduced risks of renewing low-quality plants  
- Identified improvement opportunities for medium-performing plants  
- Framework can be re-used when new data is available  

---

##  Tools & Libraries
- **Python**: pandas, numpy, scikit-learn  
- **Clustering**: KMeans  
- **Visualization**: matplotlib, PCA  
- **Evaluation**: Elbow Method, Silhouette Score  

---
