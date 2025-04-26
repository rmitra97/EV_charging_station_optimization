**🚗🔋 EV Charging Station Optimization**

_By: Rashmila Mitra, Zeel Shah, Arjun Lamba (March 2025)_





**🧠 Executive Summary**
As electric vehicle (EV) adoption grows rapidly, optimizing charging station placement and pricing becomes critical for operational efficiency and user convenience.


1. This project leverages machine learning techniques to:
2. Strategically optimize station placement using geospatial clustering and Integer Linear Programming (ILP).
3. Predict station demand using classification models.
4. Develop dynamic pricing models that maximize revenue based on demand elasticity across cities.

Our analyses highlighted demand variations, optimized station coverage, and city-specific pricing strategies to enhance EV adoption and infrastructure scalability.


**🗺 Dataset**
**Sourced from Kaggle:** 5,000 EV charging stations across global locations.


**Features included:**
1. Location: latitude, longitude, distance from city centers.
2. Station details: charger type, capacity, availability, parking spots, maintenance logs.
3. Usage patterns: average users/day, cost per kWh, customer satisfaction scores.


**After data cleaning:**
1. Removed 500 invalid city entries.
2. Removed 730 water-based locations using shapefiles.
3. Final dataset: 3,770 valid EV stations.



## 🔍 Project Workflow

| Step | Description |
|:---|:---|
| **EDA** | Summary statistics, feature correlation, usage distributions |
| **Station Clustering** | KMeans clustering (optimal k = 15), cluster-city mapping |
| **Placement Optimization** | ILP to place 45 new stations, with constraints on demand zones |
| **Demand Prediction** | Random Forest Classifier (51.3% accuracy) for cluster-based demand |
| **Pricing Optimization** | Demand-based dynamic pricing model using revenue maximization |
| **Validation** | Geospatial heatmaps, pricing error analysis, demand cluster accuracy |



Validation	Geospatial heatmaps, pricing error analysis, demand cluster accuracy




**📈 Key Results**
1. Optimal k = 15 clusters identified for city-level segmentation.
2. ILP Optimization successfully placed 45 new stations across 15 cities (max 3 per city).
3. Random Forest Classifier achieved:
      Accuracy: 51.3%
      Mean Absolute Error (MAE): 2.12
4. Global Optimal Charging Price: ~$0.33/kWh balancing affordability and revenue.
5. City-Specific Insights:
     - Mumbai had the highest optimal price ($0.50/kWh).
     - Beijing had the lowest optimal price ($0.25/kWh).



**⚡ Challenges Faced**
1. Initial models (Linear Regression, XGBoost) showed poor accuracy.
2. Tradeoff between:
    - 5 clusters (high model accuracy but poor city-level granularity).
    - 15 clusters (lower accuracy but better real-world segmentation).
    - Data loss after removing water points slightly impacted final model performance.


**🔮 Future Scope**
1. Enhance Demand Prediction: Integrate hybrid models combining Random Forest with boosting or deep learning.
2. Dynamic Pricing Models: Adapt prices based on seasonal, hourly, and competitor-driven demand shifts.
3. Geospatial Optimization:Incorporate real-time traffic density and energy grid data for smarter placement.

