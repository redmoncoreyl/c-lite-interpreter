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

Two sample programs are given as part of the repository:
- `./sample-programs/demo.clite`
- `./sample-programs/numberGuesser.clite`.

Try running them and inspecting their source code to get a feel for the type of programs you can make!

## Supported features
C-Lite supports the following features:
- one data type: integer
- any variable name starting with `[a-zA-Z]`
- receiving input with the `in` keyword
- printing output with `out` keyword
- five arithmetic operations (+ - * / %)
- `if` and `while` control structures
- six conditionals (==, !=, <, >, <=, >=)

### Hello world program
You can print out messages using the `out` keyword:

```
out "Hello world\n"
exit

```

A valid C-Lite program must end with the `exit` command and a blank line.

### Variables
You can store integer data in variables:

```
variable = 5
out variable
exit

```

To store a value in a variable, make sure the command matches this regex:
```
[a-zA-Z][a-zA-Z0-9]+ = [1-9][0-9]+
```
More specifically, the equals sign must be surrounded by spaces and the variable must start with a letter.

### Receiving input
You can receive input from the user using the `in` keyword:

```
value = 0
out "Input your value: "
in value
out "Your value is: "
out value
exit

```

### Printing output
You have already seen printing output, but you should know, there are only two usages of `out`. Printing strings and priting a single variable:

```
value = 5
out "The value is: "
out value
exit

```

When printing a string, you may use a single new line at the end of the string:

```
out "After this is a new line\n"
exit

```

### Arithmetic operations
You can store the result of an arithmetic operation in a variable like this:

```
result = 5 + 1
out result
exit

```

There are five arithmetic operations: +, -, *, /, %.

Be sure to use the correct syntax. The only way to use arithmetic operations is with five space-separated tokens. The first token is a variable, the second token is an equals, the third is a number or variable, the fourth is one of the five operations, and the fifth is a number or variable.

### Control structures: if and while
You can control the flow of the program using `if`:

```
age = 0
out "Enter your age: "
in age
if age < 21
  out "You aren't old enough to drink :("
end
if age >= 21
  out "It's party time! :)"
end
exit

```

Sections inside `if` are terminated with `end`.

You can loop using `while`:

```
a = 1
while a < 20
  b = a % 2
  if b == 1
    out "odd: "
    out a
    out "\n"
  end
  a = a + 1
end
exit

```

Sections inside `while` are terminated with `end`. As you can see in this example, nested `if` and `while` are also supported.

### Conditionals
Six conditionals are supported: ==, !=, <, >, <=, >=. They are only supported in the condition section of `if` and `while`. Make sure the conditional operator is surrounded by spaces on either side.

## Currently not supported
Here are some of the feature that are currently not supported:
- for loops
- comments
- syntax error detection
- logical operators &, |, and ^
- new line characters arbitrarily located within print strings
- multiple data types
- complex expressions with more than one operator

## Sample programs
Two sample programs are given as part of the repository:
- `./sample-programs/demo.clite`
- `./sample-programs/numberGuesser.clite`.

`demo.clite`: comprised of four demonstrative sections:
- line  1: Fibonacci section - demonstrates while
- line 17: Division section - demonstrates input
- line 28: Odd section - shows % and "if" inside of while
- line 41: Multiplication section - demonstrates nested while

`guess.clite`: real world program example. guesses a users positive number using exponentiation.
