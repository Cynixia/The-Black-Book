# Resonance
**The phenomenon of increased amplitude when the frequency of a waveform in an applied periodic force is similar or matches the natural frequency of a system.**

## RLC Circuits
**The condition where the [[impedance]] is purely resistive.**

At resonance,
- The source voltage is held *completely* across $R$.
- The [[Power Angle and Power Factor#Power Factor|power factor]] is unity; voltage and current in [[phase]].
- The [[transfer function]] $\mathbf{H}(\omega)=\mathbf{Z}(\omega)$ is at a *minimum*.
- The inductor and capacitor voltage may *exceed* the source voltage.

The value of $\omega$ that causes resonance is the *resonant* or *natural* frequency, $\omega_{0}$. For  *both* series and parallel RLC circuits, it is given by
$$\omega_{0}=\frac{1}{\sqrt{LC}}$$
The *half-power frequencies* are the frequencies where the dissipated power is *half* the maximum or half the value *at resonance*. At half-power frequencies,
$$|\mathbf{H}(\omega)|=\frac{1}{\sqrt{2}}$$
The half-power *bandwidth*, $B$, is the frequency range in which the magnitude of the transfer function is at least $\frac{1}{\sqrt{2}}$.
$$B=\omega_{2}-\omega_{1}$$
RLC circuits also have a *quality factor*, $Q$, which is a dimensionless quantity describing the *selectivity* of the circuit. The *higher* the quality factor, the smaller the range which approaches resonance, and the longer a circuit resonates.
$$Q=\frac{\omega_{0}}{B}$$
For a *high-Q* circuit, where $Q\ge 10$, the half-power frequencies are practically *symmetrical* around the resonant frequency and can be approximated as
$$\begin{align*}
\omega_{1}\approx\omega_{0}-\frac{B}{2} \\
\omega_{2}\approx\omega_{0}+\frac{B}{2}
\end{align*}$$
### Series Resonance
The *half-power frequencies* are
$$\begin{align*}
\omega_{1}&=-\frac{R}{2L}+\sqrt{\left(\frac{R}{2L}\right)^{2}+\frac{1}{LC}} \\
\omega_{2}&=\frac{R}{2L}+\sqrt{\left(\frac{R}{2L}\right)^{2}+\frac{1}{LC}}
\end{align*}$$
The *quality factor* is given by
$$Q=\frac{\omega_{0}L}{R}=\frac{1}{\omega_{0}CR}$$
The *bandwidth* can be found with
$$B=\frac{R}{L}$$
The half-power frequencies can also be expressed in terms of the quality factor.
$$\omega_{1},\omega_{2}=\omega_{0}\sqrt{1+\left(\frac{1}{2Q}\right)^{2}}\pm\frac{\omega_{0}}{2Q}$$

![[RLCSeriesCircuit.svg|600]]

### Parallel Resonance
The *half-power frequencies* are
$$\begin{align*}
\omega_{1}&=-\frac{1}{2RC}+\sqrt{\left(\frac{1}{2RC}\right)^{2}+\frac{1}{LC}}\\
\omega_{2}&=\frac{1}{2RC}+\sqrt{\left(\frac{1}{2RC}\right)^{2}+\frac{1}{LC}}
\end{align*}$$
The *quality factor* is given by
$$Q=\omega_{0}RC=\frac{R}{\omega_{0}L}$$
The *bandwidth* can be found with
$$B=\frac{1}{RC}$$
As in an series RLC circuit, the half-power frequencies can also be expressed in terms of the quality factor.
$$\omega_{1},\omega_{2}=\omega_{0}\sqrt{1+\left(\frac{1}{2Q}\right)^{2}}\pm\frac{\omega_{0}}{2Q}$$

![[RLCParallelCircuit.svg|600]]