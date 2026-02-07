# Linking Code
ModHez needs a way to link code, so it uses #Import and @Acquire, 
but they serve different purposes in the linking system.

## #Import
In ModHez, `#Import("", "")` allows you to **statically link** code.
Inside the "" go a filepath or a URL to the library, and
Modder will embed that at compile-time. Inside the *second* "" goes the name of it,
which can have dots.

## @Acquire
This is the modern way to **dynamically link** code.
Inside the "" of `@Acquire("", "")` will go a URL or filepath,
but the library is loaded and used at _runtime_. Same "name-rule" with the second "".

## Trust Model
You can link to **ModHez Code, Zig Code, C Code, C++ Code, and Compiled Code** via #Import and @Acquire.
If you **statically link** to **source code** (ModHez, Zig, C, C++), the library is automatically "Trusted"
because you can view it directly.
If you **statically link** to **compiled code**, you, the developer, must manually "Trust" it by
putting the Modder flag `--trust-{module-paths-seperated-by-commas-here}`.
If you **dynamically link** source code, it is also automatically "Trusted."
If you **dynamically link** compiled code, you need to trust it
*and* the user needs to trust it. The user can trust it in these ways:

- Allow it
- Or the library is in a folder that only root/admin can write to

## Modular Hierarchies
Every imported thing is *modular* with the dots and stuff.
A cool project-level trick is:
```ModHez
#Import("/path/to/project/root/", "Proj")
```
Which will import the modules in the project.
