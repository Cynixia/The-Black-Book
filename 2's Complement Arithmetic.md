# 2's Complement Arithmetic
2's complement arithmetic is the most prevalent arithmetic representation and works with both *signed and unsigned* operands. 2's complement arithmetic can be implemented using simple [[Adder|adders]].

## Addition
Addition using 2's complement numbers requires *no special process*, even if the operands are of different signs. 

The carry-out bit from the most significant bit position is *discarded* and the result will be a [[Signed Binary Numbers#Signed 2's complement|signed 2's complement]] number.

For example, when adding $-6$ and $-13$:
$$11111010+11110011=\cancel{1}11101101$$
The 2's complement of the result gives the magnitude as $00010011$ which is $19$, as expected.

## Subtraction
Subtraction with 2's complement numbers is achieved by adding the *2's complement* of the *subtrahend* to the minuend.

The carry-out bit from the most significant bit position is *discarded*.

For example, when subtracting $6$ from $13$:
$$11111010+00001101=00000111$$

## Implementation
Below is a 2's complement adder/subtractor, consisting of 4 [[Adder#Full adder|full adders]] and XOR gates.

![[2sComplementAdderSubtractor.svg|900]]

If $\text{Sub}=0$, the vector signal $B$ enters the full adders and the carry-in is $0$, and $A+B$ is calculated.

If $\text{Sub}=1$, the vector signal $B$ is *complemented* and the carry-in is $1$, allowing for the 2's complement to be obtained and thus $A+(-B)=A-B$ is calculated.