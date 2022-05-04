# Laplace Transform Circuit Element Model
To use the [[Laplace transform]] for circuit analysis, circuit elements must be converted to a model in the *complex frequency domain* before applying steady-state analysis methods. The [[Laplace Transform#Inverse Laplace transform|inverse transform]] of the solution can then be taken to retrieve the solution in the *time domain*.

The conversion is done by taking the Laplace transform of equations established in the time domain, such as [[Ohm's law]].

## Resistor
The properties of a resistor does not depend on frequency. Thus,
$$V(s)=RI(s)$$
## Inductor
For an [[inductor]],
$$\begin{align*}
V(s)&=sLI(s)-Li(0^+) \\
I(s)&=\frac{1}{sL}V(s)+\frac{i(0^+)}{s}
\end{align*}$$

![[InductorLaplace.svg]]

## Capacitor
For a [[capacitor]],
$$\begin{align*}
I(s)&=sCV(s)-Cv(0^{+})\\
V(s)&=\frac{1}{sC}I(s)+\frac{v(0^+)}{s}
\end{align*}$$

![[CapacitorLaplace.svg]]