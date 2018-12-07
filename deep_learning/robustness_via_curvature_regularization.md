# Robustness via curvature regularization, and vice versa

This paper examines the relationship between curvature of the loss function and adversarial robustness. This work seems very similar to the FMS simulations I was working on previously. Based on that I'm already skeptical of this paper, since in practice(unless I had a bug in my implementation), adding the regularizer does not confer much robustness benefit. And also to be fair this was on MNIST while they are using CIFAR10 and SVHN.

I do like how Figure 1 was laid out. It really made the point obvious that adversarial fine-tuning pushed examples away from the decision boundary.

In the related works section, they mentioned that the linearity, on the contrary, was not a problem. This is troubling because in the Goodfellow FGSM paper and [On the Geometry of Adversarial Examples](https://github.com/rraju1/papers/blob/master/deep_learning/On_Geometry_adverserial_examples.md), they both point out the issue of using a low-dimensional decision boundary to seperate high-dim data.

Not sure why to take the Hessian of loss wrt input pixels. What does this signify? 

Figure 2 is used to show the loss with ad training is in a flat minima? Flat minima gives robustness?
Figure 3 is pretty cool which shows that I am far from the decision boundary with fine tuning. (Don't I show this Fig 1)?

I can't comment on the mathematics because I don't really understand if the quadratic approximation is even valid so I have to assume it's right. Analysis of proof is also just unclear
Results are compared to PGD but accuracy is actually bad like 45% with 20 iterations. Maybe this is impressive? I should look at this attack

Overall, I'm feeling like I don't really know about this one, chief. 

https://arxiv.org/pdf/1811.09716.pdf
