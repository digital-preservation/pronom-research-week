# FreeHand (Aldus FreeHand Drawing File Format)

http://justsolve.archiveteam.org/wiki/FreeHand

### Added missing signature
* x-fmt/304	Aldus Freehand Drawing	4	fh4

### Added new signatures
* CHLdev/1 Aldus FreeHand Drawing version 1
* CHLdev/2 Aldus FreeHand Drawing version 2

### Extensions
Aldus FreeHand versions 1 & 2 on a Macintosh did not use extensions, but it would be easy to use FH1 & FH2.

### FreeHand versions 4 & 5
The file format for versions 4 & 5 of FreeHand are very similar, both begin with the same magic header "AGD1", but often a version 4 file will include the string "Aldus FreeHand 4.0 file." So signature is based on this string. There are a few instances where samples do not have this string and are identical to version 5 files. In fact, a file created in version 5, then exported out as version 4 can be bit identical. 
