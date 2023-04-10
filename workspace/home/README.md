# Prosper Loan Data Exploration
## by Sunny Ebinum


## Dataset

> Provide basic information about your dataset in this section. If you selected your own dataset, make sure you note the source of your data and summarize any data wrangling steps that you performed before you started your exploration.

The Prosper loan dataset contains 113,937 loans with 81 variables on each loan. These includes the loan amount, borrower rate (or interest rate), current loan status, borrower income, borrower occupation and many others. The dataset is available [here](https://www.google.com/url?q=https://s3.amazonaws.com/udacity-hosted-downloads/ud651/prosperLoanData.csv&sa=D&ust=1581581520570000) while the data dictionary is available [here](https://www.google.com/url?q=https://docs.google.com/spreadsheet/ccc?key%3D0AllIqIyvWZdadDd5NTlqZ1pBMHlsUjdrOTZHaVBuSlE%26usp%3Dsharing&sa=D&ust=1554486256024000).

Three numeric variables `BorrowerAPR`, `ProsperScore`, `EmploymentStatusDuration` and one categorical variable `EmploymentStatus` had missing values. I replaced the missing rows of the numeric columns with their respective means and that of employee status with its most common value (mode).

I also collapsed some levels of employment status and income range.


## Summary of Findings

> Summarize all of your findings from your exploration here, whether you plan on bringing them into your explanatory presentation or not.

During exploration, I found out that interest rates appeared to be influenced by loan term, loan amount, employment status, income range, verification of income, associated risk and home ownership.

Specifically, interest rate appeared lowest for short term loans (12 months) while annual percentage rates (APR) was highest for short term loans. Larger loans had lower interest rates. However, increasing loan amount was more favorable for mid-term and long-term loans. 

Higher income and being employed (whether by oneself or not) or retired was associated with lower interest rates. Home owners (excluding unemployed ones) and Income-verified earners (including zero earners) also enjoyed lower relatively lower interest rates.

Generally, an increasing prosper score (or lowering risk score) was associated with lower interest rates. Generally, also, verified-income earners also had lower risks. Diving deeper, I saw that verified-income earners only had lower interest rates for mid-level risks, indicated by prosper score 5 - 7. For very low or very high risk loans, income verification did not seem to matter. It even appeared to slightly favor borrowers with unverified income.

For the explanatory presentation, I'll focus only on interest rates, loan amount and term.


## Key Insights for Presentation

> Select one or two main threads from your exploration to polish up for your presentation. Note any changes in design from your exploration step here.

Here, I'm mostly interested on the influence of two features - term and loan amount, on borrower (or interest) rate. Firstly, I introduced the main response variale (interest rate) with a histogram showing the distribution of interest rates.

Secondly, I created a histogram showing the distribution of log of loan amount since it's a more symmetric distribution. I changed the xtick labels from the log base 10 format to normal decimals to encourage readability or user friendliness.

Lastly, using three side-by-side scatterplots, I explored the relationship between loan amount and interest rates for the three loan terms (i.e., short, mid and long terms). 

