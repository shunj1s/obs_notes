```python
np.random.poisson(lam=1.0, size=None)
```
$$f(k;\lambda) = \frac{\lambda^k e^{-\lambda}}{k!}$$
describes probability of $k$ events occurring within interval $\lambda$ 

commonly using a "signal to noise ratio"
higher the SNR the better

Why do we use poisson statistics?
- flux density measuring the average arrival rate of photons ($r$)
- Thus, the number of photons that are EXPECTED to arrive = $r\tau$, but actually differs
	- independent of earlier arrivals (uncorrelated)
- If we expect to detect ($N$) photons, we can expect to receive $N = N \pm \sqrt{N}$ during any given run
- thus, the probability of detecting exactly $N$ photons:
$$p(N) = \exp(-(N))\frac{(N)^N}{N!}$$
or:
$$p(N) = \exp(-r\tau)\frac{(r\tau)^N}{N!}$$
^ the poisson distribution!
most importantly:
$$\sigma = \sqrt{(N)} = \sqrt{r\tau}$$
