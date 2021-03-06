# Concurrent-MIPS-Simulator

Achieving parallelization in mips code using c++ concurrency features The project aims at implementing a subset of MIPS simulator. 

Which would focus on two aspects :- 

1.Finding the section of code that can be parallelized and running it concurrently using threads. 

2.The c++ code will also find whether a loop can be parallelized. If yes then each iteration would run on different thread.

3.Syntax error handling (run time errors detection).



Compile code using

g++ -std=c++11 GROUP11.cpp -lpthread.



Description:-

A C++ code which will read a MIPS assembly code from a file and will find the set of instructions (in vicinity) which can be run in parallel.

eg.

If the sequential code is following 

add $t0 $t1 $t2 
mul $t3 $t1 $t2 
lw $s1 0($t1)

Three treads can run concurrently on the above 3 instructions.

The c++ code will also find whether a loop can be parallelized. If yes then each iteration would run on different thread.

As of now, we have thought of following MIPS instructions to implement:-

Arithmetic: add, addi, sub, mul

Logic: and, andi, or, ori, nor

Comparison: slt, slti

Load/Store: lw, sw

Control flow: beq, bne, j

halt (to stop the execution)
