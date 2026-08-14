### 2-Bit Adder/Subtractor Demo

Demonstrates the 2-bit adder/subtractor performing arithmetic on two 2-bit inputs. Four SPDT switches on the left side of the breadboard set inputs A and B, while a separate SPDT switch selects between addition and subtraction. The 3-bit result is displayed using three red LEDs.

<a href="https://youtu.be/pEOp_cC26Ko">
  <img src="https://img.youtube.com/vi/pEOp_cC26Ko/maxresdefault.jpg" width="450">
</a>

▶️ **[Watch demo on YouTube](https://youtu.be/pEOp_cC26Ko)**

## Operations performed in demo

| Operation | Carry Output | Decimal Result |
|---|---|---|---|
| `01 + 00 = 01` | 0 | 1 + 0 = 1 |
| `01 + 01 = 10` | 0 | 1 + 1 = 2 |
| `11 + 01 = 00` | 1 | 3 + 1 = 4 |
| `11 + 11 = 10` | 1 | 3 + 3 = 6 | 
| `00 - 00 = 00`| 1 | 0 - 0 = 0 |
| `10 - 00 = 01` | 1 | 2 - 0


### ALU Flags Demo

Demonstrates the status flags responding to arithmetic operations performed by the 2-bit adder/subtractor. Four LEDs on the right side of the breadboard indicate the resulting flags:

- **Red:** Negative
- **Yellow:** Zero
- **Green:** Signed Overflow
- **Blue:** Carry Out

<a href="https://youtu.be/QMhGtFEnRMo">
  <img src="https://img.youtube.com/vi/QMhGtFEnRMo/maxresdefault.jpg" width="450">
</a>

▶️ **[Watch demo on YouTube](https://youtu.be/QMhGtFEnRMo)**
