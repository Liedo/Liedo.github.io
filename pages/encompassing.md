# Encompassing Test 

Independently of whether the null hypothesis $$ E[e^2_{t}-\breve{e}^2_{t}]=0 $$  of the 
Diebold-Mariano test is rejected or not, it is relevant 
to understand the extent to which our model forecasts encompass those of the benchmark, 
or those are encompassed by the benchmark.  

Because of the obvious symmetry of both statements, we consider the first one alone in this document. 
If our forecasts $$ y_{t|\mathcal{F}_{i}} $$ 
encompasses a given benchmark 
$$ \breve{y}_{t|\mathcal{F}_{i}} $$ ,  
the difference between those benchmark forecasts and ours will not be a relevant factor 
at explaining our own forecast error. In other words, the regression coefficient $$ \lambda $$ 
will not be significantly different from zero in the following regression:

$$
\begin{equation}
\begin{array}{ccc}
  \underbrace{y_{t}-y_{t|\mathcal{F}_{i}}}_{e_{t}}  &   =   &   \lambda \underbrace{(\breve{y}_{t|\mathcal{F}_{i}}-y_{t|\mathcal{F}_{i}})}_{e_{t}-\breve{e}_{t}}+ \xi_{t}    \label{encompass} \\
&   \Updownarrow    & \nonumber \\
   y_{t}=  &   \lambda \breve{y}_{t|\mathcal{F}_{i}}  &    + (1-\lambda) y_{t|\mathcal{F}_{i}}+ \xi_{t}   \label{combi}
\end{array}
\end{equation}
$$



$$
\begin{equation}
\begin{array}{ccc}
  \underbrace{y_{t}-y_{t|\mathcal{F}_{i}}}_{e_{t}}    &  = & \lambda \underbrace{(\breve{y}_{t|\mathcal{F}_{i}}-y_{t|\mathcal{F}_{i}})}_{e_{t}-\breve{e}_{t}}+ \xi_{t}  \\
   & \Updownarrow   &    
\end{array}
\end{equation}
$$

 
$$
\begin{eqnarray}
\underbrace{y_{t}-y_{t|\mathcal{F}_{i}}}_{e_{t}}&=& \lambda \underbrace{(\breve{y}_{t|\mathcal{F}_{i}}-y_{t|\mathcal{F}_{i}})}_{e_{t}-\breve{e}_{t}}+ \xi_{t}  \label{encompass} \\
&\Updownarrow& \nonumber \\
y_{t}=& \lambda \breve{y}_{t|\mathcal{F}_{i}}&  + (1-\lambda) y_{t|\mathcal{F}_{i}}+ \xi_{t} \label{combi}
\end{eqnarray}
$$

Following Harvey, Leybourne and Newbold (1998), the statistical significance 
of the $$ \lambda $$ coefficient in regression \ref{encompass} can be used to reject 
the null hypothesis that our model encompasses the benchmark. In this case of rejection, 
equation (\ref{combi}) suggests that a combination of the two forecast would yield a 
more informative forecast. 

By construction, the value of the coefficient of a regression 
$$ \breve{e_{t}} =\alpha\breve{e_{t}}-e_{t}+\xi_{t} $$ is equal to $$ 1-\lambda $$, 
but it is not necessarily true that the \textit{rejection} of the 
null hypothesis in the first case implies the *acceptance*  of the symmetric statement.

The test-statistic is computed as follows. When the null hypothesis is that our model encompasses the benchmark, we define the sequence 
$$ \{d_{t}\}^{T}_{t=1} $$ , where $$ d_{t}=e_{t}(e_{t}-\breve{e_{t}}) $$ , and we 
compute $$ E1=\dfrac{\bar{d}}{\sqrt{\dfrac{2\pi\hat{f}_{d}(0)}{T}}} $$ , exactly as in equation (\ref{DMTEST}).  

  
### [Notation](notation.md)
### [Diebold-Mariano Test](dmtest.md)
### [Encompassing Test](encompassing.md)
### [Bias and Efficiency](bias.md)
