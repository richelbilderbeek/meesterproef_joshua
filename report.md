#Comparing two epitope prediction programs

* Joshua van Waardenberg
 
## Introduction

We will use the R packages MHCNuggets and EpitopePrediction to predict the ic50 values of randomly generated Epitopes. (?)
To compare these results they will be plotted into a scatter plot using the R library ggplot.

## Hypothesis

We expect the highest prediction of MHCNuggets to also be the highest prediction of EpitopePredictions. We don't expect them to match completely because the calculations could be made using different settings meaning different values can mean the same thing.
However, by comparing how high a value is compared to other values calculated by the same tool to how high the other tool's values are compared to it's own calculations, we can get an idea of if it corresponds.

## Methods

We use the R programming language in RStudio, with the libraries MHCNuggets and EpitopePrediction.

## Results

There is seemingly no correlation between the results of MHCNuggets and EpitopePrediction, it even happens that one of the higher results of MHCNuggets corresponded to the lower results of EpitopePrediction.

## Conclusion

Possible is that at least one of the two libraries is wrong. But it's also possible that both are right, but are making different assumptions.

## Discussion

MHCNuggets predicts the values using tensorflow, EpitopePrediction uses (....). One of these methods might be less precise.

## References

https://github.com/richelbilderbeek/ep_vs_mhcn
