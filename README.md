# Yulu - Hypothesis Testing & Customer Acquisition Analysis

## 📚 Overview

This project analyzes Yulu's electric scooter delivery business using hypothesis testing techniques. The analysis focuses on understanding customer acquisition patterns, retention rates, and building predictive models for membership upgrades using statistical inference methods.

---

### **Business Problem**

- Determine if customers upgrade to paid memberships based on historical behavior
- Test hypotheses about customer churn using statistical significance
- Identify factors influencing membership decisions with rigorous testing

---

### **Analysis Approach**

**Key Insights:**
- 📊 **Dataset**: 305 records covering 4 months (76 scooters × 4 months)
- 🔍 **Variables Analyzed**: 
  - Customer churn status (0 = not churn, 1 = churned)
  - Monthly charges for billing analysis
  - Tenure to assess customer lifetime value
- 🎯 **Objective**: Test hypotheses about membership upgrade drivers using statistical methods

---

### **Methodology Highlights**

| Aspect | Analysis | Result |
|--------|----------|--------|
| Sample Size | 305 records | Hypothesis testing sample |
| Method | Statistical inference + hypothesis testing | Significance testing |
| Variables | Churn status, monthly charges, tenure | Multi-variable analysis |

---

### **Strategic Recommendations**

✅ **Hypothesis Testing**: Apply statistical methods to validate business assumptions  
✅ **Churn Prediction**: Build models to predict which customers will upgrade or churn  
✅ **Retention Strategy**: Focus efforts on high-value customers based on statistical analysis  

---

### **Technical Implementation**

```python
# Hypothesis testing for customer retention
import pandas as pd
from scipy import stats

def test_churn_hypothesis(df):
    # Calculate descriptive statistics
    mean_monthly_charge = df['Monthly_Charges'].mean()
    
    # Test hypotheses about churn probability
    z_stat, p_value = stats.ztest([0, 1], loc=0.5)
    
    return {
        'churn_probability': (df['Churn'] == 1).sum() / len(df),
        'monthly_charge_mean': mean_monthly_charge
    }
```

---

### **Business Impact**

Hypothesis testing enables Yulu to:
- Make statistically significant decisions about customer retention strategies
- Validate marketing hypotheses before implementing campaigns
- Optimize resource allocation based on statistical evidence rather than intuition

---

*By Rahul Sharma | Senior Business Analyst with expertise in hypothesis testing and predictive analytics*
