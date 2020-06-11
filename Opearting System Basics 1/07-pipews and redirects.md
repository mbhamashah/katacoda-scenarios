# Pipes & Redirects

## Pipes & redirects (stdio/stderr)

### Standard output ( stdout)
standard output is a default place for an output to go. Generally this is your terminal. The Linux operating system has a concept of “a default place for output to go”. shell is constantly monitoring the default output place. When your shell sees new output it prints on the screen so that we can read it. other wise it  echo "welcome"  would send “welcome” to that default placefor an output. 

### Standard Input (stdin)

Standard input (stdin) is the default place where commands listen for more info. For example, if we type cat with no arguments then it will listens for input on stdin and outputting to stdout until we send    it an EOF character ( CTRL+d).


@cat $
@welcome$
@ welcome again$
@How are you doing in the class?$
type now [ctrl+d]


### Pipe 

This command is used to redirect output of one command to another command. 

Let's create a sample file. In case you have any sample .txt file then it can be used.

@vi samplefile.txt$

press i and insert some text. Example - This is a sample file. press Esc key, type :wq and press enter

@cat samplefile.tx$

@cat filename | less$ we will see out one page at a time.


### Redirection operator

I/O redirection command will redirect the output of a command to a file 

@Echo “wibble” > file.txt$

@cat file.txt$


### Standard error

Standard error (“stderr”) is like standard input and standard, default place where error messages go. To see some stderr messages let's try to catting a file that does not exist. 

@cat non-existent-file.txt$

you will see the standard error on your screen.