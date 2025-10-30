- [[optical response functions]]
- beam pass (how it responds to the signal, as a measure of frequency)
- detector behavior
using these factors, we can calibrate our telescope measurements!

calibration data (like ucla summer observation center!)
- clara will send documents

take data related to **optical response**
- nowadays, telescopes have thousands of detectors (TES detectors)
	- optical response measured 50-60 times each--LOTS of detector calibration images
- Use optical response to determine whether these calibration images are good or bad

Gaussian beam model <= parametrized by **width**, **shape**, etc.
	- compute parameters for every detector in focal plane--if the beam is too elongated, we shouldn't keep the beam
- Using these parameters to compute the best possible beam transfer function

With many, many beam images --> we want to use machine learning!
- classification of beam images !!! how would we do this?
	- probably CNNs, image recognition, etc.
- set of beams--> how do we apply machine learning to classify these beams as "good" or "bad"?
	- scikitlearn? tensor flow?
- detectors see a small part of the sky--the beam shows how well the detector sees the sky
- the further from the center of the beam, the less the detector sees
- very exploratory project--we could get onto something quite interesting, but don't put too much pressure on yourself! 
- 
	- 