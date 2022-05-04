# Dot Convention
**Convention for denoting the relative instantaneous polarities of [[Inductance#Mutual inductance|magnetically coupled]] inductors.**

A current *entering* the dotted terminal of one coil produces a *positively sensed* voltage at the dotted terminal of the second coil.

![[DotConvention.svg]]

Note that the value of $v_{2}$ is taken with respect to *how it is defined on the diagram*, as in with the positive terminal on the top.

Additionally, $i_{2}$ has been shown to indicate the flow of current in the right loop if it is *completely driven* by the mutual inductance.

## Inductors in series
For magnetically coupled coils in series, where the dots are on the *same side* of both inductors, the connection is called *series-aiding*.
$$L_{\text{eq}}=L_{1}+L_{2}+2M$$
![[DotConventionSeriesAiding.svg|550]]

The opposite case is known as a *series-opposing* connection.
$$L_{\text{eq}}=L_1+L_2-2M$$
![[DotConventionSeriesOpposing.svg|600]]

## Inductors in parallel
For magnetically coupled coils in parallel, if the dots are on the *same side*,
$$L_\text{eq}=\frac{L_{1}L_{2}-M^{2}}{L_{1}+L_{2}-2M}$$
![[DotConventionParallelSame.svg|400]]

If the dots are on *opposite sides*,
$$L_\text{eq}=\frac{L_{1}L_{2}-M^{2}}{L_{1}+L_{2}+2M}$$
![[DotConventionParallelOpposite.svg|400]]