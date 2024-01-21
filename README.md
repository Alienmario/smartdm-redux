# smartdm-redux
```
Smart file downloader which seeks dependencies from the engine.
Never download unused files or list individual files by hand again!
Supports resolving dependencies for .mdl and .vmt files and precaching.
This is a full rewrite by Alienmario of the original SmartDM by Zephyrus.

SmartDM.Add(...) is the main entry point and likely all you'll need.
To enable debugging, add "#define SMARTDM_DEBUG" before this include.
Useful debug command: dumpstringtables

Usually linux servers will not ship with shaders,
prohibiting automatic detection of shader parameters needed to resolve .vmt material files.
To overcome this, this include pairs with a cache file in SM's data folder.
This file is automatically generated if missing and shaders are available (e.g. on Windows).
Loading game specific (smartdm_shader_cache_<gamefoldername>.txt) or general (smartdm_shader_cache.txt)
caches is attempted before querying the game engine.

To enable scanning the custom folder, smartdm needs to be added as path id in gameinfo.txt
For example in HL2DM, the custom folder entry would look like this:
game+mod+smartdm			hl2mp/custom/*

Requirements:
 - Min SourceMod version: 1.12 - build 6963 (older builds possible if shader cache already exists)
```
