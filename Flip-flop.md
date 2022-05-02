# Flip-flop
**A synchronous [[Level and Edge Triggering#Edge-triggered|edge sensitive]] storage element.**

Flip-flops store an inputted state indefinitely until it is triggered to change but a clock signal.

## D flip-flop
A *data* or *delay* flip-flop is the most fundamental flip-flop and is the flip-flop that uses the *least* amount of gates. Other flip-flops can be constructed using D flip-flops and additional combinational logic.

![[DFlipFlop.svg|250]]

A D flip-flop is constructed from two D latches and inverters. A *positive-edge*-triggered D flip-flop uses two inverters whereas a *negative-edge*-triggered one uses one.

![[DFlipFlopConstruction.svg]]

In the *positive-edge*-triggered D flip-flop:
- When *clock* is off, the master latch is enabled and the slave latch is disabled. Thus, $Y=D$.
- When *clock* is on, the opposite is true and thus $Q=D$.

In the *negative-edge*-triggered D flip-flop:
- When *clock* is on, the master latch is enabled and the slave latch is disabled. Thus, $Y=D$.
- When *clock* is off, the opposite is true and thus $Q=D$.

The [[Characteristic Equation#Digital Electronics|characteristic equation]] of a D flip-flop is $Q_{\text{next}}=D$.

The [[excitation table]] is:

| $Q$ | $Q_{\text{next}}$ | $D$ |
| --- | ----------------- | --- |
| $0$ | $0$               | $0$ |
| $0$ | $1$               | $1$ |
| $1$ | $0$               | $0$ |
| $1$ | $1$               | $1$    |

## JK flip-flop
A JK flip-flop behaves similarly to an [[Latch#SR latch|SR latch]] but it does permit an input of $J=K=1$, the equivalent to $S=R=1$.

![[JKFlipFlop.svg|250]]

The [[Characteristic Equation#Digital Electronics|characteristic equation]] of a JK flip-flop is $Q_{\text{next}}=J\bar{Q}+\bar{K}Q$.

The [[Characteristic Table|characteristic]] and [[Excitation Table|excitation tables]] are:

| Characteristic |     |                   |            |     | Excitation |                   |          |          |            |
|:--------------:|:---:|:-----------------:|:----------:|:---:|:----------:|:-----------------:|:--------:|:--------:|:----------:|
|      $J$       | $K$ | $Q_{\text{next}}$ | **Action** |     |    $Q$     | $Q_{\text{next}}$ |   $J$    |   $K$    | **Action** |
|      $0$       | $0$ |        $Q$        |    Hold    |     |    $0$     |        $0$        |   $0$    | $\times$ |    Hold    |
|      $0$       | $1$ |        $0$        |   Reset    |     |    $0$     |        $1$        |   $1$    | $\times$ |    Set     |
|      $1$       | $0$ |        $1$        |    Set     |     |    $1$     |        $0$        | $\times$ |   $1$    |      Reset      | 
|      $1$       | $1$ |     $\bar{Q}$     |   Toggle   |     |    $1$     |        $1$        | $\times$ |   $0$    |           Hold |

## T flip-flip
A *toggle* flip-flop toggles its output when triggered. It is the same as a JK flip-flop when $J=K$.

![[TFlipFlop.svg|250]]

The [[Characteristic Equation#Digital Electronics|characteristic equation]] of a T flip-flop is $Q_{\text{next}}=T\bar{Q}+\bar{T}Q$.

The [[Characteristic Table|characteristic]] and [[Excitation Table|excitation tables]] are:

| Characteristic |                   |            |
|:--------------:|:-----------------:|:----------:|
|      $T$       | $Q_{\text{next}}$ | **Action** |
|      $0$       |        $Q$        |    Hold    |
|      $1$       |     $\bar{Q}$     | Toggle           |

| Excitation |                   |     |            |
|:----------:|:-----------------:|:---:|:----------:|
|    $Q$     | $Q_{\text{next}}$ | $T$ | **Action** |
|    $0$     |        $0$        | $0$ |    Hold    |
|    $0$     |        $1$        | $1$ |   Toggle   |
|    $1$     |        $0$        | $1$ |   Toggle   |
|    $1$     |        $1$        | $0$ | Hold           |
