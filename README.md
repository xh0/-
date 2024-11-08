# Глина
 A new type system for various uses 
 
## Data Types
 
### Unit type
```
() // Unit type
```

### Scaler types

```vb
i32  // int32
u32  // unsigned 32 bit integer
f64  // 64 bit float
bool // bool
bit  // one bit
char // uncode char
byte // 8 bit char
```

### Compound types  
##### Arrays (shopping list style)
```js
10 bool
8 bit
50 char
3 3 i32 // jagged array
10 10 10 byte
3i16 // NOT ALLOWED
```

##### Dynamic size types
```cpp
char* // list of chars (string)
byte* // bytes list of any length
```
##### Tuples
```csharp
(i8, char, bool)
(i32, (char, char),((i32,f64),(bool)))
```

##### Structs (named tuples)
```rust
(Name:50 char, age:i8, Salary:f32)
```


### Unions

```
(char | bool) // char or bool
(i32 | f32) // float or int
```

### Nullable types
```
char? // char or nothing
i32? // int or nothing
```
### Named types
_Named types is nothing but aliased types_
```
(Name: String, Website: URL) // String is char*, URL is String
```


### Templated types
```
List<i32> // list of ints
Dict<String,Tel> // Dict of String and Tel
```

### Enums

```
[ Right | left | Top = 5 | Down ] // Right=0, Left=1, and Down=6 as expected

// Flags enum detected by usage or items (ALL or NONE constants)
[ 
   None = NONE
   Sunday|
   Monday|
   Tuesday| 
   Wednesday|
   Thursday|
   Friday| 
   Saturday|
   Everyday = ALL
]

// Heterogeneous enums
[
	Foo | // 0 of type i8
	Bar | // 1 of type i8
	Value = "Unknown" 
]

// Tagged enums
[
	EveryDay |
	On<Date> |
	Every<i8>
]

```

