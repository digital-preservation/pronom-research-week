# Microsoft Project

http://fileformats.archiveteam.org/wiki/Microsoft_Project

Currently missing signature:
* x-fmt/244	Microsoft Project	95	mpp

Current signature for:
* x-fmt/243	Microsoft Project	4.0	mpp

Looks for `<Sequence>14 00 00 00 'MSProject.Docfile.4' 00</Sequence>` which seems to have a typo. Should be a capital "F" in DocFile. Microsoft Project 95 also is a DocFile.4 but additional has the version `MSProject.Project.4_1`

This is submission for an updated x-fmt/243 with adjustment and new signature for x-fmt/244