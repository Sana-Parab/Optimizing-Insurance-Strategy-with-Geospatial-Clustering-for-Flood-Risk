# Optimizing-Insurance-Strategy-with-Geospatial-Clustering-for-Flood-Risk

Leveraged clustering techniques and geospatial analytics to evaluate flood exposure and improve insurance coverage strategies. Integrated Precisely's Geoaddressing and FloodRisk APIs to geocode properties, assess proximity to flood zones, and identify underinsured properties. _Properties were grouped into risk-based clusters to support more accurate underwriting, strategic premium adjustments, and targeted upsell initiatives._

📍 **Project Context – Montpelier, VT**
This project focuses on evaluating flood risk across Montpelier, Vermont, using a combination of geospatial intelligence, property attributes, and risk assessment models. The objective was to enable insurers to identify coverage gaps and fine-tune pricing strategies for flood-prone properties.

🎯 **Highlights & Insights**
Flood Context: The severe floods of 2023 and 2024 emphasized the urgent need for enhanced flood risk modeling and insurance preparedness.
Geospatial Analysis: Utilized Precisely’s APIs to obtain accurate flood zone data and property-level geocoding.
Clustering Strategy: Employed K-Means to classify over 10,000+ properties into five distinct flood risk categories.
Insurance Gaps: Conducted Insurance-to-Value (ITV) analysis to surface underinsured properties based on a threshold of <80%.
Business Impact: Supported more precise policy pricing, reduced exposure through better coverage recommendations, and uncovered upsell potential in high-risk areas.

🔄 **Project Workflow**
1. _Data Collection & Enrichment_
Dataset: 10,311 property records from Address Fabric.
Standardization: Cleaned and validated address data via Geoaddressing API.
Flood Enrichment: Fetched flood zone classifications using FloodRisk API.
Final Dataset: 10,170 usable property entries post-validation.

2. _Data Cleaning & Validation_
Removed duplicates via unique property key (PBKEY) checks.
Ensured geographic and ZIP code accuracy.
Verified structural and market value attributes for modeling reliability.

3. _Risk Clustering & Feature Engineering_
Key Variables: Distance to 100-year flood zones, elevation, construction type, and market value.
Reduced dimensionality using PCA.
Applied K-Means clustering to derive five meaningful risk segments.

4. _Risk Segmentation Output_
Cluster 1: Low risk – high elevation, minimal flood exposure.
Cluster 2: Low-moderate risk – structurally sound, moderate proximity.
Cluster 3: Moderate risk – near riverbanks.
Cluster 4: Moderate-high risk – adjacent to high-risk flood zones.
Cluster 5: High risk – situated within FEMA AE zones.

5. _Underinsurance Detection_
Calculated ITV = Policy Value / Assessed Value.
Properties with ratios under 80% flagged as underinsured.
Highlighted potential for premium adjustments and coverage expansion.

📊 **Impact on Insurance Strategy**

_Underwriting Accuracy_: Better segmentation allows for refined pricing based on risk exposure.
_Revenue Growth_: Identified upsell opportunities through ITV analysis and policy gaps.
_Risk Sharing & Resilience_: Insights support community-level planning and reinsurance partnerships.


🧠 **Skills & Tools**
_Data Science & ML_: pandas, numpy, sklearn, scipy.stats, matplotlib, seaborn
_Geospatial Tools_: Precisely Geoaddressing & FloodRisk APIs
_Clustering & Feature Reduction_: K-Means, Principal Component Analysis (PCA)
_Insurance Analytics_: Insurance-to-Value (ITV), FEMA zone risk classification

**Presentation Link** - https://precisely-flood-risk-mitigation.my.canva.site/
