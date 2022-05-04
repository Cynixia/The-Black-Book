# Partial Fraction Decomposition
**The decomposition of a rational fraction into a sum of a polynomial and at least one fraction with a simpler denominator.**
$$\frac{f(x)}{g(x)}=p(x)+\sum_{i}\frac{f_{i}(x)}{g_{i}(x)}$$
For each $i$,
- $g_{i}(x)$ is a *power* of an *irreducible polynomial*
- $f_{i}(x)$ is a polynomial is of a *smaller degree* than $g_{i}(x)$

For any real numbers $a$, $b$, $c$, $p$, $q$,  and $r$,

|             Rational function             |                                        Partial fraction decomposition                                         |
|:-----------------------------------------:|:-------------------------------------------------------------------------------------------------------------:|
| $\frac{f(x)}{(ax+p)(bx+q)(cx+r)\;\cdots}$ |                             $\frac{A}{ax+p}+\frac{B}{bx+q}+\frac{C}{cx+r}+\cdots$                             |
|         $\frac{f(x)}{(ax+b)^{n}}$         |                 $\frac{A_{1}}{ax+b}+\frac{A_{2}}{(ax+b)^{2}}+\cdots+\frac{A_{n}}{(ax+b)^{n}}$                 |
|    $\frac{f(x)}{(ax+b)^{n}(cx+d)^{m}}$    | $\frac{A_{1}}{ax+b}+\cdots+\frac{A_{n}}{(ax+b)^{n}}+\frac{B_{1}}{(cx+d)^{m}}+\cdots+\frac{B_{m}}{(cx+d)^{m}}$ |
|    $\frac{f(x)}{(ax+b)^{n}(px^{2}+qx+r)^{m}}$     |                                    $\frac{A_{1}}{ax+b}+\cdots+\frac{A_{n}}{(ax+b)^{n}}+\frac{B}{px^{2}+qx+r}+\cdots+\frac{B_{m}}{(px^{2}+qx+r)^{m}}$                                     |
|     $\frac{f(x)}{(ax^{2}+bx+c)^{n}}$      |      $\frac{A_{1}}{ax^{2}+bx+c}+\frac{A_{2}}{(ax^{2}+bx+c)^{2}}+\cdots+\frac{A_{n}}{(ax^{2}+bx+c)^{n}}$       |
|                 $\vdots$                  |                                                   $\vdots$                                                    |

The expressions in the table are valid for any denominator as long as the denominator consists of *irreducible factors* and is of a *larger degree* than the numerator.
