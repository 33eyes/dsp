[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

>> 1. The problem
>>    Are first babies lighter or heavier than others? How does this difference compare to the difference in pregnancy length for first and other babies?
>>
>> 2. How I solved it 
>>    I used Cohen’s effect size to quantify the weight difference between first babies and other babies in the data provided in the exercise. I compared that difference to the pregnancy length difference, quantifies using Cohen's effect size in the textbook.
>>
>> 3. The solution, using CohenEffectSize function defined in the textbook:
>>    ipython code:
>>    ```
>>    # Cohen’s effect size for the weight difference between first babies and other babies
>>    CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
>>    ```
>>    Result: -0.088672927072602006
>>    This result shows that the difference in weight means is 0.09 standard deviations. While it shows that first babies on average are lighter in the given data, the difference may be too small to be significant, depending on context. Compared to Cohen's effect size of pregnancy length for first and other babies (0.029 standard deviations, stated in the textbook), this difference is greater.
