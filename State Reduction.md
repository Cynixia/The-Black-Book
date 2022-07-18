# State Reduction
**The reduction of the number of flip-flops in a circuit by the removal of redundant states.**

A state can be *redundant* if it is *equivalent* to another state.

Two states are *equivalent* if, for a given input, they produce the *same output* and transition the circuit to the *same state* or a pair of *equivalent states*.

To find equivalent states, an *implication table* is used.

## Implication table
**A table of cells corresponding to every possible pair of states and filled with the status of their equivalence.**

The steps to filling in an implication table using a [[state table]] are:
- Fill cells with equivalences those combinations depend on.
- Eliminate pairs of states for which their *outputs* are *different*.
- Eliminate pairs of states that depend on an equivalence subsequently deemed impossible.
- Repeat above steps, from the leftmost column to the right and top to bottom, until the implication table is filled.

> [!Example]
| Present <br /> state | Next <br /> state |       | Output |       |
| -------------------- | ----------------- | ----- | ------ | ----- |
|                      | $X=0$             | $X=1$ | $X=0$  | $X=1$ |
| $a$                  | $d$               | $b$   | $0$    | $0$   |
| $b$                  | $e$               | $a$   | $0$    | $0$   |
| $c$                  | $g$               | $f$   | $0$    | $1$   |
| $d$                  | $a$               | $d$   | $1$    | $0$   |
| $e$                  | $a$               | $d$   | $1$    | $0$   |
| $f$                  | $c$               | $b$   | $0$    | $0$   |
| $g$                  | $a$               | $e$   | $1$    | $0$      |
>
Note that cells corresponding to any pairs for which the outputs are different can immediately be eliminated. In addition, the pair $d,e$ have the same outputs and the same next states and so it can immediately be marked as equivalent.
>
![[ImplicationTableExample.svg]]
>
For the final step, the remaining undetermined cells can be filled by referring to the filled cells.
>
$a,f$ are not equivalent as $c,d$ are not equivalent;  $b,f$ are not equivalent as $c,e$ are not equivalent.
>
Thus, the sets of equivalent states are $a, b$ and $d,e,g$.  