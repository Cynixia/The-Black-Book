# Inductance
**The tendency of an electrical conductor to oppose a change in the current flowing through it.**

|                   Inductance                   |
|:----------------------------------------------:|
|                      $L$                       |
|               henry ($\text{H}$)               |
| $\text{kg}\;\text{m}^2\;\text{s}^{-2}\;A^{-2}$ |

Inductance is defined as the ratio of the *induced voltage* to the *rate of change* of the *current* causing it.

An electrical conductor will *induce* a magnetic field around it when a *changing* electric current is flowing through it, as described in [[Faraday's law of induction]]. This magnetic field in turn induces a *back EMF* that opposes the change in current according to [[Lenz's Law]].

Inductance depends on the *geometry* of the conductor and the *magnetic permeability* of nearby materials, such as the core.

A component designed specifically to add inductance is known as an [[inductor]] which usually consists of a coil of wire. The voltage an inductor induces across itself is caused by its *self inductance*.

## Mutual inductance
**The phenomenon in which the magnetic flux caused by the current through an inductor induces a voltage in another in proximity.**

*Mutual inductance* is also the measurement of the amount of *magnetic coupling* between the inductors. 

Suppose there are two coils, coil $1$ and coil $2$.
![[MutualInductance.svg]]

The *total flux*, $\phi$, of coil $1$ is equal to $\phi_{11}+\phi_{12}$.

The effect of $\phi_{11}$, where the subscript denotes the effect of coil $1$ on coil $1$, is the effect of the *self inductance* of the coil. It can be expressed as follows:
$$v_{1}=L_{1}\frac{di_{1}}{dt}\Longleftrightarrow\mathbf{v}_{1}=j\omega L_{1}\mathbf{I}_{1}$$
The effect of $\phi_{12}$ is the effect of the *mutual inductance* between the coils, denoted as $M$ and measured in *henrys* ($H$).
$$v_{2}=M\frac{di_{2}}{dt}\Longleftrightarrow\mathbf{v}_{2}=j\omega M\mathbf{I}_{2}$$
This is also true in reverse, as in, if coil $2$ was connected to the current source instead of coil $1$.

Note the *polarity* of the voltages are *not* explicitly stated in the above equations.