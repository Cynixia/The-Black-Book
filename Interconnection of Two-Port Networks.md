# Interconnection of Two-Port Networks
It is common to find circuits where several [[Two-Port Network|two-port networks]] are interconnected in *series*, *parallel*, or are *cascaded* together.
## Series connection
In *series*, two two-port networks share input currents and their input voltages add.
$$\begin{align*}
\mathbf{V}_{1}&=\mathbf{V}_{1a}+\mathbf{V}_{1b} \\
\mathbf{V}_{2}&=\mathbf{V}_{2a}+\mathbf{V}_{2b}
\end{align*}$$
The *Z-parameter* matrix for the combined network is the sum of the individual Z-parameter matrices of each network.
$$\mathbf{Z}=\mathbf{Z}_A+\mathbf{Z}_B$$

![[TwoPortNetworkSeries.svg|500]]

## Parallel connection
In *parallel*, the networks share port voltages and the total input current is equal to the sum of the individual input currents.
$$\begin{align*}
\mathbf{I}_{1}&=\mathbf{I}_{1a}+\mathbf{I}_{1b} \\ \mathbf{I}_{2}&=\mathbf{I}_{2a}+\mathbf{I}_{2b}
\end{align*}$$
$$\begin{align*}
\mathbf{V}_{1}&=\mathbf{V}_{1a}=\mathbf{V}_{1b} \\\mathbf{V}_{2}&=\mathbf{V}_{2a}=\mathbf{V}_{2b}
\end{align*}$$
The *Y-parameter* matrix for the combined network is the sum of the individual Y-parameter matrices of each network.
$$\mathbf{Y}=\mathbf{Y}_{A}+\mathbf{Y}_{B}$$
![[TwoPortNetworkParallel.svg|800]]

## Cascading networks
When networks are *cascaded*, the outputs on one network becomes the input of the next one. The *transmission parameters* of the combined networks equals to *matrix multiplication* of the individual transmission matrices of each network.
$$\mathbf{T}=\mathbf{T}_{A}\mathbf{T}_{B}$$
![[TwoPortNetworkCascaded.svg]]