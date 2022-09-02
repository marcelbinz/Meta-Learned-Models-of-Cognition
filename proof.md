## **Performance-based justification for Bayesian inference**

We proof that the predictive posterior distribution $$p(x_{t+1} | x_{1:t})$$ maximizes the log-likelihood of future observations averaged over the data-generating distribution:

$$
\begin{equation*}
p(x_{t+1} | x_{1:t}) = \text{arg}\max_q \mathbb{E}_{p(\mu, x_{1:t+1})} \left[ \log q(x_{t+1} | x_{1:t})\right]
\end{equation*}
$$

The essence of this proof is to show that the predictive posterior distribution is superior to any other reference distribution $$r(x_{t+1} | x_{1:t})$$ in terms of the log-likelihood:

$$
\begin{align*}
    \mathbb{E}_{p(\mu, x_{1:t})} \left[
	\log p(x_{t+1}  | x_{1:t}) \right] \geq \mathbb{E}_{p(\mu, x_{1:t})} \left[
	\log r(x_{t+1} | x_{1:t}) \right]
\end{align*}
$$

or equivalently that:

$$
\begin{align*}
    \mathbb{E}_{p(\mu, x_{1:t})} \left [ \log \frac{p(x_{t+1}  | x_{1:t})}{r(x_{t+1}  | x_{1:t})} \right] \geq 0
\end{align*}
$$

Proofing this conjecture is straightforward [1]:

$$\begin{align*}
    &\mathbb{E}_{p(\mu, x_{1:t})} \left [ \log \frac{p(x_{t+1}  | x_{1:t})}{r(x_{t+1}  | x_{1:t})} \right] \\
	= &\sum_{\mu} \sum_{x_{1:t}} \sum_{x_{t+1}} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} p(x_{t+1} | \mu )p(x_{1:t} | \mu) p(\mu)\\
	= &\sum_{x_{1:t}} \sum_{\mu} \sum_{x_{t+1}} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} p(x_{t+1} | \mu )p(x_{1:t} | \mu) p(\mu)\\
	= &\sum_{x_{1:t}} \sum_{\mu} \sum_{x_{t+1}} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} p(x_{t+1} | \mu )p(\mu | x_{1:t}) p(x_{1:t})\\
	= &\sum_{x_{1:t}} \left[ \sum_{\mu} \sum_{x_{t+1}} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} p(x_{t+1} | \mu )p(\mu | x_{1:t}) \right] p(x_{1:t})\\
	= &\sum_{x_{1:t}} \left[ \sum_{x_{t+1}} \sum_{\mu} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} p(x_{t+1} | \mu )p(\mu | x_{1:t}) \right] p(x_{1:t})\\
	= &\sum_{x_{1:t}} \left[ \sum_{x_{t+1}} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} \left[\sum_{\mu} p(x_{t+1} | \mu )p(\mu | x_{1:t})  \right] \right] p(x_{1:t})  \\
	= &\sum_{x_{1:t}} \left[ \sum_{x_{t+1}} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} p(x_{t+1} | x_{1:t})  \right] p(x_{1:t}) \\
	= &\sum_{x_{1:t}} \text{KL} \left[p(x_{t+1} | x_{1:t}) || r(x_{t+1} | x_{1:t}) \right] p(x_{1:t})\\
	&\geq 0
\end{align*}
$$

Note that while we used sums in our proof, which assumes that relevant quantities take discrete values, the same ideas can be readily applied to continuous-valued quantities by replacing sums with integrals.

### **References:**

[1] Aitchison, J. (1975). Goodness of prediction fit. *Biometrika, 62(3)*, 547-554.
