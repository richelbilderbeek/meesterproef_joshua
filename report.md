#Comparing two epitope prediction programs

* Joshua van Waardenberg
 
## Introduction

We will use the R packages MHCNuggets and EpitopePrediction to predict the ic50 values (....)

## Hypothesis

We expect MHCNuggets and EpitopePredictions to predict around the same values. And that when the values relative to the other predictions are compared that we get a graph with a straight line through the line y = x.

[RJCB: this is a fine first hypothesis. However, both tools predict IC50 values
based on different settings (compare predicting Celsius versus Fahrenheit).
The lowest values in tool A, however, should be lowest in tool B]

## Methods

We use the R programming language in RStudio, with the libraries MHCNuggets and EpitopePrediction.

## Results

The results of MHCNuggets are completely different from the EpitopePrediction results.

[RJCB: one day, the words 'completely different' should be described
a bit more precise :-) ]

## Conclusion

At least one of the libraries is wrong.

[RJCB: Or both are wrong, or both are right from their own assumptions]

## Discussion

MHCNuggets predicts the values using tensorflow, EpitopePrediction uses (....). One of these methods is less precise.

## References

github

## Acknowledgements

(who/what to put here?)
