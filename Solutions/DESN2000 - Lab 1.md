# DESN2000 - Lab 1
## Loading your First Program
>[!Example] If loaded correctly, you should notice activity on your QVGA Base Board. What happens?

Various lights on the board strobe or flash.

## Debug Mode
>[!Example] What is the difference between the disassembly window and the source window?

The disassembly window shows the actual instructions which are loaded onto the processor.

The source window shows the source code, which looks like typical human-readable and written code including pseudo-instructions and comments.

## Building your First Program
>[!Example] Describe what *first_project* does.

*first_project* turns on and then off each red LED labelled LED1-4 on the board in a cycle.

## Debugging your First Program
>[!Example] Why doesn't this program (*first_debug*) work like the previous one? What bug is present?

In *first_debug*, the value assigned to *max* is 0xFFF instead of 0x1FFFFF, which significantly shortens the delay between the activation of each LED.
Thus, to our eyes the speed of the switching of the LEDs is fast enough to appear as though all LEDs are on at the same time instead of the LEDs cycling.

## Tracing Execution and Observing Registers
>[!Example] List the order in which registers R0 through to R8 are modified.

| R0  | R5  | R4  | R8  | R1  | R3  | R2  | R6  | R7  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
|     |     |     |     |     |     |     |     |     |

## Debugging PC-Relative Load Instructions
>[!Example] How would you change the second load instruction (line 14 of *ldr_basic.s*) to load *a* into R2 instead of *b*?
```armasm
ldr r2, [pc, #4]
```
