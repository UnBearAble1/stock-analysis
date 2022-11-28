# Stock analysis and code refactoring of selected stocks during 2017 and 2018

## Overview of Project

### This project refactored code created to review twelve stocks and reduce the time of execution to enable an analysis for potentially thousands of stocks. The output of this code shows the percentage increase or decrease for identified stocks for years 2017 and 2018 as well as the volume traded for each stock. Lastly, it displays the time taken to run the code to show that the refactoring has reduced the time needed to execute the code.

## Results

### The key to refactoring the code was to remove the need for a nested loop to go through each stock in the provided array. By creating a tickerindex to hold values for each stock defined in the ticker array, to track increases in ticker volume and to compare the ticker starting price and ticker ending price, we were able to reduce the amount of times the code needed to loop by a significant factor.

### For 2017, the initial code ran in several seconds and with the refactored code, it was able to run in only .078 seconds. As with the initial results, the highest performing stock was DQ and the stock with the highest traded volume was SPWR. Since Steve's family believes there is a correlation between trading volume, it is important to note that SPWR, had the highest volume and an overall growth of 23.1% whereas the best performing stock DQ, grew at 199.4% but had only modest trading value at approximately 35 million. The worst performing stock, TERP, decreased in value by 7.2% and had a trading volume of approximately 139 million.

![Refactored 2017 Code](https://github.com/UnBearAble1/stock-analysis/blob/main/Resources/VBA_Challenge_2017.png)

### For 2018, the refactored code was able to run in only .0625 seconds, greatly reducing the amount of time from the initial code. The only two stocks to have positive growth this year were ENPH with volume of 607 million and growth of 81.9% and RUn/ with a trading volume of approximately 502 million and growth of 84.0%. another highly traded stock, SPWR, shrunk by 44.6% with approximately 538 million in trading volume. The worst performing stock, DQ, shrunk by 62.6% and had a trading volume of approximately 107 million. This analysis also shows that past performance is no indication of future performance.

![Refactored 2018 Code](https://github.com/UnBearAble1/stock-analysis/blob/main/Resources/VBA_Challenge_2018.png)

## Summary

### In general, refactoring code offers benefits when trying to improve code that was created to process small amounts of data, but whose performance may have suffer due to more and more data being involved. Code should be refactored if it doesn't scale for the amount of volume needed. Additionally, if it is a frequently used routine, even if it only takes a relatively short time to execute, if it is run many many times, it can begin to cost the user time. Disadvantages can include the time required to refactor and if the code is worth refactoring if there are other demands for the business. Especially if the code is used to support legacy tools, there's always the question of whether is should be refactored or if another process should be created to solve the issue

### In this example, the refactored code has the advantage of having a drastically reduced time to complete and will enable many more stocks to be reviewed quickly. The downside to this code is that the initial ticker array still needs to be manually entered, so if there are 30 stocks to be reviewed, all arrays will have to be updated which will still be a time intensive manual process. Including some type of database that can be drawn from to automatically populate the arrays would greatly improve this code and allow it to scale easily with the end user responsible for upkeeping the list of stocks to be reviewed.
