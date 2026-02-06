# 8-Bit CPU Design & Implementation (VHDL)
Project Type: Academic Portfolio (Digital Systems) Language: VHDL Tools: Intel Quartus II Prime, ModelSim/Waveform Simulation, Schematic Entry (BDF). Implemented on Altera DE2-115 FPGA

![IMG_9578 2](https://github.com/user-attachments/assets/75276b93-95f5-41ad-af82-a9798c8328d3)


## 📖 Project Overview
This project involves the design, simulation, and implementation of a simplified 8-bit Central Processing Unit (CPU). The system integrates custom sequential and combinatorial logic modules to fetch instructions, process data, and manage control flow. The design demonstrates a modular approach to hardware architecture, targeting FPGA deployment.

## 🛠 Tech Stack & Skills
Hardware Description Language: VHDL

EDA Tools: Intel Quartus Prime (Schematic & Code entry), ModelSim

Concepts: Finite State Machines (FSM), ALU Design, Digital Logic, Datapath & Control, Timing Analysis

Hardware Interface: 7-Segment Displays (SSEG), Gated D-Latches

## ⚙️ System Architecture
The CPU is composed of four primary sub-systems integrated to execute custom microcode instructions:

### 1. Arithmetic Logic Unit (ALU) Core
Functionality: Capable of performing 8-bit arithmetic and Boolean operations.

Operations Supported: Summation, 2's Complement, Bitwise NAND/OR, Logical Shifts (SHL), and parity modification.

Logic Integration: Includes conditional logic to compare register values against external inputs (e.g., ID verification sequences).

### 2. Finite State Machine (Control Unit)
Role: Acts as the synchronized program counter.

Mechanism: Cycles through 8 distinct states to generate control signals for the decoder and synchronize the datapath.

### 3. Memory & Storage (Gated Latches)
Components: Two 8-bit Gated D-Latches (Reg A and Reg B).

Role: Temporary storage for binary operands (e.g., storing decimal values 35 and 76) to ensure stable data flow during ALU operations.

### 4. Instruction Decoder
Type: 4:16 Decoder.

Role: Converts 3-bit FSM state outputs into "1-hot" control codes to select specific ALU operations, allowing for scalable instruction sets.

## 🚀 Key Features
Modular Design: Components (Latches, Decoders, FSM) were designed individually and integrated into a top-level machine entity.

Custom Microcode: Implemented a unique instruction set including complex operations like "Summation minus 5" and "Odd/Even Bit Swapping".

Verification: Validated via extensive Waveform simulation to ensure correct timing, state transitions, and arithmetic accuracy.

## 📊 Simulation Results
The design was verified using Quartus Waveform simulations:

Confirmed correct state transitions (0 → 1 → ... → 7).

Validated ALU output correctness against truth tables for logical and arithmetic operations.

Verified correct signaling for Seven Segment Display outputs based on comparison logic.
