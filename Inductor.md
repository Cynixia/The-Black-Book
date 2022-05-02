# Inductor
**A passive two-terminal electrical component that stores energy in a magnetic field when current flows through it.**

![[Inductor.svg|200]]

An inductor is typically a coil of wire and is characterised by its [[inductance]].

The *current* through an inductor *can not* change *instantaneously*, as this would theoretically collapse and induce a magnetic field instantly.

## Inductors in series and parallel
The total inductance of a *series* of inductors is the sum of the individual inductances.
$$L_{\text{eq}}=L_1+L_{2}+\cdots+L_{n}$$

![[InductorsSeries.svg|600]]

The total impedance of *parallel* inductors is the reciprocal of the sum of the reciprocals of their impedances. 
$$L_{\text{eq}}=\frac{1}{\frac{1}{L_1}+\frac{1}{L_{2}}+\cdots+\frac{1}{L_{n}}}$$

![[InductorsParallel.svg|600]]

## Impedance
The [[impedance]] of an inductor is
$$\mathbf{Z}=j\omega L$$
- $\omega$ - [[angular frequency]], radians per second
- $L$ - [[inductance]], $\text{H}$

The current *lags* the voltage by $90^{\circ}$ in an inductor. 

At DC, an inductor acts like a *short circuit* as the lack of changing current means no magnetic field is induced.
At high frequencies, an inductor acts like an *open circuit* as the rapidly changing current will be mitigated by its inductance.

![[InductorFrequencyResponse.svg|550]]

## Voltage
The *voltage* across an inductor is
$$V=L \frac{di}{dt}$$
Note that this implies that the current through an inductor *can not* change *instantaneously*, as this would require an infinitely large applied voltage.

## Current
The *current* through an inductor is
$$i(t)=\frac{1}{L}\int_{t_0}^{t}v(t)\;dt+i(t_{0})$$
## Stored energy
The *energy* stored in the magnetic field of an inductor is
$$w(t)=\frac{1}{2}L\;i(t)^2$$