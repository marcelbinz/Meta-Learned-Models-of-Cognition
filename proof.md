
## **Performance-based justification for Bayesian inference**

We proof that the predictive posterior distribution <img src="img/img1.svg" /> maximizes the log-likelihood of future observations averaged over the data-generating distribution:

<img src="img/img2.svg" />

The essence of this proof is to show that the predictive posterior distribution is superior to any other reference distribution <img src="img/img6.svg" /> in terms of the log-likelihood:

<img src="img/img3.svg" />

or equivalently that:

<img src="img/img4.svg" />

Proofing this conjecture is straightforward [1]:

<img src="img/img5.svg" />

Note that while we used sums in our proof, which assumes that relevant quantities take discrete values, the same ideas can be readily applied to continuous-valued quantities by replacing sums with integrals.

### **References:**

[1] Aitchison, J. (1975). Goodness of prediction fit. *Biometrika, 62(3)*, 547-554.

