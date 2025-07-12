# RISC-V-Assembler-and-Five-Stage-Pipelined-processor
# Components:
  1. RIS-V Assembler
  2. Pipelined processor

# 🔧 RISC-V ASSEMBLER:
this components converts **RISC-V assembly instructions** into **32-bit binary machine code**. The project supports a wide range of instruction types as defined in the RISC-V base integer instruction set.

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
