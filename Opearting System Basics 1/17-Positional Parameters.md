#Positional Parameters

## Postional Parameters

So far we have modified our back up script and parameterized it. However we can make it even better when we can take back up of any user's directory. If we can specify user name at time of running backup then it will make much easier for system administrator to take backup of for any user.

We use positional parameters with bash script to achieve this goal.

Let's take an example.

`vi pos_param.sh`{{execute}}

Press 'i'

'#! /bin/bash`{{execute}}

'echo $1 $3`{{execute}}

'echo $#`{{execute}}

'echo $*`{{execute}}


Press Esc, :wq , enter key


`chmod +x pos_param.sh`{{execute}}


`./pos_param.sh  101 102 219`{{execute}}

We print using `echo $1 $3` command that prints only 1st postional parameter (101) and 3rd positional parameter(219). 2nd positional parameter was omitted. 

 
Let's improve our backup script.

`vi newbackup.sh`{{execute}} 

Press 'i'


`if [ -z $1 ]; then  `{{execute}}
`	user=$(whoami)  `{{execute}}
`else`{{execute}}
	`if [ ! -d "/home/$1" ]; then`{{execute}}
		` echo "Requested $1 user home directory doesn't exist."`{{execute}}
		`exit 1`{{execute}}
	`fi`{{execute}}
	`user=$1`{{execute}}
`fi`{{execute}}
	
`#!/bin/bash`{{execute}}

`# Modified backup script`{{execute}}

`input_directory=/root/user`{{execute}}

`output_file=/root/user/backup/backup_$(date +%Y-%m-%d_%H%M%S).tar.gz`{{execute}}

`# The function total_files reports a total number of files for a given directory.`{{execute}}

`function count_files {`{{execute}}
        
`		find $1 -type f | wc -l`{{execute}}

`}`{{execute}}

`# The function total_directories reports a total number of directories`{{execute}}

`# for a given directory. `{{execute}}


`function count_directories {`{{execute}}

`        find $1 -type d | wc -l`{{execute}}

`}`{{execute}}


`function total_count_archived_directories {`{{execute}}

`        tar -tzf $1 | grep  /$ | wc -l`{{execute}}

`}`{{execute}}


`function total_count_archived_files {`{{execute}}

`        tar -tzf $1 | grep -v /$ | wc -l`{{execute}}

`}`{{execute}}


`tar -czf $output_file $input_directory 2>/root/user/script_error/null/error.txt`{{execute}}


`source_files=$( count_files $input )`{{execute}}

`source_directories=$( count_directories $input )`{{execute}}

 . 
`total_archived_files=$( total_count_archived_files $output )`{{execute}}

`total_archived_directories=$( total_count_archived_directories $output )`{{execute}}

`echo "Files to be included: $source_files"`{{execute}}

`echo "Directories to be included: $source_directories"`{{execute}}

`echo "Files archived: $total_archived_files"`{{execute}}

`echo "Directories archived: $total_archived_directories"`{{execute}}

`if [ $source_files -eq $total_archived_files ]; then`{{execute}}

`echo "Backup of $input is completed as requested!"`{{execute}}

`echo "Please find the details of the output backupfile.:"`{{execute}}

`ls -l $output`{{execute}}

`else`{{execute}}
 
`	 echo "Backup of $input failed. please check !"`{{execute}}

`fi`{{execute}}

`echo "Total files to be included in the back up are :"`{{execute}}

`count_files $input_directory`{{execute}}

`echo "Total directories to be included in the back are :"`{{execute}}

`count_directories $input_directory`{{execute}}


Now press Esc key + :wq followed by enter key

`ls -l `{{execute}}


`chmod +x newbackup.sh`{{execute}}


`./newbackup.sh`{{execute}}

