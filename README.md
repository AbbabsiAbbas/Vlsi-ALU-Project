# 4-Bit ALU Design - Final Project

## Project Overview
This project is aimed at providing hands-on experience in the design and implementation of a simplified 4-bit Arithmetic Logic Unit (ALU) using **Cadence Virtuoso** and **gpdk045/gsclib045 technology**. The process simulates the steps used in the microelectronics industry for large-scale integrated circuits.

## Project Stages
### 1. Planning Stage (Due: March 10, 2024)
- **Block-level logical diagram**: Design and sketch a logical diagram of the 4-bit ALU circuit.
- **Estimation of cells**: Estimate the number of cells/components required using `gsclib045`.
- **Floor plan sketch**: Draw a preliminary floor plan for the layout of the ALU.
- **Area estimation**: Estimate the area required for the layout.
- **Output**: A report summarizing the planning stage.

### 2. Implementation Stage (Due: May 9, 2024)
- **Design logical schematic**: Build the detailed schematic using `gsclib045` cells.
- **Measure critical path delay**: At supply voltages of 700mV and 1.2V.
- **Max clock frequency**: Determine the maximal clock frequency at both supply voltages.
- **Design and build layout**: Using hierarchical structure, perform DRC, LVS, and parasitic extraction (QRC).
- **Final Report**: Submit a detailed report with schematics, test results, and optimization comments.

## ALU Specifications
- **Inputs**: Two 4-bit inputs `A[3:0]`, `B[3:0]` and one 5-bit opcode.
- **Outputs**: One 4-bit output `Y[3:0]`.
- **Operations**: 
  - ADD: `Y = A + B`
  - SUB: `Y = A - B`
  - XOR: `Y = A XOR B`
  - Barrel Shift Right: `Y = Barrel Shift Right(A, i)` (where `i` is defined in opcode).
- **Encoding**: Two’s complement representation for arithmetic operations.
  
## Adder Selection Algorithm
Based on group member IDs, the adder topology is selected as follows:
- `y = (sum of group IDs mod 6) + 1`
- Depending on the value of `y`, one of the following adders is selected: Brent-Kung, Sklansky, Kogge-Stone, Han-Carlson, Knowles [2,1,1,1], or Ladner-Fischer.

## Tools and Technologies
- **Cadence Virtuoso**
- **gpdk045/gsclib045 technology**
- **DRC, LVS, QRC for layout verification**


---

This project is part of the VLSI course at Tel Aviv University - israel and is supervised by DR Asia Ben Cohen.
