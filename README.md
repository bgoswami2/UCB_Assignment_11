# Used Car Price Analysis - What Drives the Price of a Car?

## Executive Summary

This project analyzes 426,000 used car listings to identify the key factors that drive vehicle prices. Using the CRISP-DM methodology and multiple regression models, we developed a predictive model to help used car dealerships optimize their inventory and pricing strategies.

## Business Problem

**Client:** Used Car Dealership  
**Objective:** Understand what factors make a car more or less expensive to optimize inventory selection and pricing strategy for maximum profitability.

## Key Findings

### Primary Price Drivers (Ranked by Impact)

1. **Vehicle Age (Year)** - HIGHEST IMPACT
   - Newer vehicles command significantly higher prices
   - Optimal range: 0-5 years old
   - Price depreciation accelerates after 10 years

2. **Mileage (Odometer Reading)** - HIGHEST IMPACT
   - Lower mileage directly correlates with higher prices
   - Sweet spot: Under 75,000 miles
   - Significant price drop above 150,000 miles

3. **Manufacturer/Brand** - MEDIUM-HIGH IMPACT
   - Premium brands retain value better
   - Brand reputation significantly affects pricing
   - Top value-retaining brands identified

4. **Vehicle Condition** - MEDIUM IMPACT
   - "Excellent" and "Like New" condition vehicles command 20-30% premium
   - Reconditioning investments show high ROI

5. **Transmission Type** - MEDIUM IMPACT
   - Automatic transmission preferred and adds value
   - Manual transmission limited to specialty markets

6. **Fuel Type** - MEDIUM IMPACT
   - Gas and hybrid vehicles show strongest demand
   - Electric vehicle market emerging but still niche

7. **Drive Train** - MEDIUM IMPACT
   - AWD/4WD commands premium in certain markets
   - Regional preferences vary significantly

## Methodology

### CRISP-DM Framework Applied

1. **Business Understanding**
   - Defined as a supervised regression problem
   - Target variable: Vehicle price
   - Goal: Identify and quantify feature impact on price

2. **Data Understanding**
   - Dataset: 426,880 used car listings
   - Features: 18 variables including year, mileage, manufacturer, condition, etc.
   - Extensive exploratory data analysis (EDA)
   - Missing value analysis
   - Correlation analysis

3. **Data Preparation**
   - Removed duplicates and outliers
   - Handled missing values (imputation and dropping)
   - Feature engineering (age, log transformations)
   - Created categorical age groups
   - Reduced high-cardinality features (top N categories)
   - Train-test split (80-20)
   - Standardization and one-hot encoding

4. **Modeling**
   - Multiple regression models tested:
     - Linear Regression (baseline)
     - Ridge Regression
     - Lasso Regression
     - Random Forest Regressor
     - Gradient Boosting (via hyperparameter tuning)
   - Cross-validation (5-fold CV)
   - Grid search for hyperparameter optimization

5. **Evaluation**
   - Metrics used: R², RMSE, MAE, Cross-validation scores
   - Best model selected based on test R² score
   - Residual analysis performed
   - Feature importance analysis
   - Model interpretation for business insights

6. **Deployment**
   - Executive summary for dealership stakeholders
   - Actionable recommendations organized by priority
   - Visual summaries of price drivers
   - Implementation roadmap provided


## Actionable Recommendations

### Immediate Actions (High Impact)

1. **Focus on Optimal Age Range**
   - Priority: 0-5 year old vehicles
   - Secondary: 6-10 year old vehicles
   - Minimize inventory older than 15 years

2. **Target Optimal Mileage**
   - Premium tier: Under 30,000 miles
   - Standard tier: 30,000-75,000 miles
   - Avoid: Over 200,000 miles

3. **Invest in Reconditioning**
   - Upgrade "Good" to "Excellent" condition
   - Expected impact: $2,000-$4,000 price increase

### Strategic Recommendations

4. **Brand Portfolio Optimization**
   - Include 20-30% premium brands for higher margins
   - Balance with popular mainstream brands for volume

5. **Transmission & Drivetrain Mix**
   - Automatic transmission: 80-90% of inventory
   - AWD/4WD: Regional adjustments

6. **Fuel Type Strategy**
   - Gas: 70-75% primary inventory
   - Hybrid: 15-20% growing segment
   - Electric: 5-10% emerging market

### Pricing Strategy

7. **Dynamic Pricing**
   - Use predictive model for initial pricing
   - Adjust for local market conditions
   - Quick markdown strategy for aged inventory

### Risk Mitigation

8. **Avoid These Characteristics**
   - Vehicles older than 20 years (unless classic)
   - Extremely high mileage (>250,000 miles)
   - Salvage or rebuilt titles
   - Unknown condition ratings

## Expected Business Impact

Implementing these recommendations is projected to deliver:
- **15-25%** improvement in inventory turnover rate
- **10-15%** increase in gross profit margins
- **20-30%** reduction in aged inventory (90+ days)
- More competitive pricing and faster sales
- Better alignment with consumer preferences

## Technical Details

### Files in Repository
- `prompt_bgoswami2_11.ipynb` ([Link to Jupiter Notebook](https://github.com/bgoswami2/UCB_Assignment_11/blob/main/prompt_bgoswami2_11.ipynb)) - Main analysis notebook with complete CRISP-DM workflow
- `data/vehicles.csv` - Used car listings dataset
- `README.md` - This file


