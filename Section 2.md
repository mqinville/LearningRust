 - All var declarations are immutable by default, once assigned it cant be changed
	 - This helps guarantee safe concurrency (No spin locks/mutexes, threads wont change values unknowingly)
	 - `let var = value;` defines an immutable varaible (Cannot be changed)
	 - `let mut var = value;` defines a mutabke value (Can be changed)
		 - Though you are allowed to change the value of a mutable variable, you can not assign the value of another data type to it.
 - Rust is strongly typed, but specification of data type not required at declaration time
	 - The rust compiler will infer the type of the varaible being delcared.
		 - Can still explicityly declare by doing `let var : <type> = value;`
	 - Use generic keyword `let` to define a variable
- **Common data types**
	1. `i32` and `u32` $\implies$ Signed/Unsigned 32 bit integers
	2. `f32` and `f64` $\implies$ 32bit and 64 bit floating point numbers
	3. `bool` $\implies$ Boolean
	4. `char` $\implies$ CHaracters
- Rust does not have implicit typecasting
	- Assigning `8` to a floating point variable will cause compilation errors, use `8.` or `8.0` instead
- Difference Between Variables and Constants
	- **Constants
		- Always immutable
		- Data type cannot be inferred by the compiler, must be declared
		- Used often in global scope
		- Cant be assigned to runtime values ex `var1=var2+1`
		- Constant values can be used at compile time 
		  `let myArray:[i32; ARRAY_LENGTH]`
		- Cannot be shadowed [[Shadowing]]
	- **Variables
		- Immutable by default, can be made mutable with `mut`
		- Data type can be inferred by compiler
		- Used locally
		- Variables can be assigned to runtime values `x=y+1`
		- Variable values cannot be used at compile time
		- Variables can be shadowed [[Shadowing]]