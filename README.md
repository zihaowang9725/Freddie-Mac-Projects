# Category

A total of five parts have been designed, which are progressive in terms of business significance and programming difficulty:
- Part 1 – Changes in Mortgage Portfolio (Exploratory Data Analysis)
- Part 2 – Risk/Delinquency Model (Logistic Regression and Decision Tree)
- Part 3 – Prepayment Model (Regression/Classification Model)
- Part 4 – Transition of Loan Status (Develop a Transition Matrix)
- Part 5 – Examine How Characteristics of Loans Impact Loan Performance (Survival Analysis)

# Project Purposoe

- Learn how to transit from exploratory data analysis to data modeling. 
- Gain finalcial industry domain knowledge and analytics skill - Although the data used is mortgage data, the same method and some domain knowledge are also applicable to credit cards, car loans, personal loans, student loans, and other fields.
- Know how to apply modeling skills to some similar fields - Some specific modeling methods are also applicable to marketing applications such as direct mail campaigns. 
- Build project management/documentation skills by self-design project steps - The project description deliberately uses a format similar to model documentation. 

# Source of Data

Freddie Mac Single Family Loan-Level Dataset: (Loggin is required to download the dataset)

http://www.freddiemac.com/research/datasets/sf_loanlevel_dataset.html

Download the quarterly datasets of 2008 and 2009. Each zipped file contains two parts:

- Origination Data:
Loan characteristics such as FICO, LTV, CLTV, property type, occupancy status, etc.
- Performance Data by Month:
Status of every loan in each month since it enters the Freddie Mac book.

# Freddie Mac General User Guide (Served as a data dictionary) 
Download the General User Guide and carefully review it to understand the meaning of each variable:

http://www.freddiemac.com/fmac-resources/research/pdf/user_guide.pdf

-----------------------------------------------------------------------------------------------------------------------------------------------------------------


# Part 1: Changes in Mortgage Portfolio (Exploratory Data Analysis)

Examine changes in mortgage portfolio after the financial meltdown in 2008. This is a
pure exploratory data analysis.

## 1.1 Backround
Before the financial meltdown in the third quarter of 2008, many people purchased houses for investment purposes, i.e., they expected the property value to go up quickly so that they could profit from reselling. Lenders also applied very lax policies in underwriting, i.e., no need for income verification or for down payment when reviewing loan applications.

Since the financial meltdown, the US government imposed more strict policies for underwriting. For example, the requirement for FICO score has become higher, and income verification is needed.

## 1.2 Getting the Sample and Aggregating Data 


Origination Data need to be aggregated

The sample loans data from 2008 Q1 to 2009 Q4 should meet the following criteria:

- Single family home 
- 30-year fixed rate 
- FICO score between 550 and 850 
- A random sample of 1% is good enough


Performance Data by Month need to be aggregated to derive a delinquency flag for each loan:

- A loan has reached 90+ days in delinquency
- A loan has shown recovery amount as recovery usually comes after foreclosure and repossession by the bank (REO)
- A loan has been modified, i.e., interest rate reduction after negotiating with the bank
- As older loans have longer performance histories and hence are more likely to encounter delinquency, I selected performance data of 5 years for each loan

## 1.3 Hypothesis

1. After the financial meltdown, loans in general have high credit scores (FICO).
2. After the financial meltdown, the portion of subprime loans (FICO < 660) decreased substantially in the mortgage portfolio.
3. Before the financial meltdown, many borrowers thought they could profit from the increased value of the houses in a few years, so portion of purchases (i.e., buying a house rather than refinancing an existing mortgage) was higher. After the meltdown, portions of purchases went down. Lower interest rates in 2009 also boosted the market for refinancing.
4. The quality of loans originated after meltdown is considerably higher, i.e., their delinquency rate is much lower compared to those loans originated before the meltdown.

