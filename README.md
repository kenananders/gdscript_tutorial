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

