# Time-Series-Forecasting-ML-Estimate-the-unit-sales-of-Walmart-retail-goods---Revision-1

The M5 dataset, generously made available by Walmart, involves the unit sales of various.  <br />
products sold in the USA, organized in the form of grouped time series. More specifically, <br />
the dataset involves the unit sales of 3,049 products, classified into 3 products <br />
categories (Hobbies, Foods, and Household) and  <br />
7 product departments, in which the above-mentioned categories are disaggregated.  <br />
The products are sold across ten stores, located in three States (CA, TX, and WI).  <br />
In this respect, the bottom level of the hierarchy, i.e., product-store unit sales  <br />
can be mapped across either product categories or geographical regions.  <br />

Data was imported and the following analysis was done:  <br />
1) Plotting of <br />
 a) Aggregate daily unit Sales per Store <br />
   The graphs show that CA_3 is the highest selling store (units wise)
   some of the stores have change points in their trend(CA_2, TX_2, WI_2) <br />
  b) Daily sales pattern).  <br />
    plots above show that all the stores have the lowest sales on Christmas day <br />
  c) Day-of-week sales pattern).  <br />
     Plots show that sales are higher during weekends <br />
 d) Monthly sales pattern).  <br />
    Most stores have august (month 8) as the highest-selling store. Some have other months. <br />
    Details below: CA_1 – 8, CA_3 -8, C A_4-, TX_1=8, TX_2=8, TX_3=8, <br />
     WI_1=12, WI_2=9, WI_3=2 <br />
 e) Quarterly sales pattern).  <br />
    Most stores have Q3 as the highest-selling store. some have others. Details below: <br />
    CA_1 -Q3, CA_3 -Q3, CA_4-Q3, TX_1=Q3, TX_2=Q3, TX_3=Q3, WI_1=Q4,  <br />
     WI_2=Q4, WI_3=Q1. <br />

2) Inventory classification- Inventory was classified as A,B,C per sales revenue and 10 random Item_Ids samples selected. <br />
A sample of 10 Item-Ids were selected due to the limited computational power available but the same model may be used for the complete set of Item_ids. <br />

3) Hierarchical forecasting - using bottoms up methodology<br />

4)Plotting/ forecasting of daily sales data for CA_3 (highest sales store) <br />
  a) Using SARIMAX and weekends as the exogenous variable <br />
  b) Using Holt Winters <br />
  c) Using FB Prophet <br />
    
5)Creating Features for the Machine learning model <br />
  	 a) F1- Time series features <br />
 	   b) F2- Expanding Features <br />
     c) F3- Difference Features <br />
  	 d) F4- Lag and Rolling features <br />
  	 e) F5- Datetime and cyclical features <br />
 	   f) F6- sell price, snap, and Holiday Features <br />
     
6) Dropping missing data <br />

7) Creating target(Y) columns for direct forecasting (28 days) <br />
 Care was taken to ensure that there is no data leakage and forecast at time t was done using data <br />
 on or before time t-1 and all target Ys for the forecasts were after time (>=)t+1 <br />
 
8) Accuracy was checked using a  Naive forecast for establishing a baseline <br />

9) Important Features were determined using Lasso <br />

10) Direct Forecasting for 28 days was done using Lasso <br />

11) Recursive forecasting for 28 days were done using XGBoost  <br />

12) Plotting was done with Accuracy metric <br />
   	  a) Item Level <br />
      b) Daily levels for stores, state total, and overall WMT <br />
      c) Plotting of results <br />

