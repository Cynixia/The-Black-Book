# Complement of a Boolean Function
**A [[Boolean Functions|function]] whose output values complements that of another function.**

The complement of a function can be found in two ways:
- [[DeMorgan's Laws]]
- Complementing each [[Boolean Functions#Literals|literal]] of its [[Duality#Boolean Algebra|dual]].

> [!Example]
> ## DeMorgan's Theorem
> $F=\bar{X}Y\bar{Z}+\bar{X}\bar{Y}Z$
> $$\begin{flalign}
\bar{F}&=\overline{\bar{X}Y\bar{Z}+\bar{X}\bar{Y}Z} &\\
&=\overline{(\bar{X}Y\bar{Z})}\overline{(\bar{X}\bar{Y}Z)} &\\
&=(X+\bar{Y}+Z)(X+Y+\bar{Z})
\end{flalign}$$

> [!Example]
> ## Dual of a Function
> $$\begin{flalign}
F_{dual} &= (\bar{X}+Y+\bar{Z})(\bar{X}+\bar{Y}+Z) &\\
\therefore \bar{F} &= (X+\bar{Y}+Z)(X+Y+\bar{Z})
\end{flalign}$$