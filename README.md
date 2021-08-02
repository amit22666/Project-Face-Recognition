# Project-Face-Recognition
Python Script that captures images from your webcam video stream

## Pipeline of the project


###
What is Haarcascade_frontalface_alt XML?

That is an XML file containing serialized Haar cascade detector of faces (Viola-Jones algorithm) in the OpenCV library. It is coded list of decision trees in which each vertex test one Haar Feature and each list claims “this is not face” or “this could be face”. It can be used the check that a part of image is face. Combined with the sliding window algorithm, it provides face detector. Particularly this file is for frontal faces only and the “alt” means that it is not the standard OpenCV solution but result of another - alternative - dataset and training.

Viola-Jones algorithm

Initialize the weights
Normalize the weights
Select the best weak classifier (based on the weighted error)
Update the weights based on the chosen classifiers error
Repeat steps 2–4 T times where T is the desired number of weak classifiers

What is Boosting?
Boosting is a machine learning meta-algorithm that aims to iteratively build an ensemble of weak learners, in an attempt to generate a strong overall model.

Lets look at the highlighted parts one-by-one:

1. Weak Learners: A ‘weak learner’ is any ML algorithm (for regression/classification) that provides an accuracy slightly better than random guessing.
2.  
For example, consider a problem of binary classification with approximately 50% of samples belonging to each class. Random guessing in this case would yield an accuracy of around 50%. So a weak learner would be any algorithm, however simple, that slightly improves this score – say 51-55% or more. Usually, weak learners are pretty basic in nature. Some examples are Decision Stumps or smaller Decision Trees

Ensemble: The overall model built by Boosting is a weighted sum of all of the weak learners. The weights and training given to each ensures that the overall model yields a pretty high accuracy (sometimes state-of-the-art).

Iteratively build: Many ensemble methods such as bagging/random forests are capable of training their components in parallel. This is because the training of any of those weak learners does not depend on the training of the others. That is not the case with Boosting

At each step, Boosting tries to evaluate the shortcomings of the overall model built till the previous step, and then generates a weak learner to battle these shortcomings. This weak learner is then added to the total model. Therefore, the training must necessarily proceed in a serial/iterative manner.

Meta-algorithm: Since Boosting isn’t necessarily an ML algorithm by itself, but rather uses other (basic) algorithms to build a stronger one, it is said to be a ‘meta’ algorithm

What are the drawbacks of Boosting?
The most obvious drawback of boosting is the computational complexity.
The biggest criticism for Boosting comes from its sensitivity to noisy data.
https://codesachin.wordpress.com/2016/03/06/a-small-introduction-to-boosting/

Resources

https://github.com/opencv/opencv/tree/master/data/haarcascades

https://fairyonice.github.io/Object-detection-using-Haar-feature-based-cascade-classifiers-on-my-face.html

https://ieeexplore.ieee.org/document/990517
