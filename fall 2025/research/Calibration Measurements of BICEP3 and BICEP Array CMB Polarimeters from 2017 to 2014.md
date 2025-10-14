- small-aperture refracting telescopes to measure primordial gravitational wave signatures in CMB (predicted by inflation)
- differential response between detectors with a pair --> affect result of polarized sky signal

# 1. introduction
- CMB e modes and b modes to probe tensor flutuations
- r constraint - tensor to scalar ratio, parameterizes the amplitude of tensor fluctuations
- detectors come in orthogonal pairs - V and H detectors
- primordial b modes (dr. verges' paper!!! review this if possible)
#  2. far field beam measurements with thermal source
* what is a [[far field distance]]?
* BICEP3 has far field distance < 200m --> use DSL locations for **ground based calibration measurements**
* mirror redirects rays on horizon --> unpolarized source 
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

# Far field beam measurements with polarized source at 95 GHz

$E\rightarrow B$ leakage: systematic arising due to per-pair polarization mismatch/mixing of polarization modes. **"Polarized Beam Response**".
	Less prominent than $T\rightarrow P$ leakage as E-mode power << T.
What exactly is $T \rightarrow P$ leakage? re-examine, return, and add a note on this.

To measure Polarized Beam Response, we use a linearly polarized source rather than a thermal source. Then, separate link between temperature and polarization by using maps at different angles/orientations. 

Generally, each detector measures:
$$ \int [B_T(x)T + \boldsymbol{B}^\boldsymbol{T}_p\boldsymbol{BP}]\delta(x - x')d\boldsymbol{x}'$$
where: $$B_p = [\begin{matrix}B_Q(\boldsymbol{x}) \\ B_U(\boldsymbol{x})\end{matrix}]$$
$$\boldsymbol{R} = [\begin{matrix}\cos(2\Phi) & -s\sin(2\Phi) \\ \sin(2\Phi) & \cos(2\Phi)\end{matrix}]$$
$$ P = [\begin{matrix} Q & U \end{matrix}]$$



[^1]: equation to be modeled in python! thus, its important to have a good understanding
