# Two-Port Network
**An electrical network with two separate ports for input and output.**

![[TwoPortNetwork.svg]]

*Two-port networks* are mathematically modelled by 2x2 matrices of [[Complex Number|complex numbers]], known as a set of *parameters*. They establish the relationship between the following variables.
- $V_{1}$ - voltage across port $1$
- $I_{1}$ - current into port $1$
- $V_{2}$ - voltage across port $2$
- $I_{2}$ - current into port $2$

Two-port networks may be [[Interconnection of Two-Port Networks|interconnected]] in several ways.

## Impedance parameters
$$\left[\begin{matrix} \mathbf{V}_{1}\\ \mathbf{V}_{2} \end{matrix}\right]=\left[\begin{matrix} \mathbf{Z}_{11} & \mathbf{Z}_{12} \\ \mathbf{Z}_{21} & \mathbf{Z}_{22} \end{matrix}\right]\left[\begin{matrix} \mathbf{I}_{1}\\ \mathbf{I}_{2} \end{matrix}\right]$$
The [[impedance]] parameters, denoted as *Z-parameters*, relate the terminal voltages to the terminal currents. Their values are evaluated by leaving the ports *open circuited* and have dimensions of *ohms*.
$$\begin{align*}
\mathbf{Z}_{11}&=\left.\frac{\mathbf{V}_{1}}{\mathbf{I}_{1}}\right|_{\mathbf{I}_{2}=0}\qquad \mathbf{Z}_{12}=\left.\frac{\mathbf{V}_{1}}{\mathbf{I}_{2}}\right|_{\mathbf{I}_{1}=0} \\
\mathbf{Z}_{21}&=\left.\frac{\mathbf{V}_{2}}{\mathbf{I}_{1}}\right|_{\mathbf{I}_{2}=0}\qquad \mathbf{Z}_{22}=\left.\frac{\mathbf{V}_{2}}{\mathbf{I}_{2}}\right|_{\mathbf{I}_{1}=0}
\end{align*}$$
- $\mathbf{Z}_{11}$ - open circuit input impedance
-  $\mathbf{Z}_{12}$ - open circuit transfer impedance from port $1$ to port $2$
-  $\mathbf{Z}_{21}$ - open circuit transfer impedance from port $2$ to port $1$
-  $\mathbf{Z}_{22}$ - open circuit output impedance

In a *linear* two-port network with *no dependent* sources,
$$\mathbf{Z}_{12}=\mathbf{Z}_{21}$$
It is possible that impedance parameters *do not exist* for a two-port network.

## Admittance parameters
$$\left[\begin{matrix} \mathbf{I}_{1}\\ \mathbf{I}_{2} \end{matrix}\right]=\left[\begin{matrix} \mathbf{Y}_{11} & \mathbf{Y}_{12} \\ \mathbf{Y}_{21} & \mathbf{Y}_{22} \end{matrix}\right]\left[\begin{matrix} \mathbf{I}_{1}\\ \mathbf{I}_{2} \end{matrix}\right]$$
The [[admittance]] parameters, denoted as *Y-parameters*, have dimensions of *siemens*. Their values are evaluated by *short circuiting* the ports.
$$\begin{align*}
\mathbf{Y}_{11}&=\left.\frac{\mathbf{I}_{1}}{\mathbf{V}_{1}}\right|_{\mathbf{V}_{2}=0}\qquad \mathbf{Y}_{12}=\left.\frac{\mathbf{I}_{1}}{\mathbf{V}_{2}}\right|_{\mathbf{V}_{1}=0} \\
\mathbf{Y}_{21}&=\left.\frac{\mathbf{I}_{2}}{\mathbf{V}_{1}}\right|_{\mathbf{V}_{2}=0}\qquad \mathbf{Y}_{22}=\left.\frac{\mathbf{I}_{2}}{\mathbf{V}_{2}}\right|_{\mathbf{V}_{1}=0}
\end{align*}$$
- $\mathbf{Y}_{11}$ - short circuit input admittance
-  $\mathbf{Y}_{12}$ - short circuit transfer admittance from port $1$ to port $2$
-  $\mathbf{Y}_{21}$ - short circuit transfer admittance from port $2$ to port $1$
-  $\mathbf{Y}_{22}$ - short circuit output admittance

In a *linear* two-port network with *no dependent* sources,
$$\mathbf{Y}_{12}=\mathbf{Y}_{21}$$
## Hybrid parameters
$$\left[\begin{matrix} \mathbf{V}_{1}\\ \mathbf{I}_{2} \end{matrix}\right]=\left[\begin{matrix} \mathbf{h}_{11} & \mathbf{h}_{12} \\ \mathbf{h}_{21} & \mathbf{h}_{22} \end{matrix}\right]\left[\begin{matrix} \mathbf{I}_{1}\\ \mathbf{V}_{2} \end{matrix}\right]$$
The *hybrid* parameters, denoted as *h-parameters*, are a combination of impedance, admittance, voltage gain, and current gain. The direction of gain is described from the perspective of the port denoted port $1$.
$$\begin{align*}
\mathbf{h}_{11}&=\left.\frac{\mathbf{V}_{1}}{\mathbf{I}_{1}}\right|_{\mathbf{V}_{2}=0}\qquad \mathbf{h}_{12}=\left.\frac{\mathbf{V}_{1}}{\mathbf{V}_{2}}\right|_{\mathbf{I}_{1}=0} \\
\mathbf{h}_{21}&=\left.\frac{\mathbf{I}_{2}}{\mathbf{I}_{1}}\right|_{\mathbf{V}_{2}=0}\qquad \mathbf{h}_{22}=\left.\frac{\mathbf{I}_{2}}{\mathbf{V}_{2}}\right|_{\mathbf{I}_{1}=0}
\end{align*}$$
- $\mathbf{h}_{11}$ - short circuit input impedance
-  $\mathbf{h}_{12}$ - open circuit reverse voltage gain
-  $\mathbf{h}_{21}$ - short circuit forward current gain
-  $\mathbf{h}_{22}$ - open circuit output admittance

In a *linear* two-port network with *no dependent* sources,
$$\mathbf{h}_{12}=-\mathbf{h}_{21}$$

### Inverse hybrid parameters
$$\left[\begin{matrix} \mathbf{I}_{1}\\ \mathbf{V}_{2} \end{matrix}\right]=\left[\begin{matrix} \mathbf{g}_{11} & \mathbf{g}_{12} \\ \mathbf{g}_{21} & \mathbf{g}_{22} \end{matrix}\right]\left[\begin{matrix} \mathbf{V}_{1}\\ \mathbf{I}_{2} \end{matrix}\right]$$
The *inverse hybrid* parameters, denoted as *g-parameters*, form the *inverse matrix* of the hybrid matrix.

$$\begin{align*}
\mathbf{g}_{11}&=\left.\frac{\mathbf{I}_{1}}{\mathbf{V}_{1}}\right|_{\mathbf{I}_{2}=0}\qquad \mathbf{g}_{12}=\left.\frac{\mathbf{I}_{1}}{\mathbf{I}_{2}}\right|_{\mathbf{V}_{1}=0} \\
\mathbf{g}_{21}&=\left.\frac{\mathbf{I}_{2}}{\mathbf{V}_{1}}\right|_{\mathbf{I}_{2}=0}\qquad \mathbf{g}_{22}=\left.\frac{\mathbf{V}_{2}}{\mathbf{I}_{2}}\right|_{\mathbf{V}_{1}=0}
\end{align*}$$
- $\mathbf{g}_{11}$ - open circuit input admittance
-  $\mathbf{g}_{12}$ - short circuit reverse current gain
-  $\mathbf{g}_{21}$ - open circuit forward voltage gain
-  $\mathbf{g}_{22}$ - short circuit output impedance

## Transmission parameters
$$\left[\begin{matrix} \mathbf{V}_{1}\\ \mathbf{I}_{2} \end{matrix}\right]=\left[\begin{matrix} \mathbf{A} & \mathbf{B} \\ \mathbf{C} & \mathbf{D} \end{matrix}\right]\left[\begin{matrix} \mathbf{V}_{2}\\ -\mathbf{I}_{2} \end{matrix}\right]$$
The *transmission* parameters, denoted as *T-parameters* or *ABCD-parameters*, relates the variables of the input port to the output port. Note that $-\mathbf{I}_{2}$ is used such that when networks are *cascaded*, the output current of one stage becomes the input current on the next.
$$\begin{align*}
\mathbf{A}&=\left.\frac{\mathbf{V}_{1}}{\mathbf{V}_{2}}\right|_{\mathbf{I}_{2}=0}\qquad \mathbf{B}=-\left.\frac{\mathbf{V}_{1}}{\mathbf{I}_{2}}\right|_{\mathbf{V}_{2}=0} \\
\mathbf{C}&=\left.\frac{\mathbf{I}_{1}}{\mathbf{V}_{2}}\right|_{\mathbf{I}_{2}=0}\qquad \mathbf{D}=-\left.\frac{\mathbf{I}_{1}}{\mathbf{I}_{2}}\right|_{\mathbf{V}_{2}=0}
\end{align*}$$
- $\mathbf{A}$ - open circuit voltage ratio
-  $\mathbf{B}$ - negative short circuit transfer impedance
-  $\mathbf{C}$ - open circuit transfer admittance
-  $\mathbf{D}$ - negative short circuit current ratio

### Inverse transmission parameters
$$\left[\begin{matrix} \mathbf{V}_{2}\\ \mathbf{I}_{2} \end{matrix}\right]=\left[\begin{matrix} \mathbf{a} & \mathbf{b} \\ \mathbf{c} & \mathbf{d} \end{matrix}\right]\left[\begin{matrix} \mathbf{V}_{1}\\ -\mathbf{I}_{1} \end{matrix}\right]$$
The *inverse transmission* parameters, denoted as *T'-parameters*, *T-parameters*, or *abcd-parameters*, form the *inverse matrix* of the transmission matrix.
$$\begin{align*}
\mathbf{a}&=\left.\frac{\mathbf{V}_{2}}{\mathbf{V}_{1}}\right|_{\mathbf{I}_{1}=0}\qquad \mathbf{b}=-\left.\frac{\mathbf{V}_{2}}{\mathbf{I}_{1}}\right|_{\mathbf{V}_{1}=0} \\
\mathbf{c}&=\left.\frac{\mathbf{I}_{2}}{\mathbf{V}_{1}}\right|_{\mathbf{I}_{1}=0}\qquad \mathbf{d}=-\left.\frac{\mathbf{I}_{2}}{\mathbf{I}_{1}}\right|_{\mathbf{V}_{1}=0}
\end{align*}$$
- $\mathbf{a}$ - open circuit voltage gain
-  $\mathbf{b}$ - negative short circuit transfer impedance
-  $\mathbf{c}$ - open circuit transfer admittance
-  $\mathbf{d}$ - negative short circuit current gain

## Relationships between parameters
The six sets of parameters of the same two-port network are all *interrelated*.

The *impedance* and *admittance* matrices can be interchanged by *matrix inversion*.
Likewise, the *hybrid* and *inverse hybrid* and the *transmission* and *inverse transmission* matrices can also be interchanged by matrix inversion.
$$\begin{align*} &[\mathbf{Z}]=[\mathbf{Y}]^{-1}\qquad &[\mathbf{Y}]=[\mathbf{Z}]^{-1} \\
&[\mathbf{h}]=[\mathbf{g}]^{-1}\qquad &[\mathbf{g}]=[\mathbf{h}]^{-1} \\
&[\mathbf{T}]=[\mathbf{T}']^{-1}\qquad &[\mathbf{T}']=[\mathbf{T}]^{-1} \\
\end{align*}$$

The remaining conversions can be achieved using *determinants*.

|               |                                                             $\mathbf{Z}$                                                              |                                                             $\mathbf{Y}$                                                              |                                                              $\mathbf{h}$                                                               |                                                             $\mathbf{g}$                                                              |                                                   $\mathbf{T}$                                                   |                                                  $\mathbf{T}'$                                                   |
|:-------------:|:-------------------------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------------------:|:---------------------------------------------------------------------------------------------------------------------------------------:|:-------------------------------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------:|:----------------------------------------------------------------------------------------------------------------:|
| $\mathbf{Z}$  |                 $\begin{matrix} \mathbf{Z}_{11} & \mathbf{Z}_{12} \\ \mathbf{Z}_{21} & \mathbf{Z}_{22} \end{matrix}$                  | $\frac{1}{\Delta\mathbf{Y}}\left[\begin{matrix}\mathbf{Y}_{22}&-\mathbf{Y}_{12}\\-\mathbf{Y}_{21}&\mathbf{Y}_{11}\end{matrix}\right]$ |         $\frac{1}{\mathbf{h}_{22}}\left[\begin{matrix}\Delta\mathbf{h}&\mathbf{h}_{12}\\-\mathbf{h}_{21}&1 \end{matrix}\right]$         |       $\frac{1}{\mathbf{g}_{11}}\left[\begin{matrix}1&-\mathbf{g}_{12}\\ \mathbf{g}_{21}&\Delta\mathbf{g} \end{matrix}\right]$        |          $\frac{1}{C}\left[\begin{matrix}\mathbf{A}&\Delta\mathbf{T}\\ 1&\mathbf{D}\end{matrix}\right]$          |  $\frac{1}{\Delta\mathbf{c}}\left[\begin{matrix}\mathbf{d}&1\\ \Delta\mathbf{t}&\mathbf{a}\end{matrix}\right]$   |
| $\mathbf{Y}$  | $\frac{1}{\Delta\mathbf{Z}}\left[\begin{matrix}\mathbf{Z}_{22}&-\mathbf{Z}_{12}\\-\mathbf{Z}_{21}&\mathbf{Z}_{11}\end{matrix}\right]$ |                 $\begin{matrix} \mathbf{Y}_{11} & \mathbf{Y}_{12} \\ \mathbf{Y}_{21} & \mathbf{Y}_{22} \end{matrix}$                  |        $\frac{1}{\mathbf{h}_{11}}\left[\begin{matrix}1&-\mathbf{h}_{12}\\ \mathbf{h}_{21}&\Delta\mathbf{h} \end{matrix}\right]$         |       $\frac{1}{\mathbf{g}_{22}}\left[\begin{matrix}\Delta\mathbf{g}&\mathbf{g}_{12}\\ -\mathbf{g}_{21}&1 \end{matrix}\right]$        |         $\frac{1}{B}\left[\begin{matrix}\mathbf{D}&-\Delta\mathbf{T}\\ -1&\mathbf{A}\end{matrix}\right]$         | $\frac{1}{\Delta\mathbf{b}}\left[\begin{matrix}\mathbf{a}&-1\\ -\Delta\mathbf{t}&\mathbf{d}\end{matrix}\right]$  |
| $\mathbf{h}$  |        $\frac{1}{\mathbf{Z}_{22}}\left[\begin{matrix}\Delta\mathbf{Z}&\mathbf{Z}_{12}\\-\mathbf{Z}_{21}&1 \end{matrix}\right]$        |       $\frac{1}{\mathbf{Y}_{11}}\left[\begin{matrix}1&-\mathbf{Y}_{12}\\ \mathbf{Y}_{21}&\Delta\mathbf{Y} \end{matrix}\right]$        |                  $\begin{matrix} \mathbf{h}_{11} & \mathbf{h}_{12} \\ \mathbf{h}_{21} & \mathbf{h}_{22} \end{matrix}$                   | $\frac{1}{\Delta\mathbf{g}}\left[\begin{matrix}\mathbf{g}_{22}&-\mathbf{g}_{12}\\-\mathbf{g}_{21}&\mathbf{g}_{11}\end{matrix}\right]$ |         $\frac{1}{D}\left[\begin{matrix}\mathbf{B}&\Delta\mathbf{T}\\ -1&\mathbf{C}\end{matrix}\right]$          |  $\frac{1}{\Delta\mathbf{a}}\left[\begin{matrix}\mathbf{b}&1\\ \Delta\mathbf{t}&\mathbf{c}\end{matrix}\right]$   |
| $\mathbf{g}$  |       $\frac{1}{\mathbf{Z}_{11}}\left[\begin{matrix}1&-\mathbf{Z}_{12}\\ \mathbf{Z}_{21}&\Delta\mathbf{Z} \end{matrix}\right]$        |       $\frac{1}{\mathbf{Y}_{22}}\left[\begin{matrix}\Delta\mathbf{Y}&\mathbf{Y}_{12}\\ -\mathbf{Y}_{21}&1 \end{matrix}\right]$        | $\frac{1}{\Delta\mathbf{h}}\left[\begin{matrix}\mathbf{h}_{22}&-\mathbf{h}_{12}\\ -\mathbf{h}_{21}&\mathbf{h}_{11} \end{matrix}\right]$ |                 $\begin{matrix} \mathbf{g}_{11} & \mathbf{g}_{12} \\ \mathbf{g}_{21} & \mathbf{g}_{22} \end{matrix}$                  |         $\frac{1}{A}\left[\begin{matrix}\mathbf{C}&-\Delta\mathbf{T}\\ 1&\mathbf{B}\end{matrix}\right]$          |  $\frac{1}{\Delta\mathbf{d}}\left[\begin{matrix}\mathbf{c}&-1\\ \Delta\mathbf{t}&\mathbf{b}\end{matrix}\right]$  |
| $\mathbf{T}$  |         $\frac{1}{\mathbf{Z}_{21}}\left[\begin{matrix}\mathbf{Z}_{11}&\Delta\mathbf{Z}\\1&\mathbf{Z}_{22}\end{matrix}\right]$         |      $\frac{1}{\mathbf{Y}_{21}}\left[\begin{matrix}-\mathbf{Y}_{22}&-1\\ -\Delta\mathbf{Y}&-\mathbf{Y}_{11} \end{matrix}\right]$      |       $\frac{1}{\mathbf{h}_{21}}\left[\begin{matrix}-\Delta\mathbf{h}&-\mathbf{h}_{11}\\ -\mathbf{h}_{22}&-1 \end{matrix}\right]$       |        $\frac{1}{\mathbf{g}_{21}}\left[\begin{matrix}1&\mathbf{g}_{22}\\ \mathbf{g}_{11}&\Delta\mathbf{g} \end{matrix}\right]$        |                 $\begin{matrix} \mathbf{A} & \mathbf{B} \\ \mathbf{C} & \mathbf{D} \end{matrix}$                 | $\frac{1}{\Delta\mathbf{t}}\left[\begin{matrix}\mathbf{d}&\mathbf{b}\\ \mathbf{c}&\mathbf{a}\end{matrix}\right]$ |
| $\mathbf{T}'$ |         $\frac{1}{\mathbf{Z}_{12}}\left[\begin{matrix}\mathbf{Z}_{22}&\Delta\mathbf{Z}\\1&\mathbf{Z}_{11}\end{matrix}\right]$         |      $\frac{1}{\mathbf{Y}_{12}}\left[\begin{matrix}-\mathbf{Y}_{11}&-1\\ -\Delta\mathbf{Y}&-\mathbf{Y}_{22} \end{matrix}\right]$      |         $\frac{1}{\mathbf{h}_{12}}\left[\begin{matrix}1&\mathbf{h}_{11}\\ \mathbf{h}_{22}&\Delta\mathbf{h} \end{matrix}\right]$         |      $\frac{1}{\mathbf{g}_{12}}\left[\begin{matrix}-\Delta\mathbf{g}&-\mathbf{g}_{22}\\ -\mathbf{g}_{11}&-1 \end{matrix}\right]$      | $\frac{1}{\Delta\mathbf{T}}\left[\begin{matrix}\mathbf{D}&\mathbf{B}\\ \mathbf{C}&\mathbf{A}\end{matrix}\right]$ |                 $\begin{matrix} \mathbf{a} & \mathbf{b} \\ \mathbf{c} & \mathbf{d} \end{matrix}$                 |

## Types of two-port networks
A two-port network is *symmetrical* if its *input impedance* is equal to its *output impedance*.
$$
\mathbf{Z}_{11}=\mathbf{Z}_{22}
$$
A network is *reciprocal* if the voltage at port $2$ due to the current applied at port $1$ is equal to the voltage at port $1$ due to the current applied at port $2$. A network consisting entirely of linear passive components will typically be reciprocal.
$$\begin{gather*}
\mathbf{Z}_{12}=\mathbf{Z}_{21} \\
\mathbf{y}_{12}=\mathbf{y}_{21} \\
\mathbf{h}_{12}=-\mathbf{h}_{21} \\
\mathbf{AD}-\mathbf{BC}=1 \\
\mathbf{ad}-\mathbf{bc}=1
\end{gather*}$$
