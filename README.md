# Telco Customer Churn Analysis Project  
![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange?logo=jupyter) ![Python](https://img.shields.io/badge/Python-3.8-blue?logo=python) ![Pandas](https://img.shields.io/badge/Pandas-Data%20Analysis-blue) ![Plotly](https://img.shields.io/badge/Plotly-Interactive-green)

Welcome to the **Telco Customer Churn Analysis Project**! This Jupyter Notebook project explores customer churn data from a fictional telecommunications company in California, modeled on an IBM dataset. The analysis transforms raw data into actionable insights about customer behavior and retention.

---

## 📚 Table of Contents

- [Introduction](#introduction)
- [Data Overview](#data-overview)
- [Analysis & Methods](#analysis--methods)
- [Key Findings](#key-findings)
- [Conclusions & Recommendations](#conclusions--recommendations)
- [Further Research](#further-research)
- [Usage](#usage)
- [Data Sources](#data-sources)
- [Credits](#credits)
- [License](#license)

---

## Introduction

This project analyzes customer churn for a telco company that provided home phone and Internet services to **7,043 customers in California**.  
**Main Objectives:**  
- Identify reasons behind subscription cancellations.  
- Determine when churn occurs most frequently.  
- Analyze the impact of billing, contract type, and other factors on customer retention.  
- Use statistical methods (e.g., correlation matrices, chi-square tests) and interactive visualizations to draw insights.

---

## Data Overview

The dataset, **Telco_customer_churn.xlsx**, comprises 33 variables over 7,043 observations including:  
 **CustomerID:** A unique ID that identifies each customer.

**Count:** A value used in reporting/dashboarding to sum up the number of customers in a filtered set.

**Country:** The country of the customer’s primary residence.

**State:** The state of the customer’s primary residence.

**City:** The city of the customer’s primary residence.

**Zip Code:** The zip code of the customer’s primary residence.

**Lat Long:** The combined latitude and longitude of the customer’s primary residence.

**Latitude:** The latitude of the customer’s primary residence.

**Longitude:** The longitude of the customer’s primary residence.

**Gender:** The customer’s gender: Male, Female

**Senior Citizen:** Indicates if the customer is 65 or older: Yes, No

**Partner:** Indicate if the customer has a partner: Yes, No

**Dependents:** Indicates if the customer lives with any dependents: Yes, No. Dependents could be children, parents, grandparents, etc.

**Tenure Months:** Indicates the total amount of months that the customer has been with the company by the end of the quarter specified above.

**Phone Service:** Indicates if the customer subscribes to home phone service with the company: Yes, No

**Multiple Lines:** Indicates if the customer subscribes to multiple telephone lines with the company: Yes, No

**Internet Service:** Indicates if the customer subscribes to Internet service with the company: No, DSL, Fiber Optic, Cable.

**Online Security:** Indicates if the customer subscribes to an additional online security service provided by the company: Yes, No

**Online Backup:** Indicates if the customer subscribes to an additional online backup service provided by the company: Yes, No

**Device Protection:** Indicates if the customer subscribes to an additional device protection plan for their Internet equipment provided by the company: Yes, No

**Tech Support:** Indicates if the customer subscribes to an additional technical support plan from the company with reduced wait times: Yes, No

**Streaming TV:** Indicates if the customer uses their Internet service to stream television programing from a third party provider: Yes, No. The company does not charge an additional fee for this service.

**Streaming Movies:** Indicates if the customer uses their Internet service to stream movies from a third party provider: Yes, No. The company does not charge an additional fee for this service.

**Contract:** Indicates the customer’s current contract type: Month-to-Month, One Year, Two Year.

**Paperless Billing:** Indicates if the customer has chosen paperless billing: Yes, No

**Payment Method:** Indicates how the customer pays their bill: Bank Withdrawal, Credit Card, Mailed Check

**Monthly Charge:** Indicates the customer’s current total monthly charge for all their services from the company.

**Total Charges:** Indicates the customer’s total charges, calculated to the end of the quarter specified above.

**Churn Label:** Yes = the customer left the company this quarter. No = the customer remained with the company. Directly related to Churn Value.

**Churn Value:** 1 = the customer left the company this quarter. 0 = the customer remained with the company. Directly related to Churn Label.

**Churn Score:** A value from 0-100 that is calculated using the predictive tool IBM SPSS Modeler. The model incorporates multiple factors known to cause churn. The higher the score, the more likely the customer will churn.

**CLTV:** Customer Lifetime Value. A predicted CLTV is calculated using corporate formulas and existing data. The higher the value, the more valuable the customer. High value customers should be monitored for churn.

**Churn Reason:** A customer’s specific reason for leaving the company. Directly related to Churn Category.

---

## Analysis & Methods

The notebook uses powerful Python libraries to perform a comprehensive analysis:  

```python
import pandas as pd
import numpy as np
from matplotlib import pyplot as plt
import seaborn as sns
import plotly.express as px
import scipy.stats as stats
import statsmodels.api as sm
%matplotlib inline
```

**Key Steps:**  
- **Data Cleaning & Preprocessing:**  
  Removing irrelevant columns, handling missing values, and converting data types.
- **Exploratory Data Analysis (EDA):**  
  Visualizations (heatmaps, scatter plots, histograms) to understand distributions and detect missing data.
- **Statistical Testing:**  
  Chi-square tests and ANOVA to examine relationships between churn reasons and contract types.
- **Interactive Mapping:**  
  Plotly is used to visualize geographic trends in churn based on customer location and contract details.

---

## Key Findings

- **Churn Drivers:**  
  The primary reasons for cancellation include support issues, competitive offers (better speeds, more data), and pricing concerns.
- **Timing:**  
  A significant number of cancellations occur within the first month of a month-to-month contract.
- **Billing Impact:**  
  Monthly charges have a modest positive correlation with customer tenure, though they explain only a fraction of the variability.
- **Contract Types:**  
  Longer-term contracts (One Year, Two Year) show lower churn rates compared to month-to-month subscriptions.

---

## Conclusions & Recommendations

The analysis provides strong evidence that addressing early churn drivers—such as improving customer support and revising contract terms—could significantly improve customer retention. Tailored interventions could potentially convert early churn into long-term engagement, thereby increasing overall customer lifetime value (CLTV).

---

## Further Research

Future directions include:  
- **Predictive Modeling:**  
  Develop a machine learning model to predict churn risk and identify key contributing factors.
- **Customer Segmentation:**  
  Cluster customers by demographics and behavior for personalized retention strategies.
- **Temporal Analysis:**  
  Incorporate longer-term data to monitor churn trends over time.
- **Data Enrichment:**  
  Integrate additional data sources (customer feedback, market trends) for deeper insights.

---

## Usage

### Prerequisites
- Python 3.8+
- Jupyter Notebook

### Installation & Setup

1. **Clone the Repository:**
   ```bash
   git clone https://github.com/Sabdikay/Telco-Customer-Churn-Analysis-IBM-Dataset.git
   cd customer-churn-IBM-dataset
   ```
2. **Install Dependencies:**
   ```bash
   pip install pandas numpy matplotlib seaborn plotly scipy statsmodels
   ```
3. **Launch the Notebook:**
   ```bash
   jupyter notebook
   ```
4. **Open and run `customer-churn-IBM-dataset.ipynb` to explore the analysis.**

---

## Data Sources

- **Telco_customer_churn.xlsx** provided by IBM  
  [IBM Telco Customer Churn Data]([https://community.ibm.com/accelerators/?context=analytics&query=telco%20churn&type=Data&product=Cognos%20Analytics](https://community.ibm.com/community/user/businessanalytics/blogs/steven-macko/2019/07/11/telco-customer-churn-1113))

---

## Credits

**Project Developed by:**  
**Alnur Nurumov**

*Inspired by real-world datasets and advanced analytics methodologies.*

---

## License

This project is licensed under the [MIT License](LICENSE).

---

Feel free to explore, contribute, and share your thoughts on this project. Let's drive insights from data together!  
🚀📊✨
