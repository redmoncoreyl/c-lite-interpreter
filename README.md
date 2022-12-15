# C-Lite Interpreter
This project implements an interpreter for an invented language called C-Lite. An interpreter reads a program line by line and executes the instruction (as opposed to a comiler which translates a program into instructions which a computer can more quickly process).

## Getting started
To get started, use this command to compile the interpreter:

```
g++ CLiteInterpreter.cpp -o clite
```

Then, to run a C-Lite program use the following command:

```
[executable] [c_lite_program_file]
```

Two sample programs are given as part of the repository: `./sample-programs/demo.clite` and `sample-programs/numberGuesser.clite`. Try running them and inspecting their source code to get a feel for the type of programs you can make!

## Supported features
C-Lite supports the following features:
- one data type: integer
- any variable name starting with `[a-zA-Z]`
- receiving input with the `in` keyword
- printing strings with `out` keyword
- `if` and `while` control structures
- five arithmetic operations (+ - * / %)
- six conditionals (==, !=, <, >, <=, >=)

Note, there is no syntax error detection. The interpreter
assumes the program is syntactically correct.

Control structures if and while are terminated with "end"
keyword. Programs are terminated with the "exit" keyword.

Examples of the syntax are given in test.clite and guess.clite.

test.clite: comprised of four demonstrative sections
  line  1: Fibonacci section - demonstrates while
  line 17: Division section - demonstrates input
  line 28: Odd section - shows % and "if" inside of while
  line 41: Multiplication section - demonstrates nested while

guess.clite: real world program example. guesses a users
  positive number using exponentiation.
