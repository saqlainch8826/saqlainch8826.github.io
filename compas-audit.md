### COMPAS Algorithmic Bias Audit

**Introduction**

COMPAS is a proprietary risk-assessment tool used in U.S. 
criminal-justice settings, especially by judges, probation 
officers, and correctional agencies to estimate recidivism 
risk. This project investigates whether COMPAS produces 
racially disparate error rates and unfairly labels 
defendants as high risk. The data comes from ProPublica's 
cleaned Broward County, Florida COMPAS dataset, assembled 
from court records and COMPAS screening records. False 
positive and false negative rates were computed because 
they show how often the system over- or under-predicts 
risk across racial groups.

**Key Findings**

Across 3,696 African-American defendants and 2,454 
Caucasian defendants, the false positive rate was 44.8% 
for African-American defendants and 23.5% for Caucasian 
defendants, meaning Black defendants were more often 
wrongly labeled as likely to reoffend when they did not. 
The false negative rate was 28.0% for African-American 
defendants and 47.7% for Caucasian defendants, meaning 
White defendants were more often wrongly labeled low risk 
when they later did reoffend. These two findings suggest 
that the algorithm's errors are not random; it behaves 
differently across race groups in a systematic way.

![COMPAS Misclassification Errors by Race](https://raw.githubusercontent.com/saqlainch8826/compas-bias-audit/main/compas_bias_chart.png)

*Source: ProPublica COMPAS Recidivism Dataset (2016). 
Chart computed from raw data using Python, pandas, 
and matplotlib.*

**Policy Implications**

In the real world, this bias means some defendants are 
more likely to be unfairly treated as dangerous and held 
to stricter conditions, while others may be underestimated 
and receive less scrutiny than they should. Courts and 
policymakers should not rely on a single opaque risk score 
as decisive evidence. Such tools should be permitted only 
if they pass independent public audit, their methodology 
can be challenged, and they serve only as limited inputs 
alongside human judgment. If they cannot meet those 
conditions, they should not guide sentencing or pretrial 
detention decisions.

**Full Analysis**

- [View full notebook with code and methodology](https://colab.research.google.com/drive/15heHvrtRpmre9zuDxyYwj2OqdWbpGWhj?usp=drive_link)
- [Public GitHub repository](https://github.com/saqlainch8826/compas-bias-audit)
