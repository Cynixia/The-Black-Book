# Thevenin's and Norton's Theorem
*Thevenin's theorem* states that a [[Linear Circuit|linear]] *two-terminal* circuit can be replaced by an equivalent circuit consisting of a voltage source $\mathbf{V}_{\text{Th}}$ in *series* with an [[impedance]] $\mathbf{Z}_{\text{Th}}$. 

*Norton's theorem* states that a *linear two-terminal* circuit can be replaced by an equivalent circuit consisting of a current source $\mathbf{I}_{\text{Th}}$ in *parallel* with an impedance $\mathbf{Z}_{\text{N}}$.

Thevenin's and Norton's theorem are [[Duality#Electrical circuits|duals]] of each other.

Thevenin's and Norton's theorem are also related by [[source transformation]], and thus
$$\mathbf{Z}_{\text{Th}}=\mathbf{Z}_{\text{N}}$$
![[TheveninNortonEquivalents.svg|1000]]

## Thevenin voltage
The *Thevenin voltage*, $\mathbf{V}_{\text{Th}}$, is equal to the *open circuit voltage* at the terminals.

## Norton current
The *Norton current*, $I_{\text{N}}$, is equal to the *short circuit current* when the terminals are connected together.

## Thevenin impedance
The *Thevenin impedance*, $\mathbf{Z}_{\text{Th}}$, can be found by the following methods.
- The *input resistance* measured at the terminals when *all* independent sources are off. This *does not work* if there are *any* dependant sources.
- Ratio of the Thevenin voltage to the Norton current.
- Turning off *all* independent sources and attaching an *arbitrary* voltage or current source to the terminals and measuring the *resulting current* or *voltage* respectively. For simplicity, these sources are often set to $1\angle 0^{\circ}$.

![[TheveninResistance.svg|1000]]