# Week 1
1. What is a "Directive" in assembly code?
   - it's an instruction but in assembly. 

2. Briefly explain the concepts *super scalar and pipeline*. 
   - in order for the CPU to work as efficiently as possible we get take the instruction an make it like a assembly line, this we call a pipeline, and a scalar is a unit that executes the instructions in the pipeline, if we have a super scalar it means that we have more than one scalar, and it can execute more instructions simultaneous.    

3. What does a C-compiler like gcc do? What is the difference between C-code, assembly code and machine code?
   - gcc performs the compilation step to build a program, and then it calls other programs to assemble the program and to link the program's component parts into an executable program that you can run.
   - it takes the code and compiles so i can run on the selected operating system, the differences is the deferent language models, c is using assembly code that uses machine code, so we are able to read the code to understand what the machine does,     

4. (KEY PROBLEM) Based on the examples of C-code and assembly code we have covered in this chapter, explain what each line in the following assembly code does:
    01 .text   -> tells the assembler to switch to text segment 
	02 .globl main -> tells the assembler the linker beacuse the object files will use it 
	03 main: -> represent the entry point of the program. where the CPU will begin and execute instructions 
	04 pushq %rbp -> Save the current value %rbp on the stack
	05 movq %rsp, %rbp -> Copies the %rbp to the %rsp 
	06 movl $0, -4(%rbp) ->moving the immediate value 0 into the memory location that is 4 bytes offset from the %rbp 
	07 jmp .L2 -> jumpes to .L2 in the code(mby  if)
	08 .L3: -> a label in memory that the assembler can jump to  
	09 addl $1, -4(%rbp) -> adds 1 to the 0 in memory 
	10 addl $1, -4(%rbp) -> adds 1 to the 1 in memory
	11 .L2: -> label in memory so we can jump to it
	12 cmpl $9, -4(%rbp) -> sees if the variable in -4 is 9 if not it goes next
	13 jle .L3 -> jumpes to L3 if its less or eqiual than 9
	14 movl $0, %eax -> set's the eax register to 0 
	15 popq %rbp -> restores the original value of the %rbp 
	16 ret -> returns from the function 
	````
	assembly
	01 .text
	02 .globl main
	03 main:
	04 pushq %rbp       ; Prologue: Save the current value of %rbp on the stack
	05 movq %rsp, %rbp  ; Set %rsp as the new value of %rbp
	06 movl $0, -4(%rbp) ; Initialize a local variable to 0
	07 jmp .L2          ; Jump to label .L2

	08 .L3:
	09 addl $1, -4(%rbp) ; Increment the local variable by 1
	10 addl $1, -4(%rbp) ; Increment the local variable by 1 again

	11 .L2:
	12 cmpl $9, -4(%rbp) ; Compare the local variable with 9
	13 jle .L3           ; Jump to label .L3 if less than or equal to 9

	14 movl $0, %eax     ; Set the return value to 0 (returning an integer)
	15 popq %rbp         ; Epilogue: Restore the original value of %rbp
	16 ret               ; Return from the function
```
