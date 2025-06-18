# Custom Compiler Project

A robust compiler implementation that translates a custom programming language into x86-64 assembly code. This project demonstrates the fundamental components of compiler design, including lexical analysis, parsing, and code generation.

## Project Overview

This compiler is designed to process source code written in a custom language (`.unn` files) and generate executable programs. It follows the traditional compiler pipeline:

1. **Lexical Analysis**: Breaks down source code into tokens
2. **Parsing**: Converts tokens into an Abstract Syntax Tree (AST)
3. **Code Generation**: Transforms the AST into x86-64 assembly code
4. **Assembly & Linking**: Converts assembly to an executable

## Features

- **Lexical Analysis**
  - Token types: INT, KEYWORD, SEPARATOR, OPERATOR, IDENTIFIER, STRING, COMP
  - Line number tracking for error reporting
  - Support for various operators and separators

- **Parser**
  - Abstract Syntax Tree (AST) generation
  - Syntax error detection
  - Support for complex expressions and statements

- **Code Generator**
  - x86-64 assembly output
  - NASM-compatible assembly code generation
  - Integration with GCC for final executable creation

## Prerequisites

- GCC (GNU Compiler Collection)
- NASM (Netwide Assembler)
- Make (optional, for building)

## Installation

1. Clone the repository:
```bash
git clone [repository-url]
cd compiler
```

2. Compile the project:
```bash
gcc -o compiler main.c lexer.c parser.c codegenerator.c -I.
```

## Usage

To compile a source file:

```bash
./compiler input.unn output_name
```

This will:
1. Read the source file `input.unn`
2. Generate assembly code
3. Create an executable named `output_name`

### Example

```bash
./compiler program.unn myprogram
```

This will create an executable named `myprogram` from the source file `program.unn`.

## Project Structure

- `main.c`: Entry point and program flow control
- `lexer.h/c`: Lexical analysis implementation
- `parser.h/c`: Parser implementation
- `codegenerator.h/c`: Assembly code generation
- `hashmap/`: Supporting data structures

## Development

### Building from Source

1. Compile the project:
```bash
gcc -o compiler main.c lexer.c parser.c codegenerator.c -I.
```

2. Run tests:
```bash
./compiler test.unn test_program
```

### Adding New Features

1. Lexical Analysis: Add new token types in `lexer.h`
2. Parser: Extend grammar rules in `parser.c`
3. Code Generation: Add new instruction patterns in `codegenerator.c`

## Contributing

1. Fork the repository
2. Create a feature branch
3. Commit your changes
4. Push to the branch
5. Create a Pull Request

## License

Apache 2.0

## Authors

Isaac Pemberton

## Acknowledgments

- NASM for assembly support
- GCC for linking and optimization 
