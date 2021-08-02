# Project-Face-Recognition
Python Script that captures images from your webcam video stream

## Pipeline of the project


###
What is Haarcascade_frontalface_alt XML?

That is an XML file containing serialized Haar cascade detector of faces (Viola-Jones algorithm) in the OpenCV library. It is coded list of decision trees in which each vertex test one Haar Feature and each list claims “this is not face” or “this could be face”. It can be used the check that a part of image is face. Combined with the sliding window algorithm, it provides face detector. Particularly this file is for frontal faces only and the “alt” means that it is not the standard OpenCV solution but result of another - alternative - dataset and training.

Resources

https://github.com/opencv/opencv/tree/master/data/haarcascades

https://fairyonice.github.io/Object-detection-using-Haar-feature-based-cascade-classifiers-on-my-face.html

https://ieeexplore.ieee.org/document/990517
