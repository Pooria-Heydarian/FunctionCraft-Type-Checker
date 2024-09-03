# FunctionCraft-Type-Checker

Welcome to the **FunctionCraft Type Checker** project, developed as part of a Compiler Design course. This project focuses on creating a robust type checker for a functional programming language, ensuring that all operations and function calls within the language are semantically correct and free of type errors.

## Features

- **Type Checking**: Implements a comprehensive type checking mechanism that validates the types of operands, function arguments, and iterables.
- **Error Handling**: Identifies and reports various semantic errors, such as mismatched operand types, incorrect function argument types, and non-iterable loops.
- **AST Traversal**: Leverages the Visitor design pattern to effectively traverse and analyze abstract syntax trees (ASTs), ensuring accurate type inference.
- **Symbol Table Management**: Implements a symbol table to manage variable and function scope, aiding in accurate type checking during the compilation process.

## Project Structure

The project is organized into several key components:

- **AST Nodes**: Classes representing different elements of the language's abstract syntax tree.
- **Type Checker**: Core logic for type inference and validation, ensuring the program's semantic correctness.
- **Symbol Table**: Manages the scopes and bindings of identifiers, facilitating accurate variable and function resolution.
- **Parsers**: Generated from ANTLR grammar files, these parsers interpret the custom language syntax and generate the corresponding AST.
- **Utilities**: Includes additional tools such as the ANTLR jar, necessary for generating the parsers.

## Type Inference Errors

The type checker is capable of detecting the following types of errors:

1. **NonSameOperands**: Ensures that the operands of an operation are of the same type.
2. **IsNotIterable**: Validates that only iterable types (e.g., lists, ranges) are used in `for` loops.
3. **ChopArgumentTypeMisMatch**: Ensures that the `chop` function is only applied to strings.
4. **RangeValuesMisMatch**: Verifies that only integer values are used as range bounds.
5. **AppendArgumentsTypeMisMatch**: Checks that elements being appended to a list match the type of the list's existing elements.


