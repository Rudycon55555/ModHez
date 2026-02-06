# Modder
ModHez's toolchain is named **`Modder`**,
and it bundles **Zig Toolchain + ModHez Transpiler + Any Other Optional Stuff**.

## Build Files
Modder should read **`Modderfile`** from the current directory when **`modhez build`** is run.
The Modderfile is **written in ModHez *itself***, and it tells Modder how to
- **Transpile the ModHez project into Zig**
- **Generate build.zig and build.zig.zon**
- **Build it with `zig build`**
- **Log certain errors**
