# Variables

## Variables

Variables are the core of any computer programming. Variables are used to store data, modify data, and (re)use them in the whole program.

There are some pre defined variables which are are used at various places. Let's explore it further.

On your terminal run this command and let's see what is the outcome.

`whoami$

This gives you the user name which is used to login to your session.

`date`{{execute}}

This gives you today's date.

Now if we want to today's day
` day= $(date +%A)`{{execute}}
`echo $day`{{execute}}

Bash version

`echo $BASH_VERSION`{{execute}}

This will give bash version in your terminal.

Let's see you want to greet someone, then we can define a variable and assign a value.

greeting = "This is a sample greeting message which can be modified as per your language porefereance"

`echo $greeting  `{{execute}}


Now that we have some basics of variables. Let's use them in our script and how it can help us writing a good reusable script.


Let's create a new script with `vardemo.sh`

`vi vardemo.sh`{{execute}}

`#!/bin/bash`

`greeting="Hello DevOps Enthusiast!"`

`user=$(whoami)`

`day=$(date)`

`echo "$greeting . Your user id is $user! Today is $day. Today we are learning basics of Operating System!"`

`echo "Your Bash shell version is: $BASH_VERSION. Enjoy your class!"`


We have used a combination of variables and commands. You can see that it gives us a lot more agility. We can customise it without rewriting everything from scratch.



Now let's customize our back up script. I am assuming that you still have a user sub directory under root. If not then please follow previous steps to create files and directory structure. If not then you can change input_directory name and output_file name as mentioned in the script. 

|- root

|--user

|----backup

|----subdir1


`#!/bin/bash`

`# Modified backup script `

`input_directory=/root/user`

`output_file=/root/user/backup/$backup_home_$(date +%Y-%m-%d_%H%M%S).tar.gz`

`tar -czf $output_file $input_directory`

`echo "Backup of $input is completed as requested! Please find the details of the output backupfile.:"`

`ls -l $output`



