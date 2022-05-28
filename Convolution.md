# Convolution
**An operation on two functions that produces a third function that expresses how the graph of one is affected by the other.**

The convolution of $f$ and $g$ is denoted as $f*g$.
$$(f*g)(t)=\int_{-\infty}^{\infty}f(\tau)g(t-\tau)\;d\tau$$
Note that the *variable of integration* is the *dummy variable* $\tau$ and $t$ is used to introduce an offset.
In words, the formula can be described as the *area* under the function $f(\tau)$ *weighted* by the function $g(-\tau)$ and *shifted* by amount $t$.

If the functions are *supported* only on $[0,\infty)$, then the integration limits can be changed.
$$(f*g)(t)=\int_{0}^{t}f(\tau)g(t-\tau)\;d\tau$$

Visually, the graph of the function $g$ is *reversed* and *slid* along the $\tau$-axis by varying $t$ from $-\infty$ to $\infty$.

![[Convolution.svg]]

## Properties
|                                  |                    Property                    |
|:--------------------------------:|:----------------------------------------------:|
|            $f*g=g*f$             |                  Commutation                   |
|        $f*(g*h)=(f*g)*h$         |                  Association                   |
|         $a(f*g)=(af)*g$          | Association under <br /> scalar multiplication |
|      $f*(g+h)=(f*g)+(f*h)$       |                  Distribution                  |
| $\overline{f*g}=\bar{f}*\bar{g}$ |   Complex conjugation  |

### Singularity functions
The convolution of a function with the [[Singularity Function#Unit impulse function|unit impulse function]] returns the function.
$$f(t)*\delta(t)=f(t)$$
$$f(t)*\delta(t-t_{0})=f(t-t_{0})$$

The convolution of a function with the *derivative* of the unit impulse function returns the derivative of the function.
$$f(t)*\delta'(t)=f'(t)$$

The convolution of a function with the [[Singularity Function#Unit step function|unit step function]] gives an integral.
$$f(t)*u(t)=\int_{-\infty}^{t}f(\tau)\;d\tau$$

## Examples
### Three regions
There are three regions of analysis in the convolution of $e^{-t}$ over the interval $t>0$ and a two high, one second pulse.

![[Convolution3RegionsFunctions.svg|600]]

The *starting point* chosen is arbitrary but allows $f(t-\tau)$ to lie initially completely to the left of $g(\tau)$.
For $t<0$, there is *no overlap* of the functions, thus
$$(f*g)(t)=0,\qquad t<0$$
![[Convolution3Regions1.svg|500]]

For $0<t<1$,
$$\begin{align*}
(f*g)(t)&=\int_{-\infty}^{\infty}f(t-\tau)g(\tau)\;d\tau \\
&=\int_{0}^{t}2e^{-(t-\tau)}\;d\tau \\
&=2(1-e^{-t}),\qquad 0<t<1
\end{align*}$$
Note that the integral here is simplified from the interval $-\infty<\tau<\infty$ to include *only* the region where there is *overlap*.
![[Convolution3Regions2.svg|500]]

For $t>1$,
$$\begin{align*}
(f*g)(t)&=\int_{0}^{1}2e^{-(t-\tau)}\;d\tau \\
&=2e^{-t}(e-1),\qquad t>1
\end{align*}$$
Again, the integral here has been simplified by limiting the interval to only the region of overlap.
![[Convolution3Regions3.svg|500]]

Thus,
$$(f*g)(t)=\begin{cases}
0, & t<0 \\
2(1-e^{-t}), & 0<t<1 \\
2e^{-t}(e-1), & t>1
\end{cases}$$
### Five regions
There are five regions of analysis in the convolution of the following $f(t)$ and $g(t)$.

![[Convolution5RegionsFunctions.svg|600]]


For $0<t<1$, there is *no overlap* of the functions, thus
$$(f*g)(t)=0,\qquad 0<t<1$$
![[Convolution5Regions1.svg|500]]

For $1<t<2$, the functions overlap between $1$ and $t$.
$$(f*g)(t)=\int_{1}^{t}(2)(1)\;d\tau=2t-2,\qquad 1<t<2$$

![[Convolution5Regions2.svg|450]]

For $2<t<3$, the functions completely overlap between $(t-1)$ and $t$.
$$(f*g)(t)=\int_{t-1}^{t}(2)(1)\;d\tau=2,\qquad 2<t<3$$


![[Convolution5Regions3.svg|450]]

For $3<t<4$, the functions overlap between $(t-1)$ and $3$.
$$(f*g)(t)=\int_{t-1}^{3}(2)(1)\;d\tau=8-2t,\qquad 3<t<4$$
![[Convolution5Regions4.svg|450]]

For $t>4$, $f(t-\tau)$ is slid completely to the right of $g(\tau)$ and thus there is once again *no overlap*.
$$(f*g)(t)=0,\qquad t>4$$

Thus,
$$(f*g)(t)=\begin{cases}
0, &0\le t\le1 \\
2t-2, &1\le t\le 2 \\
2, &2\le t\le 3 \\
8-2t, &3\le t\le 4 \\
0, &t\ge t
\end{cases}$$
