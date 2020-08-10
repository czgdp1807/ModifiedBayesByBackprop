Modified Bayes By Backprop
==========================

About
-----

Our work, which builds on top of the work done by Blundell et. al, 2015, has made the following three contributions,

1. We have modified the Bayes by Backprop algorithm developed by Blundell et. al, for learning probability distributions over the weights of a neural network. We have decoupled the Negative Log Likelihood (NLL) and KL divergence components of the cost function. This trick enables using weights of a pre-trained neural network as means of the underlying distribution of the weights, which then requires only optimising the cost function over the variance of the distribution of the weights. The experiments conducted also showed that the means of the distribution of weights is associated with the NLL component of the cost function and variance is associated with the KL divergence component.

2. After training the neural network using our algorithm we provided it with both in distribution and OOD inputs and compared the uncertainties predicted for both the cases. We observed that the uncertainties predicted for the former case were significantly lower than those for the later case.

3. We also analyzed the uncertainties predicted by our neural network for adversarial inputs generated using FGSM (Goodfellow et. al, 2015). We observed that uncertainties predicted were similar to those for OOD inputs. This helped us in concluding that our neural network was capable of detecting adversarial inputs thus being more secure than ANNs using point estimates.

Experimenting
-------------

You can experiment with the notebooks in this repository if you have the access to a Google account. Just follow the steps given below,

1. Clone this repository.
2. Upload the folder `bnn`, under this project root, to your Google drive. Make sure, it should be directly under, `/content/drive/My Drive`.
3. Open the notebooks using https://colab.research.google.com/ and you are good to go.

Note that, when the notebook will mount the drive, once you exectue the first cell, you should choose that Google account where you uploaded the bnn folder.

There are some pre-trained weights available under, `bnn/weights/mnist` for ready use.