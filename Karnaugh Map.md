# Karnaugh Map
**A method of simplifying [[Boolean Algebra]] expressions through pattern recognition.**

A single K-map represents a Boolean function.

![[4x4KMap.svg|450]]

The cells are ordered in *Gray code* and each cell corresponds to a [[Minterms and Maxterms#^dd3c36|minterm]] of the expression or a row of its truth table.

Cells are filled with the *output value* expression of the minterm input combination they represent.

Cells may also be filled with [[Don't Care Condition|don't care conditions]], which can be used as either $1$s or $0$s.

A K-map grid is *toroidally* connected, and cells whose minterms differ by *only one* literal are *adjacent* to each other. In the following grid the dot-marked cells are adjacent.

The Boolean expression directly derived from a K-map is *not necessarily fully minimised*. Often the expression can still be minimised further using [[Boolean algebra]].

![[4x4KMapAdjacency.svg|425]]

## Grouping
Simplification is performed by grouping adjacent cells containing $1$s into groups with an area of a *power of two*, known as *implicants*.

Implicants always take the form of *rectangles* in a K-map.

When grouping, groups are made *as large as possible* and secondary to this, *overlap* is allowed but should be *minimised*.

### Implicants
**A product term that implies a function.**
Alternatively, an *implicant* is a product term for which the function has the value $1$ for *all [[Minterms and Maxterms#^dd3c36|minterms]]* containing the product term.

On a K-map these correspond to any rectangles composed of cells containing $1$s.

For example, the function $f(x,y,z,w)=xy+yz+w$ has the obvious implicants $xy$, $yz$, and $w$ and any product terms containing these implicants will also imply the function.

#### Prime implicants
**An implicant which is no longer an implicant if any [[Boolean Functions#Literals|literal]] is removed.**

Prime implicants correspond to rectangles containing *as many* squares as possible.

#### Essential prime implicant
**An implicant that contains the only occurrence of a minterm of the function.**

Essential prime implicants correspond to rectangles containing at least one cell with a $1$ *not included* in any other prime implicant.

### Example
> [!Simplifying a function with don't care conditions]
$F(A,B,C,D)=\sum m(1,3,7,11,15)$ with [[Don't Care Condition|don't care conditions]] $d(A,B,C,D)=\sum m(0,2,5)$.
>
![[4x4KMapExample.svg|500]]
>
$\therefore F(A,B,C,D)=\bar{A}D+CD$
>
Note the inclusion of a [[don't care condition]] in $\bar{A}D$. $CD$ is an *essential prime implicant* whilst $\bar{A}D$ is just a *prime implicant* as it can also be replaced with $\bar{A}\bar{B}$.
>
Also, the derived expression is *not yet* in its *minimised* form, and can still be factored once.