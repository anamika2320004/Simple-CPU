# Simple CPU (16-bit)

## Project Overview
This is a simple **16-bit CPU** implemented in Verilog using EDA Playground.  
The CPU demonstrates the basics of CPU design, including **registers, ALU operations, program counter, instruction memory, and control flow**.

### What You’ll Learn
- Designing a small **instruction set**  
- Building a **register file**  
- Implementing a **simple ALU**  
- Creating a **control unit using FSM**  
- Running simulations and observing outputs in **tabular format**  

---

## Features
- 16-bit CPU with 4 general-purpose registers (R0–R3)  
- Supports basic instructions:  
  - `MOV` (move register)  
  - `ADD` (addition)  
  - `SUB` (subtraction)  
  - `HLT` (halt execution)  
- Instruction memory: 16 words  
- ALU output displayed on every clock cycle  
- Execution stops at HLT instruction  

---

## Files
| File | Description |
|------|-------------|
| `txt file` | Verilog module for the CPU, including registers, ALU, and program memory and  Testbench for simulating the CPU, generating clock, and displaying outputs |

---

## Simulation Setup
1. Open [EDA Playground](https://www.edaplayground.com/)  
2. Select **SystemVerilog + Icarus Verilog**  
3. Paste `code and testbench` into separate tabs  
4. Run the simulation to view outputs in the console  

---

## Console Output Example

| PC | Instr            | R0 | R1 | R2 | R3 | ALU |
|----|-----------------|----|----|----|----|-----|
| 0  | 0001000000010000 | 3  | 3  | 2  | 1  | 3   |
| 1  | 0010000000100000 | 5  | 3  | 2  | 1  | 5   |
| 2  | 0011000100110000 | 5  | 2  | 2  | 1  | 2   |
| 3  | 1111000000000000 | 5  | 2  | 2  | 1  | 2   |

> Notes:  
> - **PC** = Program Counter  
> - **Instr** = Current instruction in binary  
> - **R0–R3** = Register values  
> - **ALU** = ALU output  

---

## How it Works
1. On **reset**, all registers and PC are initialized  
2. Instructions in `instr_mem` execute sequentially  
3. **ALU** performs computation for each instruction  
4. Execution stops at the `HLT` instruction, keeping PC, registers, and ALU output stable  
5. `$display` statements in the testbench show CPU state every clock cycle  

---

## Future Improvements
- Add more instructions: `AND`, `OR`, `XOR`, `NOT`, `JMP`  
- Add **branching and conditional execution**  
- Implement **stack and memory operations**  
- Expand instruction set for **realistic CPU simulation**
