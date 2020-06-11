# Files & Directories
## File management in Bash
---
Files are collections of bits or characters stored in directories/folders (those terms are interchangeable). Let's start by looking at files and directories...

### List directories and files 

This command is used to list directory. 


`ls`{{execute}}


if we use -l option with it then it will give output in long list format

`ls -l`{{execute}}


### Copy command

command is used for copying files and directories from one location to another.

Lets first create some directories. 

`mkdir devops1`{{execute}}

`mkdir devops2`{{execute}}

`cd  devops1`{{execute}}

`touch samplefile.txt`{{execute}}

`ls`{{execute}}


Now that we have few directories and one sample file. We want to copy samplefile.txt from devops1 directory ro devops2 directory with new name samplefilecopied.txt.


`cp samplefile.txt /root/devops2/samplefilecopied.txt `{{execute}}

`cd /root/devops2 `{{execute}}

`ls -l `{{execute}}


### Move file

Now let's move samplefilecopied.txt from devops2 directory to devops1 directory

`mv /root/devops2/samplefilecopied.txt /root/devops1/samplefilecopiedmoved.txt`{{execute}}


### Home sweet home
Every linux user has a home directory, let's move to ours. To do so we use `cd`{{execute}} (try it now). We can see what the current directory, called the working directory, is by issuing the command `pwd`{{execute}} or outputting the `$PWD` variable: `echo $PWD`{{execute}}. The home directory is where bash looks for its initialisation scripts, which start with one called .bashrc (more about that later).

Your home directory can also be referred to by the symbol `~`, which is called 'Tilda', or by the variable `$HOME`.

### Create new directories
To create a new directory called 'wibble' we would type `mkdir wibble`{{execute}} (I use the term 'wibble' a lot, because its fast to search for with few false positive results). To create a set of nested directories all at once we would use the `-p` flag like this `mkdir -p src/main/java`{{execute}}. The `-p` flag also promises to never throw an error, which can be quite a useful feature when creating directories in a script. Once a directory is created we can move to it `cd src/main/java`{{execute}}. 

### Files
In Linux almost everything is a file. A file is actually a pointer to a collection of bytes, and some very strange things are classed as files in Linux. We can create an empty file using the command `touch`, as in `touch myfile.txt`{{execute}}. 

### Remove files and directories

So now if want to remove a file then we can use rm command. First let's check if the file exist.


`cd /root/devops1`{{execute}}

`ls`{{execute}}

Now that file exist. In this case we are going to remove file samplefilecopiedmoved.txt

`rm samplefilecopiedmoved.txt`{{execute}}

`rm -rf` can remove files and directories recursively. Hence we have to be very careful when we want to use this command.

`rm -rf \root\devops1`{{execute}}

### 


