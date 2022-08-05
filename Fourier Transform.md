# Fourier Transform
**A transform that decomposes any non-[[periodic function]] in the time domain into the frequency domain as a set of complex [[Sinusoid|sinusoids]].**
$$F(\omega)=\mathcal{F}[f(t)]=\int_{-\infty}^{\infty}f(t)e^{-i\omega t}\;dt$$
The *Fourier transform* is an extension of the [[Fourier series]] which *lengthens* the period of any function to *infinity* and treating it like a periodic function.

The Fourier transform of a function outputs a *complex-valued* function. 

The plot of the magnitude of this function against frequency is its *amplitude spectrum*; the magnitude at a frequency is the *amplitude* of a *constituent sinusoid* at that frequency.
Likewise, the plot of its [[phase]] is its *phase spectrum*.

The relationship between the Fourier transform and the Laplace transform can be seen in the [[comparison of the Laplace and Fourier Transform]].

## Inverse Fourier transform
A function in the time domain can be reconstructed from its transform in the frequency domain via the *inverse Fourier transform*.
$$f(t)=\mathcal{F}^{-1}[F(\omega)]=\frac{1}{2\pi}\int_{-\infty}^{\infty}F(\omega)e^{i\omega t}\;d\omega$$
The function $f(t)$ and its transform $F(\omega)$ are known as a *Fourier transform pair*.

## Properties of the Fourier transform
|               $f(t)$               |                    $F(\omega)$                     |                     Property                      |
|:----------------------------------:|:--------------------------------------------------:|:-------------------------------------------------:|
|   $a_{1}f_{1}(t)+a_{2}f_{2}(t)$    |      $a_{1}F_{1}(\omega)+a_{2}F_{2}(\omega)$       |                     Linearity                     |
|              $f(at)$               |        $\frac{1}{\vert a\vert}F(\frac{\omega}{a})$        |                   Time scaling                    |
|            $f(t-t_{0})$            |           $e^{-i\omega t_{0}}F(\omega)$            |                   Time shifting                   |
|       $f(t)e^{i\omega_{0}t}$       |               $F(\omega-\omega_{0})$               | Frequency shifting or <br /> amplitude modulation |
|            $f^{(n)}(t)$            |              $(i\omega)^{n}F(\omega)$              |               Time differentiation                |
| $\int_{-\infty}^{t}f(\tau)\;d\tau$ | $\frac{F(\omega)}{i\omega}+\pi F(0)\delta(\omega)$ |                 Time integration                  |
|              $f(-t)$               |           $F(-\omega)=F^{*}(\omega)$[^1]           |                     Reversal                      |
|               $F(t)$               |                 $2\pi f(-\omega)$                  |                    [[Duality]]                    |
|        $f_{1}(t)*f_{2}(t)$         |            $F_{1}(\omega)F_{2}(\omega)$            |       [[Convolution]] in <br /> time domain       |
|   $F_{1}(\omega)*F_{2}(\omega)$    |              $2\pi f_{1}(t)f_{2}(t)$               | Convolution in <br /> frequency domain                                                  |

[^1]: $F^{*}(\omega)$ is the complex conjugate of $F(\omega)$.

## Fourier transform pairs
Many Fourier transforms involve [[Singularity Function|singularity functions]].

|        $f(t)$         |                         $F(\omega)$                         |
|:---------------------:|:-----------------------------------------------------------:|
|      $\delta(t)$      |                             $1$                             |
|          $1$          |                    $2\pi \delta(\omega)$                    |
|        $u(t)$         |           $\pi \delta(\omega)+\frac{1}{j\omega}$            |
| $u(t+\tau)-u(t-\tau)$ |              $2\frac{\sin \omega\tau}{\omega}$              |
|    $\vert t\vert$     |                   $\frac{-2}{\omega^{2}}$                   |
|    $\text{sgn}(t)$    |                     $\frac{2}{j\omega}$                     |
|     $e^{-at}u(t)$     |                    $\frac{1}{a+j\omega}$                    |
|     $e^{at}u(-t)$     |                    $\frac{1}{a-j\omega}$                    |
|  $t^{n}e^{-at}u(t)$   |               $\frac{n!}{(a+j\omega)^{n+1}}$                |
| $e^{-a\vert t\vert}$  |                $\frac{2a}{a^{2}+\omega^{2}}$                |
|  $e^{i\omega_{0}t}$   |                $2\pi\delta(\omega-\omega_0)$                |
|  $\sin \omega_{0}t$   | $i\pi[\delta(\omega+\omega_{0})-\delta(\omega-\omega_{0})]$ |
|  $\cos \omega_{0}t$   | $\pi[\delta(\omega+\omega_{0})+\delta(\omega-\omega_{0})]$                                                            |
