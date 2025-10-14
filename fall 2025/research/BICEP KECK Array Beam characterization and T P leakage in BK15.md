## 3 GAUSSIAN BEAM PARAMETERS
* Approximated by elliptical Gaussians

3.1 COORDINATE SYSTEM
- instrument-fixed, spherical coordinate system independent of orientation w/ respect to celestial coordinates
- P (location of detector pair) = $(r,\theta)$  from boresight $B$
	- $r$ is radial distance from $B$
	- $\theta$ is counterclockqise angle looking out from telescope towards the sky

3.2 BEAM FITTING AND STATISTICS
- local $(x', y')$ Cartesian coordinate system
$$ B(\boldsymbol{x}) = \frac{1}{\Omega}e^{-\frac{1}{2}(x-\mu)^t\Sigma^{-1}(x-\mu)}$$
(see [[Calibration Measurements of BICEP3 and BICEP Array CMB Polarimeters from 2017 to 2014]] for earlier equation)

Additionally,
$$ \boldsymbol{\Sigma} = (\begin{matrix}\sigma^2(1 + p) & c\sigma^2 \\ c\sigma^2 & \sigma^2(1-p)\end{matrix})$$
where $\sigma$ is the beamwidth, and $p$ and $c$ are the ellipticities in "plus" and "cross direction".

major axis oriented along $x'$ or $y'$ axis $\rightarrow$ $+p$ or $-p$ ellipticity
total elipticity $e = \sqrt{p^2+c^2}$

**differential parameters** : differences of per-detector fits (between the orthogonal pairs)
ex. $d\sigma = \sigma_a-\sigma_b$.

How are the paraemeters generated?
- best fit of $\sigma$, $p$, and $c$ in each mapping run.
- Remove measurements where the detector is flawed (focus of project)
- Take median across all measurements for each individual detector
- Measurement uncertainty = central 68% of distribution of measurements
- FPU median = median across focal plane
- FPU scatter measures spread of best-estimate parameters

3.3 MEASURED BEAM PARAMETERS
* BK15 dataset beamwidths:
	* $0.305\degree$ (43' FWHM, 95 GHz)
	* 0.210$\degree$ (30' FWHM, 150 GHz)
	* 0.141$\degree$ (20' FWHM, 220 GHz)
* $p$ and $c$ are generally near 0
* so, are the only parameters being fitted for p and c ?
	* $\mu$ is known, $\Omega$ is known, $x$ is the parameter, and $\Sigma$ comes from p and c --> only fit for p and c
However, $B(\boldsymbol{x})$ is the equation to create the gaussian--what about what is actually produced by each detector in the results?



