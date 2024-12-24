Compound data types can store multiple values in rust. Thesevalues can also be of different data types. Rust has two kinds of compound data type : **Arrays** and **Tuples**.

**Arrays** - Square brackets, same type
- All variables must be of the same type
- Have a fixed length
- Stored on the stack (Static allocation)
- To delcare:
```
// Without type annotation
let variable_name = [element1, element2, ..., elementn];

// With type annotation
let variable_name [<data_type>; SIZE] = [element1, element2 , ... elementn]

// To have an array with 'y', 'x' amount of times
let array = [y; x]
```

**Tuples** - Round brackets, same types
- Have a fixed length similar to arrays
- Elements can be of different (or same) scalar types
- Tuples are also stored on the stack (Static allocation)
- To declare:
```
// Without type annotation
let tuple_name = (element1, element2, ..., elementn)

// With typeannotation
let variable_name: (data_type, ...) = (element1, element2, ...,
```

**Slices** are parts of existing compund types. A slice consists of the slice operator `.. or ..=` and a start and end index. To create a slice we use the reference `&` of the compound type we are slicing

Example:
```
let my_array = [0, 1, 2, 3, 4, 5, 6, 7, 8, 9];

let my_slice = &my_array[0..4]; // Slice of an array from index 0 to 4 (exclusive)

let my_slice_inc =  &my_array[0..4=] // Slice of array from index 0 to 4 (inclusive, same as doing 0 to 5 exclusive)

// 0,1,2,3  -- Elements from index 0 to 4
```