# Credit Card Customer Churn Analysis

![CI logo](https://codeinstitute.s3.amazonaws.com/fullstack/ci_logo_small.png)

## Declaration of Academic Integrity & AI Collaboration
This project, Credit Card Customer Churn Analysis, is entirely my own original work. Artificial intelligence tools (such as GitHub Copilot and Gemini) were utilized strictly as consultative coding assistants for syntax optimization, debugging, and drafting documentation. All final code execution, data transformations, interpretations, and strategic recommendations represent my personal intellectual effort and project ownership.

## Dataset Content
- Source: Publicly available Credit Card Customer dataset.
- Description: The dataset contains demographic information, customer age, salary, credit limit, total transaction amounts, utilization ratios, and a target churn indicator (whether the customer closed their account). 

## Repository Link
GitHub Repository for Unite 1 Customer Churn Analysis https://github.com/R2822201/unite-1-credit-card-customer-churn-analysis

GitHub Repository: [Unit 1 Credit Card Customer Churn Analysis](https://github.com/R2822201/unite-1-credit-card-customer-churn-analysis)

## Project Board Link
GitHub Publicly available URL address for Unit 1 Project Board Customer Churn Analysis here: [https://github.com/users/R2822201/projects/1/views/1]
https://github.com/users/R2822201/projects/1/views/1

## Kaggle Datasets Link
Kaggle Datasets BankChurners .csv File
https://www.kaggle.com/datasets/sakshigoyal7/credit-card-customers

# Business Requirements
As a data analyst assisting a retail bank manager, this project addresses increasing customer churn in credit card services 
1. Business Requirement 1: Investigate and visualise how customer attributes (such as credit limit, transaction frequency, and total transaction amount) correlate with customer churn status.
2. Business Requirement 2: Develop analytical insights to identify customers at high risk of churning, enabling the bank to implement proactive retention strategies.

## Hypothesis and How to Validate
1. Hypothesis 1: Customers with lower total transaction counts and lower transaction amounts are significantly more likely to churn.
   - Validation Method: Visualised through distribution plots and Seaborn box plots comparing active versus churned customer activity.
2. Hypothesis 2: Higher revolving balances and lower credit limits correlate with higher attrition rates.
   - Validation Method: Evaluated using Pandas grouping statistics and correlation heatmaps.

## The Rationale to Map Business Requirements to Data Visualizations
- Business Requirement 1 Mapping: Conducted a correlation study using Pandas and generated heatmaps and scatter plots via Seaborn to inspect how features like credit limit and transaction volume relate to churn.
- Business Requirement 2 Mapping: Created comparative bar charts and descriptive statistical groupings to segment high-risk customer profiles for targeted retention.

## Analysis Techniques Used
- ETL Pipeline: Pandas and NumPy were utilized for data extraction, handling missing values, encoding categorical features, and removing outliers.
- Exploratory Data Analysis (EDA): Matplotlib and Seaborn were used to generate histograms, correlation matrices, and comparative bar charts.
- AI Tool Integration: GitHub Copilot was integrated into the IDE to suggest and optimize data-cleaning syntax. All generated code snippets were manually tested, evaluated, and verified.

## Data Visualization & Exploratory Data Analysis (EDA)
To address the core business requirements and evaluate customer attrition risk, exploratory data analysis was conducted using Python ( Matplotlib and Seaborn ). A multi-panel 2x2 visualization dashboard was generated to examine key demographic, financial, and regional indicators:

1. Overall Customer Churn Distribution (`sns.countplot`) 
   - Purpose: Evaluates overall customer exit rate versus retained customers to establish baseline class imbalance.
   - Finding: Illustrates the ratio of active cardholders versus attrited customers, providing foundational metrics for stakeholder review[cite: 17].

2. Customer Age Density Distribution (`sns.kdeplot`) 
   - Purpose: Investigates demographic risk factors by analyzing age distributions across retention status.
   - Finding: Highlights specific age brackets that exhibit higher propensities for closing credit card accounts.

3. Credit Limit vs. Churn Status (`sns.boxplot`) 
   - Purpose: Evaluates financial exposure and credit limits against customer attrition.
   - Finding: Compares median credit limits and outlier distributions between retained and churned customer segments.

4. Card Category & Churn Breakdown (`sns.countplot`) 
   - Purpose: Analyzes product tier usage (Blue, Silver, Gold, Platinum) relative to customer churn.
   - Finding: Determines whether specific card tiers experience disproportionate customer attrition rates.

## Interactive Credit Card Design & Risk Tiers URL here: https://share.gemini.google/pbE99oW8AEvK
To visually differentiate high-risk versus retained customer tiers (Gold and Silver designs), an interactive 3D tilting display was developed. 

View Interactive Demo: [Access Interactive Bank Card Demo](https://share.gemini.google/pBE99oW8AEvk)

![Credit Card Churn Risk Tiers - Gold and Silver Design](images/card_designs.png)

![image.png](attachment:image.png)

## Methodologies and Data Handling Rationale
- Data Preparation & Cleaning: Pandas and NumPy were utilized for systematic data extraction and handling missing values. Data cleaning steps were chosen to maintain dataset integrity while ensuring missing or anomalous records did not skew statistical correlations or visual distributions.
- Visualisation Rationale: Matplotlib and Seaborn were selected to generate distribution plots, correlation matrices, and scatter plots to highlight multivariate relationships and satisfy stakeholder visibility requirements.

## Data Cleaning & Preparation Rationale
To ensure data integrity and prepare the dataset for exploratory data analysis, systematic cleaning steps were performed in `02_data-cleaning.ipynb`:

1. Data Ingestion & Inspection:
   - Loaded the raw dataset (`BankChurners.csv`) using Pandas.
   - Inspected dataset shape, data types, and checked for missing values or anomalous records.

2. Handling Missing Values & Anomalies:
   - Evaluated null values across columns to ensure no critical demographic or financial metrics were skewed.
   - Cleaned and filtered rows to maintain data consistency.

3. Data Export for Analysis:
   - Exported the cleaned, analysis-ready dataset to `data/cleaned_bank_churn.csv` so that subsequent visualization and modeling notebooks can ingest standardized features seamlessly.

## Dataset & Analysis Limitations
- Dataset Constraints: The dataset reflects historical retail banking behavior and may not account for sudden macroeconomic shifts, external market shocks, or uncaptured customer satisfaction metrics.
- Methodological Limitations: Exploratory data analysis and correlation studies identify patterns and relationships, but do not establish direct causation until full predictive machine learning classification models are implemented in future iterations.
- AI Tool Constraints & Code Evaluation: Code snippets and documentation phrasing assisted by GitHub Copilot and Gemini were manually reviewed, tested, and refactored to ensure accuracy, eliminate redundant syntax, and prevent security or performance vulnerabilities.

## Exploratory Data Analysis (EDA) Results
To evaluate customer attrition risk and address core business requirements, a multi-panel exploratory visualisation dashboard was generated using Matplotlib and Seaborn:

![Exploratory Data Analysis Dashboard](images/data_visualisation_matplotlib_&_seaborn.png)

### Dashboard Breakdown & Insights:

1. Overall Customer Churn Distribution (`sns.countplot` - Top Left)
   - Purpose: Compares active cardholders versus attrited customers to gauge class imbalance.
   - Insight: Highlights the total volume of retained customers versus those who closed their accounts, establishing a clear baseline for churn rates.

2. Customer Age Density Distribution (`sns.kdeplot` - Top Right)
   - Purpose: Examines demographic vulnerability across customer age brackets.
   - Insight: Illustrates overlapping density curves that identify specific peak age ranges most prone to credit card attrition.

3. Credit Limit vs. Churn Status (`sns.boxplot` - Bottom Left)
   - Purpose: Evaluates financial exposure and median credit limits between retained and churned customers.
   - Insight: Compares spread and outliers in credit limits to determine whether card limits correlate with account cancellation.

4. Card Category & Churn Breakdown (`sns.countplot` - Bottom Right)
   - Purpose: Analyzes product tier usage (Blue, Silver, Gold, Platinum) relative to churn status.
   - Insight: Demonstrates the concentration of customer volume and attrition across different card tiers.

5. Project Board Kanban Workflow (images/project_board.png)
Figure 1: Agile project management board tracking user stories, tasks, and MoSCoW prioritization across Backlog, Todo, In Progress, and Done columns.  

## Unfixed Bugs
- No critical bugs remain in the production notebooks. Minor Pandas future-deprecation warnings regarding dataframe slicing were addressed and refactored during testing.

## Development Roadmap
- Future iterations will incorporate Scikit-learn machine learning classification models (Logistic Regression and Random Forest) to score churn probability directly.

## Main Data Analysis Libraries
- Pandas & NumPy: For data manipulation, cleaning, and numerical computations.
- Matplotlib & Seaborn: For exploratory data visualizations and correlation matrices.

## Credits
- Dataset sourced from public banking data repositories.
- Code Institute template standards and curriculum guidelines.
