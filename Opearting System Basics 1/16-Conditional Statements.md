# Conditional Statements

## Conditional Statements

In this section, are going to discuss about conditional statements in bash shell scrpting. Using these statement, we can add more logic to our scripts. Fundamental concept is that if certain conditions meets then excute certain other steps.  if not then do something else.


We `if`, `then` and `else`. For example, we can improve our backup script by comparing number of files exist in the source directory and resulting backup file. If both number matches then only our backup is taken correctly. Otherwise something is not correct.\


Let's take few simple examples. We want to compare two numbers ( number1 and number2) and then compare if number1 is less than number 2 , if yes then print number1 is less than number 2. However if above condition is not true then print - Number 1 is greater than number2.


`vi numbercomparator.sh`$


press `i` 


`#!/bin/bash`{{execute}}

`numer1=100`{{execute}}

`number2=200`{{execute}}

`if [ $number1 -lt $number2 ]; then`{{execute}}

`    echo "$number1 is less than $number2!"`{{execute}}

`else`{{execute}}

`   echo "$num_a is greater than $num_b!"`{{execute}}

`fi`{{execute}}


`Press Esc , :wq , then enter key


`Now let's give execute persmission to the script.


`chmod +x numbercomparator.sh`{{execute}}

`./numbercomparator.sh`{{execute}}


the Psuedocode for this  kind of backup script will be something like this 

If number of files source directory and traget file is same then print `OK` else print 'An error has occurred`

