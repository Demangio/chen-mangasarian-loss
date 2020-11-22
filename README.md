# Chen-Mangasarian-loss




This repo contains Keras implementation of Chen Mangasarian Loss [1], and an example notebook to use it.


Pinball Loss is defined by:

![Pinball](https://github.com/Demangio/chen-mangasarian-loss/blob/main/pictures/pinball.PNG?raw=true)

Chen Mangasarian Loss is a C2 approximation of Pinball Loss, defined by:

![Chen Mangasarian](https://github.com/Demangio/chen-mangasarian-loss/blob/main/pictures/chen_manga.PNG?raw=true)

Where <b>alpha</b> is the quantile probability (between 0 and 1 excluded), <b>x</b> the difference between quantile value and observed value, and <b>a</b> is a smoothing parameter.
Chen and Mangasarian have demonstrated that when a -> 0, their loss tends to Pinball Loss.

In addition to that, the loss was offset to keep the same minimum as Pinball for every quantile. It gave the best results for me.

Here is a plot to illustrate smoothing:

![](https://github.com/Demangio/chen-mangasarian-loss/blob/main/pictures/plot.PNG?raw=true)

[1] C., & Mangasarian, O. L. (1996). A class of smoothing functions for nonlinear and mixed complementarity problems. Computational Optimization and Applications, 5(2), 97–138. https://doi.org/10.1007/BF00249052
