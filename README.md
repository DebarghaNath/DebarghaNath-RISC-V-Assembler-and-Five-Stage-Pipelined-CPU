# RISC-V-Assembler-and-Five-Stage-Pipelined-processor

## Components:
1. RISC-V Assembler  
2. Pipelined Processor

---

# 🔧 RISC-V ASSEMBLER

This component converts **RISC-V assembly instructions** into **32-bit binary machine code**. The project supports a wide range of instruction types as defined in the RISC-V base integer instruction set.

## 📝 Overview

This tool is designed to:

- ✅ Parse RISC-V assembly instructions  
- ✅ Detect their format (R, I, S, B, U, J types, and subtypes)  
- ✅ Encode them into their corresponding binary format  
- ✅ Store and manage the binary instructions in a simulated instruction memory  

## 🚀 Features

- ✅ Supports all basic RISC-V instruction formats:
  - **R-Type**: `ADD`, `SUB`, `MUL`, `AND`, `OR`, etc.
  - **I-Type**: `ADDI`, `ANDI`, `ORI`, etc.
  - **IL/IR-Type**: `SLLI`, `SRLI`, `SRAI`, etc.
  - **S-Type**: `SW`, `SB`, `SH`
  - **B-Type**: `BEQ`, `BNE`, `BGE`, etc.
  - **J-Type**: `JAL`
  - **JL-Type**: `JALR`
  - **U-Type** (Upper Immediate): `LUI`, `AUIPC`
- ✅ Converts immediate values to correct binary format  
- ✅ Encodes full 32-bit binary instructions from text  
- ✅ Simulated instruction memory for loading & fetching  
- ✅ Modular C++ class-based architecture  

---

# ⚙️ FIVE-STAGE PIPELINED PROCESSOR

This component simulates a **5-stage pipelined CPU**, emulating real hardware behavior by modeling the classic **instruction pipeline** stages: **Fetch, Decode, Execute, Memory, and Write Back**.

## 📝 Overview

This simulation is designed to:

- ✅ Emulate the five stages of a RISC-V pipeline  
- ✅ Handle instruction-level parallelism  
- ✅ Track and resolve data hazards (forwarding and stalls)  
- ✅ Simulate control hazards via branch prediction/stalling  
- ✅ Maintain register and memory states throughout execution  

## 🚀 Features

- ✅ **Instruction Fetch (IF)**: Fetches instructions from instruction memory  
- ✅ **Instruction Decode (ID)**: Decodes instructions and reads registers  
- ✅ **Execution (EX)**: Performs ALU operations and computes addresses  
- ✅ **Memory Access (MEM)**: Handles memory read/write for load/store instructions  
- ✅ **Write Back (WB)**: Writes results back to the register file  
- ✅ **Hazard Detection Unit**:
  - Detects **data hazards** and inserts **NOPs** when needed  
  - Implements **data forwarding** where possible to reduce stalls  
- ✅ **Control Hazard Handling**:
  - Detects and handles branches with basic prediction/stalling  
- ✅ **Register File & Memory Simulation**:
  - Simulates a 32-register file and RAM  
  - Displays final states of registers and memory  
- ✅ **Performance Metrics**:
  - Instruction count, stall count, and cycle count tracking  
  - Computes **CPI (Cycles Per Instruction)**   
