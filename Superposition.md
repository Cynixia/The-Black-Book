# Superposition
**The principle that for all linear systems, the net response caused by several stimuli is the sum of the responses caused by each stimulus individually.**

A function $F(x)$ is a linear function if it satisfies the superposition principle. Superposition is defined by the properties of *additivity* and *homogeneity* for any scalar $a$.
$$\begin{align*} F(x_{1}+x_{2})&=F(x_{1})+F(x_{2}) \\
F(ax)&=aF(x)
\end{align*}$$

## Circuit analysis
Superposition is useful for analysing [[Linear Circuit|linear circuits]] with different independent sources. It is also the only method of analysing circuits whose sources are of *different frequencies*. Such circuits require *separate frequency domains* and must have their individual responses added in the *time domain*.

When analysing the response to one individual source, all other *independent* sources are disabled.
- When a *current source* is disabled, it is replaced by an *open circuit*.
- When a *voltage source* is disabled, it is replaced by a *short circuit*.
