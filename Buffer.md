# Buffer
**A gate that acts as an electrical amplifier between circuits.**
$$F=X$$
![[Buffer.svg|200]]

Buffers isolate their input and output circuits and also improves voltage and current levels so stay within range for logical circuits.

### 3-state buffer
**A buffer with an additional input control line.**

| EN  | IN  | OUT |
|:---:|:---:|:---:|
| $0$ | $X$ | $Z$ |
| $1$ | $0$ | $0$ |
| $1$ | $1$ | $1$ |

![[3StateBuffer.svg|350]]

When disabled, a 3-state buffer outputs a [[High Impedance#Digital Electronics|high impedance]] state.