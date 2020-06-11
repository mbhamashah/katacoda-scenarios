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

tar -cvf filename.tar samplefile.txt filename1 filename2

Let's first create one more file in our devops2 directory

touch samplefile2.txt

use this command to create an archive 

tar -cvf archive.tar samplefile.txt samplefile2.txt


To extract file from an archive
tar -xvf archive.tar

