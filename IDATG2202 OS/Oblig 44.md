### 1. 100% CPU-intensive process (does computations continously) uses five minutes to complete on a dual-core CPU with hyperthreading. If we start four such processes on the same system, how much time would pass before they all complete?

### 2. How does a modern operating system make it possible to run multiple processes "simultaneously" (at the same time) on a CPU?
### 3. How long does a clock cycle (clock period) last on a 3 GHz CPU?

### 4. If ~/bin is in the environment variable PATH, it means that:
### 5. The assembly code (AT&T/GNU syntax)  mov -4(%rbp), %eax  does the following:
### 6. The relationship between commands, system calls and instructions is: 
### 7. What is it called when a write operation is not completed until data has been written to both cache and internal memory?
### 8.  What will be printed on the screen (in the terminal window) by the following program (given that it does not fail in any way)?
```
main ()  {  
   int p;  
   p = fork();  
   if(p==0) {  
       printf("Child!");  
       exec("/usr/bin/gedit")  
   }  
   printf("Parent!");  
   return 0;  
}
```
### 9. Which instructions can be executed in user mode?
### 10.  Why can't the operating system (OS) execute a normal sequential process (e.g. a standard C program you have written without any use of fork) in parallel on a dualcore CPU?
### 11. A Minor Page Fault occurs if the page being accessed:
### 12. A page frame is located in:
### 13. How many pages do you have in a 32-bit (single-level) address space with page size 4KB?
### 14. Processes X and Y arrive at time 0, while process Z arrive 3ms later. They all need 3ms of CPU time. They execute on the CPU according to First In First Out (FIFO):
### 15. Processes X and Y arrive at time 0, while process Z arrive 3ms later. They all need 3ms of CPU time. They execute on the CPU according to First In First Out (FIFO): CPU:   X X X Y Y Y Z Z Z  Time: 0 1 2 3 4 5 6 7 8 9 (in other words, they have all completed execution after 9ms has passed). What is the average turnaround time?
### 16. Processes X and Y arrive at time 0, while process Z arrive 3ms later. They all need 3ms of CPU time. They execute on the CPU according to First In First Out (FIFO):CPU:   X X X Y Y Y Z Z Z   Time: 0 1 2 3 4 5 6 7 8 9 (in other words, they have all completed execution after 9ms has passed). What is the average response time?
### 17. The purpose of the Translation Lookaside Buffer (TLB) is:
### 18.  The term _Working Set_ describes:
### 19. What is the typical size of a time slice (time quantum) when using round-robin scheduling?
### 20. When we have scheduling with a Multi-Level Feedback Queue with four queues Q3, Q2, Q1 and Q0 (Q3 is the highest priority) and the following situation:

- time slice is 7ms
- at time 0 process P0 arrives and 1ms later process P1 arrives
- P0 does I/O every 3ms and the I/O takes 2ms
- P1 only wants to use the CPU as much as possible and does not do any I/O

In which queue is P1 after 11ms has passed since time 0?
### 21. With 64KB page size, what is the virtual page number (VPN) in the virtual address  0x8E554C ?
### 22. A _barrier_ is a synchronization primitive from pthread that:
### 23. A mutex lock is a variable that:
### 24. A race condition is when:
### 25. The most important property of the machine instruction XCHG is:
### 26. What is _memory-mapped I/O_?
### 27.
### 28. 
### 29.
### 30. 
