8-Bit Binary ↔ Gray Code Converter

Datapath and Control Path Based Design (Verilog)
📌 Project Overview

This project implements an 8-bit Binary to Gray code and Gray to Binary code converter using a custom datapath and Moore-based control unit.
The design strictly follows resource-constrained RTL architecture principles, making it suitable for VLSI design and verification learning.

The converter operates sequentially using:

Dedicated registers

A shared interconnect bus

A single XOR logic unit

A finite state machine (FSM) for control

🎯 Key Objectives

Design a hardware-efficient code converter

Separate datapath and control path

Use only one XOR gate

Avoid bus contention using tri-state buffers and MUXes

Implement a Moore FSM for process control

Verify functionality using a testbench

🔁 Supported Conversions
Convert Signal	Operation
0	Binary → Gray
1	Gray → Binary
🧩 Architecture Overview
🔹 Datapath Components

R1 (8-bit PIPO Register)
Stores the input binary or gray code

R2 (8-bit PIPO Register)
Stores the converted output code

R3 (1-bit Register)
Holds the current bit for XOR operation

R4 (1-bit Register)
Holds the previous bit for XOR operation

Single XOR Gate
Used for both conversion modes

Shared 8-bit Interconnect Bus
Implemented using tri-state buffers and multiplexers

🔹 Control Path

Moore-based Finite State Machine (FSM)

Controls:

Register read/write signals

Bus access

Conversion flow

Generates Done signal after successful conversion

🕹️ Control Signals
Inputs

Clock – System clock

Start – Initiates conversion

Convert – Selects conversion mode

Outputs

R1_in, R1_out

R2_in, R2_out

R3_in, R3_out

R4_in, R4_out

Done – Indicates completion of conversion

🔄 Process Flow

Wait in IDLE state until Start is asserted

Copy MSB directly from R1 to R2

Transfer adjacent bits from R1 to R3 and R4

Perform XOR using a single XOR gate

Store result bit-by-bit into R2

Assert Done after full 8-bit conversion

⚙️ Design Constraints

Only one XOR gate is used

No direct combinational conversion

All transfers happen through the shared bus

FSM implemented strictly in Moore style

No bus contention allowed

🧪 Verification

Functional verification is performed using a Verilog testbench

Testbench validates:

Binary → Gray conversion

Gray → Binary conversion

FSM control behavior

Done signal timing
