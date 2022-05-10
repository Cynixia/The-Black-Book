# Energy in a Coupled Circuit
The instantaneous energy stores in [[Inductance#Mutual inductance|coupled inductors]] is given by
$$w=\frac{1}{2}L_{1}i_{1}^{2}+\frac{1}{2}L_{2}i_{2}^{2}\pm Mi_{1}i_{2}$$
The final term is *added* if *both* currents *enter or leave* the dotted terminals. Otherwise, the term is *subtracted*.

![[EnergyCoupledCircuit.svg]]

## Coupling coefficient
The energy within a circuit cannot be negative. Thus, there is an *upper limit* to mutual inductance.
$$M\le\sqrt{L_{1}L_{2}}$$
The *coupling coefficient*, $k$, describes the extent to which the mutual inductance approaches the upper limit. It exists in the interval $0\le k\le 1$.
$$k=\frac{M}{\sqrt{L_{1}L_{2}}}$$
- If $k=1$, then the coils are *perfectly coupled*. ^074941
- If $k<0.5$, then the coils are *loosely coupled*.
- If $k>0.5$, then the coils are *tightly coupled*.