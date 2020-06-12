# Simple Backup Bash Shell Script

## Backup Bash Shell Script

Let's take develope a basic back up script, a routine work which we need to do eveyr day or quite frequently.

We want to take back up of a directory including all files and sub directories. We will be using tar command for it.

First let's create some files and sub-directories.


`dir`{{execute}}
`ls -l`{{execute}}
`mkdir user
`touch backupfile1.txt`{{execute}}
`mkdir subdir1`{{execute}}
`mkdir backup`{{execute}}
`cd subdir1`{{execute}}
`touch backupfile2.txt`{{execute}}
`ls -l`{{execute}}

you should see you backupfile2.txt`{{execute}}

`cd ..`{{execute}}


So now we have few files and sub directories.

`vi backupscript.sh`{{execute}}

Now press i, then we need to import bash

`#!/bin/bash`

`tar -czf ./backup/myhomebackup.tar.gz  .`

Now press Esc key and :wq , press enter.

Now you should have a file in backup directory.



