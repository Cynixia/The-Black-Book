# Standard Forms of a Boolean Function
There are two pairs of dual *standard* or *canonical* forms of Boolean Functions. Both contain only [[Minterms and Maxterms]].
- Minterm canonical form - maxterm canonical form
- Sum of products - product of sums

Standard forms are a more desirable expression for circuit implementation.

## Minterm/Maxterm canonical form
These forms correspond to a specific row of the truth table of a function can be directly derived from one.

These forms are denoted by a $\sum$ or $\prod$ symbol and numbers corresponding to the binary combination of variables.

### Minterm canonical form
**The expression of a function as a logical sum (OR) of [[Minterms and Maxterms#^dd3c36|minterms]] for which the function value is 1.**

#### Example
$F(X,Y,Z)=\sum{m(0,2,5,7)}$ 

|$X$|$Y$|$Z$|$F$|
|-|-|-|-|
|$0$|$0$|$0$|$1$|
|$0$|$0$|$1$|$0$|
|$0$|$1$|$0$|$1$|
|$0$|$1$|$1$|$0$|
|$1$|$0$|$0$|$0$|
|$1$|$0$|$1$|$1$|
|$1$|$1$|$0$|$0$|
|$1$|$1$|$1$|$1$|

### Maxterm canonical form
**The expression of a function as a logical product (AND) of [[Minterms and Maxterms#^01522f|maxterms]] for which the function value is 0.

The previous example can be expressed in the following maxterm canonical form.
$F(X,Y,Z)=\prod M(1,3,4,6)$

## SOP/POS form
These forms are similar to minterm/maxterm canonical form but *do not* need all variables in every term. They are the simplified forms derived using [[Boolean Algebra]] and can be directly implemented as a *two-level circuit*.

### Sum of products form
**The expression of a function as a logical product (OR) of AND terms.**

#### Example
$F=\bar{Y}+\bar{X}Y\bar{Z}+XY$

![[SumOfProductsCircuit.svg|500]]

### Product of sums form
**The expression of a function as a logical sum (AND) of OR terms.**

#### Example
$F=X(\bar{Y}+Z)(X+Y+\bar{Z})$

![[ProductOfSumsCircuit.svg|500]]