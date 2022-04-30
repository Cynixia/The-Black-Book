# Radix complement
The *radix complement* of an $n$ digit number $N$ in radix $r$ is defined as
$$r^n-N$$
In practice, the radix complement is more easily found by adding $1$ to the *diminished radix complement*, which is defined as
$$(r^n-1)-N$$
This is because $r^n-1$ is the digit $r-1$ repeated $n$ times. Thus, the diminished radix complement of a number is found by *complementing* each digit with respect to $b-1$. That is, the difference between each digit and $b-1$.

In *digital circuits*, complements allow for the same logic to be used for addition and subtraction, since subtraction can be implemented as addition using complements.

## Subtraction by addition
For a minuend $M$ and substrahend $S$, subtraction by addition is performed as follows:
- Add the diminished radix complement of $M$ to $S$.
- If $M \ge S$, then the answer is the diminished radix complement of the sum.
- If $M < S$, then the answer is the sum *plus* $1$, with a *minus sign*, and *without* the leading digit.

## Binary numbers
As there are only two digits in binary, the 1's complement of a binary number $N$ is easily found by *inverting* every bit in $N$. The 2's complement can then be found by adding $1$. 

## Examples
### Finding 10's complement
To find the 10's complement of $873$, the 9's complement is found first.

The 9's complement is $999 - 873 = 126$. Adding one to the result gives $127$, which is equal to $10^{3}-873$.

### Finding 2's complement
To find the 2's complement of $01110011$, the 1's complement is found first.

The 1's complement is just the number with its bits inverted, which is $10001100$. Adding one gives the 2's complement $10001101$.

### Subtraction by addition - base 10 - positive
To determine $873 - 218$, the 9's complement of the minuend, $873$, is added to the subtrahend $218$. The 9's complement of that result will give the difference.

The 9's complement of $873$ is $126$. Adding this to the minuend gives $344$.

The 9's complement of $344$ is $655$, which is equal to $873-218$.

### Subtraction by addition - base 10 - negative
To determine $89-92$, the 9's complement of the minuend, $89$, is added to the subtrahend $92$.

This results in $102$. As the minuend is *smaller* than the subtrahend, the difference is determined to be $-3$.

### Subtraction by addition - base 2 - positive
To find $00110000 - 00010100$, the 1's complement of the minuend is added to the subtrahend.

The 1's complement of the minuend is $00001111$ and added to the subtrahend it becomes $00100011$.

The 1's complement of the sum gives the correct answer $00011100$.

### Subtraction by addition - base 2 - negative
To find $1000011 - 1010100$, the 1's complement of $1000011$ is added to the $1010100$.

The 1's complement is $0111100$ and added to the subtrahend it becomes $10010000$.

Adding a $1$, removing the leading digit, and adding a minus sign to the sum gives the correct answer $-00010001$.