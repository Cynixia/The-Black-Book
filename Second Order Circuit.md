# Second Order Circuit
**A circuit characterised by a second-order differential equation.**

A second order circuit consists of resistive elements with two types of energy storage elements, either a [[capacitor]], [[inductor]], or [[Operational Amplifier|op-amp]]. 

The characterising second-order homogeneous differential equation is often expressed as
$$\frac{d^{2}x(t)}{dt^2}+2\alpha\frac{dx(t)}{dt}+\omega_{n}^{2}x(t)=f(t)$$
- $\alpha$ - *damping* factor
- $\omega_{n}$ - *natural frequency*, radians per second

The *damped frequency* of the circuit is given by
$$\omega_{d}^{2}=\omega_{n}^{2}-\alpha^{2}$$
The [[characteristic equation]] and its roots are
$$s^{2}+2\alpha s+\omega_{n}^{2}=0\qquad\begin{align*}
s_{1},s_{2}&=-\alpha\pm\sqrt{\alpha^{2}-\omega_{n}^{2}} \\
&=-\alpha\pm j\omega_{d}
\end{align*}$$
The characteristic equation is also equal to the denominator of the [[transfer function]] of the circuit.

## Natural or transient response
The *general solution* to the *homogeneous* equation describes the *natural* or *transient* response of the circuit and depends on the roots of the characteristic equation.

- *Overdamped* - $s_{1}$, $s_{2}$ are *distinct real* roots.
$$\alpha>\omega_{n}\Rightarrow \alpha^{2}-\omega_{n}^{2}>0\qquad x_{t}(t)=A_{1}e^{(-\alpha+\omega_{d})t}+A_{2}e^{(-\alpha+\omega_{d})t}$$
- *Underdamped* - $s_{1}$, $s_{2}$ are *distinct complex* roots.
$$\alpha<\omega_{n}\Rightarrow\alpha^{2}-\omega_{n}^{2}<0\qquad x_{t}(t)=e^{-\alpha t}(A_{1}\cos(\omega_{d}t)+A_{2}\sin(\omega_{d}t))$$
- *Undamped* - $s_{1},s_{2}$ are *distinct complex* roots and the solution is purely sinusoidal.
$$\alpha=0\Rightarrow s_{1},s_{2}=\pm j\omega_{d}=\pm j\omega_{n}\qquad x_{t}(t)=A_{1}\cos(\omega_{d}t)+A_{2}\sin(\omega_{d}t)$$
- *Critically damped* - $s_{1}$, $s_{2}$ are *equal real* roots.
$$\alpha=\omega_{n}\Rightarrow \alpha^{2}-\omega_{n}^{2}=0\qquad x_{t}(t)=A_{1}e^{-\alpha t}+A_{2}t e^{-\alpha t}$$

## Forced or steady-state response
The *forced* or *steady-state* response is typically derived directly from the circuit itself and is the response of the circuit to a source.
$$x_{ss}(t)=x(\infty)$$
## Total response
The *total* response of the circuit is the [[superposition]] of the *transient* and *steady-state*  response. Constants remaining the equations can be obtained using any *initial conditions* specified.
$$x(t)=x_{t}(t)+x_{ss}(t)$$