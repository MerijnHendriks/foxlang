# Frequently Asked Questions

## Language syntax

### Why is underscore (`_`) not allowed in the indentifier

It is reserved for the compiler to generate special identifiers to avoid name clashing (for example, method overloads)

### Why are there no decimal literal suffixes (`u`, `l`, `ul`, `f`)

Those are inconsistent as they are only available for `uint`, `long`, `ulong` and `float` opposed to all decimal literals.
In addition, you can already explicitly cast decimal literals to the correct type (for example `long val = (long)1000000000 * 10`).  

## TextMate language definition

### Why is everything separated in the repository

This makes it easier for me to make changes to the language as I don't have to repeat myself.
It also allows for more precise token information to use by the parser.
