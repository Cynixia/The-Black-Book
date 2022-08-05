# Binary Multiplication
Binary digit multiplication is equivalent to the Boolean [[Logical Operations#Conjunction|AND]] function.

| $a\times b$ | $b=0$ | $b=1$ |
|:-----------:|:-----:|:-----:|
|    $a=0$    |  $0$  |  $0$  |
|    $a=1$    |  $0$  |  $1$  |

As in decimal multiplication, *partial products* are calculated then summed up for the result. In binary multiplication, partial products are either *all zero* or the same as the *multiplicand*, i.e. $1011$ in the below example.

An $m$ digit *multiplicand* by $n$ digit *multiplier* multiplication generates *up to* an $m+n$ digit result.

The following is the computation of $11\times 14=154$.

![[BinaryMultiplicationUnsigned.svg|250]]

*Multiplying* a number by $2^{k}$ shifts the number to the *left* by $k$ bits.  *Dividing* a number by $2^{k}$ shifts the number to the *right* by $k$ bits.

## Signed 2's complement multiplication
In [[Signed Binary Numbers#Signed 2's complement|signed 2's complement]] multiplication, the multiplicand, multiplier, and all partial products must be [[Signed Binary Numbers#Sign extension|sign extended]] to the *product bit width* $m\times n$. The result is also only read up to the bit width.

Multiplication by a *positive* value creates a shorter computation overall.

The following is the computation of $-6\times 7=-42$, without and with sign extension. Note that under sign extension, the result is limited to $4+4=8$ bits.

![[BinaryMultiplicationSignedComparison.svg]]

## Implementation
### Unsigned multiplication
#### Adder tree
A simple but *slow* implementation of unsigned binary multiplication is an [[adder]] tree. 

Partial products are formed using $m\times n$ AND gates. They are then summed to form the result using adders. $n-1$ adders of $m$ bit width are required. 

The first adder receives an additional *zero* input since the *least significant bit* of the first partial product is taken as part of the result. It is appended to the *front* of the first partial product.

Each successive adder does not receive the least significant bit of the *previous* partial product summation.

Below is a 4 bit by 4 bit binary multiplier implemented by an adder tree.

![[BinaryMultiplicationAdderTree.svg]]

#### Iterative array
Binary multiplication can also be implemented as an [[Iterative Circuit|iterative array]], which is a faster method.

Each *cell* of the array receives a carry-in and a bit of the *incoming* partial product sum (PPS), the multiplicand $m$, and the multiplier $n$. It computes the *current* partial product then adds it to the *partial product sum*.

The first row of the array receives a *zero* input as the *incoming* partial product. The right-most cells also receive a *zero* input as the *carry-in*.

Below is a 4 bit by 4 bit binary multiplier implemented by an iterative array. An individual cell is also shown.

![[BinaryMultiplicationArrayCell.svg|550]]

![[BinaryMultiplicationArray.svg|875]]

### Signed 2's complement multiplication
#### Baugh-Wooley algorithm
[[Baugh-Wooley Algorithm]]
#unfinished