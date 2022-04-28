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

Asynchronous circuits commonly use *time delay devices* as storage elements. Time delay may be introduced by propagation delay instead, and therefore asynchronous circuits can be considered as combinational circuits with *feedback*.

## Storage elements
Storage elements are characterised by their number of inputs and how the inputs affect the their state.

The two types of storage elements used in sequential circuits are:
- [[Latches]]
- [[Flip-flops]]