# What Is a Compiler

At its core, a compiler is a translator. We usually think of them as translating between a human-readable language and machine code. Still, this label applies to any translation, including transpilers like Typescript, which translates into Javascript.

## How Compilers Work

Compilers move code through several passes to switch from one language to another. These passes have various uses, and a single pass may cover more than one use.

- **Lexical Analysis**: This step takes the original code and chunks it into tokens for the rest of the process.
- **Syntax Analysis/Parsing**: Create a structured representation of what the code tries to do.
- **Semantic Analyzer**: Tries to determine whether or not the program is valid.
- **Code Generation**: Create code in either an intermediate or the target language.
- **Code Optimization**: Make adjustments to the process to make it more efficient.

## Types of Programming Languages

- **Compiled Languages**: Languages that are usually translated directly into a target language or machine code by the compiler. (C, Typescript, Rust)
- **Interpreted Languages**: Languages executed directly rather than compiled. (Python, Ruby, sometimes JavaScript)
- **Just-in-Time Compilation**: A program that acts like an interpreted language but is compiled. The program is compiled at execution time. Sometimes, they are partially compiled ahead of time into an interim language. (Java, C#, JavaScript V8 engine/Node)

## Picking a Language

- **Speed**: Languages compiled into machine code are almost always significantly faster than other types. JIT languages usually outperform fully interpreted ones.
- **Reliability**: One of the most significant benefits of using a compiler is its ability to do type-checking and similar verification tasks. Given identical QA processes, compiled languages will usually have fewer bugs. In contrast, interpreted languages are sometimes easier to debug, but modern tools have closed this gap.
- **Flexibility**: Languages compiling into machine code must target a specific type of hardware architecture. In interpreted languages, the interpreter handles the hardware layer, so it's possible to distribute the same software regardless of operating system or hardware specs.
