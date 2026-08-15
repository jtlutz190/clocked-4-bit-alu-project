# Phase 3 — 4-Bit ALU

This phase scales the previous arithmetic circuit into a complete **4-bit ALU** capable of performing ADD, SUB, AND, and XOR operations on two 4-bit inputs.

<p align="center">
  <img src="photos/4bit-alu-1.jpg" width="700">
</p>

## Goal

The goal was to combine arithmetic and logic operations into a single circuit and use multiplexers to select the final output.

The ALU supports:

| Mode | Operation |
| ---- | --------- |
| `00` | ADD       |
| `01` | SUB       |
| `10` | AND       |
| `11` | XOR       |

## How It Works

An `SN74HC283N` performs 4-bit arithmetic, while `SN74HC08N` and `SN74HC86N` chips generate the AND and XOR results.

Subtraction uses two's-complement arithmetic by XORing the B input with the SUB control signal and using SUB as the carry-in.

`SN74HC157N` multiplexers select which operation is routed to the output.

The arithmetic output was also expanded to **5 bits**, allowing results such as `1111 + 0001 = 10000` and `0000 - 0001 = 11111` to be displayed directly.

## Problems Encountered

The main challenges were debugging multiplexer wiring, maintaining clean logic levels across the larger circuit, and correctly handling the fifth arithmetic output bit.

Testing each arithmetic and logic section independently made it much easier to isolate problems before combining the full ALU.

## What I Learned

This phase reinforced:

* 4-bit binary arithmetic
* Two's-complement subtraction
* Multiplexer-based operation selection
* Parallel logic operations
* 5-bit arithmetic results
* Modular ALU design
* Debugging larger digital circuits

## Demo

* [4-Bit ALU Demo](demo/)

## Next Phase

[Phase 4 — Registers](../04-registers/)
