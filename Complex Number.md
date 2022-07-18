# Complex Number
**An extension of real numbers with an imaginary unit.**

The typical complex number in *rectangular form* is
$$z=x+iy$$
where $x$ and $y$ are both *real numbers*. $x$ is the *real part* and $y$ is the *imaginary part*. Complex numbers may also be expressed in [[Polar Form of a Complex Number|polar form]].

The set of complex numbers is denoted $\mathbb{C}$. The complex numbers also form a *real vector space* of dimension two, with $[1,i]$ as its standard basis.

In *electrical engineering*, $j$ is used in place of $i$, as the latter denotes electric current.

Every complex number also has its own [[complex conjugate]], and both are used in the [[complex conjugate root theorem]].

## Operations of complex numbers
> [!Addition/subtraction]
$$z_{1}\pm z_{2}=(x_{1}\pm x_{2})+i(y_{1}\pm y_{2})$$

> [!Multiplication]
$$z_{1}z_{2}=r_{1}r_{2}\angle(\phi_{1}+\phi_{2})$$

> [!Division]
$$\frac{z_{1}}{z_{2}}=\frac{r_{1}}{r_{2}}\angle(\phi_{1}-\phi_{2})$$

> [!Inversion]
$$\frac{1}{z}=\frac{\bar{z}}{|z|^2}=\frac{1}{r}\angle{-\phi}$$

> [!Integer exponentiation]
Integer exponentiation is well defined and simplifies to [[de Moivre's formula]].
> $$z^{n}=r^{n}\angle n\phi$$

> [!Fractional exponentiation or root extraction]
Fractional exponentiation is *multi-valued* but its *principal value* is
$$\sqrt[n]{z}=\sqrt[n]{r}\angle{\frac{\phi}{n}}$$
For other values, the root can be found by *extending* [[de Moivre's Formula|de Moivre's formula]].