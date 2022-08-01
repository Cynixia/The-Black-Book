# BCD Addition
*Binary coded decimal* addition is like normal binary addition except that the result needs to be *corrected* to BCD if the binary value of any coded decimal digit *exceeds* $9$. 

This can be achieved by *adding* $6$ to any invalid BCD outputs.

For the result variable $Z$, the true BCD sum variable $S$, and the carry variable $C_{\text{out}}$:
- If $Z\le 9$, then $S=Z$ and $C_{\text{out}}=0$.
- If $Z>9$, then $S=Z+6$ and $C_{\text{out}}=1$

For example, adding $5$ and $7$ using BCD gives $1100$, which is an invalid BCD number and is just the binary equivalent $12$. By adding $6$ or $0110$ to the result, it becomes $0001\;0010$ which represents $12$ in BCD.

## Implementation
To implement the BCD addition of one digit, a four-bit [[Adder#Full adder|adder]] is followed by logic which determines if adjustment is required and a two-bit adder for the adjustment.

Note that if there is *carry out* in the four-bit adder or $Z_{3}$ *and* either $Z_{2}$ or $Z_{1}$ are on then $Z>9$. Additionally, adding $6$ or $0110$ to the result only affects the middle two bits $Z_{2}$ and $Z_{1}$.

![[BCDAdditionImplementation.svg]]