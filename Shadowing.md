When a new variable is declared with th name of an already existing variable this is knows as **Shadowing**

Rust allows shadowing within the same scope, unlike other languages like C++. When a variable is shadowed a new memory address is assigned to the newly created variable, in the program we refer to it with the same name.

```
fn main() {
    let a = 108;
    println!("addr of a: {:p}, value of a: {a}", &a);
    let a = 56;
    // Using :p is the same as %c in c, it gets the meory address
    println!("addr of a: {:p}, value of a: {a} // post shadowing", &a);

    let mut b = 82;
    println!("\naddr of b: {:p}, value of b: {b}", &b);
    let mut b = 120;
    println!("addr of b: {:p}, value of b: {b} // post shadowing", &b);

    let mut c = 18;
    println!("\naddr of c: {:p}, value of c: {c}", &c);
    c = 29;
    println!("addr of c: {:p}, value of c: {c} // post shadowing", &c);
}
```