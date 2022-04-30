# Finite State Machine
**An abstract machine that is in exactly one of a finite number of states at a time.**
## Transducer
**A finite state machine that produces outputs based on given inputs and states.**

Finite state transducers are further classfied in two types.
### Mealy machine
**A finite state transducer whose output is a function of its current state and inputs.**

![[MealyModel.svg|800]]

In a Mealy circuit, outputs can change during a clock cycle and momentary false values can occur. To prevent this inputs are *synchronised* to the clock and change at the *inactive* edge of the clock.

The output value is only accurate when sampled *immediately before* the *active edge* of the clock.

### Moore machine
**A finite state transducer whose output is only a function of its current state.**

![[MooreModel.svg|800]]

With Moore circuits, [[State Table|state tables]] do not require separate output listings for various input combinations.

### Converting between Mealy and Moore machines
Converting between the two types of machines is easy to visualise using a [[state diagram]]. The processes detailed below are applied at each state as necessary.
#### Mealy to Moore
For every *incoming* transition with a *unique* output, a Moore state needs to be duplicated into *intermediate* states, one for each output.

All new state-output combinations then need to be added to the [[state table]].

![[MealyToMoore.svg|500]]

#### Moore to Mealy
The output of a Moore state is *duplicated* onto every *incoming* transition.

In a [[state table]], the output of a particular Moore state is duplicated to *any occurance* of that state as a *next state*.

![[MooreToMealy.svg|600]]