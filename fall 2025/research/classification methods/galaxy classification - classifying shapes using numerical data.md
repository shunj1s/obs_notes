- convolutional neural network to extract features from galaxy images and classify them into spirals and ellipticals

## 1. introduction
- galaxies classified into 3 main types: elliptical, spiral, and uncertain
	- elliptical = oval or round, with evenly speckled stars
	- spirals = spiral shape wiht extending arms
	- uncertain galaxies = weird

## 2. input and output
- galaxy dataset from sdss dr7
- input included:
	- spectra (float)
	- vote fraction (float)
	- debiased vote elliptical (float)
	- debiased vote spiral (float)
	- flag spiral
	- flag elliptical
	- flag uncertain
- output included:
	- shape_of_galaxy (integer, 0 for spiral, 1 for elliptical, 2 for uncertain)

the input is not images!!!!!

yeah okay... we're gonna have to use convolutional neural networks!!!
