# Boolean Alegbra
**The branch of algebra dealing with binary variables and describing [[logical operations]].**

## Laws
The following pairs of laws are all related by the [[Duality#Boolean Algebra|duality]] principle.

|                 AND Form                 |           OR Form            |      Name       |
|:----------------------------------------:|:----------------------------:|:---------------:|
|               $X\cdot 0=0$               |           $X+1=1$            |  Annihilation   |
|               $X\cdot 1=X$               |           $X+0=X$            |    Identity     |
|               $X\cdot X=X$               |           $X+ X=X$           |   Idempotence   |
|            $X\cdot \bar{X}=0$            |        $X+\bar{X}=1$         | Complementation |
|            $\bar{\bar{X}}=X$             |                              |   Involution    |
|           $X\cdot Y=Y\cdot X$            |          $X+Y=Y+X$           |   Commutation   |
|              $X(YZ)=(XY)Z$               |      $X+(Y+Z)=(X+Y)+Z$       |   Association   |
|            $(X+Y)(X+Z)=X+YZ$             |        $XY+XZ=X(Y+Z)$        |  Distribution   |
|                $X(X+Y)=X$                |           $X+XY=X$           |   Absorption    |
|           $(X+Y)(X+\bar{Y})=X$           |       $XY+X\bar{Y}=X$        |  Minimisation   |
|            $X(\bar{X}+Y)=XY$             |       $X+\bar{X}Y=X+Y$       | Simplification  |
| $(X+Y)(\bar{X}+Z)(Y+Z)=(X+Y)(\bar{X}+Z)$ | $XY+\bar{X}Z+YZ=XY+\bar{X}Z$ | Consensus                |

### DeMorgan's Laws
The negation of a disjunction is the conjunction of the negations.
$$\overline{X+Y}=\bar{X}\bar{Y}$$

The negation of a conjunction is the disjunction of the negations.
$$\overline{XY}=\bar{X}+\bar{Y}$$
### Exclusive OR and Exclusive NOR
The *exclusive OR* or *XOR* of a set of operands is true if only one of its operands are true.
$$X\oplus Y=\bar{X}Y+X\bar{Y}=(X+Y)(\bar{X}+\bar{Y})$$
The corresponding logic gate is the XOR gate.

![[XORGate.svg|200]]

The *exclusive NOR* or *XNOR* of two operands is true if the value of both operands are equal.
$$X\odot Y=\bar{X}\bar{Y}+XY=(X+\bar{Y})(\bar{X}+Y)=(X+Y)\overline{(X\cdot Y)}$$
The corresponding logic gate is the XNOR gate.

![[XNORGate.svg|200]]
