# Banker's Algorithm Implementation

## Description
This repository contains a C++ implementation of the Banker's Algorithm, a resource allocation and deadlock avoidance algorithm used in operating systems. The algorithm is designed to prevent deadlocks by determining whether allocating a resource to a process will lead to an unsafe state.

## What I Learned
- **Deadlock Avoidance**: How operating systems can proactively prevent deadlocks by carefully managing resource allocation
- **Safety Algorithm**: How to determine if a system is in a safe state where all processes can complete
- **Resource Allocation Management**: Techniques for tracking and managing resources in a multi-process environment
- **State Space Analysis**: Analyzing different allocation states to prevent system deadlocks
- **Matrix Operations**: Using matrices to represent and manipulate resource allocation states

## Prerequisites
- Ubuntu Linux (or any Linux distribution)
- g++ compiler
- Basic knowledge of terminal commands

## Compilation and Execution

### To compile the program:
```bash
g++ "Banker's algorithm.cpp" -o banker
```

### To run the program:
```bash
./banker
```

## Program Usage
When running the program, you'll be prompted to:

1. Enter the number of processes (m)
2. Enter the number of resource types (n)
3. Input the Maximum Resource Matrix
4. Input the Allocation Matrix
5. Input the Available Resources Vector

The program will then:
1. Calculate if the current state is safe
2. Display a safe sequence if one exists
3. Allow you to make resource requests for processes
4. Determine if those requests can be granted while maintaining system safety

## Example Input
```
m: 5
n: 3
Max Matrix: 
7 5 3
3 2 2
9 0 2
2 2 2
4 3 3
Allocation Matrix:
0 1 0
2 0 0
3 0 2
2 1 1
0 0 2
Available Vector:
3 3 2
```

## Key Components of the Algorithm
- **Available**: Vector showing available resources
- **Max**: Matrix defining maximum demand of each process
- **Allocation**: Matrix showing resources currently allocated
- **Need**: Matrix indicating remaining resource needs
- **Request**: Matrix for resources requested by each process
- **Safe Sequence**: Sequence of processes that can complete without deadlock

## Contributing
Feel free to submit issues or pull requests to improve this implementation.