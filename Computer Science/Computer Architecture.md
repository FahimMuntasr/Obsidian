[[The Elements of Computing Systems.pdf]]

# **Fundamental Questions and Topics**

1. [[#What qualifies as a Computer?]]
2. [[#How does a CPU work?]]
3. [[#Registers and RAM]]
4. [[#Instructions]]
5. [[#CPU cache]]
# What qualifies as a Computer?

A computer at the lowest level is a collection of logic gates performing calculations. These logic gates are usually made using transistors. This does not mean that a computer can only be built with transistors, anything that can be used to represent boolean algebra is a viable building block for logic gates. The reason transistors are used is that currently that is the fastest and most efficient way of building logic gates.  

All computers must be able to:
- Input Data
- Process Data
- Store Data
- Output Data

# How does a CPU work?

#### Components of a processor

A modern CPU consists of the following parts:
- ALU : The arithmetic logic unit performs all logical operations on data.
- Program counter : Stores the address of the next instruction to be carried out.
- Control unit : The instructions are decoded here.
- Accumulator : The output of the current operation is stored here.
- Data register : Contains Instructions along with its respective address.
- Clock : After every tick of this clock one operation is done. The speed of the processor is determined by this "clock speed". Modern CPUs have a clock ticking at several Giga Hertz. 

A CPU communicates with memory using different buses/channels:
- Data bus : Sends data to and from the CPU
- Address bus : Sends the address of the corresponding data to and from the CPU
#### The FDE cycle

The Fetch-Decode-Execute cycle is the basis of all operations in all processors. Each step is started by a clock tick. The time between each clock tick is always constant. 

During Fetch:
- The program counter is filled with the address of the instruction to be carried out.
During Decode:
- The control unit reads the instruction and tells the ALU to perform the operation.
During Execute:
- The result of the operation carried out by the ALU is then stored in the accumulator.

#### The ALU

The arithmetic logic unit performs arithmetic and logical operations on two inputs. This is possible through logic gates and half adders. Half adders add 2 bit numbers, Two half adders are joined to create a full adder which can add 3 bit numbers. From this same method an 8-bit adder is created which does the arithmetic operations in an ALU.

# Registers and RAM

**_Registers_** are the smallest data-holding elements built into the processor itself. Registers are the memory locations that are directly accessible by the processor. The registers hold the instruction or operands currently accessed by the CPU.

**_Memory_** is a hardware device that stores computer programs, instructions, and data. The memory that is internal to the processor is primary memory (RAM). RAM is a volatile memory, meaning the primary memory data exist when the system’s power is on, and the data vanishes as the system is switched off. The primary memory contains the data required by the currently executing program in the CPU. 

# Instructions

Instructions are stored in memory which contain details of the task that needs to be done. Part of an instruction is the OP code, which tells the ALU what type of operation needs to be executed. The other part is an address or data which is needed for the operation.

# CPU cache

Modern CPUs are too fast for memory to keep up. This means that for most fetch-decode-execute cycles the CPU sits idle while the data is being fetched from the memory. This is why a cache is introduced, the smaller but faster cache stores important program data which means the CPU can reach its full speed without waiting for the memory to catch up.

