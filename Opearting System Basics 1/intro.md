# Operating System Basics 1

## The things you will use every day

#### What is an Operating System
●	According to Wikipedia
An operating system (OS) is system software that manages computer hardware, software resources, and provides common services for computer programs.

As this moment when you are reading this slide, in fact it is using a operating system in the background.

Most popular operating systems are  
Windows 
iOS
Linux



#### What is a shell?
In Linux, a shell is a command intepreter: a program that has the permission and ability to run other programs. On Linux it is possible to run many sessions, or instances, of a shell simultaneously.

#### What is bash?
Bash is a program that has the capabilities and permissions to run other programs. It is the result of decades of evolution and is highly sophisticated though is often mired in the past. It is one of the most highly developed and efficient methods of interacting with a computer. But, it is really reserved for people who deeply understand computers and who understand why a lot of things are better done with a keyboard than a mouse.


There are plenty of other shells that we could learn about, some of them are considered 'better' than bash (`fish`, for example, is excellent), for one technical reason or another (or many). But, bash is ubiquitous and is considered the reference point for a lot of other work. When you look at a shell-script it is 10x more likely to be a bash script than any other. Of special note here is 'sh' the base shell installed with most Linux distributions. A lot of scripts target that environment because it is even more widespread than bash. But, it lacks a lot of bash's sophistication and in reality can be ignored. Coding for `sh` rather than `bash` is hip and therefore you can forget it. Target Bash and you'll be ok.

There are two fundamental methods of working with bash: Terminals and Scripts

Terminals, sometimes called command-lines, sessions, or, confusingly, shells, exist for people: they hold the user-interface for a shell. Scripts are lists of bash instructions in a file that execute either in the current shell or in a new one. 

#### What will you learn?
At first we'll look at terminals, but we'll quickly move into scripts too. You'll learn a bunch of useful skills in a terminal and how to use bash, even though right now you won't learn that many commands. That's what the rest of the course is for.

Throughout this course you'll be learning keyboard shortcuts and the command-line method for doing things. It is my strong opinion that this more effectively grounds you in the fundamentals of how things work. In practice you'll be exposed to GUI's and other tools. Mostly these are used when the volume of information we have to interpret is too large for us to manage it efficiently on the command-line. However, if you can't do it on the command-line then a gui won't help you. GUI's make working with large volumes of data more convenient, but the fundamental knowledge has to be there for you to understand what the GUI is doing. Therefore, learn the keyboard shortcuts we present and use them.

The skills you'll learn here are at the core of DevOps. Your tutor initially learnt a lot of this 30 years ago, and still uses these skills on a daily basis. We will cover basic bash here, but we'll be using it in every other part of this course. We layer technical skills on top of each other, so don't think of this as a basic module, but rather as a foundational module.
