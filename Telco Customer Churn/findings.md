# Pandas Profiling
- SeniorCitizen is a bit imbalance, not as imbalance as phoneService thou
- MonthlyCharges has a lot of correlated value with others variables
- line the services feature has a lot of correlation with others services values, this would maybe lead to there being some package service, so if a person buys package A then that person would have some a certain set of packages. and there could be more than one packages and the customer would likely to choose from those packages meaning there is lil to much differences on theses features hence there is correlation, so if a person have a certain value in PhoneService, then there is a high chance that this feature can determine what value is in InternetService, cause of the packages people chose, this makes sense that MonthlyCharges has a high correlation with theses services, cause if Package A has X price and certain set of service, then package B would shows some certain price and package again, if there is 5 packages then the data values will be shown to that packages
- we could do a clustering to just prove this and see what will be shown, this is interesting, but if we would to work inside that company we can just ask what are the packages or a have the data engineer extract a column name packages, IF we are not working for this company then maybe clustering seems somewhat beneficial to us, we can talk about this more later on
- a another thing is that TotalCharges has a high cardinality, meaning not all MonthlyCharges are the same, meaning the hypothesis of there is packages could false, we will investigate this more
- NEVERMIND!!!, MonthlyCharges was an object, after i change it to a numerical, it's highly overall correlated with  MonthlyCharges
- and there is 11 missing values in TotalCharges, we can just maybe drop em, but let's look first how that 11 row looks like
- tenure is highly overall correlated with Contract
 
- the histogram of tenure shows that there is early customer that churn in the early month, or the first month, we have to dig deeper inside the people behavior that does churn in early month
- but there is a lot of person who status longer, customer with more than 70 months should be analyze as well, finding the behavior of person who stays long (high tenure value, does not need to be over 70 months)
 
- services can be split into two, phone services and internet services, (write down each column corresponding to those types)
- the value of no services has similar count value across the services columns (InternetService,PhoneService, and such)
- phone and multiple line has a count value of 682 on it
- while as for the internet service columns has 1526 count values

