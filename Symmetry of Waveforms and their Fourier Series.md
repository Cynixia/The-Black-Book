# Symmetry of Waveforms and their Fourier Series
## Even symmetry
An even function is *symmetrical* about the *vertical axis*. A function is *even* if it satisfies
$$f(-x)=f(x)$$
Its Fourier coefficients can be simplified to
$$\begin{align*}
a_{0}&=\frac{2}{T}\int_{0}^{\frac{T}{2}}f(t)\;dt \\
a_{n}&=\frac{4}{T}\int_{0}^{\frac{T}{2}}f(t)\cos n\omega_{0}t\;dt \\
b_{n}&=0
\end{align*}$$
![[EvenFunction.svg|550]]

## Odd symmetry
An odd function is *rotationally symmetrical* around the *origin*. A function is *odd* if it satisfies
$$f(-x)=-f(x)$$
Its Fourier coefficients can be simplified to
$$\begin{align*}
a_{0}&=0 \\
a_{n}&=0 \\
b_{n}&=\frac{4}{T}\int_{0}^{\frac{T}{2}}f(t)\sin n\omega_{0}t\;dt
\end{align*}$$
![[OddFunction.svg|550]]

## Half-wave symmetry
A function with half-wave symmetry has half-cycles with are *mirror images* of *adjacent* half-cycles. A function is *half-wave symmetric* if
$$f(t-\frac{T}{2})=-f(t)$$
Its Fourier coefficients can be simplified to
$$\begin{align*}
a_{0}&=0 \\
a_{n}&=\begin{cases} \frac{4}{T}\int_{0}^{\frac{T}{2}}f(t)\cos n\omega_{0}t\;dt & \text{for odd } n \\ 0 & \text{for even }n\end{cases} \\
b_{n}&=\begin{cases} \frac{4}{T}\int_{0}^{\frac{T}{2}}f(t)\sin n\omega_{0}t\;dt & \text{for odd } n \\ 0 & \text{for even }n\end{cases}
\end{align*}$$
![[HalfWaveSymmetricFunction.svg|550]]