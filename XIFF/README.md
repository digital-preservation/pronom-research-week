# XIFF (Xerox Image File Format)

http://fileformats.archiveteam.org/wiki/XIFF

### File Information
XIFF is an extension of the TIFF Format but with added feature of multi-layered image using mixed raster content. Developed by Xerox for use with the Scansoft Pagis Software. 

### Identification

Version 2 of the file format uses the standard TIFF header with the string "XEROX DIFF" beginning at offset 8. Offset 18 indicates they are version 2.

Version 3 of the file format uses the standard TIFF header with the string " eXtended " beginning at offset 8. Offset 18 indicates they are version 3.

This information comes from the XIFF 3.0 draft spec, which is only available here in this repository as far as I know, I received it directly from a developer.

### Signatures added
* CHLdev/2 Xerox DIFF Image (version 2)
* CHLdev/3 eXtended Image File (version 3)
