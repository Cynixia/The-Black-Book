# Transfer Function
**The frequency dependent [[phasor]] ratio of the output to the input of a circuit.**
$$\mathbf{H}(s)=\frac{\mathbf{Y}(s)}{\mathbf{X}(s)}$$
In most applications, it is sufficient to define $s=j\omega$ for the purpose of analysing the *frequency response*.

There are four possible *transfer* or *network functions*.
$$\begin{align*}
\text{Voltage gain, }\mathbf{H}(s)&=\frac{\mathbf{V}_\text{o}(s)}{\mathbf{V}_\text{i}(s)} \\
\text{Current gain, }\mathbf{H}(s)&=\frac{\mathbf{I}_\text{o}(s)}{\mathbf{I}_\text{i}(s)} \\
\text{Transfer impedance, }\mathbf{H}(s)&=\frac{\mathbf{V}_\text{o}(s)}{\mathbf{I}_\text{i}(s)} \\
\text{Transfer admittance, }\mathbf{H}(s)&=\frac{\mathbf{I}_\text{o}(s)}{\mathbf{V}_\text{i}(s)} \\
\end{align*}$$
The transfer function is a *complex-valued* function and thus has an associated *magnitude* $H(s)$ and [[phase]] $\phi$.

The *denominator* of the transfer function of a circuit is also the [[Characteristic Equation#Linear differential equations|characteristic equation]] of the circuit.

For the purpose of constructing [[Bode Plot|Bode plots]], transfer functions are either *factorised* or converted into *standard form*.

## Standard transfer function
**A form of a transfer function where all zeroes and poles are divided out.**

Also known as a *general* transfer function, a standard transfer function is the most common form of a transfer function.
$$\mathbf{H}(s)=\frac{A\left(1+\frac{s}{z_{1}}\right)^{a_{1}}\left(1+\frac{s}{z_{2}}\right)^{a_{2}}\cdots}{\left(1+\frac{s}{p_{1}}\right)^{a_{1}}\left(1+\frac{s}{p_{2}}\right)^{a_{2}}\cdots}$$