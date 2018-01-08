[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

>> **1. The problem**  
>>    In the BRFSS data, the distribution of heights is roughly normal with parameters µ = 178 cm and σ = 7.7 cm for men, and µ = 163 cm and σ = 7.3 cm for women.
>>    In order to join Blue Man Group, you have to be male between 5’10” and 6’1”. What percentage of the U.S. male population is in this range?  
>>
>> **2. How I solved it**   
>>    I used `scipy.stats` to generate a normal distribution with the specified mean and standard deviation of male heights. I then used the cdf() function to get the percentiles for the 5’10” and 6’1” height range boundary values, and I took the difference of the two to get the percentage of the U.S. male population in this height range.
>>
>> **3. The solution:**  
>>    ipython code:
>>    ```
>>    # Import scistats
>>    import scipy.stats
>>    
>>    # Generate a normal distribution of male heights with parameters µ = 178 cm and σ = 7.7 cm
>>    male_heights_distr = scipy.stats.norm(loc=178, scale=7.7)
>>    
>>    # Get the % of males who are between 5'10" (177.8 cm) and 6'1" (185.4 cm) tall 
>>    range_pct = male_heights_distr.cdf(185.4) - male_heights_distr.cdf(177.8)
>>    range_pct
>>    ```
>>    Result: 0.34209468294595308  
>>
>>    34.21% of the U.S. male population is between 5'10" (177.8 cm) and 6'1" (185.4 cm) tall.

