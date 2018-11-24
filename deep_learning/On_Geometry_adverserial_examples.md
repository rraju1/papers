# On the Geometry of Adversarial Examples

This paper looks at the existance of adversarial examples. This is a pretty mathy paper so it's kind of hard to hack through. The main idea seems to be that the data we sample from is from a low dimensional structure which is embedded high dimensional space. 

Their analysis apparent shows that the codimension, the difference between the dimension of data manifold and the dimension of the embeddeding space, is a key source of adversarial examples. 

In the intro, they want to make 3 things clear:
 1. being robust to one kind of norm, l_2, doesn't guaruntee robustness against another type of attack
 2. Adverserial training is not sufficient in providing robust
 3. NN classifier does not suffer from this due to decision boundary being away from the data(?)

It seems like the problem that this paper is trying to bring up is that our decision boundaries are too low dimensional. 

https://arxiv.org/abs/1811.00525