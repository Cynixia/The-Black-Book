# Fourier Series
**Any non-sinusoidal [[periodic function]] can be expressed as an infinite sum of [[Sinusoid|sinusoidal functions]].**
In trigonometric form,
$$f(t)=a_{0}+\sum_{n=1}^{\infty}(a_{n}\cos n\omega_{0}t+b_{n}\sin n\omega_{0}t)$$
The *fundamental* [[angular frequency]] or *1st harmonic*, $\omega_{0}$, is given by
$$\omega_{0}=\frac{2\pi}{T}$$
The *nth harmonic* angular frequency, $\omega_{n}$, is an *integer multiple* of the fundamental frequency.
$$\omega_{n}=n\omega_{0}$$
The constant term, $a_{0}$, is also known as the *DC component*. It can be thought of as the initial offset of the function.
$$a_{0}=\frac{1}{T}\int_{0}^{T}f(t)\;dt$$
The *Fourier coefficients*, $a_n$ and $b_{n}$, are given by
$$\begin{align*}
a_{n}&=\frac{2}{T}\int_{0}^{T}f(t)\cos n\omega_{0}t\;dt \\
b_{n}&=\frac{2}{T}\int_{0}^{T}f(t)\sin n\omega_{0}t\;dt
\end{align*}$$
Note that for all the above integrals, the *interval of integration* can be moved as long as the *length* of the interval *equals* the period.

## Amplitude-phase form
$$f(t)=a_{0}+\sum_{n=1}^{\infty}A_{n}cos(n\omega_{0}t+\phi_{n})$$
The *amplitude* and [[phase]] are related to the Fourier coefficients by
$$A_{n}=\sqrt{a_{n}^{2}+b_{n}^{2}}\qquad \phi_{n}=-\tan^{-1}\frac{b_{n}}{a_{n}}$$
## Exponential form
The Fourier series can also be expressed in *complex* or *exponential* form.
$$f(t)=\sum_{n=-\infty}^{\infty}c_{n}e^{in\omega_{0}t}$$
The coefficient, $c_n$, can be found via
$$c_{n}=\frac{1}{T}\int_{0}^{T}f(t)e^{-in\omega_{0}t}\;dt$$
## Additional notes
Due to [[Symmetry of Waveforms and their Fourier Series|symmetry]], some waveforms have some non-existing coefficients and coefficients with simpler calculations.

The coefficients of *all three forms* of the Fourier series are related by
$$A_{n}\angle\phi_{n}=a_{n}-ib_{n}=2c_{n}$$
For expressing coefficients it is useful to know values of the cosine, sine, and complex exponential function at [[List of Trigonometric Identities#Integral multiples of pi|integer multiples]] of $\pi$.

