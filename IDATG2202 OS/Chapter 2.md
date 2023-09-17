# Process 
A process is a program that has been loaded onto the memory. 
# Process API 
The Process API lets you start, retrieve information about, and manage native operating system processes. 
# Thread/Multi-threaded 
# Process States (Ready/Running/Blocked) 
A process can have three states: - **Running**: In the running state, a process is running on a processor. This means it is executing instructions. • **Ready**: In the ready state, a process is ready to run but for some reason the OS has chosen not to run it at this given moment. - **Blocked**: In the blocked state, a process has performed some kind of operation that makes it not ready to run until some other event takes place. A common example: when a process initiates an I/O request to a disk, it becomes blocked and thus some other process can use the processor. 
# PCB (Process Control Block) 
Stores all information about a process. Is used in context switching. 
# Process List/Table 
A list of all started processes. They can be running or blocked/sleeping. 
# Address Space 
Is a range of virtual addresses the OS allocates to a running program. 
# File 
An abstraction of data stored on a physical storage unit (HDD, SSD etc.). 
# Design Goals 
The design goals of a operating system is: 
- **Virtualization** 
- Create abstractions 
- **Performance** 
- Minimize overhead 
- **Security** 
- Protect/isolate applications 
- **Reliability** 
- Stability 
- **Energy-efficient** 
- Environment Friendly 
# Timesharing 
Is a technique use by an OS to share resources. The OS uses a ***context switch*** to stop a running program and start another on a given CPU. 
# Batch 
Batch processes do not have I/O. 
# Soft/Hard Real-Time Real-time 
computing is used to describe a computer system that reacts to events by performing tasks within a specific time interval. The time frame for these actions to be carried out is in the order of milliseconds. Meeting these specific time intervals are key to the effectiveness of real-time systems. If a real-time system fails to carry out actions in time, it can result in the system being inadequate or useless. *Hard real-time* systems have strict deadlines where it is critical that each action takes place inside the specified time frame, otherwise, there will be a system failure, which could result in damaging property or endangering life (ex. robotics). *Soft real-time* systems are not as strict as the system will not fail and the result of a task may still be useful (ex. multimedia). 
# Service/User Process 
**Service processes** run without needed a user to be logged in. 
# CPU/IO/Memory-Bound Processes 
**CPU-bound**: Scientific computing, machine learning, multimedia. (Hyperthreading does not help CPU-bound processes). **I/O-bound**: Waiting for I/O. **Memory-bound**: Heavy use of memory (often also CPU-bound). 
# GNU 
# POSIX 
# Bit/Byte 
# KB/MB/GB/TB/PB/EB 
# ms/us/ns 
Milli-, micro and nano seconds are speeds of different processes that happen in a computer. 
# GCC (GNU Compiler Collection)