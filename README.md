# RISC-V RV32I Assembler & Simulator

A Python-based implementation of a two-pass assembler and instruction-level simulator for the RISC-V RV32I instruction set architecture. The project translates human-readable RISC-V assembly programs into 32-bit machine code and executes them within a software-based simulation environment, providing detailed execution traces and memory state visualization.

Developed as part of the Computer Organization curriculum, this project demonstrates concepts in instruction set architecture, machine code generation, processor execution flow, memory management, and low-level systems programming.

---

## Key Features

### Assembler

* **Two-Pass Assembly Process** for accurate label resolution and forward reference handling.
* **Comprehensive RV32I Support**, including:

  * R-Type Instructions
  * I-Type Instructions
  * S-Type Instructions
  * B-Type Instructions
  * U-Type Instructions
  * J-Type Instructions
* **Robust Syntax Validation** with detailed error reporting.
* **Register and Operand Verification** to prevent invalid instruction encoding.
* **Custom Instruction Extensions**, including:

  * `rvrs`
  * `mul`
  * `halt`
  * `rst`

### Simulator

* **Instruction-Level Execution Engine** implementing RV32I execution semantics.
* **Program Counter Tracking** with precise control-flow handling.
* **Register State Visualization** after each instruction cycle.
* **Memory State Dump Generation** for post-execution analysis.
* **Two's Complement and Sign Extension Support** conforming to RV32I specifications.
* **Branch and Jump Handling** with accurate address calculations.

---

## Architecture

The project is divided into two independent modules:

### Assembler

Converts assembly source code into executable binary machine code.

```text
Assembly Program
        │
        ▼
   Two-Pass Parser
        │
        ▼
 Label Resolution
        │
        ▼
 Instruction Encoding
        │
        ▼
   Binary Machine Code
```

### Simulator

Executes generated machine code and produces execution traces.

```text
Binary Machine Code
         │
         ▼
 Instruction Decoder
         │
         ▼
 Execution Engine
         │
         ▼
 Register Updates
         │
         ▼
 Memory Operations
         │
         ▼
 Execution Trace
```

---

## Project Structure

```text
riscv-rv32i-assembler-simulator
│
├── Simple-Assembler/
│   ├── Assembler.py
│   └── run
│
├── SimpleSimulator/
│   ├── Simulator.py
│   ├── Input_Sim.txt
│   └── Output_Sim.txt
│
├── stdin.txt
└── README.md
```

---

## Requirements

* Python 3.8+
* No external dependencies required

---

## Usage

### Assemble a Program

```bash
python Simple-Assembler/Assembler.py input.asm output.bin
```

Alternatively:

```bash
python Simple-Assembler/Assembler.py < input.asm > output.bin
```

### Simulate Machine Code

```bash
python SimpleSimulator/Simulator.py output.bin trace.txt
```

Alternatively:

```bash
python SimpleSimulator/Simulator.py < output.bin > trace.txt
```

---

## Learning Outcomes

This project provided practical experience in:

* Computer Organization and Architecture
* Instruction Set Design
* Assembly Language Processing
* Machine Code Generation
* Processor Simulation
* Memory and Register Management
* Systems Programming
* Python-Based Software Engineering

---

## Future Enhancements

* Support for additional RISC-V extensions (M, C, and F)
* Pipeline simulation and hazard detection
* Cache memory simulation
* Graphical visualization of execution flow
* Interactive debugging environment
* Performance profiling and benchmarking

---

## Author

**Yuvraj Verma**

Computer Science and Bioscience
Indraprastha Institute of Information Technology Delhi (IIIT-Delhi)

GitHub: https://github.com/yuvraj-23617
