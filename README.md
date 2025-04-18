# GDScript - Programming Language Tutorial
### Based on 'The template for learning a new language'

## Entry Point
GDScript is the custom programming language made for the Godot game engine. It is syntactically similar to Python, and many of the language quirks are integrated to its game engine nature. 

There isn’t a single ‘main()’ entry point in GDScript. Scripts are attached to individual nodes (or scenes) in the Godot game engine, and there are three primary entry points: 
_ready() is a ‘setup()’ function that runs once to load and initialize variables 
_process() is a ‘loop()’ function that runs many times a second to handle specific game updates where applicable
_physics_process() is another ‘loop()’ function that runs many times a second to handle properties specific to a physics engine, where applicable

For this tutorial, we use primarily use _ready() as our ‘main()’ equivalent. 


## Simple I/O
For simple input/output, there is the _input() function which will run whenever an input event occurs. This function is specific to the game engine, which means expected input tends to be mouse/keyboard presses and movements instead of text input. 
