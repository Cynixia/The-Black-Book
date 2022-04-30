# BCD Addition
*Binary coded decimal* addition is like normal binary addition except that the result needs to be *corrected* to BCD if the binary value of any coded decimal digit *exceeds* $9$. This can be achieved by *adding* $6$ to any invalid BCD outputs.

For the BCD variables $X$, $Y$, $Z$, the sum variable $S$, and the carry variable $C_{\text{out}}$.
- If $Z\le 9$, then $S=Z$ and $C_{\text{out}}=0$.
- If $Z>9$, then $S=Z+6$ and $C_{\text{out}}=1$

For example, adding $5$ and $7$ using BCD gives $1100$, which is an invalid BCD number and is just a binary number of value $12$. By adding $6$ or $0110$ to the result, it becomes $0001\;0010$ which represents $12$ in BCD.

## Implementation
#unfinished
