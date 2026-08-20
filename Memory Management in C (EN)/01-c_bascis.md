# If Statements

if statements are the most basic form of control flow in C: very similar to other languages. Basic syntax:

```c
if (x > 3) {
	printf("x is greater than 3\n");
}
```

`if`, `else`, `else if` are also available:

```c
if (x > 3) {
    printf("x is greater than 3\n");
} else if (x == 3) {
    printf("x is 3\n");
} else {
    printf("x is less than 3\n");
}
```

### Janky Syntax

You can write an `if` statement without braces if you only have one statement in the body:

```c
if (x > 3) printf("x is greater than 3\n");
```

# Logical Operators

Logical operators let you combine multiple conditions in C. There are three main logical operators you'll use all the time:

- `&&`: Logical `AND`: true if both conditions are true
- `||` Logical `OR`:  true if either condition is true
-  `!` Logical `NOT`: inverts a boolean value

```c
int age = 25;
bool has_license = true;

if (age >= 18 && has_license) {
    printf("Can drive\n");
}
```

## Short-Circuit Evaluation

C uses short-circuit evaluation with logical operators. This means:

- With `&&`, if the first condition is false, the second isn't even checked (because the whole thing is already false)
- With `||`, if the first condition is true, the second isn't checked (because the whole thing is already true)

```c
if (x != 0 && 10 / x > 2) {
    // The division only happens if x != 0
    // This prevents a division by zero error
    printf("Safe!\n");
}
```

## Operator Precedence

Logical NOT (`!`) has higher precedence than AND (`&&`), which has higher precedence than OR (`||`). When in doubt, use parentheses to make your intent crystal clear:

```c
// without parentheses – might be confusing
if (!is_raining && is_sunny || is_weekend)

// with parentheses – much clearer
if ((!is_raining && is_sunny) || is_weekend)
```

# Type Sizes

In C, the "size" (in memory) of a type is not guaranteed to be the same on all systems. That's because the size of a type is dependent on the system's architecture. For example, on a 32-bit system, the size of an `int` is usually 4 bytes, while on a 64-bit system, the size of a `int` can sometimes be 8 bytes - of courese, you never know until you run `sizeof` with the compiler you plan on using.

However, some types are always guaranteed to be the same. Here's a list of the basic C data types along with their typical sizes in bytes. Note that sizes can vary based on the plataform (e.g, 32-bit vs. 64-bit systems):

## Basic C Types and Sizes

- `char`
	- Size: 1 byte
	- Represents: Single character.
	- Notes: Always 1 byte, but can be signed or unsigned.
- `float`
	- Size: 4 bytes
	- Represents: Single-precision floating-point number.
- `double`
	- Size: 8 bytes
	- Represents: Double-precision floating-point number.

The actual sizes of these types can be determined using the `sizeof` operator in C for a specific platform, which we'll learn about next.

# Sizeof

C gives us a way to check the size of a type or a variable: `sizeof`

You can use `sizeof` like a function (although, technically it's a unary operator, but that distinction is generally only useful for winning suepr important internet arguments).

We'll use the `sizeof` operator in the next few lessons to give us insight into the memory layout of different types in C. This will be particularly useful as we move deeper into C, and essential for understanding pointers.

## size_t

The size_t type is a special type that is guaranteed to be able to represent the size of the largest possible object in the target platform's address space (i.e. can fit any single, non-struct value inside of it)

It's also the type that `sizeof` returns

# For Loop

A `for` loop in C is a control flow statement for repeated execution of a block of code. Very similar to Python, but with a different syntax.

The syntax of a for loop in C consists of three main parts:

- Initialization
- Condition
- Final-expression

```c
for (initialization; condition; final-expression) {
    // Loop Body
}
```

