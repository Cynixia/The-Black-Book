# Encoder
**A circuit that converts $2^n$ inputs to $n$ coded outputs.**

It is the [[Duality#Boolean algebra|dual]] of a [[decoder]] circuit.

## $1$-of-$n$ encoder
$1$-of-$n$ encoders can only accept *one* HIGH input at any time. The most common encoders of this type are $2^n$-to-$n$ encoders.

### $2^n$-to-$n$ encoder
$2^n$-to-$n$-line encoders can be thought of as a circuit that encodes a decimal number, represented by a unique input line, and outputting its binary equivalent.

Below is a $4$-to-$2$-line decoder.

$A_{0}=D_{1}D_{2}\qquad A_{1}=D_{2}D_{3}$

| $D_{3}$ | $D_2$ | $D_1$ | $D_0$ | $A_1$ | $A_0$ |
|:-------:|:-----:|:-----:|:-----:|:-----:|:-----:|
|   $0$   |  $0$  |  $0$  |  $1$  |  $0$  |  $0$  |
|   $0$   |  $0$  |  $1$  |  $0$  |  $0$  |  $1$  |
|   $0$   |  $1$  |  $0$  |  $0$  |  $1$  |  $0$  |
|   $1$   |  $0$  |  $0$  |  $0$  |  $1$  |  $1$  |

![[4to2Encoder.svg|450]]

## Priority encoder
A priority encoder only outputs according to the *most significant* input that is $1$. Thus, priority encoders can accept *more than one* HIGH input at a time.

Priority encoders also have an additional output called the *valid* output, which distinguishes between when all inputs are off and when $D_0$ is off.

Below is a $4$-to-$2$ priority encoder.

$A_{0}=D_{1}\bar{D_{2}}+D_{3}\qquad A_{1}=D_{2}+D_{3}\qquad V=D_{0}+D_{1}+D_{2}+D_{3}$

| $D_{3}$ |  $D_2$   |  $D_1$   |  $D_0$   |  $A_1$   |  $A_0$   |   $V$    |
|:-------:|:--------:|:--------:|:--------:|:--------:|:--------:|:--------:|
|   $0$   |   $0$    |   $0$    |   $0$    | $\times$ | $\times$ | $0$ |
|   $0$   |   $0$    |   $0$    |   $1$    |   $0$    |   $0$    |    $1$      |
|   $0$   |   $0$    |   $1$    | $\times$ |   $0$    |   $1$    |     $1$     |
|   $0$   |   $1$    | $\times$ | $\times$ |   $1$    |   $0$    |      $1$    |
|   $1$   | $\times$ | $\times$ | $\times$ |   $1$    |   $1$    |     $1$     |

![[4to2PriorityEncoder.svg]]
