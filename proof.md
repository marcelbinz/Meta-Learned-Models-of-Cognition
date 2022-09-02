
## **Performance-based justification for Bayesian inference**

We proof that the predictive posterior distribution <img src="https://i.upmath.me/svg/p(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)" alt="p(x_{t+1} | x_{1:t})" /> maximizes the log-likelihood of future observations averaged over the data-generating distribution:

<img src="https://i.upmath.me/svg/%0A%5Cbegin%7Bequation*%7D%0Ap(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%20%3D%20%5Ctext%7Barg%7D%5Cmax_q%20%5Cmathbb%7BE%7D_%7Bp(%5Cmu%2C%20x_%7B1%3At%2B1%7D)%7D%20%5Cleft%5B%20%5Clog%20q(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%5Cright%5D%0A%5Cend%7Bequation*%7D%0A" alt="
\begin{equation*}
p(x_{t+1} | x_{1:t}) = \text{arg}\max_q \mathbb{E}_{p(\mu, x_{1:t+1})} \left[ \log q(x_{t+1} | x_{1:t})\right]
\end{equation*}
" />

The essence of this proof is to show that the predictive posterior distribution is superior to any other reference distribution <img src="https://i.upmath.me/svg/r(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)" alt="r(x_{t+1} | x_{1:t})" /> in terms of the log-likelihood:

<img src="https://i.upmath.me/svg/%0A%5Cbegin%7Balign*%7D%0A%20%20%20%20%5Cmathbb%7BE%7D_%7Bp(%5Cmu%2C%20x_%7B1%3At%7D)%7D%20%5Cleft%5B%0A%09%5Clog%20p(x_%7Bt%2B1%7D%20%20%7C%20x_%7B1%3At%7D)%20%5Cright%5D%20%5Cgeq%20%5Cmathbb%7BE%7D_%7Bp(%5Cmu%2C%20x_%7B1%3At%7D)%7D%20%5Cleft%5B%0A%09%5Clog%20r(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%20%5Cright%5D%0A%5Cend%7Balign*%7D%0A" alt="
\begin{align*}
    \mathbb{E}_{p(\mu, x_{1:t})} \left[
	\log p(x_{t+1}  | x_{1:t}) \right] \geq \mathbb{E}_{p(\mu, x_{1:t})} \left[
	\log r(x_{t+1} | x_{1:t}) \right]
\end{align*}
" />

or equivalently that:

<img src="https://i.upmath.me/svg/%0A%5Cbegin%7Balign*%7D%0A%20%20%20%20%5Cmathbb%7BE%7D_%7Bp(%5Cmu%2C%20x_%7B1%3At%7D)%7D%20%5Cleft%20%5B%20%5Clog%20%5Cfrac%7Bp(x_%7Bt%2B1%7D%20%20%7C%20x_%7B1%3At%7D)%7D%7Br(x_%7Bt%2B1%7D%20%20%7C%20x_%7B1%3At%7D)%7D%20%5Cright%5D%20%5Cgeq%200%0A%5Cend%7Balign*%7D%0A" alt="
\begin{align*}
    \mathbb{E}_{p(\mu, x_{1:t})} \left [ \log \frac{p(x_{t+1}  | x_{1:t})}{r(x_{t+1}  | x_{1:t})} \right] \geq 0
\end{align*}
" />

Proofing this conjecture is straightforward [1]:

<img src="https://i.upmath.me/svg/%5Cbegin%7Balign*%7D%0A%20%20%20%20%26%5Cmathbb%7BE%7D_%7Bp(%5Cmu%2C%20x_%7B1%3At%7D)%7D%20%5Cleft%20%5B%20%5Clog%20%5Cfrac%7Bp(x_%7Bt%2B1%7D%20%20%7C%20x_%7B1%3At%7D)%7D%7Br(x_%7Bt%2B1%7D%20%20%7C%20x_%7B1%3At%7D)%7D%20%5Cright%5D%20%5C%5C%0A%09%3D%20%26%5Csum_%7B%5Cmu%7D%20%5Csum_%7Bx_%7B1%3At%7D%7D%20%5Csum_%7Bx_%7Bt%2B1%7D%7D%20%5Clog%20%5Cfrac%7Bp(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%7Br(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%20p(x_%7Bt%2B1%7D%20%7C%20%5Cmu%20)p(x_%7B1%3At%7D%20%7C%20%5Cmu)%20p(%5Cmu)%5C%5C%0A%09%3D%20%26%5Csum_%7Bx_%7B1%3At%7D%7D%20%5Csum_%7B%5Cmu%7D%20%5Csum_%7Bx_%7Bt%2B1%7D%7D%20%5Clog%20%5Cfrac%7Bp(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%7Br(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%20p(x_%7Bt%2B1%7D%20%7C%20%5Cmu%20)p(x_%7B1%3At%7D%20%7C%20%5Cmu)%20p(%5Cmu)%5C%5C%0A%09%3D%20%26%5Csum_%7Bx_%7B1%3At%7D%7D%20%5Csum_%7B%5Cmu%7D%20%5Csum_%7Bx_%7Bt%2B1%7D%7D%20%5Clog%20%5Cfrac%7Bp(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%7Br(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%20p(x_%7Bt%2B1%7D%20%7C%20%5Cmu%20)p(%5Cmu%20%7C%20x_%7B1%3At%7D)%20p(x_%7B1%3At%7D)%5C%5C%0A%09%3D%20%26%5Csum_%7Bx_%7B1%3At%7D%7D%20%5Cleft%5B%20%5Csum_%7B%5Cmu%7D%20%5Csum_%7Bx_%7Bt%2B1%7D%7D%20%5Clog%20%5Cfrac%7Bp(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%7Br(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%20p(x_%7Bt%2B1%7D%20%7C%20%5Cmu%20)p(%5Cmu%20%7C%20x_%7B1%3At%7D)%20%5Cright%5D%20p(x_%7B1%3At%7D)%5C%5C%0A%09%3D%20%26%5Csum_%7Bx_%7B1%3At%7D%7D%20%5Cleft%5B%20%5Csum_%7Bx_%7Bt%2B1%7D%7D%20%5Csum_%7B%5Cmu%7D%20%5Clog%20%5Cfrac%7Bp(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%7Br(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%20p(x_%7Bt%2B1%7D%20%7C%20%5Cmu%20)p(%5Cmu%20%7C%20x_%7B1%3At%7D)%20%5Cright%5D%20p(x_%7B1%3At%7D)%5C%5C%0A%09%3D%20%26%5Csum_%7Bx_%7B1%3At%7D%7D%20%5Cleft%5B%20%5Csum_%7Bx_%7Bt%2B1%7D%7D%20%5Clog%20%5Cfrac%7Bp(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%7Br(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%20%5Cleft%5B%5Csum_%7B%5Cmu%7D%20p(x_%7Bt%2B1%7D%20%7C%20%5Cmu%20)p(%5Cmu%20%7C%20x_%7B1%3At%7D)%20%20%5Cright%5D%20%5Cright%5D%20p(x_%7B1%3At%7D)%20%20%5C%5C%0A%09%3D%20%26%5Csum_%7Bx_%7B1%3At%7D%7D%20%5Cleft%5B%20%5Csum_%7Bx_%7Bt%2B1%7D%7D%20%5Clog%20%5Cfrac%7Bp(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%7Br(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%7D%20p(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%20%20%5Cright%5D%20p(x_%7B1%3At%7D)%20%5C%5C%0A%09%3D%20%26%5Csum_%7Bx_%7B1%3At%7D%7D%20%5Ctext%7BKL%7D%20%5Cleft%5Bp(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%20%7C%7C%20r(x_%7Bt%2B1%7D%20%7C%20x_%7B1%3At%7D)%20%5Cright%5D%20p(x_%7B1%3At%7D)%5C%5C%0A%09%26%5Cgeq%200%0A%5Cend%7Balign*%7D%0A" alt="\begin{align*}
    &amp;\mathbb{E}_{p(\mu, x_{1:t})} \left [ \log \frac{p(x_{t+1}  | x_{1:t})}{r(x_{t+1}  | x_{1:t})} \right] \\
	= &amp;\sum_{\mu} \sum_{x_{1:t}} \sum_{x_{t+1}} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} p(x_{t+1} | \mu )p(x_{1:t} | \mu) p(\mu)\\
	= &amp;\sum_{x_{1:t}} \sum_{\mu} \sum_{x_{t+1}} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} p(x_{t+1} | \mu )p(x_{1:t} | \mu) p(\mu)\\
	= &amp;\sum_{x_{1:t}} \sum_{\mu} \sum_{x_{t+1}} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} p(x_{t+1} | \mu )p(\mu | x_{1:t}) p(x_{1:t})\\
	= &amp;\sum_{x_{1:t}} \left[ \sum_{\mu} \sum_{x_{t+1}} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} p(x_{t+1} | \mu )p(\mu | x_{1:t}) \right] p(x_{1:t})\\
	= &amp;\sum_{x_{1:t}} \left[ \sum_{x_{t+1}} \sum_{\mu} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} p(x_{t+1} | \mu )p(\mu | x_{1:t}) \right] p(x_{1:t})\\
	= &amp;\sum_{x_{1:t}} \left[ \sum_{x_{t+1}} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} \left[\sum_{\mu} p(x_{t+1} | \mu )p(\mu | x_{1:t})  \right] \right] p(x_{1:t})  \\
	= &amp;\sum_{x_{1:t}} \left[ \sum_{x_{t+1}} \log \frac{p(x_{t+1} | x_{1:t})}{r(x_{t+1} | x_{1:t})} p(x_{t+1} | x_{1:t})  \right] p(x_{1:t}) \\
	= &amp;\sum_{x_{1:t}} \text{KL} \left[p(x_{t+1} | x_{1:t}) || r(x_{t+1} | x_{1:t}) \right] p(x_{1:t})\\
	&amp;\geq 0
\end{align*}
" />

Note that while we used sums in our proof, which assumes that relevant quantities take discrete values, the same ideas can be readily applied to continuous-valued quantities by replacing sums with integrals.

### **References:**

[1] Aitchison, J. (1975). Goodness of prediction fit. *Biometrika, 62(3)*, 547-554.

