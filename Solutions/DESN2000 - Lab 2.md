# DESN2000 - Lab 2
## Implementing Basic Arithmetic
### Write down the syntax of the ARM instruction which performs subtraction.
```armasm
sub{cond}{s} Rd, Rn, shift_op
```
## Integer Numbers
### With n = 4 bits, write down the signed representation of -8 and find its 2's complement. What number does this represent? Why?
From table 5, $-8$ is represented as $1000$ in signed binary, specifically in [[Signed Binary Numbers#Signed 2's complement|signed 2's complement representation]].

To find the [[Radix Complement|2's complement]], each bit of the number is *complemented* then *one* is added.
$$1000\xrightarrow[]{\text{inversion}}0111\xrightarrow[]{+1}1000$$
Thus the 2's complement of the representation of $-8$ returns $-8$ in the same representation. This is because the range of binary values for which the leading bit is a $0$ needs to include the *decimal* $0$ and thus the decimal $8$ can not be represented using this representation with $4$ bits.

## Stepping Through a Loop
### Does R0 contain the value you expect once the loop has finished executing?
The value that was expected to be stored in R0 was $2^{31}$ which is 0x80000000 which is the value contained in R0 after execution

### What would happen if the instruction "bgt exit" was used instead in *simple_loop.s*?
The value that would be expected in R0 would be $2^{32}$ instead, which is a value that the register can not store without overflow.

## Comparing Signed and Unsigned Integers
### What condition flag configuration would indicate an unsigned number is greater than another?
Assuming the larger number is stored in the register written first in the syntax, then the condition flag configuration would be as follows:
$$\begin{gather*}
N=0 \\
Z=0 \\
C=1 \\
V=0 \\
\end{gather*}$$
Particularly, $C=1$ *and* $Z=0$ are the required conditions. Note that in ARM architecture the value of the carry flag is $1$ for when there is *no* carry.

## Lowercase to Uppercase
### Inspecting Table 7 above, what arithmetic operation would you perform to convert an ASCII character from lowercase to uppercase?
To convert a valid ASCII character from lowercase to uppercase, simply add $32_{10}$, $100000_{2}$, or $20_{16}$ to the value representing the character.