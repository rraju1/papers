# TAMING THE WAVES: SINE AS ACTIVATION FUNCTION IN DEEP NEURAL NETWORKS

This paper is looking at sine as an activation function. The purpose of looking at this paper was that the idea of the periodicity
of the activation was interesting. We thought of using this idea for seeing if the model was able not be dominated by a single feature, e.g. some tape on a stop sign.

One of the problems with using sine as an activation function is that it falls into many local minima. See Fig. 1. 

Also, not sure how the loss landscape can be defined as the integral of the loss function. (look at Goodfellow paper)

If data has large amount of low frequencies, this can be avoided as seen in Figure 3 where the global optimum is near w=0. Basically, take away is that w's cannot be large.

Is there any difference between truncated sine and tanh?

Empricial evaluations show that sin periodicty is getting ignored. => should test out in terms of big activations what happens.

what happens in swapping activations after training with relu?

https://openreview.net/pdf?id=Sks3zF9eg
