==========================================
RISC-Z - Open Instruction Set Architecture
==========================================

RISZ-Z, pronounced "risk-set", is a simple open source ISA specification. It is a reduced
instruction set architecture focusing on fast instruction decoding, while still having a well
standardized library of instructions in the base specification.

Instruction Formats
===================

RISC-Z follows a simple and strict list of instruction formats. Every instruction is a multiple of
16 bits, up to 64 bits.

Instruction Lengths
-------------------

Instructions can have the following lengths: 16, 32, 48 or 64 bits. The length can be determined by
looking at the last few bits of the opcode. The instruction width can be found using these rules:

* If bits ``[0:1]`` doesn't equal to ``11``, the instruction is 16 bits wide.
* If bits ``[0:2]`` equals to ``011``, the instruction is 32 bits wide.
* If bits ``[0:3]`` equals to ``0111``, the instruction is 48 bits wide.
* If bits ``[0:3]`` equals to ``1111``, the instruction is 64 bits wide.

Registers
=========

There are 32 registers labelled `x0` through `x31`. Each register also has a symbolic name, which
specifies the usage of each given register.

============= ============= ===========
Register Name Symbolic Name Description
============= ============= ===========
x0            zero          Always zero
x1-31                       Reserved
============= ============= ===========
