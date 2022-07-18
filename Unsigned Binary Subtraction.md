# Unsigned Binary Subtraction
In normal unsigned binary subtraction, the *subtrahend* is subtracted from the *minuend* and the result is corrected if it is *negative*.
 
If *borrowing* is required in the most significant position, then the result is *negative*.

Unsigned binary subtraction of two $n$ digit numbers, $M-S$, can be performed as follows:
- Subtract the subtrahend from the minuend.
- If *no end borrow* occurs, then $M\ge S$ , and the result is correct.
- If an end borrow occurs, then  $S>M$, the *difference* is subtracted from $2^n$, and a *minus sign* is added to the result.

The subtraction $2^{n}-S$ is known as taking the [[Radix Complement#Binary numbers|2's complement]] of $S$.

Unsigned binary subtraction can also be achieved by addition using either [[Radix Complement#Subtraction by addition|1's complement]] or *2's complement*. Thus, unsigned binary subtraction can also be implemented using [[Adder|adders]].

## Unsigned subtraction by addition using 2's complement
[[2's complement arithmetic]] can also be used for unsigned subtraction. The process is as follows:
- Add the 2's complement of the subtrahend $S$ to the minuend $M$.
- If $M\ge S$, the answer is the sum with the end carry *discarded*.
- If $M < S$, the answer needs to be corrected by taking the *2's complement* and then adding a *minus sign* to the result.

## Examples
> [!Subtraction by addition, positive, 2's complement]
To find $1010100 - 1000011$, the sum of the subtrahend with the 2's complement of the minuend is found to be $10010001$.
>
The leading digit of the result is discarded, thus giving the correct answer $10001$.

> [!Subtraction by addition, negative, 2's complement]
To find $1000011-1010100$, the sum of the subtrahend with the 2's complement of the minuend is found to be $11011111$.
>
Taking the 2's complement of and adding a minus sign to the sum gives the correct answer $-00010001$.


