# Transformer
**An electrical energy transfer device consisting of [[Inductance#Mutual inductance|magnetically coupled coils]].**

The coil directly connected to the *input* voltage source is the *primary winding*, $N_{\text{P}}$, and the coil connected to the *load* is the *secondary winding*, $N_\text{S}$.

## Ideal transformer
In an ideal transformer,
- Primary and secondary windings have *no resistance*.
- The coils are [[Energy in a Coupled Circuit#Coupling coefficient|perfectly coupled]]; $k=1$.
- The permeability of the core is *infinitely large*.
- Core losses are negligible.

As an ideal transformer is *lossless*, the primary power is *equal* to the secondary power. Thus, [[Transfer Function|transfer functions]] for voltage and current are related to the ratio of the number of turns of the windings, $n$.
$$n=\frac{N_\text{S}}{N_\text{P}}=\frac{v_\text{S}}{v_\text{P}}=\frac{i_\text{P}}{i_\text{S}}$$
![[IdealTransformer.svg|400]]

## Step-up, step-down, and isolation transformers
In a *step-up* transformer, the secondary voltage is *larger* than the primary voltage, and
$$n=\frac{N_\text{S}}{N_\text{P}}>1$$
In a *step-down* transformer, the secondary voltage is *smaller* than the primary voltage, and
$$n=\frac{N_\text{S}}{N_\text{P}}<1$$
In an *isolation* transformer, the two voltages are *equal* and the ratio of the number of turns is equal to one.

## Reflected load
A transformer can be eliminated from the analysis of the circuit by *reflecting* the circuits to a side. This does not work if there are *external connections* between the the primary and secondary circuits.

The input [[impedance]] as seen through a transformer towards the load from the primary side is the *reflected impedance*.
$$\mathbf{Z_\text{in}}=\frac{\mathbf{Z}_{L}}{n^2}$$
![[ReflectedImpedance.svg|400]]


To reflect the secondary circuit to the primary side,
- Secondary impedances are *divided* by $n^{2}$
- Secondary voltages are *divided* by $n$
- Secondary currents are *multiplied* by $n$

To reflect the primary circuit to the secondary side,
- Primary impedances are *multiplied* by $n^{2}$
- Primary voltages are *multiplied* by $n$
- Primary currents are *divided* by $n$

## Winding direction
The direction of the windings in a transformer determines the polarity of the secondary voltage with respect to the primary voltage.

![[WindingDirection.svg]]

## Dot convention
[[Dot convention]] is especially important in transformers.

If *both* $\mathbf{I_{1}}$ and $\mathbf{I}_{2}$ enter or leave the dotted terminals, then a *minus* is required in front of the turns ratio. Otherwise, it is positive.

If $\mathbf{V}_1$ and $\mathbf{V}_{2}$ are *both* positive or negative at the dotted terminals, then a turns ratio is left *positive*. Otherwise, a *minus* is placed in front.

![[TransformerDotConvention1.svg]]



![[TransformerDotConvention2.svg]]

## Transformer efficiency
**The percentage of input power delivered to the output.**
$$\eta=\frac{P_\text{out}}{P_\text{in}}\times100$$