## objective of classification:
The task takes many relatively small images of low resolution and varying mask levels. The classification should separate the images into two groups: good beam and bad beam. The bad beams are characterized by the following:
- Gaussian fit parameters outside the expected range
- Differential parameters outside the expected range
- High levels of noise
- Readout errors/glitches

Primary vector attempts:
- Random Forest
- Support Vector Machines
- **Artificial Neural Networks**
- **Convolutional Neural Networks**
- probably just implement all of these and see which one works best?
- Generative Adversarial Network (?)
	- used for generative, not necessarily what we want

Read through:
- [[analyzing supervised machine learning models for classifying astronomical objects using Gaia DR3 Spectral features.pdf]]
- [[smith-geach-2023-astronomia-ex-machina-a-history-primer-and-outlook-on-neural-networks-in-astronomy.pdf | primer on neural networks in astronomy]]
- [[draft_complete_submitted.pdf | harvard thing]]

it's possible that artificial neural networks would be a good step if we simplify the dimensions, but for image classification convolutional neural networks will work the best
- reference https://www.astroml.org/astroML-notebooks/chapter9/astroml_chapter9_Deep_Learning_Classifying_Astronomical_Images.html
- 
- 

