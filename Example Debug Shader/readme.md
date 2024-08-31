
Uses bitmasking to render numbers in 15-segment cells.

Godot Shader Debugger
Adapted from villain749 on reddit:
https://www.reddit.com/r/GraphicsProgramming/comments/12m1d36/comment/jg939n4

Allows for basic data debugging from native gdscript code.
Works with Canvas, Spatial, and Sky shaders
Displays values for floats, vectors and matricies
Values limited to -99.999 to 99.999
Float values are a little rough, use the Fix Floats toggle for integers
Obviously only works for per-frame rendered values, not per-pixel
Edit position and size in shader uniform controls in editor
Easy to add to existing code

To Use:
- Copy the code in to your script

Debug dbg = debug_construct(UV);
- Construct a dbg struct, passing a UV
- Use SCREEN_UV for sky (ONLY WORKS in forward_plus rendering)

void my_func( inout Debug dbg ) {}
- Pass the dbg to any function

dbgFloat(dbg, value);
- Call the function for your value

debug_finish(color, dbg);
- Pass your color to the finisher before applying


