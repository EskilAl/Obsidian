# Process-ID-PID
Each process has a name; in most systems, that name is a number known as a **process ID (PID)**.

# Fork
The `fork()` system call is used in Unix systems to create a new process. The creator is called the **parent**; the newly created process is called the **child**. As sometime occurs in real life, the child process is a nearly identical copy of the parent.

# Wait
The `wait()` system call allows a parent to wait for its child to complete execution. 

# Exec
The `exec()` system call allows a child to break free from its similarity to its parent and execute an entirely new program.

# Signal
Process control is available in the form of **signals**, which can cause jobs to stop, continue, or even terminate.

# User-mode
The CPU should support at least two modes of execution: a restricted user mode and a privilege (non-restricted) kernel mode.

# Kernel-mode 
The CPU should support at least two modes of execution: a restricted **user mode** and a privilege (non-restricted) **kernel mode.**

# Software-Exception-Hardware-Interrupt
Typical user application run in user mode, and use a **system call** to **trap** into the kernel to request operating system services.

# Trap-table-interrupt-vector-table
The trap instruction saves register state carefully, changes the hardware status to kernel mode, and jumps into the OS to a pre-specified destination: the **trap table.**
When the OS finishes servicing a system call. it returns to the user program via another special **return-from-trap** instruction, which reduces privileges and returns control to the instruction after the trap that jumped into the OS.

# Limited-Direct-Execution
The trap tables must be set up by the OS at boot time, and make sure that they cannot be readily modified by user programs. All of this is part of the **limited direct execution** protocol which runs programs efficiently but without loss of OS control.

# Timer-Interrupt
Once a program is running, the OS must use hardware mechanisms to ensure the user program does not run forever, namely the **Timer interrupt**. This approach is a **non-cooperative** approach to CPU scheduling. 

# Mode-Switch-Transition
Sometimes the OS, during a timer interrupt or system call, might wish to switch from running the current process to a different one, a low-level technique know as a **context switch.

# API 
Application program interface. 

