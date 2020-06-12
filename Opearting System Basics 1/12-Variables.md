# Variables

## Variables

Variables are the core of any computer programming. Variables are used to store data, modify data, and (re)use them in the whole program.

Let's create a new script with `vardemo.sh`

`vi vardemo.sh$

`#!/bin/bash`

@greeting="Hello DevOps Enthusiast!"@
@user=$(whoami)@
@day=$(date)@

@echo "$greeting . Your user id is $user! Today is $day. Today we are learning basics of Operating System!"@
@echo "Your Bash shell version is: $BASH_VERSION. Enjoy your class!"@