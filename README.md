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

## Day - 2 : Introduction to ABI and basic verification flow

#### Sum 1 to n program using SPIKE
In this picture we can get to know the contents of any register by:
> `reg 0 "ABI name of register"`

![day-1](https://user-images.githubusercontent.com/48850794/97297491-215fca00-1878-11eb-86f7-3f6c9374b924.png)

#### Application Binary Interface

RISC-V architecture has 32 registers. Application programmer, can access each of these 32 registers through its ABI name,
for example, you need know the value of stack pointer or move the stack pointer, all you need to do is “addi sp, sp, -16”,
where ‘sp’ is the ABI name of stack pointer.

![32-registers](https://user-images.githubusercontent.com/48850794/97298238-28d3a300-1879-11eb-9c24-6e7b40c1c2ac.png)

## Day - 3 : Digital Logic with TL-Verilog and Makerchip

**TL-Verilog**

Transaction-Level Verilog (TL-Verilog) is an emerging extension to SystemVerilog that supports transaction-level design methodology.
In transaction-level design, a ​transaction is an entity that moves through a microarchitecture. 

**Makerchip IDE**

Makerchip is a free online environment for developing high-quality integrated circuits. You can code, compile, simulate, and 
debug Verilog designs, all from your browser. Your code, block diagrams, and waveforms are tightly integrated.

**AND Gate - Makerchip IDE**

![Screenshot (438)](https://user-images.githubusercontent.com/48850794/97299564-22462b00-187b-11eb-9ad0-5dfbee8a5181.png)

**Pipelining in TL-Verilog - Pythagorean Theorem Implementation**

1. Single Stage pipeline

![Screenshot (440)](https://user-images.githubusercontent.com/48850794/97301600-f5474780-187d-11eb-9aff-17d5d9db7c4a.png)

2. 3 - Stage pipeline

![Screenshot (441)](https://user-images.githubusercontent.com/48850794/97302299-e01ee880-187e-11eb-89f6-945fb512c699.png)

**Sequential Calculator**

![Screenshot (443)](https://user-images.githubusercontent.com/48850794/97335354-c5ab3600-18a3-11eb-95ea-9cada592e90a.png)

## Day - 4 : Basic RISC-V CPU micro-architecture

5 stage pipeline processor consists of:
- Instruction Fetch
- Instruction Decode
- Instruction Execute
- Memory Access
- Write Back

![Screenshot (444)](https://user-images.githubusercontent.com/48850794/97336282-d6a87700-18a4-11eb-851e-b24c534fcc37.png)

## Day - 5 : Complete Pipelined RISC-V CPU micro-architecture/store

![Screenshot (411)](https://user-images.githubusercontent.com/48850794/97336558-2a1ac500-18a5-11eb-8701-86d7d2a6dfcf.png)


## Acknowledgements
- [Kunal Ghosh](https://github.com/kunalg123), Co-founder, VSD Corp. Pvt. Ltd.
- [Steve Hoover](https://github.com/stevehoover), Founder, Redwood EDA
- [Shivam Potdar](https://github.com/shivampotdar), GSoC 2020 @fossi-foundation
- [Vineet Jain](https://github.com/vineetjain07), GSoC 2020 @fossi-foundation
