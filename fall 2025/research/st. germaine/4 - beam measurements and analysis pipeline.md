[[draft_complete_submitted.pdf#page=99|draft_complete_submitted, p.99]]
- control of systematics for proper precision measurement
- detector angular response aka **beam**
- considering a detector an emitter of photons
	- reciprocity theorem: maxwell's equations are time-invariant
- thus, beam measurements are necessary for:
	- systematic control
	- converting detector timestreams into CMB maps

## 4.1 Far-Field Beam Mapping Procedure
- electromagnetic signal emitted from a receiver has two zones: near-field and far-field
- in nearfield:
	- complex wave motion
	- sensitive to phase of radiation 
- once the waves travel far enough, they can be considered "standard plane waves"
- wave separation $\approx 2D^2/\lambda$
	- $D$ = diameter of antenna element
	- $\lambda$ = radiation wavelength
- the small-aperture design of our telescopes makes our far-field distance ~100-200m (yay!)
- BICEP and Keck are in different facilities roughly 200m apart

### 4.1.1 sources
- often far-field beam mapping uses a large chopped thermal source affixed to a mast raised ~10m above the roof of the observatory
	- see [[draft_complete_submitted.pdf#page=103&rect=354,576,447,700| this thermal chopper ]]
	- also [[on modulators | this note]]
- sometimes high-power broad-spectrum noise source used
	- also used for measurements of polarization angle
	- 50$\Omega$ SMA termination whose thermal radiation is amplified $\rightarrow$ upconverted $\rightarrow$ bandpass filtered to desired frequency range
- chop signal is recorded w/ motor encoder and sent to the opposite building
- recorded simultaneously w/ detector timestreams

### 4.1.2 mirrors
- large, aluminum honeycomb mirror used to redirect light coming from the telescope to the source at the opposite building
- while beam mapping, forebaffles are removed
- mirror ensures each detector beam couples to the source
	- coverage out to a $2\degree$ radius
- keck mirror covers only 2-3 receivers at a time $\rightarrow$ multiple positions required to map the detectors at all angles

### 4.1.3 scan strategy
- experimental choices when deciding far-field beam mapping observation schedules:
	- **azimuth scan speed** want to scan fast enough to prevent schedule from becoming too long
		- Keck = $0.4\degree/$sec , BICEP3 = $0.8\degree/$ sec, Bicep Array = $0.6\degree/$sec 
	- **azimuth range**: limited by telescope field of view, but we try to guarantee that each detector sees the source out to a radius of at least $2\degree$. 
		- Keck - $22.8\degree$, BICEP3 = $30\degree$, BICEP array = $32\degree$
	- **elevation range and step size** step size is dictated by the desired pixelisation of the beam maps-generally we loko for at least two hits in each $0.1\degree$ square pixel, and thus use an elevation size of $0.05\degree$ for all experiments. Elevation range varies: ^d40fd8
		- KECK - $20\degree$, Bicep3 = $30\degree$, BICEP array = $24\degree$

## 4.2 Far-field beam map analysis pipeline
- differences in the beam response $\rightarrow$ temperature to polarization leakage
- thus, it is critical that the pipeline takes in raw beam map timestreams and generates final composite beam maps while injecting minimal systematics
- with unavoidable systematic effects, we must quantify and remove contamination 

### 4.2.1 Demodulation
- modulation can help separate the signal from the response and any other possible interception
- each source for observation is modulated in some way 
	- chop reference recorded simultaneously with the real data
	- recorded in a binary square wave
	- one demodulated sample given for each full period of the square wave
		- cosine component $\leftarrow$ uniform weighted mean of all samples when chop reference is high - mean of samples in low phase
		- sine component $\leftarrow$ same kernel $90\degree$ out of phase from cosine
	- with perfect modulation, cosine matches the source signal and sine component = 0
- imperfect demodulation can drastically impact the beam shape and noise characteristics... forever!!!!
- sometimes, the chop reference has single-value spikes or glitches in the binary chop reference, which create "hot pixels" in the beam shapes or changes in the beam maps.  ^950756
	- to minimize this, we often "clean" these imperfections via constructing an ideal square wave using the peak frequency of the Fourier transform
	- remove high-frequency anomalies
- for a large thermal chopper the physical chop method is not instantaneous $\rightarrow$ small phase shift induced, ~1.5 radians across the main beam in BICEP3
	- thus, polarized detectors in a detector pair are affected equally
	- measured beam shape slightly more elliptical in the azimuth direction

### 4.2.2 beam map coordinate system
- coordinates are calculated for the post-demodulation, downsampled timestreams
- independent of the instrument orientation with respect to the sky
- pixel $P$ containing two detectors has location $(r,\theta)$ with respect to the boresight $B$
	- $r$ is the radial distance from $B$ 
	- $\theta$ is the counterclockwise angle looking out from the telescope towards the sky
	- [[draft_complete_submitted.pdf#page=113&rect=121,448,483,648|visible in this diagram]]
- telescope pointing model converts raw mount encoder values to AZ, EL, and DK timestreams which are then converted to per-detector $(x', y')$ coordinate timestreams
	- however, exact measurements of mirror/source parameters are not strictly required
- interpolation effectively smooths the beam

### 4.2.3. 2D elliptical gaussian fits
standard 2D elliptical gaussian fit:
$$B(x) = \frac{1}{\Omega}e^{-\frac{1}{2}(x-\mu)^T\Sigma^{-1}(x-\mu)}$$
where $x = (x', y'),$ $\mu = (x_0, y_0)$, $\Omega$ is the normalization, and $\Sigma$ is the covariance matrix.
I go on about this in [[BICEP KECK Array Beam characterization and T P leakage in BK15]], so i'll leave it at that here.
- current fitting function uses Nelder-Mead method--maybe for a future implementation?
> [!PDF|] [[draft_complete_submitted.pdf#page=117&selection=17,12,17,47|draft_complete_submitted, p.117]]
> > we make automatic data-quality cuts
> 
- this is the crux of the entire research project! yippee!!!!

### 4.2.4 binning and masking
- after we get the demodulated detector timestreams, the next step is to bin them into per-detector, per-schedule beam maps, also known as "component" maps!
	- binned onto the same common grid with $0.1\degree$ square pixels, with $(x', y') = (0,0)$.
	- enforces 2 hits per pixel like stated [[4 - beam measurements and analysis pipeline#^d40fd8 | here]]
- value in a given map pixel = uniform weighted mean of all samples in pixel
- currently, observation band with the smallest beam in BICEP/Keck array is the 270 GHz band, with Gaussian $\sigma = 0.120\degree$. 
- mask is then applied to remove:
	- ground
	- mast holding source
	- South Pole Telescope 10m dish (for Keck)
	- Remove any rays from the detector that do not couple to the mirror/source

### 4.2.5 cuts and composting
 [[draft_complete_submitted.pdf#page=119&selection=16,1,18,18|draft_complete_submitted, p.119]]
- now, we can stack the 2D elliptical Gaussian fits together to create composite beam maps!
	- highest signal-to-noise representation of a detector's true beam response
- we can also use these per-detector maps for other things
	- estimating $T\rightarrow P$ leakage 
		- [[BICEP KECK Array Beam characterization and T P leakage in BK15]]
	- sensing overall optical performance
- certain conditions for each component maps, relying on automated cuts:
	- main beam must couple to the redirecting mirror and source. if the center is removed by the mask, the component map is cut.
	- the detector must be responsive, and have reasonable fit parameters. (adjusting for different frequency-bands add later?)
	- both detectors in the pair must be responsive and have reasonable fit parameters
	- the detector must remain responsive with noise levels away from the main beam.
	- the fit residual must be reasonable.
- now, once the bad maps have been cut, we can coadd them together $\rightarrow$ composite maps! 
	- stack all good composite maps onto the common $(x', y')$ grid
	- take the median in each map pixel
- also construct "split" beam maps, made by randomly separating all component maps for a detector into two halves and then taking the distance
	- estimate of noise in a given composite map at a smal radii and get more uncertainties on the $T\rightarrow P$ leakage estimates

### 4.2.6 beam window function & pipeline transfer function
- generating per-band, array-averaged beam window functions $B(l)$
- Convert measurements of the CMB into physical estimates of the on-sky-signal
$$T_{obs}(\theta,\phi) = \sum_{l=0}^\inf\sum_{m=-l}^lB_{lm}a_{lm}Y_{lm}(\theta,\phi)$$
where $B_{lm}$ is the beam window function, and $T_{obs}$ is the temperature of the sky as measured by a telescope in spherical harmonics.
- correct for the finite size of the aperture of the thermal chopper
	- observed beam is actually a convolution of the true detector beam response with a uniform circular aperture of diameter $D$
	- can correct for the aperture by dividing the observed $B(l)$ by the fourier transform of the uniform circular aperture:
$$B(l)_{true} = B(l)_{obs}/\frac{2J_1(l\theta_{chop})}{l\theta_{chop}}$$
where $J_1$ is the Bessel function of the first time and $\theta_{chop}$ is the angular radius of the thermal chopper aperture
> ex. for a thermal chopper with $D = 24$ inches at a distance 200m away, $\theta_{chop} \approx 0.087\degree$, which increases the observed $B(l)_{obs}$ by 1.2% at $l = 200$ and 7.1% at $l=500$.


