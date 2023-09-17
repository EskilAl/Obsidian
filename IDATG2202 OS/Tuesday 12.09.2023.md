
# System calls

# OS

| Steps                             |                                 |
| --------------------------------- | ------------------------------- |
| **OS**                            |**Program**                            |
| 1. Create entry for process list. |                                 |
| 2. Allocate memory for program.   |                                 |
| 3. Load program into memory.      |                                 |
| 4. Set up Stack with argc / argv. |                                 |
| 5. Clear registers.               |                                 |
| 6. Execute call main().           |                                 |
|      | 7. Run Main()                   |
|      | 8. Execute **return** from main |
| **Cleanup**                       |                                 |
| 9. Free memory of process.        |                                 |
| 10. Remove from process list.                                   |                                 |
Missing a part where the program gives away access back to the OS.

## What does a normal software (in user mode) not have access to?
- Read from I/O unit.
- Write to I/O unit.
- control instructions. 

## When does the operating system run on the CPU
- Hardware-) timer interrupt.
- press a button on keyboard (IO)
- mouse click. (IO)
- process access memory illegally.
- save file in word.
- Process that quits.

## What does it mean with Synchronic vs asynchrony interrupt
Synchronic interrupt is (Hardware-) timer interrupt. asynchrony interrupt er software interrupt, interrupt from processes or from I/O.

## Some tasks are done by user mode process (computer software), some are done by the operating system and some is done directly in the computer architecture. what?

### Boot
|OS @ Boot|Hardware|Mode|
|---|---|---|
|Initialize trap table|-|Kernel|
|Remember address of syscall handler|-|Kernel|
||||
|OS @ Run|Hardware|Program|
|(Kernel Mode)|(User Mode)|(User Mode)|
|Create entry for process list|-|Kernel|
|Allocate memory for program|-|Kernel|
|Load program into memory|-|Kernel|
|Setup user stack with argv|-|Kernel|
|Fill kernel stack with reg/PC|-|Kernel|
|return-from-trap|-|Kernel|
|restore regs (from kernel stack)|-|Kernel|
|move to user mode|-|Kernel|
|jump to main|-|Kernel|
||-||
|Run main()|-|User|
|...|-|User|
|Call system call|-|User|
|trap into OS|-|Kernel|
|save regs (to kernel stack)|-|Kernel|
|move to kernel mode|-|Kernel|
|jump to trap handler|-|Kernel|
|Handle trap|-|Kernel|
|Do work of syscall|-|Kernel|
|return-from-trap|-|Kernel|
|restore regs (from kernel stack)|-|Kernel|
|move to user mode|-|Kernel|
|jump to PC after trap|-|Kernel|
|...|-|User|
|return from main|-|User|
|trap (via exit())|-|Kernel|
|Free memory of process|-|Kernel|
|Remove from process list|-|Kernel|

This table outlines the various steps the OS takes during boot and program execution, specifying the relevant hardware and mode for each step.

