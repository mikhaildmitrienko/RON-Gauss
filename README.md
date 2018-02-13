# RON-Gauss

RON-Gauss is a system for non-interactive differentially-private data release. The implementation is based on the following paper:

*Thee Chanyaswad, Changchang Liu, and Prateek Mittal. “Coupling Random Orthonormal Projection with Gaussian Generative Model for Non-Interactive Private Data Release.” arXiv preprint arXiv:1709.00054 (2017).* (https://arxiv.org/abs/1709.00054)

Hence, please refer to this paper for more detail on the RON-Gauss model.

The implementation is for all three algorithms proposed in the paper.

## How to:

The main class to run the system is the `RON-Gauss` class. This class is initialized with three parameters:
- `algorithm` = `unsupervised`, `supervised`, or `gmm`;
- `epilonMean` = the epsilon value used for deriving the sample mean;
- `epsilonCov` = the epsilon value used for deriving the sample covariance.

The main method is the `generate_dpdata`, which takes in, among others, the private data and the dimension to reduce the data to. It then returns the differentially-private synthesized data according to the parameters set in the initialization.

Some details on the inputs of `generate_dpdata`:
1) For the `unsupervised` algorithm, only the feature data matrix `X` is needed. 
2) For the `supervised` algorithm, in addition to `X`, the training label `y` is also required, along with its range `maxY`. 
3) For the `gmm` algorithm, both `X` and `y` are required, and `y` should be the class label.


### Prerequisites

The implementation is in Python 2 and `numpy` and `scipy` are required.


## Author

* **Thee Chanyaswad**

