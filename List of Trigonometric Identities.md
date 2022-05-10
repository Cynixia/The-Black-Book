# List of Trigonometric Identities
## Pythagorean identity
The *Pythagorean identity* is the basic relationship between *sine and cosine* and is a version of the Pythagorean theorem derived from the unit circle.
$$\sin^{2}\theta+\cos^{2}\theta=1$$
Division by $\sin^{2}\theta$ and $\cos^{2}\theta$ gives
$$\tan^{2}\theta+1=\sec^{2}\theta$$
## Angle reflections
These are equivalences due to angles *reflected* about a line with a direction $\alpha$.

|         $\alpha=0$          |         $\alpha=\frac{\pi}{4}$          |     $\alpha=\frac{\pi}{2}$     |          $\alpha=\frac{3\pi}{4}$          |
|:---------------------------:|:---------------------------------------:|:------------------------------:|:-----------------------------------------:|
| $\sin(-\theta)=-\sin\theta$ | $\sin(\frac{\pi}{2}-\theta)=\cos\theta$ | $\sin(\pi-\theta)=+\sin\theta$ | $\sin(\frac{3\pi}{2}-\theta)=-\cos\theta$ |
| $\cos(-\theta)=+\cos\theta$ | $\cos(\frac{\pi}{2}-\theta)=\sin\theta$ | $\cos(\pi-\theta)=-\cos\theta$ | $\cos(\frac{3\pi}{2}-\theta)=-\sin\theta$ |
| $\tan(-\theta)=-\tan\theta$ | $\tan(\frac{\pi}{2}-\theta)=\cot\theta$ | $\tan(\pi-\theta)=-\tan\theta$ | $\tan(\frac{3\pi}{2}-\theta)=+\cot\theta$ |
| $\csc(-\theta)=-\csc\theta$ | $\csc(\frac{\pi}{2}-\theta)=\sec\theta$ | $\csc(\pi-\theta)=+\csc\theta$ | $\csc(\frac{3\pi}{2}-\theta)=-\sec\theta$ |
| $\sec(-\theta)=+\sec\theta$ | $\sec(\frac{\pi}{2}-\theta)=\csc\theta$ | $\sec(\pi-\theta)=-\sec\theta$ | $\sec(\frac{3\pi}{2}-\theta)=-\csc\theta$ |
| $\cot(-\theta)=-\cot\theta$ | $\cot(\frac{\pi}{2}-\theta)=\tan\theta$ | $\cot(\pi-\theta)=-\cot\theta$ | $\cot(\frac{3\pi}{2}-\theta)=+\tan\theta$                                          |

## Angle shifts
These are equivalences due to angles *shifted* by fractions of a *period*.

|                       Shift by quarter period                        |           Shift by half period           |      Shift by full periods      |
|:--------------------------------------------------------------------:|:----------------------------------------:|:-------------------------------:|
|             $\sin(\theta\pm\frac{\pi}{2})=\pm\cos\theta$             |      $\sin(\theta+\pi)=-\sin\theta$      | $\sin(\theta+2k\pi)=\sin\theta$ |
|             $\cos(\theta\pm\frac{\pi}{2})=\mp\sin\theta$             |      $\cos(\theta+\pi)=-\cos\theta$      | $\cos(\theta+2k\pi)=\cos\theta$ |
|             $\csc(\theta\pm\frac{\pi}{2})=\pm\sec\theta$             |      $\csc(\theta+\pi)=-\csc\theta$      | $\csc(\theta+2k\pi)=\csc\theta$ |
|             $\sec(\theta\pm\frac{\pi}{2})=\mp\csc\theta$             |      $\sec(\theta+\pi)=-\sec\theta$      | $\sec(\theta+2k\pi)=\sec\theta$ |
| $\tan(\theta\pm\frac{\pi}{4})=\frac{\tan\theta\pm1}{1\mp\tan\theta}$ | $\tan(\theta+\frac{\pi}{2})=-\cot\theta$ | $\tan(\theta+2k\pi)=\tan\theta$ |
| $\cot(\theta\pm\frac{\pi}{4})=\frac{\cot\theta\mp1}{1\pm\cot\theta}$ | $\cot(\theta+\frac{\pi}{2})=-\tan\theta$ | $\cot(\theta+2k\pi)=\cot\theta$                                |

## Angle sum and differences
$$\begin{gather*}
\sin(\alpha\pm\beta)=\sin\alpha\cos\beta\pm\cos\alpha\sin\beta \\
\cos(\alpha\pm\beta)=\cos\alpha\cos\beta\pm\sin\alpha\sin\beta \\
\tan(\alpha\pm\beta)=\frac{\tan\alpha\pm\tan\beta}{1\mp\tan\alpha\tan\beta} \\
\csc(\alpha\pm\beta)=\frac{\sec\alpha\sec\beta\csc\alpha\csc\beta}{\sec\alpha\csc\beta\pm\csc\alpha\sec\beta} \\
\sec(\alpha\pm\beta)=\frac{\sec\alpha\sec\beta\csc\alpha\csc\beta}{\csc\alpha\csc\beta\mp\sec\alpha\sec\beta} \\
\cot(\alpha\pm\beta)=\frac{\cot\alpha\cot\beta\pm1}{\cot\beta\pm\cot\alpha}
\end{gather*}$$

### Double-angle formulas
$$\begin{align*}
\sin(2\theta)&=2\sin\theta\cos\theta \\
\cos(2\theta)&=\cos^{2}\theta-\sin^{2}\theta \\
&=2\cos^{2}\theta-1 \\
&=1-2\sin^{2}\theta \\
\tan(2\theta)&=\frac{2\tan\theta}{1-\tan^{2}\theta} \\
\csc(2\theta)&=\frac{\sec\theta\csc\theta}{2} \\
\sec(2\theta)&=\frac{\sec^{2}\theta}{2-\sec^{2}\theta} \\
\cot(2\theta)&=\frac{\cot^{2}\theta-1}{2\cot\theta} \\
\end{align*}$$

## Tangent half-angle formulas
The *tangent half-angle* formulas relate the tangent of half of an angle to trigonometric functions of the full angle.

If $t=\tan\frac{\theta}{2}$,
$$\begin{gather*}
\sin\theta=\frac{2t}{1+t^{2}} \\
\cos\theta=\frac{1-t^{2}}{1+t^{2}} \\
\tan\theta=\frac{2t}{1-t^{2}}
\end{gather*}$$

## Product-to-sum identities
$$\begin{gather*}
\sin\alpha\sin\beta=\frac{\cos(\alpha-\beta)-\cos(\alpha+\beta)}{2} \\
\cos\alpha\cos\beta=\frac{\cos(\alpha-\beta)+\cos(\alpha+\beta)}{2} \\
\sin\alpha\cos\beta=\frac{\sin(\alpha+\beta)+\sin(\alpha-\beta)}{2} \\
\cos\alpha\sin\beta=\frac{\sin(\alpha+\beta)-\sin(\alpha-\beta)}{2} \\
\tan\alpha\tan\beta=\frac{\cos(\alpha-\beta)-\cos(\alpha+\beta)}{\cos(\alpha-\beta)+\cos(\alpha+\beta)}
\end{gather*}$$

## Sum-to-product identities
$$\begin{gather*}
\sin\alpha\pm\sin\beta=2\sin\left(\frac{\alpha\pm\beta}{2}\right)\cos\left(\frac{\alpha\mp\beta}{2}\right)\\
\cos\alpha+\cos\beta=2\cos\left(\frac{\alpha+\beta}{2}\right)\cos\left(\frac{\alpha-\beta}{2}\right) \\
\cos\alpha-\cos\beta=-2\sin\left(\frac{\alpha+\beta}{2}\right)\sin\left(\frac{\alpha-\beta}{2}\right) \\
\tan\alpha\pm\tan\beta=\frac{\sin(\alpha\pm\beta)}{\cos\alpha\beta}
\end{gather*}$$

## Euler's formula
**The fundamental relationship between the trigonometric functions and the complex exponential function.**
$$e^{i\theta}=\cos \theta+i\sin \theta$$
$$\begin{gather*}
\sin \theta=\frac{e^{i\theta}-e^{-i\theta}}{2i} \\
\cos \theta=\frac{e^{i\theta}+e^{-i\theta}}{2} \\
\tan \theta=-i\frac{e^{i\theta}-e^{-i\theta}}{e^{i\theta}+e^{-i\theta}}
\end{gather*}$$
Euler's formula is used to derive [[de Moivre's formula]].

## Integer multiples of $\pi$
|       Function        | Value                                                                                                 |
|:---------------------:|:----------------------------------------------------------------------------------------------------- |
| $\sin \frac{n\pi}{2}$ | $\begin{cases} (-1)^{\frac{n-1}{2}}, &n=\text{odd}\\ 0, &n=\text{even} \end{cases}$                   |
| $\cos \frac{n\pi}{2}$ | $\begin{cases} (-1)^{\frac{n}{2}}, &n=\text{even}\\ 0, &n=\text{odd} \end{cases}$                     |
|      $\sin n\pi$      | $0$                                                                                                   |
|      $\cos n\pi$      | $(-1)^{n}$                                                                                            |
|     $\sin 2n\pi$      | $0$                                                                                                   |
|     $\cos 2n\pi$      | $1$                                                                                                   |
| $e^{\frac{in\pi}{2}}$ | $\begin{cases} (-1)^{\frac{n}{2}}, &n=\text{even}\\ i(-1)^{\frac{n-1}{2}}, &n=\text{odd} \end{cases}$ |
|      $e^{in\pi}$      | $(-1)^n$                                                                                              |
|     $e^{2in\pi}$      | $1$                                                                                                      |

