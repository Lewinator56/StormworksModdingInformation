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
    <Version>mod_version</version>
</Metadata>
```
