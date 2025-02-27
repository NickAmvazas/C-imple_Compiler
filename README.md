# C-imple_Compiler
C-imple: A Custom Language for Compiler Design 

## Project Overview
C-imple is a custom language designed to demonstrate the key concepts of compiler design. The project was divided into three phases, each focusing on a specific aspect of the compilation process:
1. Lexical and Syntax Analysis:__ Tokenization and parsing of the source code.

2. __Intermediate Code Generation:__ Production of intermediate code (quads) and equivalent C code.

3. __Symbol Table and Final Code Generation:__ Management of the symbol table and generation of assembly code.

The project was implemented in __Python 3.8__ and uses a recursive descent parser for syntax analysis. The final output is assembly code that can be assembled using __MARS 4.5__.

## Phases of the Project
#### 1. First Phase: Lexical and Syntax Analysis

- __Lexical Analysis:__ The __lex()__ function reads the source code character by character and generates tokens. These tokens are stored in a list and passed to the syntax analyzer.

- __Syntax Analysis:__ The syntax analyzer uses a recursive descent approach to validate the structure of the source code based on the grammar of C-imple. It ensures the code adheres to the language's rules.

#### 2. Second Phase: Intermediate Code Generation
- __Intermediate Code:__ The source code is translated into intermediate code represented as __quads__ (four-tuples). Each quad consists of an operator and three operands.

- __C Code Generation:__ If the source code does not contain functions or procedures, an equivalent C program is generated.

#### 3. Third Phase: Symbol Table and Final Code Generation
- __Symbol Table:__ A dynamic symbol table is maintained to store information about variables, functions, and procedures. It grows and shrinks as the code is translated.
- __Final Code Generation:__ The intermediate code is translated into assembly language, ready to be assembled using __MARS 4.5__.

## How It Works
1. The program reads the source code file (e.g., __text.ci__).

2. The lexical analyzer (__lex()__) generates tokens, which are passed to the syntax analyzer.

3. The syntax analyzer validates the structure of the code and generates intermediate code (quads).

4. The intermediate code is used to produce:

  - An intermediate code file (e.g., __text.int__).

  - An equivalent C program (if no functions are present) (e.g., __text.c__).

  - A symbol table and final assembly code (e.g., __text.asm__).

## Run 
python3 cimple_compiler.py _[file]_.ci

The output will include:

- Intermediate code (_[file]_.int).

- Equivalent C code (_[file]_.c, if applicable).

- Assembly code (_[file]_.asm).
