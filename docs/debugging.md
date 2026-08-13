# Debugging

This document lists the issues faced when building the ALU and how I faced them.

- Throughout the whole project I faced lots of incorrect wire placement, became very familiar with how to topologically use a multimeter to debug and utilize notes to determine correct wire/node placement.
  
- Early logic ICs behaved unexpectedly and had multiple floating voltage problems, appeared to have TTL-like input behavior. Switched ICs with components sourced from Digi-Key which resolved the inconsistent input behavior.
  
- Verified arithmetic results with edge cases and cases that utilized carry logic.
  
- Reworked 5th output bit after realizing ordinary Cout is not the same as a signed extension bit.
  
- Debugged mux ICs after inconsistent behavior by adding a capacitor between VCC and GND for a clean startup.
