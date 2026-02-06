# ModHez
This has an `Ideas/` folder, with Markdown-formatted files for ideas ModHez could have. ModHez is a coding language transpiled into Zig. The transpiler (Modder, which should use a Modderfile in the project root) will bundle the Zig compiler, so it can immediatly transpile the code and generate build.zig and build.zig.zon and run `zig build`.

## Transpilers
The toolchain will be made by the community via Pull Requests (PRs) with the folder `Toolchains/<your username here>/<version>/`

## Releases
For me to publish one of your transpiler as a *release*, it must meet the following:

- [ ] **The code in `Transpilers/<name>/<version>/` must be _source_ code.**
- [ ] **I must have reviewed it and am fine with it.**
- [ ] **I might edit it a little.**
- [ ] **I'll bundle it with the Zig toolchain and compile it, then release it.**

If followed correctly, you'd get:

- [x] **The code in `Transpilers/<name>/<version>/` must be _source_ code.**
- [x] **I must have reviewed it and am fine with it.**
- [x] **I might edit it a little.**
- [x] **I'll bundle it with the Zig toolchain and compile it, then release it.**
