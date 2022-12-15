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

Two sample programs are given as part of the repository: `./sample-programs/guess.clite` and `demo.clite`. Try running them to get a feel for the type of programs you can make!

Note, there is no syntax error detection. The interpreter
assumes the program is syntactically correct.

The syntax is similar to C. The only variable data type is int.
Lines are terminated with a new line, not ";"

Control structures if and while are terminated with "end"
keyword. Programs are terminated with the "exit" keyword.

Supported structures:
  receiving input with "in" keyword
  "if" and "while"
  any number of lines
  any variable name starting with a character
  printing strings with "out" keyword with at most one \n
  five arithmetic operations (+ - * / %)
  six conditionals (==, !=, <, >, <=, >=)
  white space is ignored

Examples of the syntax are given in test.clite and guess.clite.

test.clite: comprised of four demonstrative sections
  line  1: Fibonacci section - demonstrates while
  line 17: Division section - demonstrates input
  line 28: Odd section - shows % and "if" inside of while
  line 41: Multiplication section - demonstrates nested while

guess.clite: real world program example. guesses a users
  positive number using exponentiation.
