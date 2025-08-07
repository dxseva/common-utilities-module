# common-utilities-module
Common Utilities Module (common.c / common.h)

This module provides a set of utility functions for dynamic memory management and string array handling in C. It simplifies error handling and improves memory allocation safety by wrapping standard C library functions with additional checks and behavior.

    Safe memory allocation with error checking:
        s21_calloc(size_t size) — Allocates zero-initialized memory, exits with an error message if allocation fails.
        s21_realloc(void *memblock, size_t size) — Reallocates memory with error handling.
    Custom error printing:
        s21_print_error(const char *pname, const char *str) — Outputs a formatted error message to stderr.
    String array management:
        s21_push_to_string_array(char ***array, const char *element, int *num) — Dynamically adds a copy of a string to a resizable array of strings.
        s21_pull_from_string_array(char ***array, int *num) — Removes the first element from the string array and returns a copy of it. Shifts the rest of the elements to maintain order.
        
Files
    common.c — Contains the implementation of the utility functions.
    common.h — Header file that declares the utility function interfaces.
    
Use Case
These utilities are especially useful in C projects where:
    You need dynamic string arrays without using external libraries.
    You want safer and more readable memory management code.
    You prefer consistent error handling through centralized logging and termination.
