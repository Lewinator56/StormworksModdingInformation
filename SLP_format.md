# This file will describe the basic .SLP format for stormloader mods
```
ModName.slp
├── Meshes
│   ├── Mesh_folder
│   │   └── Mesh_in_folder.mesh
│   ├── Mesh.mesh
│   └── Mesh_1.mesh
├── Definitions
│   ├── Definition.xml
│   └── Definition_1.xml
├── Audio
│   ├── Audio_folder
│   │   └── Audio_in_folder.ogg
│   ├── Audio.ogg
│   └── Audio_1.ogg
├── Graphics 
├── Data
├── metadata.xml
└── index.html
```

## Folder Details
- A .SLP file is a renamed .ZIP file.
- StormLoader WILL NOT install your mod if the .slp is a renamed .rar or .7z, it MUST be a .zip.
- Requirements have been relaxed allowing the mod to exist any number of subfolders into the .slp package itself, for example:
```
ModName.slp
└── ModNamme
    ├── Meshes
    ...
```
- The only requirement in this case is that all proceeding folders before the mod content are empty other than a single subdirectory.
***
### Root
- The root folder is the one that is zipped and renamed to a .slp, this should contain at least the metadata file.
- All the other folders and files are optional
#### index.html
- Stormloader supports the addition of webpages to mods, to enable creators to add details to display in StormLoader, you can include as many pages as you like, in as many folders as you want, so long as the initial page is index.html. The folders for the webpages will not be copied into the game directory.
#### metadata.xml
- Stores metadata about a mod, its creator and version.
```
<Metadata>
    <Author>author_name</Author>
    <Version>mod_version</Version>
</Metadata>
```
***
### Meshes
- Stores mesh objects to be installed, this folder can support meshes in subfolders, as many levels down as required, however, remember to make sure subfolder paths are correct when creating definitions.
- It is reccomended that meshes are stored in a folder with the creator's name or mod name so that its easy to identify them in the stormworks directory.
***
### Definitions
- Stores block definition xmls.
- Cannot have subfolders,
***
### Audio
- Stores audio for blocks, using the .ogg format.
- This directory can have subfolders, as many levels as required, as with meshes, consider the path when defining audio in the block definitions.
***
### Graphics
- Stores graphics data files and folders.
- This folder and file strucure reflects that of the stormworks directory, to overwrite the additive shader for example, it would be like this in the mod:
```
ModName.slp
├── Graphics
│   └── shaders
│      └── additive.glslf
```
***
### Data
- Stores all other mod data files and folders not in Meshes, Definitions or Audio.
- Like the Graphics folder, this mirrors the 'data' folder in the stormworks directory, to add a custom vehicle preset with your mod, you can do so by placing it like this:
```
ModName.slp
├── Data
│   └── preset_vehicles_advanced
│      └── custom_vehicle.xml
```
- To add a modified tile, it would be like this:
```
ModName.slp
├── Data
│   └── tiles
│      └── modified_tile.xml
```
- While you can include block definitions in this folder, under the 'definitions' subdirectory, to make your mod easier to understand, its reccomended you continue using the old 'Definitions' folder in the root directoyr of your mod.
