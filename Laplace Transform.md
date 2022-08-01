# Laplace Transform
**A transform that converts a function in the time domain into a complex function in the complex frequency domain.**

The *Laplace transform* outputs a *complex-valued* function of the *complex variable* $s$. 
$$s=\sigma+i\omega$$
The relationship between the Laplace transform and the Fourier transform is detailed in the [[comparison of the Laplace and Fourier Transform]].

The *unilateral* or *one-sided* Laplace transform is
$$F(s)=\mathcal{L}[f(t)]=\int_{0}^{\infty}f(t)e^{-st}\;dt$$
The unilateral Laplace transform is defined only over $0<t<\infty$.

## Inverse Laplace transform
A primitive method of finding the inverse Laplace transform is to decompose $F(s)$ through [[Partial Fraction Decomposition|partial fractions]] and taking the inverse of each term.

## Properties of the Laplace transform
|            $f(t)$             |                    $F(s)$                     |         Property          |
|:-----------------------------:|:---------------------------------------------:|:-------------------------:|
| $a_{1}f_{1}(t)+a_{2}f_{2}(t)$ |         $a_{1}F_{1}(s)+a_{2}F_{2}(s)$         |         Linearity         |
|            $f(at)$            |          $\frac{1}{a}F(\frac{s}{a})$          |          Scaling          |
|        $f(t-a)u(t-a)$         |                 $e^{-as}F(s)$                 |       Time shifting       |
|         $e^{-at}f(t)$         |                   $F(s+a)$                    |    Frequency shifting     |
|            $f'(t)$            |                 $sF(s)-f(0^+)$                  |   First time derivative   |
|           $f''(t)$            |            $s^{2}F(s)-sf(0^+)-f'(0^+)$            |  Second time derivative   |
|           $f'''(t)$           |      $s^{3}F(s)-s^{2}f(0^+)-sf'(0^+)-f''(0^+)$      |   Third time derivative   |
|         $f^{(n)}(t)$          | $s^{n}F(s)-\sum_{k=1}^{n}s^{n-k}f^{(k-1)}(0^+)$ |   Time differentiation    |
| $\int_{0}^{t}f(\tau)\;d\tau$  |               $\frac{1}{s}F(s)$               |     Time integration      |
|            $tf(t)$            |              $-\frac{d}{ds}F(s)$              | Frequency differentiation |
|       $\frac{f(t)}{t}$        |          $\int_{s}^{\infty}F(s)\;ds$          |   Frequency integration   |
|            $f(0)$             |       $\lim_{s\rightarrow\infty}sF(s)$        |       Initial value       |
|          $f(\infty)$          |         $\lim_{s\rightarrow 0}sF(s)$          |        Final value        |
|      $f_{1}(t)*f_{2}(t)$      |              $F_{1}(s)F_{2}(s)$               |        [[Convolution]]        |

## Laplace transform pairs
As with Fourier transform pairs, some Laplace transform pairs involve [[Singularity Function|singularity functions]].

These pairs are written multiplied with a $u(t)$ term, but are omitted below. They are only defined for $t\ge 0$ and $f(t)=0$ for $t<0$.

|         $f(t)$         |                $F(s)$                 |
|:----------------------:|:-------------------------------------:|
|      $\delta(t)$       |                  $1$                  |
|         $u(t)$         |             $\frac{1}{s}$             |
|       $e^{-at}$        |            $\frac{1}{s+a}$            |
|          $t$           |           $\frac{1}{s^{2}}$           |
|        $t^{n}$         |         $\frac{n!}{s^{n+1}}$          |
|       $te^{-at}$       |         $\frac{1}{(s+a)^{2}}$         |
|     $t^{n}e^{-at}$     |       $\frac{n!}{(s+a)^{n+1}}$        |
|    $\sin \omega t$     |   $\frac{\omega}{s^{2}+\omega^{2}}$   |
|    $\cos \omega t$     |     $\frac{s}{s^{2}+\omega^{2}}$      |
| $e^{-at}\sin \omega t$ | $\frac{\omega}{(s+a)^{2}+\omega^{2}}$ |
|     $e^{-at}\cos \omega t$                   |     $\frac{s+a}{(s+a)^{2}+\omega^{2}}$                                  |
