# Comparing two epitope prediction programs

* Joshua van Waardenberg
 
## Introduction

The R packages MHCNuggets and EpitopePrediction were used to predict the ic50 values of randomly generated epitopes.
Then scatter plots were created to compare the results of the two libraries and see if they match up.

![ep_vs_mhcn.png](ep_vs_mhcn.png) 

> figure 1

![ep_vs_mhcn_log.png](ep_vs_mhcn_log.png)

> figure 2

![ep_vs_mhcn_perc.png](ep_vs_mhcn_perc.png) 

> figure 3

Ideally all the dots are on the line y = x, but the fact that they are not does not mean the results are wrong. We have to analyze these results to see if they are right or wrong.

## Hypothesis

We expect the highest prediction of MHCNuggets to also be the highest prediction of EpitopePredictions. We don't expect them to match completely because the calculations could be made using different settings meaning different values can mean the same thing.
This is determined by plotting the relative ic50 values in a graph and seeing if the trend line has a slope of 1.

## Methods

The data is made analyzable by putting it in scatterplots using the R library ggplot.
We determine if the prediction is correct by eyeballing, we expect the trend lines to have a slope of 1, which would be easy to see in the graph.

## Results

By eyeballing we see that the relative results of MHCNuggets and EpitopePrediction don't match up, it even happens that one of the higher results of MHCNuggets corresponded to the lower results of EpitopePrediction, we are able to deduct this from a negative slope, see figure 3.
After checking the data we noticed a lot of the data from EpitopePrediction falls within 1% of the highest value, while the data from MHCNuggets is spread out. That's why we decided to try plotting EpitopePrediction on a logarithmic scale while leaving MHCNuggets the same. This resulted in figure 4.

![ep_vs_mhcn_comp.png](ep_vs_mhcn_comp.png)

> figure 4

We then ordered the results of MHCNuggets and EpitopePrediction to be able to see better if the highest result of MHCNuggets also gives the highest result in EpitopePrediction. Here we expected to see the dots around a clear line. However, the result we got is figure 5.
There is no clear line visible, and the dots are spread out over the entire graph.

![ep_vs_mhcn_sort.png](ep_vs_mhcn_sort.png)

> figure 5

*An example of how the data is sorted:*

 haplotype   | sequence | ep   | mhcn | ep | mhcn
-------------|----------|------|------|----|------
HLA-A\*01:01 |REQQPQWHC |8.1   |1.3   |2   |1
HLA-A\*01:01 |VPVWESKYT |3.9   |2.5   |1   |2
HLA-A\*01:01 |IRTFCGLPD |14.3  |4.6   |3   |3
HLA-A\*02:01 |REQQPQWHC |25.3  |4.7   |3   |2
HLA-A\*02:01 |VPVWESKYT |6.5   |8.2   |1   |3
HLA-A\*02:01 |IRTFCGLPD |9.8   |2.3   |2   |1

## Conclusion

Figure 5 shows us that at least the first 3 haplotypes go wrong. But the trend line rotates closer to y = x after every haplotype.

## Discussion

It's unknown what this strange behavior is caused by. There could be a bug in one of the programs used. But we know for certain that the first 3 haplotypes are incorrect.

## References

https://github.com/richelbilderbeek/ep_vs_mhcn
