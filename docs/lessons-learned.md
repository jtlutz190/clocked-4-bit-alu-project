# Lessons Learned

This document lists all of the skills and ideas I've learned while building the ALU.


- Learned to separate logical correctness from electrical correctness. A logically correct design can still fail physically due to power issues, floating inputs, or wiring problems.

- Learned that abstraction is vital when working with larger systems. Once the ALU or registers were verified, I could treat them as functional blocks and focus on the signals entering and leaving them. I also applied this approach when designing the schematics.

- Learned the importance of documenting wiring while building dense circuits. In a large breadboard design, even a small wiring mistake or undocumented change can make debugging significantly more difficult.

- Learned that engineering is not only about building a working system, but also about documenting the design clearly and communicating how and why it works.
  
- One of the first concepts I learned during this project was the importance of pull-up and pull-down resistors. Early on, I allowed inactive inputs to float instead of defining them with pull-down resistors, which caused unreliable logic states and dim LEDs.

- Learned how to recognize floating voltages and undefined logic levels. After encountering dim LEDs and unexpected node voltages around ~0.66 V, I became much faster at identifying grounding or power issues.

- Learned how to read and use IC datasheets effectively. Datasheets became an essential reference for understanding pinouts, electrical characteristics, control inputs, and expected device behavior.

- Developed a stronger understanding of the 74HC logic family and common IC conventions, including supply pins, logic-level behavior, and the importance of properly defined inputs.

- One of the most interesting concepts I learned was how binary addition and subtraction can be implemented using Boolean logic. I especially enjoyed learning how two’s-complement subtraction allows the same adder hardware to perform both addition and subtraction.

- Learned how signed binary arithmetic works within an ALU, including the differences between carry, borrow, sign, and signed overflow.

- Learned how components such as multiplexers, registers, and 555 timers work both conceptually and as physical circuit elements within a larger digital system.

- Learned the value of incremental testing. I tested registers, clock circuits, and multiplexers on an isolated breadboard before integrating them into the main project. This helped me identify problems early and become familiar with each IC before adding it to the larger system.

- Learned the value of testing edge cases rather than relying only on simple test cases. Carry, signed overflow, and borrow behavior revealed problems that basic tests would not have detected.

- Learned the importance of designing a user-friendly circuit. In my earlier builds, I placed LEDs and input controls wherever they were easiest to wire, rather than intentionally arranging them for usability. Later designs placed inputs and indicators in more accessible and visually organized locations, making the circuit easier to operate and understand.

Overall, this project taught me how individual digital logic concepts come together to form a larger computing system. More importantly, it showed me that successful hardware design depends just as much on testing, debugging and documentation rather than just the original idea.
