# Latch
**An asynchronous [[Level and Edge Triggering#Level-triggered|level sensitive]] storage element.**

Latches will "latch" onto an inputted state until another input changes its state.

## SR latch
A *set-reset* latch is the most fundamental latch and has a *set* and a *reset* input. It can be constructed from a pair of NOR or NAND gates.

![[SRLatches.svg|500]]

Below are the implementations of an SR latch using NOR and NAND gates.

In the NAND gate application, the inputs are considered *inverted* as the gates must be *active low* for proper operation.

![[SRNORLatch.svg|350]]

![[SRNANDLatch.svg|350]]

When the *set* input turns on, the latch enters the set state $Q=1$ and $\bar{Q}=0$ and will *hold* it until the reset input turns on.
The *reset* input causes the latch to enter the reset state $Q=0$ and $\bar{Q}=1$ and *hold* it until the set input turns on.

If *both* set and reset are on, a *restricted* input combination, the latch is in an *undefined* state.

The [[Characteristic Equation#Digital Electronics|characteristic equation]] of an SR latch is $Q_{\text{next}}=\bar{R}(Q+S)$. 

The [[Characteristic Table|characteristic]] and [[Excitation Table|excitation tables]] are:

| Characteristic |     |                   |            |     | Excitation |                   |          |          |            |
|:--------------:|:---:|:-----------------:|:----------:| --- |:----------:|:-----------------:|:--------:|:--------:|:----------:|
|      $S$       | $R$ | $Q_{\text{next}}$ | **Action** |     |    $Q$     | $Q_{\text{next}}$ |   $S$    |   $R$    | **Action** |
|      $0$       | $0$ |        $Q$        |    Hold    |     |    $0$     |        $0$        |   $0$    | $\times$ |    Hold    |
|      $0$       | $1$ |        $0$        |   Reset    |     |    $0$     |        $1$        |   $1$    |   $0$    |    Set     |
|      $1$       | $0$ |        $1$        |    Set     |     |    $1$     |        $0$        |   $0$    |   $1$    |   Reset    |
|      $1$       | $1$ |     $\times$      | Undefined  |     |    $1$     |        $1$        | $\times$ |   $0$    | Undefined  |

### SR latch with control input
Adding a pair of NAND gates to an SR NAND latch allows for its operation to be controlled by an additional output.

In this kind of SR latch, the outputs only change according to the inputs when the latch is *enabled*.

The [[characteristic table]] of an SR latch with a control input is:

| $En$ |   $S$    |   $R$    | $Q_{\text{next}}$ | Action |
|:----:|:--------:|:--------:|:-----------------:|:------:|
| $0$  | $\times$ | $\times$ |        $Q$        |  Hold  |
| $1$  |   $0$    |   $0$    |        $Q$        |  Hold  |
| $1$  |   $0$    |   $1$    |        $0$        | Reset  |
| $1$  |   $1$    |   $0$    |        $1$        |  Set   |
| $1$  |   $1$    |   $1$    |     $\times$      | Undefined       |

![[SRLatchControl.svg|600]]

## D latch
A *data* or *delay* latch is an SR latch with an inverter that *forces* $S$ and $R$ to always have different values. Thus, it *does not* have a restricted input combination.

![[DLatch.svg|250]]

When $En=0$, the D latch *holds* its value. When $En=1$, $Q=D$. 

The [[characteristic table]] of a D latch is:

| $En$ |   $D$    | $Q_{\text{next}}$ | Action |
|:----:|:--------:|:-----------------:|:------:|
| $0$  | $\times$ |        $Q$        |  Hold  |
| $1$  |   $0$    |        $0$        | Reset  |
| $1$  |   $1$    |        $1$        | Set       |

![[DLatchLogicDiagram.svg]]
