# Gate Input Cost
**The number of inputs to basic logic gates in an implementation.**

Gate input cost, GIC, is typically *only* considered in circuits with basic [[Logical Operations|logic gates]]; AND, OR, and NOT gates.

It can be found graphically from a logic diagram or numerically using [[Standard Forms of a Boolean Function#SOP POS form|SOP/POS equations]].

In an SOP/POS equation, the GIC is the sum of
- *Every* literal appearance
- The number of *distinct* complemented literals
- The number of *non-literal* terms

### Example
$F=AB+\bar{C}(D+E)$

There are clearly $5$ literals, one of the literals are *complemented*, and the three *non-literal* terms are $AB$, $D+E$, and $\bar{C}(D+E)$.
Thus, the gate input cost is $9$.

![[GateInputCostCircuit.svg|500]]

## GIC of other gates
### NAND and NOR
The *equivalent* GIC of [[Universal Gate|NAND and NOR]] gates is $3$.

![[NANDNOREquivalentGIC.svg]]

### XOR and XNOR
The *equivalent* GIC of [[Boolean Algebra#Exclusive OR and Exclusive NOR|XOR and XNOR]] gates is $7$.

![[XORXNOREquivalentGIC.svg]]
