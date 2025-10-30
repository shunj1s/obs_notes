$\rightarrow$ [[draft_complete_submitted.pdf#page=50|p.50]]
- series of polarimeters at the Amundsen-Scott South Pole station
- searching for **signature of primordial gravitational waves** in the polarized CMB
- designed to maximize sensitivity at degree angular scales
## 2.1 detectors
- means of converting incident photons $\rightarrow$ electrical signal $\rightarrow$ data
	- source signal + poisson noise + noise from imperfection of detection method
- w/ cmb, bolometers are used as the key detector elements in the FPU

- so, what are bolometers?
- absorber with heat capacity $C$ coupled to a thermal bath $T_{bath}$ via a thermal link with conductance $G$
- for incident power $P$ coupling to the bolometer, the bolometer heats up by $\Delta T = \Delta P /C$ and is dissipated with $\tau = C/G$.
- Starting with BICEP2, the BICEP/Keck Array program has used **transition-edge sensors (TES)** coupled to free space
	- TES bolometer = superconductor held at superconducting transition
	- Bicep/Keck Array uses TES detectors
- TES Detector arrays are deployed at frequency bands of 30, 40, 95, 150, 220, 230, and 270 GHz

## 2.2. Detector Readout
- signals are amplify + multiplex (MUX) using superconducting quantum interference devices (SQUIDs)
- each bolometer is coupled to a single first-stage SQUID
	- 33 SQ1s coupled to 16 detector pairs are fed to a single SQ2
- SQUID series array (SSA) is mounted on the fridge bracket
- Each stage of SQUID readout must be biased so each amplifier ensures proper stability and linear amplification of TES signal at optimal $dR/d\Phi$ or $dV/d\Phi$ point
	- tuning done every fridge cycle

## 2.3 optics
- compact, on-axis refractors
- small aperture size $\rightarrow$ sensitivity at angular scales
	- 265 / 520 / 550 mm for Keck, Bicep3, and BIcep Array respectively

## 2.4 cryostat
- minimize non-cosmological radiation coupling to detectors via vacuum pumping and cryogenic cooling

## 2.5 telescope mount and observatory site
- two separate buildings at amundsen-scott south pole station
- azimuth, elevation, and boresight location
- two levels of warm, external shielding to reduce contamination from light exiting the telescope aperture
	- co-moving "forbaffle" to prevent diffraction
	- ground shield made of aluminum to reflect rays
- south pole observation provides scientific and programmatic advantages
	- lack of precipitable water vapor
	- temperature/weather stability
	- high elevation

## 2.6 observation strategy
- same 400-600 sq.deg. patch of sky observed, varying with the instantaneous field of the experiment
- discrete units of observation:
	- **elnods**: "elevation nods" that scan up-down-up in elevation at a fixed azimuth
	- **halfscans**: single scan of telescope 64.4$\degree$ in one direction in azimnth, at a constant elevation
	- **scansets**: collection of ~50 pairs of halfscans 
	- **phases**: collections of 6-10 scansets where elevation and azimuth are slightly adjusted after every pair
	- **schedules** collection of multiple phases of data at a constant boresight rotation angle
