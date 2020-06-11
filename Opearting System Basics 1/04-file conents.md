# File Contents
## File Contents

### File archiving

tar command archives the files

tar command is used with some options

-c – To create a archive


-x – Extract files from archive


-t – Display fils in archive


-v – verbose


-f – name of the arch filename .tar


`ls -l`{{execute}}


Let's first create one more file in our devops2 directory

`touch samplefile2.txt`{{execute}}

use this command to create an archive 

`tar -cvf archive.tar samplefile.txt samplefile2.txt`{{execute}}

`ls -l `{{execute}}

`rm samplefile.txt `{{execute}}
`rm samplefile2.txt`{{execute}}

`ls -l `{{execute}}

We only have a tar file in our directory

To extract file from an archive
`tar -xvf archive.tar`{{execute}}


check your results with 
`ls -l `{{execute}}


### Searching a string in a file

grep command searches for a particular pattern of characters in a file , and displays all lines that contain that pattern.

`grep DevOps samplefile.txt`{{execute}}


For case insensitive search use -i option

`grep -i DEvOPS samplefile.txt`{{execute}}

### sort the results

sort command sorts the results of a search either alphabetically or numerically. It also sorts files, file contents, and directories.

`sort samplefile.txt `{{execute}}

sort -n  returns the results as per numerical order

`sort -n samplefile.txt `{{execute}}

sort -f  returns case insensitive sorting

`sort -f samplefile.txt `{{execute}}

