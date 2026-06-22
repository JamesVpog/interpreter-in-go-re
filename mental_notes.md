# Mental Notes

things that I found while reading that doesn't quite fit into a comment in the Monkey source code

## Introduction

all interpreters take source code and evaluate it without producing a visible, intermediate result
that can be later executed

in contrast, compilers take source code and produce something the underlying machine can understand (compiled binary)

interpreters vary from just interpreting input (like Brainfuck) or having advanced parsing/compiling techniques
like JIT (just-in-time) interpreters which compile source code just-in-time into native machine code to exec

in between simple and complex interpreters is the "Tree-walking" interpreter which creates an 
AST (abstract syntax tree) from the source code. It walks the AST and interprets it

the Monkey Interpreter will be made of 5 parts:

- Lexer
- Parser
- AST 
- Internal Object System
- Evaluator

the book requires to use Go >= 1.13
