# Arithmetic Circuit
**A combinational circuit that performs arithmetic or bitwise operations on integer binary numbers.**

Arithmetic circuits are [[Iterative Circuit|iterative circuits]]. The inputs are known as *operands* and both inputs and outputs are *vector signals* which form a data [[bus]].

## Status flags
In most microprocessors arithmetic circuits use *status flags* to provide information about its operation results.
- *N* - negative - $1$ if the result is negative, $0$ if positive
- *Z* - zero - $1$ if the result is zero, $0$ if non-zero
- *C* - carry - $1$ if there is carry-out, $0$ if no carry-out
- *V* - [[Integer Overflow|overflow]] - $1$ if [[Signed Binary Numbers#Signed 2's complement|signed]] overflow, $0$ if no such overflow

For an $n$-bit arithmetic circuit, these can be implemented with:
$$\begin{align*}
N&=S_{n-1} \\
Z&=\overline{S_{n-1}}\;\overline{S_{n-2}}\cdots \overline{S_{0}} \\
C&=C_{n} \\
V&=C_{n}\oplus C_{n-1}
\end{align*}$$
where $S$ denotes *sum* bits and $C$ denotes *carry* bits.