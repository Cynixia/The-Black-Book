# Sequential Circuit
**A circuit whose output depends on the present value of its inputs and the sequence of its past outputs.**

Sequential circuits consists of a *combinational* circuit connected to *storage elements*. A *feedback path* connects the storage elements back as an input.

![[SequentialCircuit.svg]]

Sequential circuits are either *synchronous* or *asynchronous*.

## Synchronous sequential circuits
**Sequential circuits whose outputs only change at discrete instants of time.**

Synchronous circuits are timed using a *clock generator* which outputs a periodic train of pulses. As such, synchronous circuits are sometimes called *clocked sequential circuits*.

Synchronous circuits are generally *more stable* and are *easier to design*.

![[SynchronousCircuit.svg]]

## Asynchronous sequential circuits
**Sequential circuits whose outputs change whenever the inputs change.**

Asynchronous circuits commonly use *time delay devices* as storage elements. Time delay may be introduced by propagation delay instead, and therefore asynchronous circuits can be considered as just combinational circuits with *feedback*.

## Storage elements
The two types of basic storage elements used in sequential circuits are:
- [[Latch|Latches]]
- [[Flip-flop|Flip-flops]]

Storage elements are characterised by their number of inputs and how the inputs affect  their state.

## Analysis of sequential circuits
Sequential circuits are described algebraically using [[State Equation|state equations]], in tabular form using [[State Table|state tables]], and graphically using [[State Diagram#Finite state machines|state diagrams]]. 

A sequential circuit using [[Flip-flop|flip-flops]] can further be described by a set of [[Flip-flop Input Equation|flip-flop input equations]].

## Models of sequential circuits
Sequential circuits are mathematically modelled as [[Finite State Machine|finite state machines]].

## Optimisation of sequential circuits
Sequential circuits are optimised through the process of [[state reduction]].