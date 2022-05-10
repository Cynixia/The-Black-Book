# Polar Form of a Complex Number
[[Complex Number|Complex numbers]] can also be expressed in *polar form*, either using [[List of Trigonometric Identities#Euler's formula|Euler's formula]] or in angle notation as a [[phasor]].
$$z=re^{i\phi}=r\angle \phi$$
- $r=|z|=\sqrt{x^2+y^2}$ - *modulus* or *magnitude* - the distance from the origin to the point $z$.
- $\phi=\tan^{-1}\frac{y}{x}$ - *argument* or [[phase]] - angle between the vector $z$ and the positive real axis.

The *argument*, $\phi$ or $\arg (z)$, can take *infinitely many values*, with values separated by multiples of $2\pi$.

![[PolarFormComplexNumber.svg|450]]

## Principal argument
The *principal argument*, $\text{Arg}(z)$, is the argument function defined over a restricted range and is *single-valued*.
$$-\pi<\text{Arg}(z)\le\pi$$
$$\text{Arg}(z)=\tan^{-1}\left(\frac{y}{x}\right)+
{\begin{cases} 0, & z\text{ in 1st or 4th quadrant} \\
\pi, & z\text{ in 2nd quadrant} \\
-\pi, & z\text{ in 3rd quadrant} 
\end{cases}}$$
