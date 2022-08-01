# DESN2000 - Lab 3
## Functions and Procedures
> [!Example] Remembering that functions may be called in multiple different locations, can you suggest a reason why we must save the current program counter (PC) before we branch to a function?

The current program counter must be saved when we branch to a function so that after the function has completed execution then we can return to the location in 'main' where the function was called.

> [!Example] What lines of assembly code could successfully replace the line "bl larger" without using the branch with link instruction? Ordinary branch is permitted. Make sure to save the correct value in LR.
```armasm
sub lr, PC, #4
b larger
```

## Functions and the Stack
> [!Example] What will happen to the program in this situation?

The program will continue executing indefinitely.

## Stack Manipulation using Load and Store Multiple
> [!Example] What addressing mode (db, ib, da, or ia) should be used to store R5, R6, and R7 to the stack? Write the instruction. Explain your answer.
```armasm
stmdb sp!, {r5-r7}
```
The stack pointer will be at the previous full address before the stack is accessed. Thus, the pointer must be moved to the next smaller address before the variable is stored, so as to not overwrite other useful data.

## AAPCS-Compliant Maximum Value Function
> [!Example] When entering the function, where are the six arguments stored?

The arguments alpha to delta are stored in `r0`-`r3` and the arguments sigma and theta are stored at the bottom of the stack.