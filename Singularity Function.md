# Singularity Function
**A function that is discontinuous and contains singularities.**

## Unit step function
The *unit step function*, $u(x)$, also known as the *Heaviside step function*, is defined as
$$u(x)=\begin{cases} 0, &x<0 \\
1, &x>0 \end{cases}$$
The function may be *shifted*,
$$u(x-x_{0})=\begin{cases} 0, &x<x_{0}  \\
1, &x>x_{0} \end{cases}$$
There are various other conventions, such as $u(0)=0$ or $u(0)=\frac{1}{2}$.

![[UnitStepFunction.svg|500]]
![[UnitStepFunctionShifted.svg|500]]

## Unit impulse function
The *unit impulse function*, $\delta(x)$, also known as the *Dirac delta function*, is zero for all values except at $t=0$, where it is undefined. Its integral over the *entire real line* is equal to $1$.
$$\int_{-\infty}^{\infty}\delta(x)\;dx=1$$
The function is noted for its *sampling* or *sifting* property.
$$\int_{a}^{b}f(x)\delta(x-x_{0})\;dt=f(x_0)$$
![[UnitImpulseFunction.svg]]