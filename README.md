# Category

A total of five parts have been designed, which are progressive in terms of business significance and programming difficulty:
- Part 1 – Changes in Mortgage Portfolio (Exploratory Data Analysis)
- Part 2 – Risk/Delinquency Model (Logistic Regression and Decision Tree)
- Part 3 – Prepayment Model (Regression/Classification Model)
- Part 4 – Transition of Loan Status (Build a Transition Matrix)
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


# Part 1:Changes in Mortgage Portfolio (Exploratory Data Analysis)

Examine changes in mortgage portfolio after the financial meltdown in 2008. This is a
pure exploratory data analysis.

## Backround
Before the financial meltdown in the third quarter of 2008, many people purchased houses for investment purposes, i.e., they expected the property value to go up quickly so that they could profit from reselling. Lenders also applied very lax policies in underwriting, i.e., no need for income verification or for down payment when reviewing loan applications.

Since the financial meltdown, the US government imposed more strict policies for underwriting. For example, the requirement for FICO score has become higher, and income verification is needed.


