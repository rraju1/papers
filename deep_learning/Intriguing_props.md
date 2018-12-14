# Intriguing properties of neural networks

This is a very important paper because it is the one that introduces the notion of adverserial examples in ML.

There are 2 claims made in the abstract:
  1. There is no distinction between individual high level units and random linear combinations of high level units.
  2. Neural nets are discontinous in their mapping and adverserial examples exist to misclassify the network by perturbing the input slightly at an imperceptible level.
  
I will make the first claim more clear. Previously as described in the paper, it was speculated that, at higher layers, individual neurons acted as a distinguished basis for extracting semantic information. However, after, experimenting and masking all the activations between normal basis and random basis, these end up practically being the same. Rather than individual units, it seems that it is some set of linear combination of units that are able to capture all these features.

This was done on MNSIT and ImageNet with performing an inner product on the activation and a basis vector. One was with a natural basis and one with a random basis. This is shown in Figures 1, 2 for MNIST and 3, 4 for ImageNet. This segways into the fact that this could have counterintuitive properties as we'll see with adverserial examples.

The paper goes on to describe that these deep layers are a way to encode a non-local generalization prior over the input space. What this means in laymen terms is that output unit can assign non-significant probabilities over regions where there are no training examples. The underlying assumption here is adding a small perturbation won't impact the output very much. However as we know this is false and definitely not the case.

The paper describes an optimization method that minimizes the 2-norm of r, the perterbation, s.t. f(x + r) = l, x + r exist in [0,1]. This is a difficult problem to solve so they use box-constrained L-BFGS to get an approximation. See the paper for more concrete details. In Tables 1, 2, they prove that the generalization error over these examples is terrible. They also ran an experiment where they split the training set of MNIST and these adverserial examples still existed. So transferiability is an issue. And in the last section, they go over an analysis of the Lipschitz constants in each layer. Their conclusion was is that penalizing the upper bound of the Lipschitz constant may be useful. 

Slides on Bo Li's website: [Slides](http://nebula.wsimg.com/3b1c9dcbb65e2367da1d1ad685a8360b?AccessKeyId=619655DB521D0ED197FE&disposition=0&alloworigin=1)

https://arxiv.org/pdf/1312.6199.pdf
