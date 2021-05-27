# Frequently Asked Questions

## Why is underscore (`_`) not allowed in the indentifier

It is reserved for the compiler to generate the names.

## Why are there no decimal literal suffixes (`u`, `l`, `ul`, `f`)

It's inconsistent as they are only available for `uint`, `long`, `ulong` and `float` opposed to all decimal literals.  
In addition, you can cast the number to the correct type.  
Thus, it seems redundant to include.
