# Base Conversion
In general, a number is converted to decimal first before it is converted to the target base.

The integer part and fractional part are converted by separate methods, then the results are joined with a radix point (known as a decimal point in base 10).

## Integer part
To convert the integer part, it is successively divided by the base into *quotient and remainder* form until the quotient is *zero*. The remainders are then read in *reverse order* of quotient size for the result.

> [!Example]
Converting $56180_{10}$ to base $20$.
> $$\begin{aligned}
 56180 \div 20 = 2809\;r\;&0 \\
 2809 \div 20 = 140\;r\;&9 \\
 140 \div 20 = 7\;r\;&0 \\
 7 \div 20 = 0\;r\;&7\\
 \end{aligned}$$
Thus, $56180_{10}=7090_{20}$

## Fractional Part
To convert the fractional part, it is successively multiplied by the base into an *integer product and fraction* until the fraction is *zero*. The integer products are then read in order.

Note that in each successive multiplication, only the fractional part of the preceding step is multiplied.

> [!Example]
Converting $0.6875_{10}$ to binary.
> $$\begin{align}
0.6875 \times 2 =\;&1.375 \\
0.375 \times 2 =\;&0.75 \\
0.75 \times 2 =\;&1.50 \\
0.50 \times 2 =\;&1.0 \\
\end{align}$$
Thus, $0.6875_{10}=0.1011_{2}$  


