# Signed Binary Numbers
*Signed* binary numbers are represented in circuits by defining the *most significant* bit as the *sign* bit. This bit is $0$ for *positive* numbers and $1$ for *negative* numbers.

There are several methods of signed binary number representation.

## Sign-magnitude
In *sign-magnitude* representation, also known as *signed magnitude*, the remaining bits after the sign bit represent the magnitude of the number.
$$\begin{align*} 00011001_{2}&=25_{10}\\
10011001_{2}&=-25_{10} \end{align*}$$
| Binary value | Sign-magnitude <br /> interpretation |
|:------------:|:------------------------------------:|
|  $00000000$  |                 $0$                  |
|  $00000001$  |                 $1$                  |
|   $\vdots$   |               $\vdots$               |
|  $01111101$  |                $125$                 |
|  $01111110$  |                $126$                 |
|  $01111111$  |                $127$                 |
|  $10000000$  |                 $-0$                 |
|  $10000001$  |                 $-1$                 |
|  $10000010$  |                 $-2$                 |
|   $\vdots$   |               $\vdots$               |
|  $11111101$  |                $-125$                |
|  $11111110$  |                $-126$                |
|  $11111111$  | $-127$                                     |

Sign-magnitude representation has multiple consequences to consider during implementation:
- Zero exists as a *signed zero*.
- Addition and subtraction require *different behaviour* depending on the sign bit.
- Arithmetic results need to be *corrected*.

## Signed 1's complement
In *signed* [[Radix Complement|1's complement]] representation, a negative number is represented as the *bitwise complement* of the positive number. 
$$\begin{align*} 00011001_{2}&=25_{10}\\
11100110_{2}&=-25_{10} \end{align*}$$
| Binary value | Signed 1's complement <br /> interpretation |
|:------------:|:-------------------------------------------:|
|  $00000000$  |                     $0$                     |
|  $00000001$  |                     $1$                     |
|   $\vdots$   |                  $\vdots$                   |
|  $01111101$  |                    $125$                    |
|  $01111110$  |                    $126$                    |
|  $01111111$  |                    $127$                    |
|  $10000000$  |                   $-127$                    |
|  $10000001$  |                   $-126$                    |
|  $10000010$  |                   $-125$                    |
|   $\vdots$   |                  $\vdots$                   |
|  $11111101$  |                    $-2$                     |
|  $11111110$  |                    $-1$                     |
|  $11111111$  |                    $-0$                     |

Signed 1's complement has the following consequences:
- Zero exists as a *signed zero*.
- Addition requires doing an *end-around carry*.

## Signed 2's complement
In *signed* [[Radix Complement|2's complement]] representation, a negative number is represented as the bitwise complement of the positive number *plus* $1$.
$$\begin{align*} 00011001_{2}&=25_{10}\\
11100111_{2}&=-25_{10} \end{align*}$$
| Binary value | Signed 2's complement <br /> interpretation |
|:------------:|:-------------------------------------------:|
|  $00000000$  |                     $0$                     |
|  $00000001$  |                     $1$                     |
|   $\vdots$   |                  $\vdots$                   |
|  $01111110$  |                    $126$                    |
|  $01111111$  |                    $127$                    |
|  $10000000$  |                   $-128$                    |
|  $10000001$  |                   $-127$                    |
|  $10000010$  |                   $-126$                    |
|   $\vdots$   |                  $\vdots$                   |
|  $11111110$  |                    $-2$                     |
|  $11111111$  |                    $-1$                     |

Signed 2's complement is the preferred representation as it does not have the consequences of *sign-magnitude* and *1's complement* representations.

Additionally, [[2's complement arithmetic]] can be implemented using the same circuits used in [[Adder|unsigned binary addition]].

### Negative signed 2's complement binary to decimal
To convert a negative signed 2's complement binary number to decimal, either:
- Take the *2's complement* of the negative number to find the corresponding positive number, then adding a *minus sign*.
- Convert the number as usual but *remove* the value of the most significant bit.

For example, for the $8$-bit number $1110\;1101$:
- 2's complement is $0001\;0011_{2}=19_{10}$, thus $1110\;1101_{2}=-19_{10}$
- $1110\;1101_{2}=2^{0}+2^{2}+2^{3}+2^{5}+2^{6}-2^{7}=-19_{10}$

## Sign extension
To represent a signed $n$-bit number with additional bits, the extra bits are set to the value of the most significant bit.

For example, to convert $-7$ from $4$-bits to $8$-bits:
$$1001\longrightarrow 1111\;1001$$