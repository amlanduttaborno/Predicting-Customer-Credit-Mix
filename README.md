# Predicting Customer Credit Mix - End-to-End Machine Learning Workflow

## Project Overview
This project implements a comprehensive machine learning pipeline to predict customer credit mix categories based on financial and demographic data. The goal is to help financial institutions assess credit health and provide personalized recommendations for credit improvement.

## Dataset
- **Source**: Bank customer financial data
- **Records**: Thousands of customer records with monthly snapshots
- **Target Variable**: Credit_Mix (Poor, Standard, Good)
- **Features**: 27 columns including income, debt, payment behavior, and credit history

## Project Workflow

### 1. Data Preprocessing
**Data Cleaning:**
- Handled invalid values (e.g., '24_' in Age column)
- Cleaned numerical columns containing string values with special characters
- Addressed missing values using median (numerical) and mode (categorical) imputation

**Feature Engineering:**
- Converted Credit_History_Age from string to numerical format
- Created derived features where appropriate
- Handled categorical variables through encoding:
  - One-hot encoding for Occupation, Payment patterns
  - Label encoding for Type_of_Loan and target variable

**Outlier Treatment:**
- Used IQR method to cap extreme values
- Applied consistent treatment across all numerical features

### 2. Exploratory Data Analysis (EDA)
**Comprehensive Analysis:**
- Target variable distribution analysis
- Correlation matrix of all features
- Distribution plots of key numerical features
- Boxplots showing relationship between features and credit mix
- Categorical feature analysis against target variable

**Key Insights:**
- Identified most correlated features with credit mix
- Discovered patterns in payment behavior across credit categories
- Analyzed income and debt relationships with credit health

### 3. Model Building
**Algorithms Implemented:**
1. **Logistic Regression**: Baseline classification model
2. **Random Forest**: Ensemble method with 100 trees
3. **Gradient Boosting**: Sequential boosting algorithm
4. **Support Vector Machine**: With probability calibration
5. **K-Nearest Neighbors**: Distance-based classification
6. **Naive Bayes**: Probabilistic classifier
7. **AdaBoost**: Adaptive boosting ensemble

**Data Preparation:**
- Standardized all features for model consistency
- Stratified train-test split (80-20) maintaining class distribution

### 4. Model Evaluation
**Performance Metrics:**
- Accuracy: Overall classification correctness
- Precision: Measure of exactness
- Recall: Measure of completeness
- F1-Score: Balanced measure of precision and recall
- Confusion Matrix: Detailed error analysis

**Initial Results:**
- Random Forest and Gradient Boosting showed best performance
- All models achieved reasonable accuracy (>75%)
- Identified best-performing models for further optimization

### 5. Hyperparameter Tuning
**Optimization Methods:**
- Randomized Search CV for efficient parameter exploration
- 3-fold cross-validation for robust performance estimation
- F1-score as primary optimization metric

**Tuned Models:**
- Random Forest: Optimized tree depth and sample parameters
- Gradient Boosting: Tuned learning rate and subsampling
- Logistic Regression: Optimized regularization strength

### 6. Final Model Selection
**Best Performing Model**: Optimized Random Forest
- Achieved highest F1-score on test data
- Provided good feature interpretability
- Demonstrated robust performance across credit categories

**Cross-Validation**: 5-fold CV confirmed model stability
**Feature Importance**: Identified key predictors of credit health

### 7. Actionable Insights & Recommendations
**Customer Segmentation:**
- Developed strategies for each credit mix category
- Personalized recommendations based on predictive features

**Financial Institution Guidance:**
- Early warning system for at-risk customers
- Product recommendation framework
- Credit improvement action plans

**Key Findings:**
- Monthly income and debt levels are primary predictors
- Payment behavior significantly impacts credit mix
- Credit utilization ratio is crucial for credit health

## Technical Implementation
- **Programming Language**: Python 3.9+
- **Main Libraries**: pandas, numpy, scikit-learn, matplotlib, seaborn
- **Data Processing**: Comprehensive pipeline from raw data to predictions
- **Model Deployment**: Production-ready code structure

## Business Impact
**For Customers:**
- Personalized credit improvement recommendations
- Early identification of credit issues
- Clear action plans for better credit health

**For Financial Institutions:**
- Improved risk assessment capabilities
- Targeted product recommendations
- Enhanced customer relationship management
- Data-driven decision making

## Results & Performance
- **Final Accuracy**: >80% on test data
- **Best Model**: Random Forest with tuned parameters
- **Key Predictors**: Income, debt levels, payment behavior
- **Business Value**: Actionable insights for credit management

## Future Enhancements
- Real-time prediction capabilities
- Integration with banking systems
- Advanced deep learning approaches
- Customer lifetime value predictions
- Dynamic model updating with new data
