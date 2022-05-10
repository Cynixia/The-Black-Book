# Adder
**An [[arithmetic circuit]] that performs addition of numbers.**

The most common adders operate on binary numbers.

## Half adder
A *half adder* adds two *single* binary digits and has two outputs, *sum* and *carry*. The carry output is also known as the *carry-out* of the adder.
$$S=A\oplus B \qquad C=AB$$

| Inputs |     | Outputs |     |
|:------:|:---:|:-------:|:---:|
|  $A$   | $B$ |   $C$   | $S$ |
|  $0$   | $0$ |   $0$   | $0$ |
|  $0$   | $1$ |   $0$   | $1$ |
|  $1$   | $0$ |   $0$   | $1$ |
|  $1$   | $1$ |   $1$   | $0$    |


![[HalfAdder.svg|500]]

## Full adder
A *full adder* adds three input bits, two *operands* and one *carry-in* bit. The carry-in bit is the bit "carried in" from a previous operation stage, such as the bit "carried out" but a half adder.
$$S=A\oplus B\oplus C_{\text{in}} \qquad C_{\text{out}}=AB+C_{\text{in}}(A\oplus B)$$

| Inputs |     |                 |     Outputs      |     |
|:------:|:---:|:---------------:|:----------------:|:---:|
|  $A$   | $B$ | $C_{\text{in}}$ | $C_{\text{out}}$ | $S$ |
|  $0$   | $0$ |       $0$       |       $0$        | $0$ |
|  $0$   | $0$ |       $1$       |       $0$        | $1$ |
|  $0$   | $1$ |       $0$       |       $0$        | $1$ |
|  $0$   | $1$ |       $1$       |       $1$        | $0$ |
|  $1$   | $0$ |       $0$       |       $0$        | $1$ |
|  $1$   | $0$ |       $1$       |       $1$        | $0$ |
|  $1$   | $1$ |       $0$       |       $1$        | $0$ |
|  $1$   | $1$ |       $1$       |       $1$        | $1$ |

A full adder can be constructed from two half adders and an OR gate.

![[FullAdder.svg]]

## Ripple-carry adder
A *ripple-carry adder* is an adder constructed from *cascading* $n$ full adders. This type of adder can add $n$-bit numbers.

Each full adder inputs $C_{\text{in}}$ from the $C_{\text{out}}$ output of the previous adder. The *first* adder can be replaced by a half adder.

Ripple-carry adders can accept all $n$-bit inputs simultaneously but each adder must wait for the carry to *propagate* through every previous adder. Thus, ripple-carry adders are *easy to design* but are *slow*.

## Carry-lookahead adder
A *carry-lookahead adder* utilises the concepts of *generating* and *propagating* carries.

The addition of two *single* bit digits $A$ and $B$ *generates* if the addition will *always carry*. This occurs when $A=B=1$ and will occur regardless of any carry-in bit.
$$G_{i}=A_{i}B_{i}$$
The addition of two single bit digits $A$ and $B$ *propagates* if the addition will carry *if* there is a carry-in bit. This occurs when either $A$ or $B=1$ but not both.
$$P_i=A_{i}\oplus B_{i}$$
Note that the above definitions are only dependant on a single digit of addition.

| $A$ | $B$ | $C_{\text{in}}$ | $C_{\text{out}}$ |   Carry    |
|:---:|:---:|:---------------:|:----------------:|:----------:|
| $0$ | $0$ |       $0$       |       $0$        |    None    |
| $0$ | $0$ |       $1$       |       $0$        |    None    |
| $0$ | $1$ |       $0$       |       $0$        |    None    |
| $0$ | $1$ |       $1$       |       $1$        | Propagates |
| $1$ | $0$ |       $0$       |       $0$        |    None    |
| $1$ | $0$ |       $1$       |       $1$        | Propagates |
| $1$ | $1$ |       $0$       |       $1$        | Generates  |
| $1$ | $1$ |       $1$       |       $1$        | Generates           |

The *sum* and *carry* outputs can be redefined in terms of *generate* and *propagate*.
$$S_i=P_{i}\;\oplus C_{in} \qquad C_{i+1}=G_i+C_iP_i$$
Thus, all carry bits can be calculated directly from the inputs, without needing to wait for a carry to propagate through the circuit. As such, carry-lookahead adders are *more complex* but are *faster*.

To achieve larger adders, $4$-bit carry-lookahead adders can be cascaded and connected to a group lookahead carry unit.