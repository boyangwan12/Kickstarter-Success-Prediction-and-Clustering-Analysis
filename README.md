# Kickstarter Success Prediction and Clustering Analysis

## Overview
This project analyzes Kickstarter projects to predict their likelihood of success and clusters successful projects into distinct groups. By leveraging data-driven insights, the analysis helps project creators optimize their campaigns for maximum impact.

## Table of Contents
- [Overview](#overview)
- [Data Description](#data-description)
- [Key Features](#key-features)
- [Business Insights and Impacts](#business-insights-and-impacts)
- [Results](#results)
- [Future Improvements](#future-improvements)

---

## Data Description
The dataset includes Kickstarter project data such as:
- **Goal**: Funding goal normalized to USD.
- **Time to Launch**: Days between project creation and launch.
- **Campaign Duration**: Total campaign length in days.
- **Main Category**: Project category.
- **Other Features**: Indicators like `video`, `feature image`, and textual attributes.

### Preprocessing Steps
1. Removed post-launch features (e.g., `backers_count`, `pledged`) to ensure only pre-launch data is used for predictions.
2. Normalized monetary values using exchange rates for consistency.
3. Encoded categorical variables into dummy variables.
4. Transformed skewed features with log transformations to improve model accuracy.
5. Selected features using LASSO and Random Forest to enhance performance.

---

## Key Features

### 1. **Prediction of Kickstarter Project Success**
- Built classification models to predict whether a project will succeed.
- Logistic Regression was chosen for its balance of accuracy (**78.65%**) and interpretability.

### 2. **Clustering Analysis**
- Identified 3 distinct clusters among successful projects:
  1. **Premium & Ambitious Projects**: High funding goals and long campaigns.
  2. **Mid-Range Projects**: Moderate goals and shorter durations.
  3. **Small-Scale & Niche Projects**: Low funding goals and minimal campaigns.
- Used Principal Component Analysis (PCA) to reduce data dimensionality for effective clustering.

---

## Business Insights and Impacts

### Insights for Project Creators
- **Goal Setting**: Projects with realistic, well-justified goals are more likely to succeed.
- **Campaign Duration**: Longer campaigns are beneficial for ambitious projects, while shorter campaigns perform better for creative, mid-range projects.
- **Presentation Matters**: Features like videos, high-quality descriptions, and engaging visuals significantly increase the likelihood of success.

### Cluster-Specific Strategies
- **Cluster 1: Premium & Ambitious Projects**
  - Require significant upfront investment in professional design and marketing.
  - Action: Provide consultation services or premium tools to help creators refine their campaign materials.
- **Cluster 2: Mid-Range Projects**
  - Rely on compelling storytelling to connect with audiences emotionally.
  - Action: Offer storytelling workshops and narrative templates to enhance campaign engagement.
- **Cluster 3: Small-Scale & Niche Projects**
  - Focus on efficiency and leveraging free or low-cost resources.
  - Action: Create budget-friendly templates and guidance on using grassroots marketing strategies.

### Broader Impacts
- Empower creators to launch campaigns with greater confidence by offering actionable insights.
- Help crowdfunding platforms identify high-potential projects for promotion and support.
- Enhance the overall success rate of Kickstarter campaigns, benefiting both creators and the platform.

---

## Results
- **Classification Accuracy**: Logistic Regression achieved 78.65% on the test set.
- **Clustering Silhouette Score**: 0.35 for 3 clusters using PCA-reduced data.

---

## Future Improvements
- Incorporate external data (e.g., social media metrics) to improve prediction accuracy.
- Explore advanced machine learning techniques like XGBoost and deep learning models.
- Develop personalized recommendation systems for campaign optimization.
