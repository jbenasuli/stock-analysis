# stock-analysis

## Overview of Project

The purpose of this project was to create a VBA script to parse annual stock market data for a given set of tickers. When run, the script prompts the user to input a year and then generates a table which contains the ticker, total daily volume, and annual return for each stock represented in the dataset.

Having successfully created a VBA script, which performs as detailed above, further work was done to refactor the original script. The purpose of refactoring the working script was to improve performance in anticipation of the script being used to analyze a far greater set of stocks in the future.

## Results

### Stock Performance

2017 results

- 2017 was overall a very good year. Every stock, with the exception of TERP (-7.2%), saw their share prices increase. DQ and SEDG performed particularly well posting gains of 199.4% and 184.5% respectively.

![2017-results](resources/2017-results.png)

2018 results

- 2018 by comparison was an overall poor year for this basket of stocks. With the exception of ENPH (+81.9) and RUN (+84.0%), all the stocks posted negative annual returns. It was a particularly bad year for DQ and JKS, which had annual returns of -62.6% and -60.5% respectively.

![2018-results](resources/2018-results.png)

### Execution Times

The execution time results below highlight the superior execution time achieved by refactoring the AllStockAnalysis code.

Original script execution times:

- 2017 Analysis: the original code ran in .296875 seconds

![2017-original-runtime](resources/module-2017-runtime-.75_size.png)

- 2018 Analysis: the original code ran in .2841797 seconds

![2018-original-runtime](resources/module-2018-runtime-.75_size.png)

Refactored script execution times:

- 2017 Analysis: the refactored code ran in .078125 seconds

![2017-refactored-runtime](resources/VBA_Challenge_2017.png)

- 2018 Analysis: the refactored code ran in .0703125 seconds

![2018-refactored-runtime](resources/VBA_Challenge_2018.png)

## Summary

The general advantage to refactoring code is increased efficiencies. Key benefits of refactored code are listed below:

- Using less memory and decreased execution times
- Simplifying and improving existing code helps ensure future work is streamlined
- Increased readability allowing for other stakeholders to better understand/work with the script

Despite the numerous potential gains from refactoring code, it is important to weigh the cost of resources that will be required to increase the efficiency of code, which already works, without adding any additional functionality to it.

### Advantages

The primary advantage to refactoring the original VBA script is the reduction in execution time. As detailed above, the time needed for the script to run for each year is drastically lower. For 2017 the execution time was reduced by 73.7%, and for 2018 the execution time was reduced by 75.3%. Such a reduction in execution time is an encouraging sign that this code could handle a much larger dataset.

### Disadvantages

Despite the efficiency gains noted above, one could argue that this refactoring has not been a worthwhile use of resources. The sample dataset is quite small, and the percentage decreases in execution time may not prove to be as significant with larger datasets. Furthermore, there are significant functionality improvements that should have been considered prior to refactoring. One example of this is that the script must have a hardcoded list of all tickers to be analyzed. As such, manual adjustments must be made to the script each time new stocks are listed, existing stocks are delisted, or the desired basket of stocks to analyze is changed by the user.
