# Design Decisions

This document lists the reasoning behind the design choices of the ALU.

- When researching which ICs were appropriate for the logic gate, I chose 74HC logic over LSTTL because the HC family worked cleanly with the project's original ~4.5 V supply and CMOS-style input behavior.
  
- Used a 74HC283N adder chip instead of building the full adder from logic gates to preserve space and represent system-level design.
  
- Used muxes to select between modes to preserve 74HC logic instead of combining functions with larger gate networks.
  
- Added a 5th signed result bit so two signed 4-bit inputs can be represented without losing range.
  
- Kept only the signed overflow flag as a 4-bit overflow to see whether the result would be truncated if converted back to 4-bits. Removed Z,N,C flags in the 4-bit ALU because I believed they were redundant and I didn't necessarily need them.
  
- Used registers for inputs and outputs to gain experience and add a sense of memory to the ALU. Could also be utilized if I wanted to upgrade my ALU in a v2 build.
  
- Added manual and auto clock settings in order to gain experience, replicate a real global clock line in a CPU, and so the registers can update continuously.
  
- Chose to stop before implementing full opcode sequencing/control logic so the scope stayed focus on a manageable ALU system (and not a breadboard mess). Would defnitely be interested in adding sequence coding in a v2 build, aiming for a full CPU architecture.
  
- 3D printed an ALU case to consolidate the 2 separate breadboards onto one common platform. Made it easier to carry/rotate.
