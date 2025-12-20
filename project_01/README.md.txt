# Project 1 — Boolean Logic

This project implements the basic combinational logic gates as part of **Nand2Tetris Part 1**.

The design follows the intended course methodology:
- **NAND** is used as the only primitive gate.
- Simple gates are built directly from NAND.
- More complex gates are constructed hierarchically using previously built components.

---

## Design Approach

The implementations follow a bottom-up hardware abstraction model:

1. **Primitive level**
   - `Nand` (provided by the platform)

2. **Elementary gates (built directly from NAND)**
   - `Not`
   - `And`
   - `Or`

3. **Multi-bit versions (built from elementary gates)**
   - `Not16`
   - `And16`
   - `Or16`

4. **Data-selection logic (built from lower-level gates)**
   - `Mux`
   - `Mux16`
   - `DMux`
   - `DMux4Way`
   - `DMux8Way`

Each layer reuses components from the previous layer, reinforcing modular design and abstraction.

---

## Implemented Chips

- **Elementary:** `Not`, `And`, `Or`
- **16-bit:** `Not16`, `And16`, `Or16`
- **Multiplexers:** `Mux`, `Mux16`
- **Demultiplexers:** `DMux`, `DMux4Way`, `DMux8Way`

---

## Verification

- All chips were tested using the **official Nand2Tetris Hardware Simulator**
- Each implementation passes the provided `.tst` and `.cmp` test scripts
- Designs strictly adhere to the course’s hardware constraints

---

## Learning Outcome

By completing this project, I reinforced:

- Hierarchical hardware design
- Abstraction in digital logic
- Reuse of lower-level components to build complex systems
- How all computation can ultimately be constructed from a single primitive gate

This project forms the foundation for all subsequent CPU, memory, and system-level components.
