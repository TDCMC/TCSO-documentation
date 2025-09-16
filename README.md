# Trauma Center: Second Opinion documentation

This repository contains data about the structure of files used in the surgery game released by Atlus for the wii with the name "Caduceus Z: Futatsu no Chou Shittou" in Japan, and "Trauma Center: Second Opinion" elsewhere.

## Extracting the game files

The game contains a variety of file formats that may need to be extracted.

### Extracting the rom

Use the [Wiimms ISO Tools](https://wit.wiimm.de/download.html) to extract the game.

`wit x --source <The rom file> <Destination for extracting>`

Every relevant file should then be inside `<Destination>/DATA/files`

### Extracting .pak files

Use the [PackTools](https://github.com/tge-was-taken/AtlusFileSystemLibrary/releases) provided by the Atlus Filesystem Library to extract the .pak files.

`PAKPack.exe unpack <The .PAK file>`

### Extracting .tpx files

1. Download the [tpxtopng](https://archive.vg-resource.com/thread-36020-post-655483.html#pid655483) tool provided by Akaiji
2. Open the application
3. Drag and drop the .tpx files into the application window
4. Click on the "Convert" button

### Extracting .bm2 files

This part might be a bit tricky since .bm2 files seem to have different formats and encodings that may need to be tested.

Use the AtlusScriptCompiler tool provided by [Atlus Script Tools](https://github.com/tge-was-taken/Atlus-Script-Tools/releases) to extract the .bm2 files

`AtlusScriptCompiler.exe -Library tc2 -Encoding <Text encoding> -OutFormat <Version of the file> -In <the .bm2 file>`