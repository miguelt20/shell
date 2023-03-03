<h1 align="center"> 
    Shell 
</h1>

<p align="center">
    <img alt="Shell Image" src ="https://i.pinimg.com/236x/e8/ba/a0/e8baa0dde0068757010c6da293720ba9.jpg" />
</p>

<p align="center">
    The shell is a program that takes commands from the keyboard and gives them to the operating system to perform. In the old days, it was the only user interface         available on a Unix-like system such as Linux. Nowadays, we have graphical user interfaces (GUIs) in addition to command line interfaces (CLIs) such as the shell.

    This repository contains the basic steps to learn how to use a shell properly and take advantage of it.
</p>

## Basic commands

Here are some of the basic commands to navigate, manipulate files or to look for help in the Man pages.
- `pwd`
- `cd`
- `ls` 
- `cp`
- `mv`
- `rm`
- `touch`
- `mkdir`
- `help`
- `man`
- `less`
- `file`
- `ln`
- `type`
- `which`

## Permissions
Every file and directory in your UNIX/Linux system has following 3 permissions and here are some of the commands to change or give permissions to a file.
- `chmod`
- `sudo`
- `su`
- `chown`
- `chgrp`
- `id`
- `groups`
- `whoami`
- `adduser`
- `useradd`
- `addgroup`

## Loops and Conditions
### Loops
Loops allow us to take a series of commands and keep re-running them until a particular situation is reached. They are useful for automating repetitive tasks.

*Simple syntax*

```bash
while [ condition ];
do
    # statements
    # commands
done  
```

### Conditions
The conditional statement is used in any programming language to do any decision-making tasks. This statement is also used in bash to perform automated tasks like another programming language, just the syntax is a little bit different in bash.

*Simple syntax*

```bash
if [condition]
then
   statement1
else
   statement2
fi
```

## I/O Redirection
By using some special notations we can redirect the output of many commands to files, devices, and even to the input of other commands.

### Standard Output
Most command line programs that display their results do so by sending their results to a facility called standard output. By default, standard output directs its contents to the display. To redirect standard output to a file, the ">" character is used like this:

```bash
user@bash$ ls > file_list.txt
```
In this example, the ls command is executed and the results are written in a file named file_list.txt. Since the output of ls was redirected to the file, no results appear on the display.

Each time the command above is repeated, file_list.txt is overwritten from the beginning with the output of the command ls. To have the new results appended to the file instead, we use ">>" like this:

```bash
user@bash$ ls >> file_list.txt
```
When the results are appended, the new results are added to the end of the file, thus making the file longer each time the command is repeated. If the file does not exist when we attempt to append the redirected output, the file will be created.

### Standard Input

Many commands can accept input from a facility called standard input. By default, standard input gets its contents from the keyboard, but like standard output, it can be redirected. To redirect standard input from a file instead of the keyboard, the "<" character is used like this:

```bash
user@bash$ sort < file_list.txt
```
In the example above, we used the sort command to process the contents of file_list.txt. The results are output on the display since the standard output was not redirected. We could redirect standard output to another file like this:
```bash
user@bash$ sort < file_list.txt > sorted_file_list.txt
```
As we can see, a command can have both its input and output redirected. Be aware that the order of the redirection does not matter. The only requirement is that the redirection operators (the "<" and ">") must appear after the other options and arguments in the command.

## Processes and Signals

A process can be thought of as an instance of a program in execution. We called this an ‘instance of a program’, because if the same program is run lets say 10 times then there will be 10 corresponding processes.

Moving ahead, each process has its own unique process ID through which it is identified in the system. Besides it own ID, a parent’s process ID is also associated with a process.

Here are some commands to take control of these processes:

- `ps`
- `pgrep`
- `pkill`
- `kill`
- `exit`
- `trap`
