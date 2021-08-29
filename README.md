# Stock Analysis


## Purpose

This analysis is meant to take data from the last several years of the stock market, focusing on 12 specific stocks. Using the written code, each stocks' total daily trade volume and over all annual return can be caluculated by putting in the year in question. The code was originally written but to make it run more effeciently, a refactored version of the script was generated.

## Results

### Analysis

I started by pulling the output sheet set up code and ticker array from Sub AllStockAnalysis as shown here:

![VBA_output_array.png](VBA_output_array.png)

I then created a tickerIndex, setting it to zero. Ticker volumes were calculated by checking rows for tickerIndexes and increasing the volume each time a tickerIndex was found:

![VBA_tickerVolume.png](VBA_tickerVolume.png)

Starting prices and ending prices were found using If statements checking to see the first time a tickerIndex appeared by checking against the row above it and pulling the price. Ending prices were identified by checking to see if tickerIndex for the row below matched. These values are then used to calculate the percentage of return on the stock for the indicated year.

![VBA_tSP_tEP.png](VBA_tSP_tEP.png)

### Findings

The results are color coded to show positive or negative returns at a glance in red or green. Stocks ENPH and RUN were the only two stocks to show positive returns in both years of 2017 and 2018.



## Summary

### Pros and Cons of Refactoring

Refactoring code, in general, makes it more succinct and efficient. A more efficient code, in the end, will leave fewer places for errors or bugs, however, the process of refactoring does provide more opportunities for such mistakes.

Refactoring can also manipulate the end results in unwanted ways if not done correctly, however, having a cleaner code makes it easier to come back to, or apply to different scenarios as the data grows or changes. It is important to have code clearly and cleanly notated so that whether it is a group project or an individual returning after some time, it is clear what each section is meant to do.


### Original vs Refactored VBA script

The run time is the most quantifiable advantage to the refactored VBA script. The original script took almost 1 sceond to run, while the refactored was able to be ran around 0.1-0.2 seconds. The disadvantage is primarily in human error. When I was refactoring the code, I was having to catch new mistakes that I was making after have a working script already. However, now that I have debugged the refactored script and labeled it clear, I will be able to come back at any time in the future and use the script for additional years of data if they were to ever be added.

