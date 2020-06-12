# Functions

Functions allow a programmer to efficiently reuse its code by organizing it in such a way that if he/she needs to perform same activity again, he can call the function and use it. It increased efficiency, execution speed as well as readablity of the script.

It is also possible to write entire script without function. However you may end up with a inefficient, hard to maintain , hard to read and understand code so making it very hard to troubleshoot it.

In other words, a function is a collection of diffrent commands in to a single command. For example if you need to do a sum multiple time in a script, then we can define sum function and whereever we need to sum, we will just pass the input and get the output.
 
Functions are defined by using the function keyword and followed by function body enclosed by curly brackets.


Let's define a function.

`vi print_function.sh`{{execute}}

press 'i'

`#!/bin/bash`{{execute}}

`function print_user_info {`{{execute}}
`	echo " User Name: $(whoami)"`{{execute}}
`}
`print_user_info`{{execute}}


Press Esc key and :wq followed by enter.

`chmod +x print_function.sh`{{execute}}

`./print_function.sh`{{execute}}


