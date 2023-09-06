# Cool resources about PL and Compilers
### Tufts CS107

A collection of the state of the art from throughout computer history.

**This is a living document**
In a fully democratic fashion, please delete or add anything you wish via PR.
Add yourself as a contributors if you do!
[Make a PR](https://github.com/jzimmerman135/CS107-resources)

Contributors: 
- Jacob Zimmerman (2023)
- Ronit Singh (2023)

\*\* opinion

------------

# Compiled languages we like

#### Rust 
(imperative) 2016

- "Borrow checker" semantics associate a lifetime with a chunk of memory, this guarantees at compile time that pointers are valid.
- Trait system for polymorphism
- Like C++ without segfaults
- A fantastic, practical language \*\*

#### Haskell 
(pure functional) 1992

- Pure functions allow compile time correctness guarantees

#### Vale 
(imperative) 2020

- Generational indices for fast reference counting (automatic memory management)

#### Scheme
(functional s-exp) 1972

- Compiled using continuation passing style
- Features the most powerful control flow primitive in all programming `(call/cc ...)` \*\*

#### Idris 
(pure functional) 2020s

- First class types! Extends type inference for types to have values, `typeof append = Vec n -> Vec (n + 1)` 
- Printf is a well-typed operation!

#### Racket 

(functional s-exp) 1990s

- Code as data, meaning code can be passed as a value, leading to powerful meta programming
- Highly extendable syntax means you can create embedded languages in very little code

#### Go 

(imperative) 2007

- First class concurrency and concurrent data structures

#### CSS 

(declarative) 1996, *but only interesting post 2010*

- CSS belongs in this list to point out that languages don't need to be Turing complete to be *powerful*
- CSS *programs?* describe rules and relationships, and the runtime will figure out the rest
- You use pattern matching to tell the program **what** it should do rather than **how**, 
  which is always cool even if the program just calculates a webpage layout
- It is remarkably expressive, doesn't take much to do useful things

- Worth thinking about: is CSS *programming*? \*\*

--------

## Fascinating compiler stuff

#### Future of Programming 

[Presentation](https://www.youtube.com/watch?v=8pTEmbeENF4&t=2s) by Bret Victor (30 minutes)

- A **must watch** for those interested in PL, or really any CS student \*\*
- History and future of how we **collaborate** with computers

#### matt.might.net

[Blog by Matt Might](matt.might.net), a professor of PL at Univ Utah.

- Great blog to for a low level understanding of higher level language features
- Particularly good for Lisp-y features like syntax macros and lambda functions

#### Compiling with Continuations

[Textbook, available online](https://www.cambridge.org/core/books/compiling-with-continuations/7CA9C36DCE78AD82218E745F43A4E740) by Andrew Appel

- Helps lay out the continuation abstraction 
- In depth technique for compiling functional languages.
- A different way of representing compilation, conceptually very fascinating
- Uses Standard ML

#### Parsing With Zippers

[Paper](https://michaeldadams.org/papers/parsing-with-zippers/parsing-with-zippers.pdf)
and [presentation](https://www.youtube.com/watch?v=6Wi-Kc6LDhc) by Pierce Darragh and Michael Adams, 2021.

- Very creative and elegant parsing technique
- Full CFG parser generator in 81 lines of OCaml
- Paper won an functional pearl award (given to particularly beautiful functional algorithms)
- Fundamentally different to state machine (NFA) parsers like Yacc

#### Reflections on Trusting Trust 

[Turing award acceptance speech](https://www.win.tue.nl/~aeb/linux/hh/thompson/trust.html) by Ken Thompson, about early UNIX era.

- Legendary undetectable UNIX hack
- Adds a vulnerability by sneaking a secret backdoor into the **compiler's compiler**.

--------

## Computer Language History

There was a time early in computer history, when computers were rapidly growing in speed and capability, and researchers' questions outgrew the 
capabililty of the programming tools for their time.
With these new powerful machines nobody knew really what the best way "program" was. The following decades lead to immense creativity
and created many of the features we consider *advanced* even today.

Put yourself in the shoes of the pioneering men and women igniting the computer era,
unlearn what you consider "programming" to be,
and try to think how you would want to communicate with your computer

#### Assembly 
- Kathleen Booth, 1947
- Before this, people programmed in machine code

#### Fortran
- John Backus, 1958
- The first popular *high level* — at the time — language 
- Originally typed on punch cards
- Majority of the programs running on the most powerful supercomputers today is still written Fortran
- Highly imperative, similar to c

#### Lisp 
- John McCarthy, 1960
- First high-level language
- Garbage collected automatic memory management
- Dynamic typing
- Used to build the "Meta-circular Evaluator", which some call the greatest program ever written. A Lisp interpreter written in ~80 lines of Lisp.

#### Snobol
- David Farber, 1962
- Pattern matching control flow construct

#### C
- Brian Kernighan & Dennis Ritchie, 1972
- Most popular programming language of all time
- You probably know it

#### Prolog
- Alain Colmerauer, 1972
- Logic based programming, rather than imperative or functional
- Users input constraints in the form of facts and relationships, the runtime discovers solutions
- Simple, elegant syntax with a powerful runtime
- Highly declarative, you say **what you want** and the computer figures it out

#### Smalltalk
- Alan Kay, 1972
- Everything is an object — values, control flow, runtime, IDE, etc.
- Message passing interfaces for encapsulation
- Inheritance
