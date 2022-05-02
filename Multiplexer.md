# Multiplexer
**A circuit that selects an input from several and forwards it to a single output.**

A multiplexer or *mux* of $2^{n}$ *information* inputs has $n$ *select* lines. The inputs are labelled according to the binary combination of the select lines.

The inverse of a multiplexer is a [[demultiplexer]].

Below is a $4$-to-$1$-line multiplexer.

$Z=(I_{0}\bar{S_{0}}\bar{S_{1}})+(I_{1}S_{0}\bar{S_{1}})+(I_{2}\bar{S_{0}}S_{1})+(I_{3}S_{0}S_{1})$

| $S_1$ | $S_0$ |  $Z$  |
|:-----:|:-----:|:-----:|
|  $0$  |  $0$  | $I_0$ |
|  $0$  |  $1$  | $I_1$ |
|  $1$  |  $0$  | $I_2$ |
|  $1$  |  $1$  | $I_{3}$      |

![[4to1Multiplexer.svg|300]]

A multiplexer can be implemented using a [[decoder]], $2$-input AND gates, and an OR gate.

Below is the same $4$-to-$1$-line multiplexer.

![[4to1MultiplexerConstruction.svg|800]]

## Cascading multiplexers
Larger multiplexers are implemented by *cascading* smaller multiplexers.

Below is an $8$-to-$1$-line multiplexer implemented using cascading multiplexers.

![[8to1CascadingMultiplexers.svg]]

## Multiplexer implementations
Multiplexers can be used to implement [[Boolean functions]]. The functions need to be *decomposed* with [[Boole's expansion theorem]] first, such that a variable or a set of variables can act as the select lines.

### Example - Boolean equation, 1 select line
$$\begin{flalign}
F&=\bar{A}\bar{C}+AB+AC &\\
&=A(B+C)+\bar{A}(\bar{C})
\end{flalign}$$
![[MultiplexerImplementationBooleanEquation1.svg|500]]

### Example - Boolean equation, 2 select lines
To use both $A$ and $B$ as select lines, $B$ needs to be included in every term through the multiplication by $B+\bar{B}=1$. Decomposition is applied twice.
$$\begin{flalign}
F&=\bar{A}\bar{C}+AB+AC &\\
&=AC(B+\bar{B})+AB(1)+\bar{A}\bar{C}(B+\bar{B}) &\\
&=ABC+A\bar{B}C+AB(1)+\bar{A}B\bar{C}+\bar{A}\bar{B}\bar{C} &\\
&=AB(1)+A\bar{B}(C)+\bar{A}B(\bar{C})+\bar{A}\bar{B}(C)
\end{flalign}$$
![[MultiplexerImplementationBooleanEquation2.svg|550]]

### Example - minterm canonical form
$F(A,B,C,D)=\sum m(1,3,4,11,12,13,14,15)$

If $A$ and $B$ are the select lines, a [[Karnaugh Map|K-map]] can be used to find the combinations of the other variables that correspond with each input, i.e. $AB = 00$, $AB=01$ etc.

For example, if $AB=01$, then the minterm $\bar{C}\bar{D}$ is HIGH according to the function. Thus, $\bar{C}\bar{D}$ must be the value forwarded to the output when $AB=01$.

![[MultiplexerImplementationMintermCanonicalKMap.svg|400]]

![[MultiplexerImplementationMintermCanonical.svg|550]]