# Bias 

In order to assess whether our forecasts are unbiased, 
we will simply test the statistical significance of the average error. 
In some cases, the time series of forecast errors 
$$ \{e_{t}\}^{T}_{t=1} $$ may be autocorrelated 
to some extent even when they are based on a model with IID innovations. 
In such cases, the variance associated to the estimate of the average forecast error may be large. 
The test statistic has exactly the same form as the previous tests discussed so far, 
and it follows a standard normal distribution under the null of unbiased forecasts:  
$$ BIAS=\dfrac{\bar{e}}{\sqrt{\dfrac{2\pi\hat{f}_{e}(0)}{T}}} $$


# Efficiency 

We will test here a necessary condition for our forecasts to be efficient: absence of autocorrelation. 
In the same spirit as the tests described above, we will assess the statistical significance of the forecast errors' autocorrelation. 
Thus,  our sequence $$ \{d_{t}\}^{T}_{t=1} $$ will be defined with $$ d_{t}=e_{t}e_{t-1} $$.


### [Notation](notation.md)
### [Diebold-Mariano Test](dmtest.md)
### [Encompassing Test](encompassing.md)
### [Bias and Efficiency](bias.md)
### [Implementation in JDemetra+](jdimplementation.md)