# Integer Overflow
**The event in which an arithmetic operation attempts to create a value outside the range that can be represented by a given number of digits.**

For *unsigned* operations, if there is a carry-out of the *most significant bit* then an overflow has occurred with a carry or a borrow from the most significant bit.

For [[Signed Binary Numbers#Signed 2's complement|signed]] operations, a *signed* overflow has occurred if the carry-in of the *sign bit* is *not equal* to the carry-out. This causes the sign of the result to be *incorrect*.

An overflow and its type are indicated using [[Arithmetic Circuit#Status flags|status flags]] in arithmetic circuits.
