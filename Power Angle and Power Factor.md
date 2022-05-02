# Power Angle and Power Factor
## Power Angle
**The phase of [[complex power]].**
$$\theta_{v}-\theta_i$$
The power angle is also the difference of the [[phase]] of the *voltage* and the *current* of the load which is the phase of the *load impedance*.

## Power Factor
**The ratio of the [[Average or Real Power|real power]] dissipated in the load to the apparent power of the load.**

It is defined as the cosine of the power angle. Power factor is *unitless* and is expressed with whether it is *leading* or *lagging*. This corresponds with whether the *current* is leading or lagging.
$$pf=\cos(\theta_{v}-\theta_{i})$$

- If $\theta_{v}-\theta_{i}=0$, the load is *purely resistive*, $pf=1$, and the apparent power delivered is the [[Average or Real Power|real power]].
- If $\theta_{v}-\theta_{i}=\pm 90^{\circ}$, then the load is *purely reactive*, $pf=0$, and no real power is delivered.
- If $-90^{\circ}<\theta_{v}-\theta_{i}<0^{\circ}$, then the load is *net capacitive* and the $pf$ is *leading*.
- If $0^{\circ}<\theta_{v}-\theta_{i}<90^{\circ}$, then the load is *net inductive* and the $pf$ is *lagging*.

### Power factor correction
**The correction of power factor towards unity.**

The closer the power factor is to unity, the less total [[Complex Power#Reactive power|reactive power]] within the system and thus the less total [[Complex Power#Apparent power|apparent power]] required to be sourced.

To achieve power factor correction, a purely reactive load is added *in parallel* to an existing load. Using a purely reactive load theoretically keeps the magnitude of the [[Average or Real Power|real power]] the same.

- If the power factor is *lagging*, implying a *net inductive* load, then a *shunt* [[capacitor]] is required with a capacitance of
$$C=\frac{Q_{C}}{\omega V^{2}_{\text{RMS}}}$$
$Q_{C}$ refers to the *leading reactive power* that the capacitor needs to *eliminate* and $V$ is the source voltage.

- If the power factor is *leading*, implying a *net capacitive* load, then a *shunt* [[inductor]] is required with an inductance of
$$L=\frac{V_{\text{RMS}}^{2}}{\omega Q_{\text{L}}}$$
$Q_L$ is the *leading reactive power* that the inductor needs to *provide*.

Below are power triangles before and after correction using a shunt capacitor.

![[CapacitativePowerFactorCorrection.svg|800]]

These power triangles show correction using a shunt inductor.

![[InductivePowerFactorCorrection.svg|800]]