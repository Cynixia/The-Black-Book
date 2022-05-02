# Capacitor
**A passive electrical component that stores energy in an electric field when a voltage is applied across it.**

![[Capacitor.svg|200]]

Most capacitors consist of a pair of electrical conductors, commonly known as *plates*, separated by a *dielectric medium*. Capacitors are characterised by their [[capacitance]].

The *voltage* across a capacitor *can not* change *instantaneously*, as this would theoretically destroy and create an electric field instantly.

## Capacitors in series and parallel
The total capacitance of a *series* of capacitors is the reciprocal of the sum of the reciprocals of their capacitances.
$$C_{\text{eq}}=\frac{1}{\frac{1}{C_{1}}+\frac{1}{C_{2}}+\cdots+\frac{1}{C_n}}$$

![[CapacitorsSeries.svg|600]]

The total capacitance of *parallel* capacitors is the sum of the individual capacitances.
$$C_{\text{eq}}=C_{1}+C_{2}+\cdots +C_{n}$$

![[CapacitorsParallel.svg|600]]

## Impedance
The [[impedance]] of a capacitor is
$$\mathbf{Z}=\frac{1}{j\omega C}=-\frac{j}{\omega C}$$
- $\omega$ - [[angular frequency]], radians per second
- $C$ - [[capacitance]], $\text{F}$

The current *leads* the voltage by $90^{\circ}$ in a capacitor.

At DC, a capacitor acts like an *open circuit* as the charge simply accumulates on either plate and the electric field exactly balances the source voltage. 
At high frequencies, the charge on the plates accumulate less, generating a weaker opposing electric field, thus acting like a *short circuit*.

![[CapacitorFrequencyResponse.svg|550]]

## Voltage
The *voltage* across a capacitor is
$$v(t)=\frac{1}{C}\int_{t_0}^{t}i(t)\;dt+v(t_{0})$$

## Current
The *current* through a capacitor is
$$i=C\frac{dV}{dt}$$
Note that this implies that the voltage across a capacitor *can not* change *instantaneously*, as this would require an infinitely large current.

## Stored energy
The *energy* stores in the electric field of a capacitor is
$$w(t)=\frac{1}{2}C\;v(t)^2$$