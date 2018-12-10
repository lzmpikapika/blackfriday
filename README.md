# blackfriday
BlackFriday Consumer Behavior Analysis
## Problem definiton

Through the data analysis of the Black Five consumers and the comparison of consumers of different factors, like gender, age and so on. Understand the composition of the major consumer groups in the Black Friday, training and testing the data, and predict that has specific factors consumers cost on the Black Friday will be in the future.

## Background

Many studies and researchers have done a lot of research on this before our research.Why do people have such high enthusiasm for the Black Friday? What contributed to the high sales of Black Friday? Researchers are very interested in these aspects.Merchants also attach great importance to these research.Because the Black Friday is vital to the economic development of the year.“This season is crucial for the economy because around 30 percent of annual retail sales occur between Black Friday and Christmas. For some retailers, such as jewelers, it's even higher, at almost 40 percent.(The Balance,2018)”.Through previous years' research, we can know that sales of Black Friday are growing steadily year by year.“There has been a steady growth since 2012 in the amount of money spent by each shopper.Compared to 2016, there has been a 0.4% increase, in other words, each shopper spent about $935.58 and in 2017, each shopper spent $967.13.(sellerapp.com , 2018).”For consumers, their focus on goods is also shifted from quality to price.“Last year, 46% of shoppers said the quality was the most important factor in buying a gift, while 30% said the lowest price was most important, a 16% gap. This year's results show the gap closing (44% vs. 36%, or an 8% gap). In other words, consumers seem to be getting more price-focused.(Friday and 2018, 2018)”. Based on these aspects, Black Friday has become a hot topic in data analysis.

Non-academic Approaches: What Is Black Friday? Sales and Trends.

<https://www.thebalance.com/what-is-black-friday-3305710>

##Type of model and rationale {.tabset}

### Linear regression

In this case use linear regression to find a relationship between all purchase and Age,Gender,Marital_Status the three aspect.


### Classifier

Used to divide the specific variables that will be observed, make independent variables more suitable for observation.

##Description of design {.tabset}

### Design



### Design and Implementation Constraints



##Data explanation

The raw data comes from the platform kaggle file “Black Friday .csv”. Dataset of 550000 observations about the black Friday in a retail store, it contains different kinds of variables either numerical(stay in current city year, purchase) or categorical(user ID, product ID, gender, age, occupant, city category, marital status, product category1,2,3). It contains missing values. Integrated data clean up duplicate data, so the new dataset has 39181 observations about the black Friday.

  New dataset has 12 columns, and there is the columns explanation:
  
User_ID: each users ID

Product_ID: each products ID

Gender: Sex of User, F(female),M(male)

Age：Age of User(Divided into 7 stages), 0-17、18-25、26-35、36-45、46-50、51-55、55+

Occupation: Occupation(Divided into 20 categories)

City_Category: Category of the City (A,B,C)

Stay_In_Current_City_Years：Number of years stay in current city

Marital_Status：0 (unmarried),1 (married)

Product_Category_1: Product Category 1

Product_Category_2: Product Category 2

Product_Category_3: Product Category 3

Purchase: Purchase amount in dollars

Independent Variables: user ID, product ID, gender, age, occupant, city category, marital status, product category1,2,3, stay in current city year

Dependent Variables: Purchase

##Identification Training and Testing Data

Training set: 90% of the entire data set. Equivalent to the first 35263 rows of the new data set.

Testing set: 10% of the entire data set. Equivalent to the end of 3918 rows of the new data set.

##Testing and validation procedure

```{r fit}
summary(fit)
```
```{r fit, echo=FALSE}
rpart.plot(fit)
```

##Results



##Reference

Sellerapp.com. (2018). SellerApp: Complete Amazon Suite for PPC, Portfolio, Keywords, Sales. [online] Available at: <https://www.sellerapp.com/black-friday-analysis-2017> [Accessed 3 Dec. 2018].

The Balance. (2018). How Much Do Americans Spend on Black Friday?. [online] Available at: <https://www.thebalance.com/what-is-black-friday-3305710> [Accessed 3 Dec. 2018].

Friday, B. and 2018, H. (2018). Holiday Shopping Survey Data 2018. [online] BlackFriday.com. Available at: <https://blackfriday.com/news/holiday-shopping-survey-data> [Accessed 3 Dec. 2018].


