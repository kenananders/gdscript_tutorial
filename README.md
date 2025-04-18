# GDScript - Programming Language Tutorial
### Based on 'The template for learning a new language'

## Entry Point
GDScript is the custom programming language made for the Godot game engine. It is syntactically similar to Python, and many of the language quirks are integrated to its game engine nature. 

There isn’t a single ‘main()’ entry point in GDScript. Scripts are attached to individual nodes (or scenes) in the Godot game engine, and there are three primary entry points: 
_ready() is a ‘setup()’ function that runs once to load and initialize variables 
_process() is a ‘loop()’ function that runs many times a second to handle specific game updates where applicable
_physics_process() is another ‘loop()’ function that runs many times a second to handle properties specific to a physics engine, where applicable

For this tutorial, we use primarily use _ready() as our ‘main()’ equivalent. Scripts can be run in the Godot game engine itself, or this github pages link for simpler, non-integrated examples:
https://gdscript-online.github.io/


## Simple I/O
For simple input/output, there is the _input() function which will run whenever an input event occurs. This function is specific to the game engine, which means expected input tends to be mouse/keyboard presses and movements instead of text input. 

The following is a brief snippet of the _input() function and how it can gather input and print output. 


## Primitive Types

- **int**: Represents integers (whole numbers)
- **float**: Represents floating-point numbers (decimal values)
- **bool**: Represents boolean values (`True` or `False`)
- **str**: Represents strings (text data)
- **null**: Represents the absence of a value

GDScript is Dyanmically typed by default but can optionally be statically typed. 

- var x = 5 # Dynamically Typed
- var x: int = 5 # Statically Typed

GDScript is also strongly typed, which means types must be explicitly converted.
- var x = 5
- var y = “6”
- var z = x + int(y)

## Operations on Primitive Types
### Arithmetic Operators
- **Addition (`+`)**: Adds two numbers.
- **Subtraction (`-`)**: Subtracts one number from another.
- **Multiplication (`*`)**: Multiplies two numbers.
- **Division (`/`)**: Divides one number by another.
- **Modulus (`%`)**: Returns the remainder of a division.
- **Exponentiation (`**`)**: Raises one number to the power of another.
### Relational Operators
- **Equal (`==`)**: Checks if two values are equal.
- **Not equal (`!=`)**: Checks if two values are not equal.
- **Greater than (`>`)**: Checks if one value is greater than another.
- **Less than (`<`)**: Checks if one value is less than another.
- **Greater than or equal to (`>=`)**: Checks if one value is greater than or equal to another.
- **Less than or equal to (`<=`)**: Checks if one value is less than or equal to another.
### Logical Operators
- **AND (`and`)**: Returns `True` if both conditions are true.
- **OR (`or`)**: Returns `True` if at least one condition is true.
- **NOT (`not`)**: Negates the condition.

Note that there is no incremental operator in GDScript (x++, x--). Correct notation would be (x+=, x-=). This exists for all Arithmetic Operators.

## Strings
Strings are immutable in GDScript. As Godot is a game engine, there is not as much emphasis on strings and string operations as there are in other popular and easy languages, like Python. There are a lot of built in methods that are helpful for converting hexcode, opening and writing to files, reading locations, and other more technical string implementations. 
### Common String Operations
- **Length**: "abc".length()         # 3
- **Upper**: "abc".to_upper()       # "ABC"
- **Find**: "abc".find("b")        # 1
- **Substring**: "abc".substr(1, 2)     # "bc"
- **Capitalize**: "abc".capitalize()     # "Abc"
- **Contains**: "abc".contains("b")      # true

## Primitive Data Structures
There are two primary data structures in GDScript - Arrays and Dictionaries. The array can operate as a resizeable list and has stack/queue operations. The Dictionary is a standard key/value pair. 
### Array
- arr.size()
- arr.push_back(5)
- arr.pop_back()
- arr[0]
- arr[0] = 100

### Dictionary
- dict.has("key")
- dict["key"] = value
- dict.erase("key")

## Structured Programming
### Code Blocks and Scope
GDScript uses indentation to define code blocks, similar to Python. It uses Lexical and Function scoping, and variables are defined with 'var' (using indentation to determine variable visibility).
