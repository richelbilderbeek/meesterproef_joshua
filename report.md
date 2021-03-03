#Comparing two epitope prediction programs

* Joshua van Waardenberg
 
## Introduction

We will use the R packages MHCNuggets and EpitopePrediction to predict the ic50 values (....)

## Hypothesis

We expect the highest prediction of MHCNuggets to also be the highest prediction of EpitopePredictions.

[RJCB: this is a fine first hypothesis. However, both tools predict IC50 values
based on different settings (compare predicting Celsius versus Fahrenheit).
The lowest values in tool A, however, should be lowest in tool B]

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
