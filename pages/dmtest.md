# Diebold-Mariano Test 

The test originally proposed by Diebold and Mariano (1995) considers 
a sample path of loss differentials $$ \{d_{t}\}^{T}_{t=1} $$. 
In the case of a squared loss function, we have $$ d_{t}=e^2_{t}-\breve{e}^2_{t} $$. 
Under the assumption that the loss differential is a covariance stationary series, 
the sample average, $$ \bar{d} $$, converges asymptotically to a normal distribution: 

$$ \sqrt{T} \bar{d}\:\:\: \underrightarrow{d}\:\:\: N(\mu, 2\pi f_{d}(0)) $$

In particular, they proposed to test the null hypothesis that 
the forecast errors coming from the two forecasts bring about the same loss:  
$$ E[e^2_{t}-\breve{e}^2_{t}]=0 $$ against the two-sided alternative. 
Thus, the resulting p-values represent the probability of 
obtaining the realized forecast error differential or 
a more extreme one in a new experiment if the null 
hypothesis was actually true. 


|   symbol	|definition   	|
|---	|---	|
|   $$ e_{t}=y_{t}-\hat{y}_{t}  $$		| forecast error|
|   $$ \breve{e}_{t}=y_{t}-\breve{y}_{t}  $$		| benchmark error|
|   $$ d_{t}=e^2_{t}-\breve{e}^2_{t} $$ 	| loss differential $$    	|


## DM Test-statistic

The test-statistic that will be used to calculate our 
p-values is computed as follows:

\begin{equation}
DM=\dfrac{\bar{d}}{\sqrt{\dfrac{2\pi\hat{f}_{d}(0)}{T}}}
\label{DMTEST}
\end{equation}

where $$ 2\pi\hat{f}_{d}(0) $$  is a consistent estimate. 
Consider $$ 2\pi\hat{f}_{d}(0)=\sum^{(T-1)}_{\tau=-(T-1)}w_{\tau}\gamma_{d}(\tau) $$ , 
where $$ \gamma_{d}(\tau)=\dfrac{1}{T}\sum^{T}_{t=|\tau|+1}(d_{t}-\bar{d})(d_{t-|\tau|}-\bar{d}) $$ . 
Under the assumption that  $$ \gamma_{d}(\tau)=0 $$  for $$ \tau\geq h $$ , 
we can use a rectangular lag window estimator by setting $$ w_{\tau}=0 $$  for  $$ \tau\geq h $$ . 
Another option is to use the Heteroschedasticity and Autocorrelation Consistent (HAC) 
estimator proposed by Newey and West (1987). In this case, the weights could be given 
by a triangular window, $$ w_{\tau}=1-\dfrac{\tau}{h} $$  for $$ \tau<h $$ . In this case, however, 
the consistency property only remains valid when the truncation lag $h$ or bandwidth is 
a function of the sample size $$ T $$. 

## *J*Demetra*+* implementation

The idea is to test the statistical significance of the regression of 
$$ e^2_{t}-\breve{e}^2_{t} $$ on an intercept.  In order to determine the statistical 
significance of the intercept, its associated standard errors need to take into account 
the autocorrelation patterns of the regression error, which are considered in the denominator 
of equation (\ref{DMTEST}). 

$$ \textsf{\textit{J}Demetra\textit{+}} $$ exploits the same unified framework 
to conduct all forecasting accuracy tests.  But given the small sample sizes that are typical 
in real-time forecasting applications, which leads to an over-rejection of the null hypothesis, 
we follow Coroneo and Iacone (2015) and use a finite sample distributions of Kiefer and Vogelsang (2005). 
The distribution of the test statistic (\ref{DMTEST}) will depend on kernel and the bandwidth chosen, which is set by default equal to $T^{0.5}$. The results can be very different than those resulting from the traditional asymptotic theory, where the test statistic would have the same distribution under the null independently of the kernel and the bandwidth used. 
