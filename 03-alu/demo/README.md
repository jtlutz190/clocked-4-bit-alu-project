### 4-Bit ALU Demo

Demonstrates the 4-bit ALU performing arithmetic and logic operations on two 4-bit inputs. Two 4-position SPST switch banks on the left side of the breadboard set inputs A and B, with each input displayed by a corresponding set of four red LEDs. The 4-bit ALU result is displayed by four red LEDs on the right side of the breadboard, while separate blue and green LEDs indicate Carry Out and Signed Overflow, respectively.

Two SPDT switches select the ALU operation using a 2-bit mode input:

* **00:** ADD
* **01:** SUB
* **10:** AND
* **11:** XOR

<a href="https://youtu.be/d8Bg-rcKisM">
  <img src="https://img.youtube.com/vi/d8Bg-rcKisM/maxresdefault.jpg" width="450">
</a>

▶️ **[Watch demo on YouTube](https://youtu.be/d8Bg-rcKisM)**

### Operations demonstrated in the video:

| Operation | Binary Result | Decimal Result | Overflow |
|---|---|---:|---|
| `0011 + 0101` | `01000` | 3 + 5 = 8 | 1 |
| `1111 + 0001` | `00000` | -1 + 1 = 0 | 0 |
| `1000 + 1000` | `10000` | -8 + -8 = -16 | 1 |
| `0101 - 0011` | `00010` | 5 - 3 = 2 | 0 |
| `0000 - 0001` | `11111` | 0 - 1 = -1 | 0 |
| `1010 - 1010` | `00000` | -6 - (-6) = 0 | 0 |
| `1010 XOR 0101` | `1111` | - | - |
| `1100 XOR 1010` | `0110`| - | - |
| `1010 AND 0101` | `0000` | - | - |
| `1100 AND 1010` | `1000` | - | - |
