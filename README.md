# StormworksModdingInformation
A repository for midding information for creating mods for stormworks, basically a knowledge dump, but organised.

# Modding Information for Stormworks
This repository will cover multiple sections of stormworks modding, including meshes, XML files and in the future documentation of formats.

## Contents
1. Modding Tools
2. Stormworks File Structure


## Modding Tools
Multipel tools are available to create mods for stormworks, they are freely available and open source. This section will cover the tools, their usage and prerequisites. It will not go into detail about how to use the tools, They all have manuals available on their respective github repositories.

### swMesh2XML
Repository : https://github.com/Lewinator56/swMesh2XML_repo
- swMesh2XML is a mesh converter tool, it takes .obj meshes exported from blender and converts them into the propriatory .mesh format used by Stormworks.
- swMesh2XML requires Microsoft .Net Core 3.1 is installed to run. It only runs on windows


### swcpmc
Repository : https://github.com/Lewinator56/swcpmc
- swcpmc is the same tool as swMesh2XML, but runs in the command line and can be run on different platforms. on linux it must be run under wine or mono. It uses only basic platform agnotic C libraries so can be recompiled to run on any platform of your choice with no issue.

### Stormloader
Repository : https://github.com/Lewinator56/StormLoader
- Stormloader is the modloader used to load mods into Stormworks. It uses a file format .slp to ensure mods are created correctly. It also has an online repository here users can upload mods, and is undergoing changes to allow installation of mods from zip files and nexus mods integration.
</p>

## Stormworks File Structure
This section will cover the file structure, linking and relationships between relevant files in the application directory. Bear in mind this only covers the structure on Windows. The structure on linux or MacOS is the same, however, finding the game's directory is slightly different.

#### Root
