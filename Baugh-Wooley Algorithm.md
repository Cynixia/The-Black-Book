# Baugh-Wooley Algorithm
**A multiplication algorithm for [[Signed Binary Numbers#Signed 2's complement|signed 2's complement]] numbers.**

It is one of the algorithms commonly used to implement [[Binary Multiplication#Implementation#Signed 2's complement multiplication|signed multiplication]].

Consider two $n$-bit numbers, $A$ and $B$, which can be represented as
$$\begin{gather*}
A=-a_{n-1}2^{n-1}+\sum_{i=0}^{n-2}a_{i}2^{i} \\
B=-b_{n-1}2^{n-1}+\sum_{j=0}^{n-2}b_{j}2^{j}
\end{gather*}$$
where $a_{i}$ and $b_{j}$ are bits of $A$ and $B$, respectively, with $a_{n-1}$ and $b_{n-1}$ being the *sign bits*. This representation is the equivalent to a method of [[Signed Binary Numbers#^878f2a|converting]] from signed 2's complement to decimal.

Their product, $P=A\times B$, can be written as
$$\begin{align*}
P={}&a_{n-1}b_{n-1}2^{2n-2}+\sum_{i=0}^{n-2}\sum_{j=0}^{n-2}a_{i}b_{j}2^{i+j}+ \\
&2^{n-1}\sum_{i=0}^{n-2}\overline{a_{i}b_{n-1}}2^{i}+2^{n-1}\sum_{j=0}^{n-2}\overline{a_{n-1}b_{j}}2^{j} \\
&-2^{2n-1}+2^{n}
\end{align*}$$
>[!Derivation]-
> For the above n-bit numbers $A$ and $B$, their product is
>$$\begin{align*}
P={}&a_{n-1}b_{n-1}2^{2n-2}+\sum_{i=0}^{n-2}\sum_{j=0}^{n-2}a_{i}b_{j}2^{i+j} \\
&-2^{n-1}\sum_{i=0}^{n-2}a_{i}b_{n-1}2^{i}-2^{n-1}\sum_{j=0}^{n-2}a_{n-1}b_{j}2^{j}
\end{align*}$$
To avoid subtraction, the [[Radix Complement|2's complement]] of the last two terms is found then added to the first terms to get the *final product*.
>
Note that the *first two* terms and the final product will have up to $2n$ bits, whilst the two *subtracted* terms only have up to $n-1$ bits.
>
Assuming $X$ is one of the subtracted terms, it can be *zero padded* [^1] to $2n$ bits so that it can be correctly added to the other terms. $X$ can be represented as
$$X=-0\times2^{2n-1}+0\times2^{2n-2}+2^{n-1}\sum_{k=0}^{n-2}x_{k}2^{k}+\sum_{l=0}^{n-2}0\times2^{l}$$
where $x_{k}=a_{i}b_{n-1}$ or $a_{n-1}b_{j}$, depending on the term. The first sum fills the bits from $2n-3$ to $n-1$ and the second sum pads the bits from $n-2$ to $0$. The above gives only the *value* of $X$ since the most significant bit - the sign bit -  is set to zero.
>
The *partial product* $X$ thus has a bit structure of
>
| **Bit** | $2n-1$ | $2n-2$ |  $2n-3$   |  $2n-4$   | $\cdots$ |   $n$   |  $n-1$  | $n-2$ | $\cdots$ | $0$ |
|:----------------:|:------:|:------:|:---------:|:---------:|:--------:|:-------:|:-------:|:-----:|:-----:|:---:|
|  **Value**   |  $0$   |  $0$   | $x_{n-2}$ | $x_{n-3}$ | $\cdots$ | $x_{1}$ | $x_{0}$ |  $0$  | $\cdots$ | $0$ |
>
The *1's complement*, or simply the complement,  of $X$ then has a bit structure of
>
|  **Bit**  | $2n-1$ | $2n-2$ |        $2n-3$        |        $2n-4$        | $\cdots$ |        $n$         |       $n-1$        | $n-2$ | $\cdots$ | $0$ |
|:---------:|:------:|:------:|:--------------------:|:--------------------:|:--------:|:------------------:|:------------------:|:-----:|:--------:|:---:|
| **Value** |  $1$   |  $1$   | $\overline{x_{n-2}}$ | $\overline{x_{n-3}}$ | $\cdots$ | $\overline{x_{1}}$ | $\overline{x_{0}}$ |  $1$  | $\cdots$ | $1$ |
>
Adding $1$ generates the *2's complement* of $X$, which is $-X$. Note that the carry of the least significant bit is propagated until bit $n-1$ which is left at an arbitrary value.
>
|  **Bit**  | $2n-1$ | $2n-2$ |        $2n-3$        | $\cdots$ |        $n$         |        $n-1$         | $n-2$ | $\cdots$ | $0$ |
|:---------:|:------:|:------:|:--------------------:|:--------:|:------------------:|:--------------------:|:-----:|:--------:|:---:|
| **Value** |  $1$   |  $1$   | $\overline{x_{n-2}}$ | $\cdots$ | $\overline{x_{1}}$ | $\overline{x_{0}}+1$ |  $0$  | $\cdots$ | $0$ |
>
If $Y$ represents the other partial product of the same form, then $-X-Y$ can be found using $-X+(-Y)$.
>
|  **Bit**  | $2n-1$ | $2n-2$ |                 $2n-3$                  | $\cdots$ |                  $n$                  |
|:---------:|:------:|:------:|:---------------------------------------:|:--------:|:-------------------------------------:|
| $-X+(-Y)$ |  $1$   |  $0$   | $\overline{x_{n-2}}+\overline{y_{n-2}}$ | $\cdots$ | $\overline{x_{1}}+\overline{y_{1}}+1$ |
>
|  **Bit**  |                $n-1$                | $n-2$ | $n-3$ | $\cdots$ | $0$ |
|:---------:|:-----------------------------------:|:-----:|:-----:|:--------:|:---:|
| $-X+(-Y)$ | $\overline{x_{0}}+\overline{y_{0}}$ |  $0$  |  $0$  | $\cdots$ | $0$ |
>
At bit $n-1$, the addition causes a carry to enter bit $n$, which adds a $2^{n}$ term to the final product.
>
Due to bit $2n-2$, the $1$ carried into bit $2n-1$ adds a $-2^{2n-1}$ term to the final product. The *minus sign* is the result of the bit being the *sign bit*.
>
Thus, the final product $P=A\times B$ is
>$$\begin{align*}
P={}&a_{n-1}b_{n-1}2^{2n-2}+\sum_{i=0}^{n-2}\sum_{j=0}^{n-2}a_{i}b_{j}2^{i+j}+ \\
&2^{n-1}\sum_{i=0}^{n-2}\overline{a_{i}b_{n-1}}2^{i}+2^{n-1}\sum_{j=0}^{n-2}\overline{a_{n-1}b_{j}}2^{j} \\
&-2^{2n-1}+2^{n}
\end{align*}$$

[^1]: *Zero padding* - adding zeroes to a signal or sequence to extend it to the necessary number of bits.