# Impedance
**The opposition to alternative current.**

*Impedance*, $\mathbf{Z}$, is the [[complex number]] extension of resistance and is also measured in *ohms* ($\Omega$).

Impedance is composed of *resistance*, $R$, and *reactance*, $X$, both measured in ohms, and is expressed as
$$\mathbf{Z}=R\pm jX=|\mathbf{Z}|\angle\theta$$
An impedance is [[Inductance|inductive]] if the imaginary part is *positive*, otherwise the impedance is [[Capacitance|capacitive]].
- In a purely *resistive* load, the current is *in phase* with voltage.
- In an *inductive* load, the current *lags* voltage.
- In an *capacitive* load, the current *leads* voltage.

The reciprocal of impedance is [[admittance]].

## Series combination
As with resistance, the total impedance of a series of components is the sum of their individual impedances.
$$\mathbf{Z}_{\text{eq}}=Z_1+Z_2+\cdots+Z_{n}$$
![[ImpedanceSeries.svg|600]]

## Parallel combination
The total impedance of parallel components is the reciprocal of the sum of the reciprocals of their impedances.
$$\mathbf{Z}_{\text{eq}}=\frac{1}{\frac{1}{\mathbf{Z}_1}+\frac{1}{\mathbf{Z}_{2}}+\cdots+\frac{1}{\mathbf{Z}_{n}}}$$

![[ImpedanceParallel.svg|600]]
