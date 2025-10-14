### per-detector beam parameters through this KEY equation[^1]


$$
B(x) = 1/\Omega\exp[-(x-\mu)^T\Sigma^{-1}(x-\mu)/2] + b
$$
where 
$\textbf{x}$ = 2D position vector $(x', y')$
$\boldsymbol{\mu}$ = beam center $(x_0, y_0)$ 
$\boldsymbol{\Omega}$ = normalization constant
$\boldsymbol{b}$ = background offset
$\boldsymbol{\Sigma}$ = covariance matrix defined as:
$$\Sigma=\boldsymbol{R}^{-1}\boldsymbol{CR}$$ 
and $\boldsymbol{R}$ is a 2x2 rotation matrix parametrized by angle $\boldsymbol{\gamma}$ of major axis with respect to $x'$.
$\boldsymbol{C}$ is given by:
$$\boldsymbol{C} = (\begin{matrix} \sigma^2_{maj} & 0 \\ 0 & \sigma^2_{min} \end{matrix})$$
So in total, the beam chan be characterized by $[x_0, y_0, \sigma_{min}, \sigma_{maj}, \gamma, \Omega, b]$.

Fitted parameters then used to derive total ellipticity:
$$e = (\sigma^2_{maj} - \sigma^2_{min})/(\sigma^2_{maj} + \sigma^2_{maj})$$
$$p = e\cos{2\gamma}$$
$$c = e\sin{2\gamma}$$
$$\sigma = (\sigma_{maj} + \sigma_{min})/2$$
where c = ellipticity cross and $\sigma$ = beamwidth.

derived beam parameters then filter out bad data and coadded per-detector maps calculate good beam window functions which smooth cmb work (think choi!)

residual beam response in pair-difference beams --> $T\rightarrow P$ leakage. 
categorize $T \rightarrow P$ leakage via beam simulations + combined outputs. Thus, we can use these to estimate effect on $\boldsymbol{r}$.