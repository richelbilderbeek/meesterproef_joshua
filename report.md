#Comparing two epitope prediction programs

* Joshua van Waardenberg
 
## Introduction

ic50 values determine how likely a strain is to be presented.
[RJCB: add: what are these IC50 values for?]

We will use the R packages MHCNuggets and EpitopePrediction to predict the ic50 values of randomly generated epitopes.

![ep_vs_mhcn.png](ep_vs_mhcn.png) 

> figure 1

![ep_vs_mhcn_log.png](ep_vs_mhcn_log.png)

> figure 2

To compare these results they will be plotted into a scatter plot using the R library ggplot.

[RJCB: what is the problem?]

![ep_vs_mhcn_perc.png](ep_vs_mhcn_perc.png) 

> figure 3

## Hypothesis

We expect the highest prediction of MHCNuggets to also be the highest prediction of EpitopePredictions. We don't expect them to match completely because the calculations could be made using different settings meaning different values can mean the same thing.
This is determined by plotting the relative ic50 values in a graph and seeing if the trend line has a slope of 1.

/However, by comparing how high a value is compared to other values calculated by the same 
/tool to how high the other tool's values are compared to it's own calculations, we can get
/ an idea of if it corresponds.

## Methods

We determine if the prediction is correct by eyeballing, we expect the trend lines to have a slope of 1, which would be easy to see in the graph.

## Results

By eyeballing we see that the relative results of MHCNuggets and EpitopePrediction don't match up, it even happens that one of the higher results of MHCNuggets corresponded to the lower results of EpitopePrediction, we are able to deduct this from a negative slope, see figure 3.
After checking the data we noticed a lot of the data from EpitopePrediction falls within 1% of the highest value, while the data from MHCNuggets is spread out. That's why we decided to try plotting EpitopePrediction on a logarithmic scale while leaving MHCNuggets the same. This resulted in figure 4, and after plotting this on a relative scale we got figure 5.

![ep_vs_mhcn_comp.png](ep_vs_mhcn_comp.png)

> figure 4

![ep_vs_mhcn_perc2.png](ep_vs_mhcn_perc2.png)

> figure 5

## Conclusion

Possible is that at least one of the two libraries is wrong. But it's also possible that both are right, but are making different assumptions.

[RJCB: erally? Is there erally a problem for all haplotypes except 1]

## Discussion

MHCNuggets predicts the values using tensorflow, EpitopePrediction uses (....). One of these methods might be less precise.

## References

https://github.com/richelbilderbeek/ep_vs_mhcn
