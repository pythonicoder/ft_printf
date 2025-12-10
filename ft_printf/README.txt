This project has been created as part of the 42 curriculum by [skasikci].

ft_printf

Description

ft_printf is a custom implementation of the C standard printf function.
The goal of the project is to recreate formatted output functionality by
supporting several format specifiers, managing variadic arguments, and
producing clean, modular, standard-compliant C code.

This project reinforces understanding of: - Variadic functions
- String and number formatting
- Pointer manipulation
- Clean algorithmic design and modular architecture

Instructions

Compilation

Compile the project using the provided Makefile: make

This will generate: libftprintf.a

Other rules: make # build the library make clean # remove object files
make fclean # remove object files and library make re # rebuild
everything

Usage

Include the header: #include “ft_printf.h”

Compile your program with the library: gcc your_program.c libftprintf.a
-I.

Use ft_printf just like the standard function: ft_printf(“Hello %s,
number: %d”, “World”, 42);

Supported Conversions

-   %c — Character
-   %s — String
-   %p — Pointer address
-   %d / %i — Signed integer
-   %u — Unsigned integer
-   %x / %X — Hexadecimal
-   %% — Percent sign

Algorithm & Data Structure Explanation

Parsing Algorithm

The format string is processed sequentially:

1.  Iterate through characters.
2.  When a ‘%’ is found, identify the next character as a format
    specifier.
3.  Retrieve the corresponding argument using va_arg.
4.  Convert the argument to a printable string (decimal, unsigned, hex,
    pointer).
5.  Write the formatted output to standard output.
6.  Increase the printed character count.

Data Structures

The project uses: - Primitive C types (int, unsigned int, char *,
pointers) - va_list for variadic argument handling - Helper functions -
Small internal buffers for number conversion

Resources

Documentation & References

-   man printf
-   C variadic functions documentation
-   Articles on number/base conversions
