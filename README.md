# SXP - Simple Extensible Processor

Forked from Opencores.org SXP repository.

## Description

32 bit pipelined processor. 
Instruction set is non conventional in that it does not use a conventional decoder for instructions. The instruction set is made by collecting together "atomic" control signals together to form the instruction. This was done to eliminate the need for the decoder and save an extra pipeline stage. As a consequence latency is reduced and recovery from pipeline flushes do not degrade performance as badly. 

The design goals for the processor were speed, small size and flexibility. 
An extensible bus architecture is supported so that extra functions and bus architectures could be tightly coupled to the processor. This would support such functions as adding DSP instructions,multiple processor and network processing to the processor. 

Please refer to /sxp/doc/instr.txt 
for more information about the instruction set. 

(The SXP processor was built from scratch using the GPL'ed Verilog simulator Icarus. The instruction set cannot be copyrighted and the architecture has been taught in computer architecture classes for more than 20 years. I feel that this core is pretty safe from copyright and IP patent concerns.) 

For more information see /sxp/doc/README.txt 
This will supply more information about the project and its 
organization. 

SXP Designers:  
Sam Gladstone  
Bob Hoffman  
Nate Gregoire  

## Features

- Verilog compatible with Icarus verilog simulator.(Latest Dev release) 
- Fast recovery from pipeline flushes 
- Instructions tightly coupled with pipeline control circuits. 
- Extensible bus architecture 
- Includes functionality for both synchronous and memory reg file 
- Interrupt handling 
- Harvard architecture

## Status

- Processor is synthesizable. (Tested with Synopsys DC) 
- Processor is fully simulatable with any Verilog simulator. 
- C++ processor model correctly follows Verilog behavior 
- "Coder" visual instruction generator works correctly. (TK/TCL) 
- Processor correctly handles interrupts. 
- Programmable timer circuit (halt signal, interrupt timer, etc.) works fine. 
- Instruction level trap (virtual memory, illegal op, etc.) being developed.
