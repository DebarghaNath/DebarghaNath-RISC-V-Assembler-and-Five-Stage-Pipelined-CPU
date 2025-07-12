# 🚀 RISC-V Assembler & Five-Stage Pipelined CPU Simulator

A complete simulation of **low-level hardware design**, this project implements a **RISC-V assembler** alongside a **five-stage pipelined processor**, both written entirely in **C++**. It demonstrates how high-level RISC-V assembly is parsed, translated to machine code, and then executed via a realistic hardware pipeline model.

---

## 🧩 Components

1. **RISC-V Assembler** – Converts RISC-V assembly instructions into 32-bit binary machine code  
2. **Pipelined Processor** – Simulates a hardware-accurate 5-stage pipelined CPU using that machine code

---

# 🔧 RISC-V ASSEMBLER

The assembler component translates **RISC-V assembly language** into corresponding **32-bit binary instructions**, storing them in a simulated instruction memory. It mimics the behavior of real-world assembler tools used in hardware systems.

### 📝 Key Responsibilities

- ✅ Parse RISC-V assembly syntax  
- ✅ Identify instruction types (R, I, S, B, U, J, and subtypes)  
- ✅ Convert registers and immediate values into binary  
- ✅ Generate 32-bit machine code for each instruction  
- ✅ Store output in instruction memory for CPU simulation

### 🚀 Features

- ✅ **Full Instruction Format Support**:
  - **R-Type**: `ADD`, `SUB`, `MUL`, `AND`, `OR`, etc.
  - **I-Type**: `ADDI`, `ANDI`, `ORI`, etc.
  - **IR/IL-Type**: `SLLI`, `SRLI`, `SRAI`, etc.
  - **S-Type**: `SW`, `SB`, `SH`
  - **B-Type**: `BEQ`, `BNE`, `BGE`, etc.
  - **J-Type**: `JAL`
  - **JL-Type**: `JALR`
  - **U-Type**: `LUI`, `AUIPC`
- ✅ Accurate handling of **immediate fields**, sign-extension, and bit-shifts  
- ✅ Modular **object-oriented design** using C++ classes  
- ✅ Ready for integration with any RISC-V backend

---

# ⚙️ FIVE-STAGE PIPELINED CPU SIMULATOR

This processor simulates the classic **5-stage RISC-V pipeline** architecture:  
**Fetch → Decode → Execute → Memory → Write Back**  
It replicates real hardware behavior, including parallel instruction processing, hazard resolution, and cycle-accurate execution.

### 📝 Core Objectives

- ✅ Emulate each pipeline stage precisely  
- ✅ Maintain **register file**, **data memory**, and **program counter**  
- ✅ Simulate pipeline **hazards** and resolve them with realistic techniques  
- ✅ Track **performance metrics** like CPI, stalls, and total cycles

### 🚀 Features

#### ✅ Pipeline Stages:
- **IF (Instruction Fetch)**: Fetches machine code from instruction memory  
- **ID (Instruction Decode)**: Decodes opcodes, extracts operands  
- **EX (Execute)**: Performs ALU operations or branch offset calculations  
- **MEM (Memory Access)**: Reads from or writes to data memory  
- **WB (Write Back)**: Updates registers with results from EX or MEM  

#### ✅ Hazard Handling:
- **Data Hazards**:
  - Data **forwarding** where applicable  
  - Automatic insertion of **NOPs** when necessary  
- **Control Hazards**:
  - **Branch stalling** to maintain correctness  
  - Optional branch prediction logic

#### ✅ Additional Features:
- Simulated **32-register file** and **memory module**  
- Easy-to-read **debug output** showing pipeline state per cycle  
- Tracks:
  - Instruction count  
  - Stall count  
  - Cycle count  
  - **CPI (Cycles Per Instruction)** calculation  

---

## 🧠 Educational Value

This project demonstrates how **hardware logic** and **software abstraction** come together:

- 🔬 Mimics how real assemblers convert human-readable code to binary  
- 🧮 Shows how CPUs execute instructions in pipelined fashion for performance  
- 💡 Helps students and hardware enthusiasts grasp low-level CPU internals

---

## 📁 File Structure

