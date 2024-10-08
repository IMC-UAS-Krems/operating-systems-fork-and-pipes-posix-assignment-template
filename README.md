[![Open in Visual Studio Code](https://classroom.github.com/assets/open-in-vscode-2e0aaae1b6195c2367325f4f02e2d04e9abb55f0b24a779b69b11b9e10269abc.svg)](https://classroom.github.com/online_ide?assignment_repo_id=15903087&assignment_repo_type=AssignmentRepo)

# Operating Systems

## Assignment 2: Fork and pipes

In this assignment, the goal is to learn how parent and child processes can communicate via pipes. Please refer to the `os_examples` repository for example code.

Write a C program that implements the following behaviour:

- The program will be started with a single command-line parameter, which should be a positive integer. The program will make sure that the program only accepts exactly one argument and that this argument is a positive integer. If not, it will output the message `Wrong usage`.
- The parent process will then start, create a pipe and a child process.
- The child process will create a string containing the decimal expression of pi with the precision given via command-line parameter (maximum 30).
- The child process will send that string using the pipe to the parent process. It will then terminate.
- The parent process will read each digit from the pipe. For each digit, it will output that digit to the console and terminate.

Example input: ``./posix_assignment 6``

Example output: ``3.141593``

Example input: ``./posix_assignment 2``

Example output: ``3.14``

Example input: ``./posix_assignment 0``

Example output: ``Wrong usage``

Example input: ``./posix_assignment bananas``

Example output: ``Wrong usage``

