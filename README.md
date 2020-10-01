
# 8085-Processor

## About Processor

This is an 8-bit RISC type Processor.  
Completes each operation in 5 clock cycles.  
It contains 4 temporary registers (register file).  
The memory size is 65,536 x 8 bit. Instructions and memory data goes by same address.  

## WORKING THEORY

Instruction is fetched in 1 clock cycle and stored in Instruction Register (IR).  
Immediate value and Decoding instruction are done in second clock cycle.  
ALU operation is done in third clock cycle and value is updated in register Rz.  
Memory reading or writing is done in fourth clock cycle and value is available at Multiplexer for writing in Register file.  
Register file get updated by new value in fifth clock cycle.  

## OPERATIONS SUPPORT

**The Processor supports the below operations with their respective op-codes:**

- ADD 0000  
- SUB 0001  
- MUL 0010  
- AND 0011  
- OR  0100  
- XOR 0101  
- MOV 0110  
- HLT 0111  
- STA 1000  
- JMP 1001  
- LDA 1010  

## INSTRUCTION FORMAT

First four MSB’s are for op-codes and the last ones for register address inside the register file.  
For STA, JMP and LDA 8 – bit memory address is to be given in the memory block next to the instruction.  
> Example

- ADD R0 R1 :-  0000 00 01
- LDA  R1 M :-  1010 01 00 M (8 - bit)
- STA R1 M  :-  1000 00 01 M (8 - bit)  Exception (register address is in last 2 bits)  
- JMP M     :-  1001 00 00  M (8 - bit)  
- HLT       :-  0111 00 00

## License

Built with ♥ by Ankur Jaiswal  under [MIT License](https://ankur.mit-license.org/)
