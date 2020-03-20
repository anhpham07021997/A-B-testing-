# Project : A/B TEST RESULT 
This project is part of Udacity Data Nanodegree program 
-------------------------------------------------------
### Project Details
The project is to understand A/B test run by an e-commerce website. My goal is to help the company understand if they should implement the new page, keep the old page, or perhaps run the experiment longer to make their decision.

### Table of Contents
- [Introduction](#intro)
- [Part I - Probability](#probability)
- [Part II - A/B Test](#ab_test)
- [Part III - Regression](#regression)
### Conclusion 

#####Part I : Probability  
- After caculate the probability of new_page and old page ,the probabiltiy of people converted to new page by control group and treatment group are closed to each others ( control group: 0.1203863045004612, and treatment group:0.11880724790277405) 

- However, there is no evidence to conclude which page is better , after hypothesis test that 
we can confirm 

##### Part II
$$H_0: P_{new}-P_{old} <=0$$
$$H_1: P_{new}-P_{old} > 0$$
Pvalue= 0.905173705140591
**=> reject the null hypothesis , new page is not better than old page**

##### Part III : 
- log=sm.Logit(df["converted"],df[["intercept","ab_page"]])
=> p value of treatment and control group is 0.190

- so we have to has other variables by adding new table csv "countries.csv"
log=sm.Logit(df4["converted"],df4[["intercept","ab_page","US","CA"]])
**=>All p_value is bigger that 0.05 => country has no significant impact on the conversion of people**


###  csv files
- ab_data.csv, countries.csv 
