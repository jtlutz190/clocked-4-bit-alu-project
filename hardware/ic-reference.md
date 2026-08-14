# IC Reference

This document summarizes the integrated circuits used in the project.
including their purpose, important control pins, and where they are used in the build.

---

## SN74HC283N — 4-Bit Binary Adder

**Purpose:** Performs 4-bit binary addition.

### Important Pins / Signals
- A1–A4 — First 4-bit operand
- B1–B4 — Second 4-bit operand
- C0 — Carry input
- S1–S4 — Sum outputs
- C4 — Carry output

### Project Notes
Subtraction is implemented by XORing each B input with the SUB control signal and
using SUB as the carry input:

`B' = B XOR SUB`

`Cin = SUB`

This allows the same adder to perform both addition and two's-complement subtraction.

---

## SN74HC157N — Quad 2-to-1 Multiplexer

**Purpose:** Selects between two 4-bit input buses.

### Important Pins / Signals
- A inputs — Input bus 0
- B inputs — Input bus 1
- Y outputs — Selected output
- S — Select input
- /E — Active-low enable

### Project Notes
Two SN74HC157N ICs are used to select between the arithmetic and logic results
before sending the final value to the output register. One is used to select between
the manual and auto clock line.

---

## SN74HC173N — 4-Bit Register

**Purpose:** Stores a 4-bit value on a clock edge.

### Important Pins / Signals
- D0–D3 — Data inputs
- Q0–Q3 — Stored outputs
- CLK — Clock
- /E1, /E2 — Active-low load enables
- /MR — Master reset

---

## SN74HC86N — Quad XOR Gate

**Purpose:** Provides four independent XOR gates.

---

## SN74HC08N — Quad AND Gate

**Purpose:** Provides four independent AND gates.

---

## SN74HC32N — Quad OR Gate

**Purpose:** Provides four independent OR gates.

---

## SN74HC04N — Hex Inverter

**Purpose:** Provides six NOT gates.

---

## NE555 — Timer

**Purpose:** Generates the automatic clock signal.

**Used in:** Clock circuit

### Important Pins
- 1 — GND
- 2 — Trigger
- 3 — Output
- 4 — Reset
- 5 — Control voltage
- 6 — Threshold
- 7 — Discharge
- 8 — VCC

### Project Notes
The NE555 is configured in astable mode to generate a slow clock suitable for
visually observing register and ALU operation.
