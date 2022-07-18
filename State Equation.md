# State Equation
**A Boolean function describing the next state of a [[sequential circuit]] in terms of the present state and inputs.**

A state equation is also known as a *transition equation* and relates the outputs of the flip-flop to the inputs of the sequential circuit.

> [!Example]
> In the following circuit, the next state is the same as the flip-flop input for D flip-flops.
>
> ![[DFlipFlopSequentialExample.svg]]
The state equations are:
> $$\begin{align*}
A(t+1)&=AX+BX \\
&=X(A+B) \\
B(t+1)&=\bar{A}X \\
Y(t+1)&=\bar{X}(A+B)
\end{align*}$$

