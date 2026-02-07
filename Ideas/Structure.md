## Project Structure
ModHez is picky about the **top-level** files and folders, but the rest is
up to you what else is there and what goes inside.

## Actual Structure Tree
```FileSystem.Tree
ProjNameHere/          # Name this project root whatever you want
├── Binaries/          # Outputted Binaries
├── Enviornment.lock          # The enviornment file
├── Modderfile          # The file Modder uses
├── Modules/          # Hierarchical code modules
├── SDKs-and-Tools/          # What you _use_
└── Temporary/          # Temporary Stuff
    ├── Developer/          # From the developer[s]
    └── Modder/          # From Modder
```

### Modules/
This is where the code goes, seperated by modules in modules and so on.
Importing 'Proj' allows you to use these via functions with dots that seperate
folders (eg., importing Proj with Modules/GUI/Home/{Index.modhez, Helper.modhez}
allows you to use the functions `Proj.GUI.Home.Index` and `Proj.GUI.Home.Helper()`)
