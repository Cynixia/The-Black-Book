# Decoder
**A circuit that converts $n$ coded inputs to a maximum of $2^n$ unique outputs.**

It is the [[Duality|dual]] of an [[encoder]] circuit.

## $1$-of-$n$ decoder
$1$-of-$n$ decoders asserts *exactly one* of its outputs or none of them. The most common decoders of this type are $n$-to-$2^{n}$-line decoders.

### $n$-to-$2^n$-line decoders
$n$-to-$2^n$-line decoders can be thought of as a circuit decoding binary into decimal, where each decimal number has its own output line.

The simplest $n$-to-$2^n$-line decoder is a $1$-to-$2$ decoder, which is used in every other larger decoder.

$D_{0}=\bar{A}\qquad D_{1}=A$

| $A$ | $D_0$ | $D_1$ |
|:---:|:-----:|:-----:|
| $0$ |  $1$  |  $0$  |
| $1$ |  $0$  |  $1$  |

![[1to2Decoder.svg|450]]

Below is a $2$-to-$4$-line decoder.

$D_{0}=\bar{A_{1}}A_{0}\qquad D_{1}=\bar{A_{1}}A_{0}\qquad D_{2}=A_{1}\bar{A_{0}}\qquad D_{3}=A_{1}A_{0}$

| $A_{1}$ | $A_0$ | $D_0$ | $D_1$ | $D_2$ | $D_3$ |
|:-------:|:-----:|:-----:|:-----:|:-----:|:-----:|
|   $0$   |  $0$  |  $1$  |  $0$  |  $0$  |  $0$  |
|   $0$   |  $1$  |  $0$  |  $1$  |  $0$  |  $0$  |
|   $1$   |  $0$  |  $0$  |  $0$  |  $1$  |  $0$  |
|   $1$   |  $1$  |  $0$  |  $0$  |  $0$  |  $1$  |

![[2to4Decoder.svg]]

#### $n$-to-$2^n$ decoder expansion
$n$-to-$2^n$-line decoders can be cascaded together into larger decoders using only 2-input AND gates.

To construct an $n$-bit decoder:
- Determine the smaller decoders required.
	   - If $n$ is *even*, use $2^n$ AND gates driven by *two* decoders of output size $2^{\frac{n}{2}}$.
	   - If $n$ is *odd*, use $2^n$ AND gates driven by a decoder of output size $2^{\frac{{n+1}}{2}}$ and a decoder of output size $2^{\frac{{n-1}}{2}}$.
- Repeat the previous step for each new decoder generated in the previous step until $n=1$.  The decoder for $n=1$ is a $1$-to-$2$-line decoder.

Below is a $3$-to-$8$-line decoder with parts from the procedure indicated. Note that the combination of 2 $1$-to-$2$-line decoders and 4 $2$-input AND gates is a $2$-to-$4$-line decoder.

![[3to8Decoder.svg]]