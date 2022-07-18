# Flip-flop Input Equation
**A Boolean equation describing the inputs to a flip-flop.**

[[Flip-flop]] input equations are derived from [[State Table|state tables]] and [[Excitation Table|excitation tables]] and used to form the output combinational circuit.

> [!Example]
> For a T flip-flop circuit, the extended state table derived from an excitation table is:
> 
>| Present <br /> state |     |  Inputs  |          | Next <br /> state |          | Flip-flop <br /> inputs |       |
|:--------------------:|:---:|:--------:|:--------:|:-----------------:|:--------:|:-----------------------:|:-----:|
|         $A$          | $B$ |   $S$    |   $F$    |     $A(t+1)$      | $B(t+1)$ |          $T_A$          | $T_B$ |
|         $0$          | $0$ |   $0$    |   $0$    |        $0$        |   $0$    |           $0$           |  $0$  |
|         $0$          | $0$ | $\times$ |   $1$    |        $0$        |   $1$    |           $0$           |  $1$  |
|         $0$          | $0$ |   $1$    | $\times$ |        $1$        |   $0$    |           $1$           |  $0$  |
|                      |     |          |          |                   |          |                         |       |
|         $0$          | $1$ |   $0$    |   $0$    |        $0$        |   $1$    |           $0$           |  $0$  |
|         $0$          | $1$ | $\times$ |   $1$    |        $1$        |   $0$    |           $1$           |  $1$  |
|         $0$          | $1$ |   $1$    | $\times$ |        $1$        |   $1$    |           $1$           |  $0$  |
|                      |     |          |          |                   |          |                         |       |
|         $1$          | $1$ |   $0$    |   $0$    |        $1$        |   $1$    |           $0$           |  $0$  |
|         $1$          | $1$ | $\times$ |   $1$    |        $0$        |   $0$    |           $1$           |  $1$  |
|         $1$          | $1$ |   $1$    | $\times$ |        $0$        |   $1$    |           $1$           |  $0$  |
|                      |     |          |          |                   |          |                         |       |
|         $1$          | $0$ |   $0$    |   $0$    |        $1$        |   $0$    |           $0$           |  $0$  |
|         $1$          | $0$ | $\times$ |   $1$    |        $1$        |   $1$    |           $0$           |  $1$  |
|         $1$          | $0$ |   $1$    | $\times$ |        $0$        |   $0$    |           $1$           |  $0$  |
>
> Note that for this particular circuit, $S=F=1$ is not a possible combination. To derive the flip-flop input equations, [[Karnaugh Map|K-maps]] can be used.
>
> ![[LightControllerTAKMap.svg|400]]
> 
> ![[LightControllerTBKMap.svg|400]]
> 
> Thus, the flip-flop input equations are
>$$\begin{align*}
T_{A}&=BF+S \\
T_{B}&=F \\
\end{align*}$$