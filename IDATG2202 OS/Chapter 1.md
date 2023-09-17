# ALU 
Arithmetic Logic Unit executes arithmetic and logical instructions on binary numbers. 
# CU
Control Unit controls the data flow and does all the preparations necessary for the ALU to execute instructions. 
# I/O 
Input / Output I/O devices are connected to the computer’s central bus, and are used by the CPU to get information out and in of the computer. These devices normally consist of a separate ”small computer” which is called a controller that has a processor, some memory, some software (firmware) and some interfaces (its own registers that the CPU can write to or read from). An example of a I/O device is the hard drive (in your laptop today this is probably a SSD, a Solid State Drive) which has a controller the CPU can ”talk to”, and it has an actual storage device behind the controller. 
# Bus 
In computer architecture, a bus (shortened form of the Latin omnibus, and historically also called data highway or databus) is a communication system that transfers data between components inside a computer, or between computers. This expression covers all related hardware components (wire, optical fiber, etc.) and software, including communication protocols. Early computer buses were parallel electrical wires with multiple hardware connections, but the term is now used for any physical arrangement that provides the same logical function as a parallel electrical busbar. Modern computer buses can use both parallel and bit serial connections, and can be wired in either a multidrop (electrical parallel) or daisy chain topology, or connected by switched hubs, as in the case of Universal Serial Bus (USB). 
# MMU 
# Controller 
# Firmware 
Software that is installed and made for specific hardware. 
# Bit vs Byte 
Bit < Byte, 8 bits in a Byte. 
# Data vs instruction 
# Instruction set 
# Micro architecture 
# Register: 
The smallest and fastest storage in the computer (typically 8 to 64 bits are stored here). 
# AX/BX/…: 
Data registers - stores variables, arguments, return values, etc). 
# SP (Stack Pointer): 
Contains the address to the top of the stack. 
# BP (Base Pointer/Frame Pointer): 
Contains the address to the bottom of the current stack frame (the stack is divided into stack frames, a stack frame is created when you execute a function call and it is deleted when you return from function). 
# IP/PC (Instruction Pointer/Program Counter): 
Contains the address to the next instruction to be loaded from memory and executed. 
# IR (Instruction Register): 
Contains the instruction that will be executed by the ALU. 
# FLAG/PSW (Flag Register/Program Status Word): 
Contains control/status information. Two examples: 1. one bit contains the result from a comparison instruction (”were the contents of two registers equal or not?”) if such an instruction has just been executed by the ALU, 2. two different bits indicate if the running program is running in user mode or kernel mode). 
# Memory/RAM Random Access Memory: 
The main memory of the computer. Programs are loaded into memory and they contain instructions and data. Everything is stored as bits (a bit is zero or one) in memory, and eight bits is called a Byte. A Byte is the smallest piece we can load from memory: every address into memory goes to a Byte, NOT a bit. 
# Address 
# Interrupt handler/routine 
# Stack/push/pop 
# Context switch 
# Assembly directive/label 
# Clock-speed/frequency/period 
# Hz 
# Pipeline 
# Micro-operations 
# Out-of-order execution
# Branch prediction 
# Superscalar 
# SMT/hyperthreading 
Is when a CPU runs two separate programs/processes at the same time so it is possible to change between them. But it does not mean that it can do arithmetic operations faster. 
# Von Neumann-bottle neck 
# Spatial/temporal locality 
# Cache line 
# Write through/back cache 
# Speculative Execution 
The CPU will try to guess the outcome of instructions and reverse if wrong. Using this will improve performance. Received attention in 2018 due to vulnerabilities, Spectre and Meltdown.