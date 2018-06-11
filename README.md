# Face-vs-Background-Classification

This project is about classifying facial region and background region using Generative model. We make use training images for
face and background to obtain the likelihood and prior distributions, later we use these values to infer the facial regions using test images.

Algorithmic Approach:
1. We make use of Generative model for detect facial region and background region.
2. Vectorise all the images in the data set for both face and background
3. For the entire data set(both face and bg), calculate  Likelihood Mean and Covariance.
4. Describe them using mvnpdf by using these parameters.
5. Compute diagonal covariance matrix.
6. For inference, we use Bayes method, we compute ratio of Prob_x_givenface to Prob_x_givenbg if >1 face, else non face, we use log
function to compare results as the values tend closer to 0 and we get indeterminate form
7. We measure the accuracy for different color spaces like RGB, Gray, YCBCr,HSV etc.
