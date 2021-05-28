# Design

## Why

In 2017 I was writing homebrew software for the Playstation Portable.
I really like the "core" features that C# 2.0 provide, but a language like C# is too heavy to run with enough headroom on a low-end device like the Playstation Portable.
Even if it is possible, porting it would be a nightmare.
There are many high-level languages with advanced features such as garbage collection, exceptions, massive build-in standard libraries and whatnot.
However, only a handful of them allow for explicit memory control, even less have intuitive syntax and none that I know of can run on embedded hardware.
Since I couldn't find anything that need, I decided to design my own language.

## Goal

The goal of this language is to be a high-level variant of C; concise, simplistic, performant, portable, object-oriented, and can be transpiled back to C.

## Syntax

Most of it's syntax is heavily influenced by C# 2.0, memory management is loosely based on C++98 and some of the other syntax is inspired by Java.

## Concept

### Minimalism

The language is designed first and foremost to work on low-end hardware with tight constraints (such as a Playstation Portable).
This means that features such as garbage collection, exceptions are not viable to provide.
Providing a large standard library isn't a good idea as more specialized programmer can come up with better solutions than what I could provide.

### Object-oriented

I decided to make the language object-oriented instead of using imperative programming as it allows for easier creation of custom types.
However, there is a catch; inheritance, polymorphism, (up/down)casting and properties are not included.
The generic type system and interfaces closely resembles C# 2.0's implementation to promote composite programming and flat hierarchy structures.

### Freedom

Access modifiers have been removed to remove needless state, it always annoyed me that I couldn't access private members that should've been made public in the library.
Instead of forcing a garbage collector, the language provides only manual memory manamgement so a programmer can manage memory when it's required or use a third-party garbage collector library.

### Consistency

Operator/cast overloading and a custom constructor allows a programmer to create custom types that are tightly intergrated into the language.
Decimal literals have been removed in favor for explicit type casting of decimal literals.
