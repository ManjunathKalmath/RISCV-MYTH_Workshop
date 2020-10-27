# RISC V (RV32I) CPU Core

This repository contains all the information about RISC V CPU Core that is builtin the 5-days Workshop “RISC-V based Microprocessor for You in Thirty Hours"

## Workshop Flow
- Day - 1 : Introduction to RISC-V ISA and GNU compiler toolchain
- Day - 2 : Introduction to ABI and basic verification flow
- Day - 3 : Digital Logic with TL-Verilog and Makerchip
- Day - 4 : Basic RISC-V CPU micro-architecture
- Day - 5 : Complete Pipelined RISC-V CPU micro-architecture/store

## Workshop Outcome
- Understanding of RISC V ISA
- RISC V GNU Toolchain
- TL-Verilog
- Designing the Digital Circuits using TL-Verilog
- RISC V RV32I microarchitecture

## Day - 1 : Introduction to RISC-V ISA and GNU compiler toolchain

**RISC V ISA**
RISC V is an open and free Instruction Set Architecture(ISA) which is enabling the modern processor design.RISC V ISA avoids over-architecting for a particular 
implementation technology and microarchitecture style.RISC V ISA is divided into base integer ISA and optional standard extensions such as Integer Multiplication 
and Division, Atomic Instructions,Single and Double Precision Floating Points which helps general purpose software development.

**RISC V GNU Toolchain**
1. To compile with RISC-V GCC compiler:
> `riscv64-unknown-elf-gcc <compiler option -O1 ; Ofast> <ABI specifier -lp64; -lp32; -ilp32> <architecture specifier -RV64 ; RV32> -o <object filename> <C filename>` 
2. To view the disassembly aka assembly code - RISC V :
> `riscv64-unknown-elf-objdump -d <object filename> | less `

In the workshop SPIKE RISC V ISA Simulator is used.
More on Spike Simulator Visit https://github.com/riscv/riscv-isa-sim

#### Sum 1 to n program using SPIKE




Check the folders for assignments for particular days.
