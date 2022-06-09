# Bode Plot
**A graph of the frequency response of a system.**

A *Bode plot* is a combination of a *magnitude* plot and a [[phase]] plot, using [[Decibel|decibels]] and *degrees* respectively, both of which are plotted against *frequency* in $\text{rad/s}$.

The frequency is shown on a *logarithmic scale*, with markings at every *power of 10*.

Bode plots only plot the magnitude and phase along the *imaginary* axis of the $s$-plane, that is, only when $s=j\omega$.

The *origin* is defined as where $\omega=1$ and $\log\omega=0$ or equivalently, where the gain is *zero*. Note that $\omega=0$ is *never* on a Bode plot as $\log_{10} 0$ does not exist.

A hand-drawn *approximate* Bode plot will consist of a *piecewise* construction of *straight line segments* and can be constructed from a *factorised* [[transfer function]] or a [[Transfer Function#Standard transfer function|standard]] one.

## Approximate plots from a transfer function
A *reference level* for the magnitude plot is typically found by considering the behaviour of the function at *low frequencies* as $\omega\rightarrow 0$. High frequencies as $\omega\rightarrow\infty$ can also be used.

A *reference phase* is found by considering the behaviour of the function for $\omega\rightarrow 0$. If the transfer function is *negative* at this limit, then the starting phase is $\pm 180^{\circ}$.

If a reference cannot be determined due to the *inexistence* of the above limits, then the transfer function must be *evaluated* at a particular frequency, preferably one far from any poles or zeroes and where the function is *constant*.

A general factorised or standard transfer function is of the following form. The process for both are the same.
$$\mathbf{H}(s)=A\prod\frac{f_{n}}{g_{n}}$$
where $f_{n}$ and $g_{n}$ are *factors*. The entire Bode plot is a [[superposition]] or the *graphical sum* of the *individual contributions* of the factors.

The *magnitude* contribution of a factor is given in decibels by
$$\text{dB}_{f}=20\log_{10}|f_{n}|$$
The *phase* contribution of a factor is given by
$$\phi_{f}=\tan^{-1}\frac{\omega}{x_{n}}=
\begin{cases}
0^{\circ} & \omega\rightarrow0 \\
45^{\circ} & \omega=x_{n} \\
90^{\circ} & \omega\rightarrow\infty \\
\end{cases}$$
where $x_{n}$ is either a zero or a pole, depending on the factor. Note that as it is sufficient to analyse only $s=j\omega$, the above phase formula is also sufficient.

Below are some types of factors found in transfer functions.

### Gain
The *gain* is a constant term in the transfer function, typically denoted by $A$.

On a Bode plot, a *positive* gain appears as a *constant magnitude* of $20\log_{10}A$ and 
*constant phase* of $0^{\circ}$.

A *negative* gain will appear as a constant magnitude of $20\log_{10}|A|$ and a constant phase of $\pm180^{\circ}$.

### Simple poles and zeroes, including at the origin
*Simple* poles and zeroes are of the following form in a factorised and standard transfer function, respectively.
$$(s+z_{n})^{a_{n}}\quad(s+p_{n})^{b_{n}}\quad\text{or}\quad\left(1+\frac{s}{z_{n}}\right)^{a_{n}}\quad\left(1+\frac{s}{p_{n}}\right)^{b_{n}}$$
#### Magnitude plot
The slope of the magnitude plot changes at all *break points* $\omega=z_{n}$ or $\omega=p_{n}$.
- For a *zero*, the slope changes to $20a_{n}\;\text{dB/decade}$.
- For a *pole*, the slope changes to $-20b_{n}\;\text{dB/decade}$.

If the zero or pole is at the *origin*, that is, when $z_{n}$ or $p_{n}=0$, then the slope follows the above rules except it must *pass through* $\omega=1$.

#### Phase plot
The slopes of the phase plot are *centred* at the zeroes or the poles.
- For a *zero*, the slope is an *increase* of ${90a_{n}}^{\circ}$ over *exactly two decades*.
- For a *pole*, the slope is a *decrease* of ${90b_{n}}^{\circ}$ over *exactly two decades*.

If the zero or pole is at the *origin*, then the plot is a *constant* $+{90a_{n}}^{\circ}$ or $-{90b_{n}}^{\circ}$, respectively.

### Quadratic poles and zeroes
*Quadratic* poles and zeroes of the following forms arise in [[Second Order Circuit|second order circuits]].
$$(s^{2}+2\alpha s+\omega_{n}^{2})^{N}\quad\text{or}\quad\left(\frac{s^{2}}{\omega_{n}^{2}}+\frac{2\alpha}{\omega_{n}}+1\right)^{N}$$
The *break point* of a quadratic factor is its *natural frequency*, $\omega_{n}$.

The Bode plot of quadratic poles and zeroes are the same as if there was a twice repeated pole or zero at the natural frequency.

#### Magnitude plot
The slope of the magnitude plot changes at all *break points*.
- For a *zero*, the slope changes to $40N\;\text{dB/decade}$.
- For a *pole*, the slope changes to $-40N\;\text{dB/decade}$. 

#### Phase plot
The slopes of the phase plot are *centred* at the zeroes or the poles.
- For a *zero*, the slope is an *increase* of $180N^{\circ}$ over *two decades*.
- For a *pole*, the slope is a *decrease* of $180N^{\circ}$ over *two decades*.

## Examples
### Approximate plot from a transfer function with a gain and simple poles and zeroes
$$\mathbf{H}(s)=\frac{10(s+100)}{s+1}$$
#### Magnitude plot
For the above transfer function, the sum of the *individual contributions* of the factors to the magnitude are
$$\begin{align*}
H(s)\;\text{dB}&=20\log_{10}10+20\log_{10}|s+100|+20\log_{10}\frac{1}{|s+1|} \\
&=20\log_{10}10+20\log_{10}|s+100|-20\log_{10}|s+1|
\end{align*}$$
These individual contributions can be plotted, with the plot before the break point *approximated* with the limit as $s\rightarrow 0$.

![[BodePlotFactorisedSimpleMagnitudeComponents.svg]]

The entire *approximate* Bode magnitude plot is the *graphical sum* of the individual contributions and is thus

![[BodePlotFactorisedSimpleMagnitude.svg|600]]

Graphically, the sum of the individual plots is $20\;\text{dB}+40\;\text{dB}+0\;\text{dB}=60\;\text{dB}$ until the first break point at $\omega=1$. Past this point, the factor $(s+1)^{-1}$ contributes a *decrease* of $20\;\text{dB/decade}$. However, past the second break point at $\omega=100$, the factor $s+100$ contributes an *increase* of $20\;\text{dB/decade}$ which *cancels out* the contribution of the previous factor.

Note that the magnitude plot agrees with the limits of the magnitude of the transfer function for low and high frequencies.
$$\lim_{\omega\rightarrow0}H(s)=1000\rightarrow60\;\text{dB}\qquad\lim_{\omega\rightarrow\infty}H(s)=10\rightarrow20\;\text{dB}$$
#### Phase plot
The sum of the individual contributions of the factors to the phase are
$$\phi=0^{\circ}+\tan^{-1}\frac{\omega}{100}-\tan^{-1}\frac{\omega}{1}$$
The entire approximate Bode phase plot is thus

![[BodePlotFactorisedSimplePhase.svg]]

Graphically, the phase is initially a constant $0^{\circ}$ until $10^{-1}$ where the factor $(s+1)^{-1}$ contributes a $90^{\circ}$ *decrease* over *exactly* two decades centred at $\omega=1$. The factor $s+100$ then *cancels out* the previous contribution by adding a $90^{\circ}$ *increase* over *exactly* two decades centred at $\omega=10^{2}$.

### Approximate plot from a transfer function with a gain, zero at the origin, and simple pole
$$\mathbf{H}(s)=\frac{10s}{s+1}$$
#### Magnitude plot
Note that the zero is at the origin and thus there is only *one break point* that can be plotted.

Due to the zero at the origin, the plot for $\omega<1$ must be an *upwards slope* of $20\;\text{dB/decade}$.

To determine the magnitude at which the break point occurs, the limit as $\omega\rightarrow\infty$ is used.
$$\lim_{\omega\rightarrow\infty}H(s)=10\rightarrow20\;\text{dB}$$
Thus, the approximate magnitude plot is

![[BodePlotFactorisedOriginMagnitude.svg|600]]

#### Phase plot
The gain and the zero at the origin contributes a *constant* phase of $0^{\circ}$ and $90^{\circ}$, respectively.

Centred at $\omega=1$ is a slope of $-90^{\circ}$ over *exactly* two decades contributed by the $s+1$ factor.

Thus, the approximate phase plot is
![[BodePlotFactorisedOriginPhase.svg|600]]
