# File Contents
## File Contents

### File archiving

tar commands archives the files

tar command is used with some options

-c – To create a archive


-x – Extract files from archive


-t – Display fils in archive


-v – verbose


-f – name of the arch filename .tar


`ls -l`{{execute}}

`tar -cvf filename.tar samplefile.txt filename1 filename2`

Let's first create one more file in our devops2 directory

`touch samplefile2.txt`{{execute}}

use this command to create an archive 

`tar -cvf archive.tar samplefile.txt samplefile2.txt`{{execute}}


To extract file from an archive
`tar -xvf archive.tar`{{execute}}

### Searching a string in a file

grep commands searches for a particular pattern of characters in a file , and displays all lines that contain that pattern.

`grep DevOps samplefile.txt`{{execute}}


For case insensitive search use -i option

`grep -i DEvOPS samplefile.txt`{{execute}}

