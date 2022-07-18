# State Table
**A table showing the inputs, present and next state, and outputs of a [[sequential circuit]].**

A state table is also known as a *transition table* and displays *all possible* binary combinations of present states and input. 

A state table is filled using logic diagrams, [[State Equation|state equations]], or [[Excitation Table|excitation tables]].

> [!Example]
For the following state equations,
>$$\begin{align*}
A(t+1)&=AX+BX \\
&=X(A+B) \\
B(t+1)&=\bar{A}X \\
Y(t+1)&=\bar{X}(A+B)
\end{align*}$$
the state table is:
>
| Present <br /> state |     | Next <br /> state |     |       |     | Output |       |
|:--------------------:|:---:|:-----------------:|:---:|:-----:|:---:|:------:|:-----:|
|                      |     |       $X=0$       |     | $X=1$ |     | $X=0$  | $X=1$ |
|         $A$          | $B$ |        $A$        | $B$ |  $A$  | $B$ |        |       |
|         $0$          | $0$ |        $0$        | $0$ |  $0$  | $1$ |  $0$   |  $0$  |
|         $0$          | $1$ |        $0$        | $0$ |  $1$  | $1$ |  $1$   |  $0$  |
|         $1$          | $0$ |        $0$        | $0$ |  $1$  | $0$ |  $1$   |  $0$  |
|         $1$          | $1$ |        $0$        | $0$ |  $1$  | $0$ |  $1$   |  $0$  | 
