[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

>> **1. The problem**  
>>    Families with many children are more likely to appear in your sample, and families with no children have no chance to be in the sample. Investigate this bias in the data sample by constructing and plotting the actual and biased distributions, and computing their means.
>>
>> **2. How I solved it**   
>>    I used the supplied Pmf class to construct the probability mass functions of the actual and biased distributions. I used the supplied BiasPmf function construct the biased distribution. I used the Mean() function call on the Pmf instances of the actual and biased distributions to get their means.
>>
>> **3. The solution:**  
>>    ipython code:
>>    ```
>>    # Get the respondent data
>>    resp = nsfg.ReadFemResp()
>>
>>    # Use the provided thinkstats2 library to construct a probability mass function 
>>    # of the actual distribution of the number of kids per household.
>>    pmf = thinkstats2.Pmf(resp.numkdhh, label='numkdhh')
>>
>>    # Plot the pmf of the actual distribution
>>    thinkplot.Pmf(pmf)
>>    thinkplot.Config(xlabel='Number of children', ylabel='PMF')
>>    ```
>>    Result:  
>>    ![pmf of the actual distribution](https://github.com/33eyes/dsp/blob/master/statistics/metis_prework_stats_ex2_img1.png "pmf of the actual distribution")
>>    
>>    ```
>>    # Compute the pmf of the biased distribution, using the BiasPmf function provided
>>    # in the textbook.
>>    biased = BiasPmf(pmf, label='biased')
>>
>>    # Plot the actual and biased pmfs in one graph to compare the two distributions.
>>    thinkplot.PrePlot(2)
>>    thinkplot.Pmfs([pmf, biased])
>>    thinkplot.Config(xlabel='Number of children', ylabel='PMF')
>>    ```
>>    Result:  
>>    ![pmfs of the actual and biased distributions](https://github.com/33eyes/dsp/blob/master/statistics/metis_prework_stats_ex2_img2.png "pmfs of the actual and biased distributions")
>>    
>>    ```
>>    # The mean of the actual distribution
>>    pmf.Mean()
>>    ```
>>    Result: 1.0242051550438309
>>    
>>    ```
>>    # The mean of the biased distribution
>>    biased.Mean()
>>    ```
>>    Result: 2.4036791006642821
>>
>>    The plot results show that the biased distribution excludes households with no children, and centers around 2-3 children per household. The actual distribution distribution shows that most households have no children, followed by households with one child as second most frequent, followed by households with two children, and so on. The large difference in the actual and biased means also shows that the bias has a strong effect here. 
