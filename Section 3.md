Rust has two kinds of data types **Scalar** and **Compound** data types.

**Scalar :** Data types storing only a single values
* Ex: Integers, Floats, Characters, Booleans
**[[Compound]] :** Data types that store multiple values, including values of different types 

Rust allows explicit typecasting of variabales with the `as` keyword.
```rust
    let b = 3.14159265359 as i32; // i32 - float is typecasted to 32 bit integer
    println!("b: {b}");
    
OUTPUT
b: 3
```
