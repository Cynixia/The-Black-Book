# Complex Power
**The quantity containing all information related to the power absorbed by a load in AC.**

Complex power, denoted $\mathbf{S}$, is measured in *volt-amperes* ($\text{VA}$). It is a [[complex number]] and can be expressed in rectangular form as
$$\mathbf{S}=P+jQ$$
- $P$ - [[average or real power]], $\text{W}$
- $Q$ - *reactive* power, $\text{VAR}$

Alternatively, in [[Polar Form of a Complex Number|polar form]],
$$\mathbf{S}=S\angle(\theta_{v}-\theta_{i})$$
- $S$ - *apparent* power, $\text{VA}$
- $\theta_{v}-\theta_{i}$ - [[Power Angle and Power Factor#Power Angle|power angle]]

Complex power can be calculated using [[AC Values#^6b76b1|peak values]] and [[AC Values#Root mean square value|root mean square values]].
$$\begin{align*} \mathbf{S}&=\frac{1}{2}\mathbf{V}\mathbf{I}^{*} \\
&=\mathbf{V}_{\text{RMS}}\mathbf{I}_{\text{RMS}} \\
&=I_{\text{RMS}}^{2}\mathbf{Z} \\
&=\frac{V_{\text{RMS}}^2}{\mathbf{Z}^{*}}
\end{align*}$$
In summary, the components of complex power are:
$$\begin{align*} \text{Complex power} - \mathbf{S}&=\mathbf{V}_{\text{RMS}}\mathbf{I}_{\text{RMS}}^{*}=P+jQ\\ &=|\mathbf{V}_{\text{RMS}}||\mathbf{I}_{\text{RMS}}|\angle(\theta_{v}-\theta_{i}) \\
\text{Apparent power} - S&=|\mathbf{S}|=|\mathbf{V}_{\text{RMS}}||\mathbf{I}_{\text{RMS}}|=\sqrt{P^{2}+Q^{2}} \\
\text{Real power} - P&=\Re(\mathbf{S})=S\cos(\theta_{v}-\theta_{i}) \\
\text{Reactive power} - Q&=\Im(\mathbf{S})=S\sin(\theta_{v}-\theta_{i}) \\
\text{Power factor} - pf&=\frac{P}{S}=\cos(\theta_{v}-\theta_{i})
\end{align*}$$
## Reactive power
Reactive power, $Q$, is the part of complex power that does *no work*. It corresponds to the energy that flows to the load then back to the source.

Its unit is *volt-ampere reactive*, $\text{VAR}$.

## Apparent power
Apparent power, $S$, is the *magnitude* of complex power. It is so called because it is the "apparent" power draw of a load, even if not all of that power does work.

Its unit is the *volt-ampere*, $\text{VA}$.

## Power triangle
It is common to represent complex power as a vector sum in the form of a *power triangle*.

![[PowerTriangle.svg|500]]