# Minterms and Maxterms
**A minterm is a product term in which each variable appears once (in complemented or uncomplemented form).**
A sum of minterms:
$$\sum{m}=XY+\bar{X}Y$$ ^dd3c36

**A maxterm is a sum term in which each variable appears once (in complemented or uncomplemented form).**
A product of maxterms:
$$\prod{M}=(\bar{X}+Y)(X+Y)$$ ^01522f

A function with $n$ variables will have $2^{n}$ minterms or maxterms.

Minterms and maxterms are written for any binary combination of variables such that its value is $1$ or $0$, respectively.

## Minterms
A variable in a minterm is *complemented* for $0$ and *not complemented* for $1$.

|$X$|$Y$|Product Term|Symbol|
|-|-|-|-|
|$0$|$0$|$\bar{X}\bar{Y}$|$m_0$|
|$0$|$1$|$\bar{X}Y$|$m_1$|
|$1$|$0$|$X\bar{Y}$|$m_2$|
|$1$|$1$|$XY$|$m_3$|

Note that if *any* one minterm is true, all other minterms are false.

## Maxterms
A variable in a maxterm is *complemented* for $1$ and *not complemented* for $0$.

|$X$|$Y$|Sum Term|Symbol|
|-|-|-|-|
|$0$|$0$|$X+Y$|$M_0$|
|$0$|$1$|$X+\bar{Y}$|$M_1$|
|$1$|$0$|$\bar{X}+Y$|$M_2$|
|$1$|$1$|$\bar{X}+\bar{Y}$|$M_3$|

Note that if *any* one maxterm is false, all other maxterms are true.