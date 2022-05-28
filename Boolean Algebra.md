# Boolean Algebra
**The branch of algebra dealing with binary variables and describing [[logical operations]].**

## Laws
The following pairs of laws are all related by the [[Duality#Boolean Algebra|duality]] principle.

|                 AND Form                 |             OR Form             |        Name         |
|:----------------------------------------:|:-------------------------------:|:-------------------:|
|               $X\cdot 0=0$               |             $X+1=1$             |    Annihilation     |
|               $X\cdot 1=X$               |             $X+0=X$             |      Identity       |
|               $X\cdot X=X$               |            $X+ X=X$             |     Idempotence     |
|            $X\cdot \bar{X}=0$            |          $X+\bar{X}=1$          |   Complementation   |
|            $\bar{\bar{X}}=X$             |                                 |     Involution      |
|           $X\cdot Y=Y\cdot X$            |            $X+Y=Y+X$            |     Commutation     |
|              $X(YZ)=(XY)Z$               |        $X+(Y+Z)=(X+Y)+Z$        |     Association     |
|            $(X+Y)(X+Z)=X+YZ$             |         $XY+XZ=X(Y+Z)$          |    Distribution     |
|                $X(X+Y)=X$                |            $X+XY=X$             |     Absorption      |
|           $(X+Y)(X+\bar{Y})=X$           |         $XY+X\bar{Y}=X$         |    Minimisation     |
|            $X(\bar{X}+Y)=XY$             |        $X+\bar{X}Y=X+Y$         |   Simplification    |
|  $(X+Y)(\bar{X}+Z)(Y+Z)=$<br />$(X+Y)(\bar{X}+Z)$|  $XY+\bar{X}Z+YZ=XY+\bar{X}Z$   |      Consensus      |
|     $\overline{X+Y}=\bar{X}\bar{Y}$      | $\overline{XY}=\bar{X}+\bar{Y}$ | [[DeMorgan's Laws]] |

## Exclusive OR and Exclusive NOR
The *exclusive OR* or *XOR* of a set of operands is true if only one of its operands are true.
$$X\oplus Y=\bar{X}Y+X\bar{Y}=(\bar{X}+Y)(X+\bar{Y})$$
The corresponding logic gate is the XOR gate. ^6c2fba

![[XORGate.svg|200]]

The *exclusive NOR* or *XNOR* of two operands is true if the value of both operands are equal.
$$X\odot Y=\bar{X}\bar{Y}+XY=(X+Y)(\bar{X}+\bar{Y})=(X+Y)\overline{XY}$$
The corresponding logic gate is the XNOR gate. ^414467

![[XNORGate.svg|200]]

### XOR Laws
|                  Laws                  |                                        |
|:--------------------------------------:|:--------------------------------------:|
|             $X\oplus 0=X$              |          $X\oplus 1=\bar{X}$           |
|             $X\oplus X=0$              |          $X\oplus \bar{X}=1$           |
| $\bar{X}\oplus Y=\overline{X\oplus Y}$ | $X\oplus \bar{Y}=\overline{X\oplus Y}$ |
